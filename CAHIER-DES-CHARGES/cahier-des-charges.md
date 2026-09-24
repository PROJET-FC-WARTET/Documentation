# Cahier des charges — Projet Wartet FC

**Version :** 1.0
**Date :** [24/09/2026]
**Client :** Royale Entente Wartet F.C.
**Contact :** [Frédéric]

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
- Gestion du calendrier et des événements.
- Gestion du stock (buvette, boutique).
- Signalement d'absence par les parents.
- Export de données (pour continuité en cas de panne).

### ❌ Hors périmètre (V1)
- Caisse enregistreuse connectée.
- E-commerce (vente en ligne).
- Application mobile native.

---

## 3. Acteurs et rôles

| Acteur | Rôle | Accès |
| :--- | :--- | :--- |
| **Admin / Webmaster** | Gérer le site et les comptes | Accès total, gestion des logs, sauvegardes, paramètres généraux |
| **Coordinateur** | Décisions sportives | Équipes, agendas, présences — **pas** de finances |
| **Coach** | Gérer son équipe | Équipe, présences, parents, modifier/annuler matchs, envoyer messages, stats joueurs, valider présences parentales |
| **Délégué au terrain** | Accueil, image du club | Agenda, contacts |
| **Gestionnaire Event** | Annonces, calendrier | Événements, pub |
| **Responsable club** | Chiffres, stock, fournisseurs | Données de gestion, validation inscriptions, communication globale (newsletter) |
| **Trésorier** | Gestion financière | Cotisations, paiements (rôle attribué au Responsable Club pour l'instant) |
| **Employé (buvette)** | Vente, stock | Stock, caisse |
| **Bénévole** | Aide ponctuelle | Pointage, inscription à des créneaux (à préciser) |
| **Arbitre** | Arbitrage des matchs | Consultation des joueurs en match, cartons (rouge/jaune) |
| **Joueurs / Parents** | Suivre son enfant / sa pratique | Calendrier, convocations, présences, mise à jour des coordonnées, consultation des documents (règlement) |

**Règles importantes :**
- Un utilisateur peut avoir **plusieurs rôles**.
- Le **Coordinateur** ne voit **pas** les données financières.
- Un **parent** ne voit **pas** les informations de l'autre parent (cas des divorces).
- La liste des acteurs doit être **extensible** (le club peut grandir).
- Les rôles **Joueurs** et **Parents** sont fusionnés.


---

## 4. Fonctionnalités principales

### 4.1 Site vitrine
- Page d'accueil "jour de match" (photo, slogan, prochain match).
- Présentation des équipes (U7 à l'équipe première).
- Actualités et annonces.
- Calendrier public des matchs et événements.

### 4.2 ERP — Gestion sportive
- Fiches des équipes et des joueurs.
- Gestion des présences (entraînements, matchs).
- Plan d'entraînement par équipe.
- Passerelles multi-équipes (un joueur peut évoluer dans plusieurs équipes).
- Rapports des coachs vers le coordinateur.

### 4.3 ERP — Vie du club
- Gestion des événements (tournois, soupers, festivités).
- Annonces publiables (avec lien Facebook/Instagram).
- Gestion du stock (buvette, boutique).
- Gestion des dotations aux joueurs (shorts, chaussettes, trainings).

### 4.4 Communication parents
- Consultation du calendrier.
- Réponse aux convocations.
- Signalement d'absence avec motif (ex: transport, maladie).

---

## 5. Contraintes techniques

- **Liberté technique totale** : le client n'impose ni langage, ni framework, ni base de données.
- Les données sensibles doivent être protégées (accès par rôle).
- Le système doit être **scalable** (passage de 4 à 10+ utilisateurs).
- En cas de panne, les données doivent pouvoir être **exportées** (continuité de service).

---

## 6. Zones d'ombre à clarifier avec le client

- [ ] Qui gère le réassort des stocks et la mise à jour des prix ?
- [ ] Qui attribue les dotations et comment on trace qui a reçu quoi ?
- [ ] Comment gère-t-on la mise à jour du catalogue des objets à vendre ?
- [ ] Les parents doivent-ils avoir un compte, ou tout passe-t-il par WhatsApp ?
- [ ] Quel est le rôle exact des **Bénévoles** ? (Que peuvent-ils voir ou faire ?)
- [ ] La fonctionnalité **Newsletter** est-elle confirmée ?
- [ ] L'**Arbitre** doit-il voir les cartons des matchs précédents pour gérer les suspensions ?
---

## 7. Livrables attendus

- Un site vitrine public responsive.
- Un ERP fonctionnel accessible par les rôles autorisés.
- Une documentation utilisateur.
- Un guide de déploiement.
