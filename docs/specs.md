# Spécifications - NAC_app

## 1. Objectifs du Projet
Application web pour les passionnés d'insectes et reptiles, offrant :
- Un **répertoire éducatif** d'espèces avec fiches détaillées (incl. exigences capacitaire en France).
- Une **gestion personnalisée** via comptes utilisateurs (listes wishlist/collection, calendrier).
- Un **suivi santé** via notes quotidiennes analysées par IA pour détecter anomalies.
- Une expérience sécurisée, intuitive, et mobile-friendly.

## 2. Public Cible
- Débutants et experts en herpétologie/entomologie.
- Utilisateurs en France (focus lois capacitaire) et international.

## 3. Fonctionnalités MVP
### Répertoire des Espèces
- Recherche par nom/type (insecte/reptile).
- Fiches : Nom, description, besoins (température, humidité, alimentation), capacitaire (oui/non + refs légales), photos.
- Dataset initial : 50-100 espèces populaires.

### Comptes Utilisateurs
- Inscription/connexion (email/mot de passe, Google).
- Listes : Wishlist (à adopter), Collection (possédés).
- Filtres : Par type, capacitaire, difficulté.

### Calendrier et Tracking
- Ajout événements : Nourrissages, mues, nettoyages.
- Notes quotidiennes : Texte + photos par animal/jour.
- Vue calendrier : Jour/semaine/mois.
- Rappels email basiques ou notification.

### IA (Basique)
- Identification espèces via photo upload.
- Analyse légère des notes (ex. détecter mots clés comme "léthargie").

## 4. Fonctionnalités Avancées (Post-MVP)
- Filtres avancés (compatibilité espèces, niveau d'expérience).
- Analyse IA des notes : Alertes santé (ex. "Baisse appétit → voir véto"), résumés hebdo.
- Notifications push real-time.
- Export notes (PDF/CSV pour véto).
- Communauté : Commentaires, forum.

## 5. Exigences Non-Fonctionnelles
- **Performance** : Chargement pages <2s.
- **Sécurité** : RGPD (consentement pour IA/notes), HTTPS, hashing mots de passe.
- **Accessibilité** : Mobile-first (responsive via Tailwind CSS).
- **Scalabilité** : Support 1000+ utilisateurs, 10k+ fiches.
- **Légal** : Disclaimers ("App éducative, consultez véto/pro").

## 6. User Stories
- En tant que **visiteur**, je veux chercher une espèce sans compte, pour découvrir ses besoins.
- En tant qu'**utilisateur**, je veux ajouter une espèce à ma wishlist, pour planifier un achat.
- En tant qu'**éleveur**, je veux logger une note quotidienne, pour suivre la santé de mon gecko.
- En tant qu'**expert**, je veux des filtres avancés, pour trouver des espèces compatibles.

## 7. Contraintes
- Données fiables : Sources open (Reptile DB, iNaturalist).
- Légal : Infos capacitaire précises (lois FR via agriculture.gouv.fr).
- Budget : Gratuit au départ (MongoDB Atlas, Vercel free tiers).

## 8. Stack Technique
- **Front-End** : Vue.js, Nuxt3, Tailwind CSS, (Daisy UI).
- **Back-End** : Node.js, Express, (Go ?, Python (fastapi) ?, Nuxt ?), Supabase (stocker db en ligne pour commencer).
- **Base de Données** : MongoDB (fiches/notes), PostgreSQL (users), Redis (cache/events).
- **IA** : Hugging Face (photo/text analysis), Pytorch (client-side).
- **Cybersécurité** : JWT, Helmet, bcrypt (argon : donne de l'avance), HTTPS.
- **DevOps** : Docker, GitHub Actions, Vercel/Render (Vercel faire gaffe si backend en go prend que les metaframework).

## 9. Prochaines Étapes
- Collecter dataset 50 espèces (CSV/JSON).
- Wireframes (Figma/Penpot).
- Schéma BD initial.