# UC-01 : Connexion d'un utilisateur

**Acteur principal :** Tous les utilisateurs (Admin, bénévoles,Coordinateur,Coach, Délégué au terrain,Gestionnaire Event,Responsable club,Employé (buvette),Parent,Joueur (majeur))
**Objectif :** Tous les utilisateurs (Admin, Bénévoles, Coordinateur, Coach, Délégué au terrain, Gestionnaire Event, Responsable club, Employé, Parent, Joueur majeur)
**Préconditions :** Avoir un compte créé par l'Admin

## Scénario nominal (étapes)
1. L'utilisateur accède au site web et clique sur le bouton "Se connecter".
2. Il saisit son nom d'utilisateur (ou e-mail) et son mot de passe.
3. Il clique sur le bouton "Se connecter".
4. Le système vérifie les identifiants en base de données.
5. Le système redirige l'utilisateur vers son tableau de bord (qui diffère selon son rôle).

## Scénarios alternatifs
- **4a. Identifiants incorrects :** Le système affiche un message d'erreur en rouge sous le champ de saisie : "Nom d'utilisateur ou mot de passe incorrect." Un bouton "Réinitialiser le mot de passe" apparaît.
- **2a. Mot de passe oublié :** L'utilisateur clique sur "Réinitialiser le mot de passe". Une nouvelle fenêtre s'ouvre. Il saisit son e-mail. Le système vérifie l'information et affiche : "Un e-mail de réinitialisation vous a été envoyé."

## Postconditions
L'utilisateur est connecté, sa session est active, et il est redirigé vers son tableau de bord.


## Éléments techniques (Backend)

> ⚠️ **Note :** Les éléments ci-dessous sont provisoires. Ils seront confirmés une fois la stack technique choisie (voir Issue #2).

- **Route(s) :** `POST /api/login`
- **Modèle(s) concerné(s) :** `User`
- **Tables impactées :** `users`