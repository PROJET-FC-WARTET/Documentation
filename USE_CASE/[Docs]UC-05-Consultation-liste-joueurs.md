# UC-05 : Consultation de la liste des joueurs

**Acteur principal :** Coach
**Objectif :** Consulter les joueurs de son équipe ou de ses équipes et leurs informations autorisées.
**Préconditions :** Être connecté en tant que Coach et être associé à au moins une équipe.

## Scénario nominal (étapes)

1. Le Coach accède à la liste de ses équipes.
2. Le système affiche les équipes auxquelles il est associé.
3. Le Coach sélectionne une équipe.
4. Le système vérifie que le Coach est autorisé à consulter l'équipe et affiche ses joueurs actifs.
5. Le système affiche pour chaque joueur : nom, prénom, date de naissance, âge, photo si disponible et informations parentales selon les droits.

## Scénarios alternatifs

2a. Aucune équipe :** Le système affiche « Aucune équipe ne vous est attribuée. »
3a. Accès non autorisé :** Le système refuse l'accès à l'équipe sélectionnée.
4a. Aucun joueur :** Le système affiche « Aucun joueur ».
5a. Photo indisponible :** Aucune photo n'est affichée.
5b. Informations parentales non autorisées :** Ces informations ne sont pas affichées.

## Postconditions

Le Coach consulte la liste des joueurs actifs de l'équipe sélectionnée avec les informations auxquelles il est autorisé à accéder.


## Éléments techniques (Backend)
- **Route(s) :** [Ex: POST /login]
- **Modèle(s) concerné(s) :** [Ex: User]
- **Tables impactées :** [Ex: users]