# Cahier des charges — Projet Wartet FC

**Version :** 1.0
**Date :** [19/09/2026]
**Client :** Royale Entente Wartet F.C.
**Contact :** [Frédéric]

---

## 1. Contexte et objectifs

Le club Wartet FC souhaite se doter d'un **site web vitrine** et d'un **ERP (gestionnaire de club)** pour :
- Moderniser son image (inspiration Premier League, ambiance "jour de match").
- Centraliser la gestion sportive (équipes, présences, agendas).
- Faciliter la communication avec les parents.
- Gérer la vie du club (événements, buvette, dressing).

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
- Pas d'arbitrage.
---

## 3. Acteurs et rôles

| Acteur | Rôle | Accès | Accès refusé | 
| :--- | :--- | :--- | :--- |
| **Admin / Webmaster** | Gérer le site et les comptes | Accès total | — |
| **Coordinateur** | Décisions sportives | Équipes, agendas, présences — **pas** de finances | Trésorerie, vente de produits, stock |
| **Coach** | Gérer son équipe | Équipe, présences, parents | Autres équipes, finances |
| **Délégué au terrain** | Accueil, image du club | Agenda, contacts | Finances, admin |
| **Gestionnaire Event** | Annonces, calendrier | Événements, pub | Données sportives sensibles |
| **Responsable club** | Chiffres, stock, fournisseurs | Données de gestion | À préciser |
| **Employé (buvette)** | Vente, stock | Stock, caisse | Gestion sportive |
| **Bénévole** | Aide ponctuelle | Pointage | Tout le reste |
| **Parent** | Suivre son enfant | Ses enfants uniquement | Informations de l'autre parent, autres enfants  - tout ce qui concerne la gestion du club.|
| **Joueur (majeur)** | Suivre sa pratique | Ses données | tout ce qui concerne la gestion du club. |

**Règles importantes :**
- Un utilisateur peut avoir **plusieurs rôles**.
- Le **Coordinateur** ne voit **pas** les données financières.
- Un **parent** ne voit **pas** les informations de l'autre parent (cas des divorces).
- La liste des acteurs doit être **extensible** (le club peut grandir).

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

---

## 7. Livrables attendus

- Un site vitrine public responsive.
- Un ERP fonctionnel accessible par les rôles autorisés.
- Une documentation utilisateur.
- Un guide de déploiement.
