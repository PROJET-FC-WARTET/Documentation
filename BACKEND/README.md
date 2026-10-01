# BACKEND — Documentation technique du code

Ce dossier contient la **documentation technique** liée au code backend du projet Wartet FC. Il ne contient **pas de code** (celui-ci vit dans le dépôt `Backend`), mais des documents de référence pour comprendre et maintenir le code.

## Rôle

- Documenter l'architecture du code backend.
- Décrire les routes de l'API et leurs paramètres.
- Expliquer les mécanismes d'authentification et de sécurité.
- Servir de référence pour les développeurs qui rejoignent le projet.

## Contenu attendu

| Fichier / Dossier | Description |
| :--- | :--- |
| `api-endpoints.md` | Liste des routes de l'API (méthode, URL, paramètres, réponses) |
| `auth-flow.md` | Description du flux d'authentification (login, 2FA, sessions) |
| `architecture.md` | Schéma de l'architecture du backend (services, dépendances) |
| `conventions.md` | Conventions de nommage, structure des dossiers, bonnes pratiques |
| `images/` | Schémas et captures d'écran liés à la documentation technique |

## Relation avec les autres dossiers

- **`../MODELE-DONNEES/`** : la structure de la base de données (MCD, MLD).
- **`../USE-CASES/`** : les spécifications fonctionnelles.
- **`../CAHIER-DES-CHARGES/`** : les besoins du client.

## Règles

- La documentation doit être **tenue à jour** à chaque évolution du code.
- Utilisez le **Markdown** pour tous les fichiers.
- Les diagrammes doivent utiliser **Mermaid** (recommandé) ou des images (dans `images/`).
- Les noms de fichiers sont en **minuscules** avec des tirets : `api-endpoints.md`.

## ⚠️ Note

Ce dossier est actuellement **vide**. Il sera rempli au fur et à mesure que le code backend sera développé.
