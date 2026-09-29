# UC-11 : Consultation des événements du club

**Acteur principal :** Tous les utilisateurs — visiteurs du site vitrine (non connectés) et utilisateurs connectés (Admin, Webmaster, Coordinateur, Coach, Délégué au terrain, Event Manager, Responsable club, Trésorier, Bénévole, Joueurs / Parents)
**Objectif :** Consulter la liste des événements du club (tournois, soupers, festivités…) à venir et passés, voir le détail d'un événement et pouvoir le partager sur les réseaux sociaux.
**Préconditions :** Aucune — la page est accessible au public, sans connexion. Les événements affichés ont été créés et publiés au préalable par l'Event Manager (voir UC-07 : Création d'un événement).

## Scénario nominal (étapes)
1. L'utilisateur arrive sur le site vitrine et clique sur « Actualités » / « Vie du club » dans le menu principal, ou sur le bouton « Découvrir la vie du club » de la page d'accueil.
2. Le système affiche la page « Événements » avec la liste des **événements à venir**, triés par date (le plus proche en premier).
3. Pour chaque événement, le système affiche une carte avec : le **visuel**, le **titre**, la **date**, l'**heure**, le **lieu** et le début de la **description**.
4. L'utilisateur peut filtrer la liste **par type** d'événement (tournoi, souper, festivité, match, autre) et/ou **par date** (mois, période).
5. Le système met à jour la liste selon les filtres choisis.
6. L'utilisateur clique sur un événement.
7. Le système affiche la fiche détaillée de l'événement : visuel en grand, titre, type, date, heure, lieu, description complète.
8. L'utilisateur clique sur le bouton « Partager » (Facebook ou Instagram).
9. Le système ouvre la fenêtre de partage du réseau social choisi avec le lien de l'événement pré-rempli.

## Scénarios alternatifs
- **2a. Aucun événement programmé :** Le système affiche le message « Aucun événement programmé » à la place de la liste, avec un lien vers le calendrier des matchs.
- **4a. Consultation des événements passés :** L'utilisateur clique sur l'onglet « Événements passés ». Le système affiche les événements déjà terminés, triés du plus récent au plus ancien.
- **5a. Aucun résultat pour les filtres choisis :** Le système affiche « Aucun événement ne correspond à votre recherche » et un bouton « Réinitialiser les filtres ».
- **6a. Événement supprimé ou introuvable :** L'utilisateur ouvre le lien d'un événement qui n'existe plus (ex : lien partagé). Le système affiche « Cet événement n'est plus disponible » et redirige vers la liste des événements.
- **7a. Événement sans visuel :** Le système affiche une image par défaut aux couleurs du club (logo Wartet sur fond vert/noir).
- **9a. Partage impossible :** Le réseau social ne répond pas ou le navigateur bloque la fenêtre. Le système affiche un bouton « Copier le lien » pour que l'utilisateur puisse partager l'événement manuellement.

## Postconditions
L'utilisateur voit la liste des événements du club (à venir et passés) et peut consulter le détail de chacun. Aucune donnée n'est modifiée en base (consultation uniquement). Si l'utilisateur a partagé un événement, le lien est publié sur le réseau social choisi.

## Éléments techniques (Backend)

> ⚠️ **Note :** Les éléments ci-dessous sont provisoires. Ils seront confirmés une fois la stack technique choisie (voir Issue #2) et le schéma de base de données validé (voir Issue #4).

- **Route(s) :**
  - `GET /api/evenements?statut=a-venir|passe&type=...&date_debut=...&date_fin=...` (liste filtrée)
  - `GET /api/evenements/{id}` (détail d'un événement)
- **Modèle(s) concerné(s) :** `Evenement`
- **Tables impactées :** `evenements` (lecture seule) — champs utilisés : `id`, `titre`, `type`, `description`, `date_evenement`, `heure`, `lieu`, `visuel_url`, `publie`
- **Règles :**
  - Route publique : aucune authentification requise.
  - Seuls les événements publiés (`publie = true`) sont renvoyés.
  - Aucune donnée personnelle (joueurs, parents, bénévoles) ni financière (`prix_ticket`, recettes) n'est exposée par ces routes.
