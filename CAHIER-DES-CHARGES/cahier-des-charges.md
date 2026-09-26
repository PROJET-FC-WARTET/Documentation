# Cahier des charges — Projet Wartet FC

**Version :** 2.1
**Date :** 26/09/2026
**Client :** Royale Entente Wartet F.C.
**Contact :** Frédéric

---

## 1. Contexte et objectifs

Le club Wartet FC souhaite se doter d'un **site web vitrine** et d'un **ERP (gestionnaire de club)** pour :
- Moderniser son image (inspiration Premier League, ambiance "jour de match").
- Centraliser la gestion sportive (équipes, présences, agendas).
- Faciliter la communication avec les parents.
- Gérer la vie du club (événements, buvette, boutique).

**Mot d'ordre :** *"Make Wartet feel like a club."*

---

## 2. Périmètre

### ✅ Inclus dans le périmètre (V1)
- Site vitrine public (présentation, actualités, calendrier).
- ERP interne (gestion sportive, présences, événements).
- Gestion des acteurs et des rôles (multi-rôles possibles).
- Gestion du calendrier et des événements (planifiable 1 an à l'avance).
- Gestion du stock (buvette, boutique).
- Signalement d'absence par les parents (avec note jointe).
- Export de données (pour continuité en cas de panne).
- Gestion du RGPD (consentement, formulaire, garantie par l'Admin).
- Gestion de l'équipement du coach (liste de matériel).
- Programmation des matchs et événements sur 1 an.

### ❌ Hors périmètre (V1)
- Caisse enregistreuse connectée (aucun couplage).
- E-commerce (aucune vente ou location en ligne).
- Billetterie en ligne.
- Application mobile native.
- Arbitrage (rôle supprimé).
- QR Code pour la gestion du stock (à étudier pour une V2).

---

## 3. Identité visuelle et charte graphique

### Couleurs du club

| Élément | Code hex | Rôle |
| :--- | :--- | :--- |
| **Vert Wartet** | `#1b4d3e` | Couleur principale |
| **Jaune Wartet** | `#ffd700` | Couleur secondaire / accents |
| **Noir** | `#0b0b0b` | Fond principal |
| **Anthracite** | `#161616` | Cartes / fond secondaire |
| **Blanc** | `#f4f4f4` | Texte principal |
| **Gris clair** | `#dcdcdc` | Texte secondaire |

### Typographie
- **Police :** Montserrat (Google Fonts)
- **Graisses :** 300, 600, 800, 900, italique 400

### Ton éditorial et slogans
- « MORE THAN FOOTBALL. ONE FAMILY. »
- « MAKE WARTET FEEL LIKE A CLUB. »
- « Ici, on joue au football. Ici, on se connaît. »
- **Ton :** Direct, populaire, chaleureux, fier.

### Inspiration
- Liverpool FC / Premier League : identité forte, photos immersives, grandes typographies, atmosphère de stade, résultats visibles, sentiment d'appartenance.

---

## 4. Acteurs et rôles

| Acteur | Rôles |
| :--- | :--- |
| **ADMIN** | Ajouter & supprimer des acteurs ** Accès complet à la DB ** Gestion des rôles/permissions (attribuer un rôle à un utilisateur) ** Gestion des sauvegardes ** Garant du RGPD |
| **WEBMASTER** | Gestion des paramètres généraux du site (textes, logo, configuration) ** Accès aux logs/historique des actions (qui a fait quoi) |
| **Coordinateur** | Gestion des équipes de jeunes (et lien avec l'équipe fanion). ** Plan annuel : Il définit la stratégie sportive. ** Gestion des joueurs : Il les déplace d'une équipe à une autre. ** Supervision des coachs : Il vérifie que le travail est fait. ** Logistique : Il s'assure que les équipes sont équipées. ** Calendrier officiel : Il gère les déplacements de matchs et modifie le calendrier officiel. |
| **Coach** | Accès au calendrier des matchs ** Gestion des présences ** Liste des équipes in/out ** Liste des matchs ** Liste des équipes et des joueurs ** Liste des terrains ** Modifier/annuler un match ou un entraînement ** Envoyer des messages/notifications à son équipe ** Accès aux statistiques des joueurs (performance, blessures) ** Droit de valider les présences déclarées par les parents ** Émettre un avis sur un joueur (visible uniquement par le Coordinateur) |
| **Délégué au terrain** | Accueil, image du club ** Agenda, contacts |
| **Event Manager (communication)** | Ajouter & suppression d'un événement/matchs/résumés sur le site ** Accès au calendrier 1 an à l'avance |
| **Responsable club** | Accès aux chiffres ** Gestion financière (cotisations, factures) ** Stock ** Fournisseurs ** Organiser - afficher les visuels pour les événements du club ** Validation des inscriptions de nouveaux membres/joueurs |
| **Trésorier** | Gestion financière (cotisations, paiements) — rôle cumulable, attribué au Responsable Club pour l'instant |
| **Bénévole** | Log-in/out ** Système de pointage ** Accès à un planning de bénévolat ** Consultation des besoins en bénévoles par événement ** Retirer - Ajouter au stock (accès modulable par l'Admin) |
| **Joueurs / Parents** | Signaler sa présence ou son absence ** Contacter le coach ** Voir le calendrier spécifique à l'enfant/événement ** Mise à jour des coordonnées/infos de l'enfant ** Consultation des documents (règlement) |

### Règles importantes
- Un utilisateur peut avoir **plusieurs rôles** (ex: Parent + Bénévole, Responsable + Trésorier).
- Le **Coordinateur** ne voit **pas** les données financières.
- Un **parent** ne voit **pas** les informations de l'autre parent (cas des divorces).
- La liste des acteurs doit être **extensible** (le club peut grandir).
- Les rôles **Joueurs** et **Parents** sont fusionnés.
- L'**Admin** est le **garant du RGPD**.
- Le **Webmaster** gère l'aspect technique et la configuration du site.

---

## 5. Fonctionnalités principales

### 5.1 Site vitrine
- Page d'accueil "jour de match" (photo, slogan, prochain match).
- Présentation des équipes (U7 à l'équipe première).
- Actualités et annonces.
- Calendrier public des matchs et événements.

### 5.2 ERP — Gestion sportive
- Fiches des équipes et des joueurs.
- Gestion des présences (entraînements, matchs).
- Plan d'entraînement par équipe.
- Passerelles multi-équipes (un joueur peut évoluer dans plusieurs équipes).
- Rapports des coachs vers le coordinateur.
- Avis du coach sur les joueurs (visible uniquement par le Coordinateur).
- Gestion de l'équipement du coach (liste de matériel : cônes, haies, ballons, échelles…).

### 5.3 ERP — Vie du club
- Gestion des événements (tournois, soupers, festivités).
- Annonces publiables (avec lien Facebook/Instagram).
- Gestion du stock (buvette, boutique) — **hors vente en ligne**.
- Gestion des dotations aux joueurs (shorts, chaussettes, trainings).
- Programmation des matchs et événements sur 1 an à l'avance.

### 5.4 Communication parents
- Consultation du calendrier.
- Réponse aux convocations.
- Signalement d'absence avec motif (ex: transport, maladie) et note jointe.
- Contact du coach via le site.

### 5.5 RGPD et conformité
- L'Admin peut cocher "Soumis au RGPD" à la création d'un compte.
- L'utilisateur (ou son représentant légal) doit signer un formulaire de consentement.
- Mention dans le règlement d'ordre intérieur.
- L'Admin est le garant du RGPD.

---

## 6. Contraintes techniques

- **Liberté technique totale :** le client n'impose ni langage, ni framework, ni base de données.
- Les données sensibles doivent être protégées (accès par rôle).
- Le système doit être **scalable** (passage de 4 à 10+ utilisateurs).
- En cas de panne, les données doivent pouvoir être **exportées** (continuité de service).
- Le calendrier doit être planifiable **1 an à l'avance**.

---

## 7. Zones d'ombre à clarifier avec le client

| Point | Statut | Décision / Action |
| :--- | :--- | :--- |
| **Arbitrage** | ✅ Résolu | Rôle supprimé, n'existe plus. |
| **Trésorier** | ✅ Résolu | Rôle cumulable, peut être attribué à une personne. |
| **Caisse enregistreuse** | ✅ Résolu | Hors scope, aucun couplage. |
| **Communication parents** | ✅ Résolu | Via le site, avec note jointe. |
| **Vente / Location en ligne** | ✅ Résolu | Aucune. |
| **Billetterie en ligne** | ✅ Résolu | Hors périmètre. |
| **Calendrier** | ✅ Résolu | Planifiable 1 an à l'avance. |
| **Event Manager** | ✅ Résolu | Rôle confirmé, séparé de l'Admin. |
| **RGPD** | ✅ Résolu | L'Admin gère le consentement, formulaire à signer. |
| **Avis du Coach** | ✅ Résolu | Visible uniquement par le Coordinateur. |
| **Cumul de rôles** | ✅ Résolu | Un utilisateur peut avoir plusieurs rôles. |
| **Bénévoles (vente)** | ❓ À préciser | Le client pense qu'ils doivent pouvoir vendre, mais l'accès doit être modulable par l'Admin. |
| **Liste du matériel** | ❓ À trancher | Statique ou dynamique ? Qui peut ajouter un type de matériel ? |
| **Typographie du site** | ❓ À trancher | L'Event Manager ou l'Admin peut-il modifier la typographie ? |
| **QR Code** | ❓ À étudier | Étude de faisabilité Node.js proposée. V2 ? |
| **Dotations** | ❓ À trancher | Qui attribue ? Comment trace-t-on ? |
| **Matchs amicaux** | ❓ À trancher | À gérer dans le calendrier ? |

---

## 8. Livrables attendus

- Un site vitrine public responsive.
- Un ERP fonctionnel accessible par les rôles autorisés.
- Une documentation utilisateur.
- Un guide de déploiement.

---

## 9. Historique des versions

| Version | Date | Modifications |
| :--- | :--- | :--- |
| 1.0 | 19/09/2026 | Version initiale |
| 2.1 | 26/09/2026 | Suppression du rôle Employé, séparation Admin/Webmaster, confirmation hors périmètre vente/billetterie en ligne |