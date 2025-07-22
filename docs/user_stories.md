# User Stories - NAC_app

Voici une liste complète et détaillée des **user stories** pour l'application **ReptoInsectHub**. Basée sur les fonctionnalités discutées : répertoire des espèces, comptes utilisateurs, calendrier et tracking (incluant notes quotidiennes, mues, nourrissages), intégration IA (identification, analyse, prédictions), cybersécurité, et extensions futures.

Chaque user story suit le format agile standard :
- **En tant que** [rôle],
- **Je veux** [fonctionnalité],
- **Afin de** [bénéfice].
- **Critères d'acceptation** : Conditions pour valider la story.
- **Priorité** : Must-have (MVP), Should-have (essentiel post-MVP), Could-have (avancé).
- **Dépendances** : Si applicable.

Structuré par modules pour clarté.

## Module 1 : Répertoire des Espèces

1. **En tant que** visiteur (non connecté),  
   **Je veux** chercher une espèce par nom, type (insecte/reptile) ou mots-clés,  
   **Afin de** découvrir rapidement des informations éducatives.  
   - **Critères d'acceptation** :  
     - Barre de recherche sur homepage.  
     - Résultats en <2s avec nom, photo, type, aperçu capacitaire.  
     - Suggestions auto-complètes basiques.  
     - Pas de compte requis.  
   - **Priorité** : Must-have (MVP).  
   - **Dépendances** : Dataset espèces.

2. **En tant que** visiteur,  
   **Je veux** consulter une fiche détaillée d'une espèce,  
   **Afin de** comprendre ses besoins d'élevage et exigences légales.  
   - **Critères d'acceptation** :  
     - Fiche : Nom, description, photos, besoins (température, humidité, alimentation, substrat, reproduction, durée de vie).  
     - Capacitaire : Oui/Non + liens lois FR + disclaimers.  
     - Mobile-friendly, zoom photos.  
   - **Priorité** : Must-have (MVP).

3. **En tant que** utilisateur connecté,  
   **Je veux** filtrer les espèces par critères avancés (famille, difficulté, capacitaire),  
   **Afin de** trouver des options adaptées.  
   - **Critères d'acceptation** :  
     - Filtres dropdown : Type, famille, difficulté, capacitaire.  
     - Mise à jour en temps réel.  
     - Sauvegarde filtres.  
   - **Priorité** : Should-have.

4. **En tant que** expert,  
   **Je veux** soumettre une nouvelle espèce ou mise à jour (modérée),  
   **Afin de** contribuer au répertoire.  
   - **Critères d'acceptation** :  
     - Formulaire avec validation (sources).  
     - Modération admin.  
     - Notification email.  
   - **Priorité** : Could-have.

## Module 2 : Comptes Utilisateurs

5. **En tant que** nouveau utilisateur,  
   **Je veux** m'inscrire avec email/mot de passe ou Google,  
   **Afin de** créer un compte sécurisé.  
   - **Critères d'acceptation** :  
     - Formulaire : Email, mot de passe validé, RGPD.  
     - Vérification email.  
     - OAuth Google.  
     - Gestion erreurs.  
   - **Priorité** : Must-have (MVP).  
   - **Dépendances** : Cybersécurité.

6. **En tant que** utilisateur,  
   **Je veux** me connecter/déconnecter,  
   **Afin de** accéder au profil sécurisé.  
   - **Critères d'acceptation** :  
     - HTTPS, "mot de passe oublié".  
     - Session JWT.  
     - Déconnexion efface session.  
   - **Priorité** : Must-have (MVP).

7. **En tant que** utilisateur,  
   **Je veux** gérer listes "Wishlist" et "Ma Collection",  
   **Afin de** organiser intérêts et animaux.  
   - **Critères d'acceptation** :  
     - Boutons ajouter/supprimer.  
     - Vue avec tri/filtres.  
     - Limite gratuite.  
   - **Priorité** : Must-have (MVP).

8. **En tant que** utilisateur,  
   **Je veux** personnaliser profil (niveau, localisation),  
   **Afin de** suggestions adaptées.  
   - **Critères d'acceptation** :  
     - Champs éditables.  
     - Options privacy.  
   - **Priorité** : Should-have.

## Module 3 : Calendrier et Tracking

9. **En tant que** éleveur,  
   **Je veux** créer calendrier pour un animal,  
   **Afin de** tracker événements.  
   - **Critères d'acceptation** :  
     - Vue jour/semaine/mois.  
     - Events : Nourrissage, mue, nettoyage (récurrents).  
     - Liaison animal.  
   - **Priorité** : Must-have (MVP).

10. **En tant que** éleveur,  
    **Je veux** ajouter note quotidienne (texte, photo),  
    **Afin de** documenter santé.  
    - **Critères d'acceptation** :  
      - Formulaire : Texte, upload.  
      - Tags suggérés.  
      - Liée calendrier.  
    - **Priorité** : Must-have (MVP).

11. **En tant que** éleveur,  
    **Je veux** rappels/notifications events,  
    **Afin de** ne pas oublier.  
    - **Critères d'acceptation** :  
      - Email/push customisable.  
      - Real-time Socket.io.  
    - **Priorité** : Should-have.

12. **En tant que** éleveur,  
    **Je veux** exporter notes/calendrier (PDF/CSV),  
    **Afin de** partager avec véto.  
    - **Critères d'acceptation** :  
      - Sélection par animal/période.  
      - Sécurisé.  
    - **Priorité** : Could-have.

## Module 4 : Intégration IA

13. **En tant que** utilisateur,  
    **Je veux** uploader photo pour identifier espèce,  
    **Afin de** fiche automatique.  
    - **Critères d'acceptation** :  
      - Upload sécurisé.  
      - IA renvoie espèce + probabilité.  
      - Suggestions ambigu.  
    - **Priorité** : Must-have.

14. **En tant que** éleveur,  
    **Je veux** analyse IA notes,  
    **Afin de** détecter anomalies.  
    - **Critères d'acceptation** :  
      - LLM : Résumé, alertes.  
      - Disclaimer.  
    - **Priorité** : Should-have.

15. **En tant que** éleveur,  
    **Je veux** prédictions IA events (mue),  
    **Afin de** anticiper.  
    - **Critères d'acceptation** :  
      - Basé historique + fiche.  
      - ML TensorFlow.  
    - **Priorité** : Could-have.

16. **En tant que** utilisateur,  
    **Je veux** chatbot IA questions,  
    **Afin de** conseils rapides.  
    - **Critères d'acceptation** :  
      - LLM Grok API.  
      - Basé fiches/data.  
    - **Priorité** : Could-have.

## Module 5 : Cybersécurité et Autres

17. **En tant que** utilisateur,  
    **Je veux** données protégées (RGPD),  
    **Afin de** privacy.  
    - **Critères d'acceptation** :  
      - Consentement IA/notes.  
      - Encryption.  
      - Supprimer compte.  
    - **Priorité** : Must-have.

18. **En tant que** administrateur,  
    **Je veux** dashboard modération,  
    **Afin de** qualité.  
    - **Critères d'acceptation** :  
      - Accès restreint.  
      - Logs.  
    - **Priorité** : Could-have.

19. **En tant que** utilisateur,  
    **Je veux** page accueil engageante,  
    **Afin de** inspiration.  
    - **Critères d'acceptation** :  
      - Carrousel top espèces.  
      - Disclaimers.  
    - **Priorité** : Should-have.

20. **En tant que** membre communauté,  
    **Je veux** commenter/forum,  
    **Afin de** échanger.  
    - **Critères d'acceptation** :  
      - Commentaires modérés.  
    - **Priorité** : Could-have.