# UC-10 : Consultation des informations de son enfant

**Acteur principal :** Parent
**Objectif :** Consulter les informations de son enfant (profil, calendrier, présences, convocations)
**Préconditions :**  Être connecté en tant que Parent

## Scénario nominal (étapes)
1. Le parent accède à la section "mes enfants"
2. Le système affiche la liste des enfants rattachés à ce compte uniquement
3. Le parent sélectionne un enfant
4. Le système affiche le détail : nom, prénom, équipe, calendrier, présences, convocations

## Scénarios alternatifs
- **1a. aucun enfant associé au compte :** Le système affiche un message d'erreur et envoie une erreur à l'admin du site
- **1b. plusieurs enfants associé :** Le parent choisit parmi la liste affichée
- **3a. Tentative d'accès à un enfant non rataché :** Si le parent tente d'accéder aux information d'un enfant qui n'est pas le sien, le système refuse l'accès et affiche une erreur

## Postconditions
Le parent voit les informations de son/ses enfant(s) uniquement

## Éléments techniques (Backend)
- **Route(s) :** [Ex: POST /login]
- **Modèle(s) concerné(s) :** [Ex: User]
- **Tables impactées :** [Ex: users]