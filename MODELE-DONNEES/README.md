# MODELE-DONNEES — Conception de la base de données

Ce dossier contient la **conception de la base de données** du projet Wartet FC : le Modèle Conceptuel de Données (MCD), le Modèle Logique de Données (MLD) et les schémas associés.

## Rôle

- Définir la structure des données du projet.
- Servir de référence pour la création des migrations et des modèles dans le dépôt `Backend`.
- Documenter les tables, leurs champs et leurs relations.

## Contenu attendu

| Fichier / Dossier | Description |
| :--- | :--- |
| `DB_V0.md` | Version 0 du schéma de la base de données (MCD + MLD) |
| `DB_V1.md` | Version 1 (à venir, après validation des Use Cases) |
| `images/` | Schémas exportés (MCD, MLD, diagrammes ER) |
| `dictionnaire-donnees.md` | Description détaillée de chaque table et champ (à venir) |

## Convention de nommage des images

| Type | Convention | Exemple |
| :--- | :--- | :--- |
| **MCD** | `mcd-vX.png` | `mcd-v0.png` |
| **MLD** | `mld-vX.png` | `mld-v0.png` |
| **Diagramme ER** | `er-vX.png` | `er-v0.png` |

**Règles :**
- Tout en minuscules.
- Pas d'espaces (tirets `-`).
- Pas d'accents.

## Relation avec les autres dossiers

- **`../USE-CASES/`** : les Use Cases qui déterminent les besoins en données.
- **`../BACKEND/`** : la documentation technique qui utilisera ce modèle.
- **`../CAHIER-DES-CHARGES/`** : les besoins du client.

## Règles

- Le schéma est **versionné** : chaque évolution majeure donne une nouvelle version (`DB_V1.md`, `DB_V2.md`, etc.).
- Les diagrammes sont rédigés en **Mermaid** (recommandé) pour être versionnables.
- Si vous utilisez des images, placez-les dans `images/` et respectez la convention de nommage.
- Le schéma doit respecter les **règles métier** définies dans le cahier des charges (multi-rôles, RGPD, confidentialité, etc.).

## Historique des versions

| Version | Date | Modifications |
| :--- | :--- | :--- |
| V0 | 26/09/2026 | Version initiale (schéma de base) |
