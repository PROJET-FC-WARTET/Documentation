# Index des Use Cases

Ce fichier liste tous les Use Cases du projet avec leur numéro, leur titre et leur statut.

> ⚠️ **Règles importantes :**
> - **Ne jamais réutiliser un numéro déjà attribué.**
> - Toujours ajouter le nouveau numéro à la fin de la liste.
> - Mettre à jour ce fichier à chaque création ou fermeture d'un UC.

**Dernier numéro attribué : UC-30**
**Prochain numéro disponible : UC-31**

⚠️ **  ** ⚠️

---

## Légende des statuts

| Statut | Signification |
| :--- | :--- |
| 📝 À faire | UC identifié mais non rédigé |
| 🔄 En cours | UC en cours de rédaction (assigné) |
| 👀 En revue | UC rédigé, en attente de validation |
| ✅ Terminé | UC validé et intégré au projet |
| ❌ Fermé | UC annulé ou obsolète |

---

## Liste des Use Cases

| # | Titre | Statut | Issue | Fichier | En attente de vérification ? |
| :--- | :--- | :--- | :--- | :--- | :--- |
| UC-01 | Connexion d'un utilisateur | ✅ Terminé | #6 | `UC-01-connexion.md` | ✅ Terminé
| UC-02 | Création d'un compte par l'Admin | 📝 À faire | #29 | `UC-02-creation-compte.md` | 
| UC-03 | Attribution des rôles à un utilisateur | 📝 À faire | #8 | `UC-03-attribution-roles.md` |  
| UC-04 | Déconnexion d'un utilisateur | 📝 À faire | #9 | `UC-04-liaison-Acteur-CDI.md` |
| UC-05 | Consultation de la liste des joueurs | ❌ Fermé | #32 | `UC-05-Consultation-liste-joueurs.md` |✅ Terminé
| UC-06 | Supprimer un utilisateur | 📝 À faire | #33 | `UC-06-supprimer-utilisateur.md` |
| UC-07 | Créer une sauvegarde de la DB | 📝 À faire | #34 | `UC-07-sauvegarde-DB.md` |
| UC-08 | Signalement d'absence avec motif | ✅ Terminé | #13 | `[Docs]-08-Signalement_dabsence.md #26` | ✅ Terminé  
| UC-09 | Réponse à une convocation | ✅ Terminé mais à modifier | #14 | `[Docs]09-Reponse-convoc.md` | ✅ Terminé
| UC-10 | Consultation des informations de son enfant | ✅ Terminé | #15 | `UC-10-informations-enfant.md` | ✅ Terminé
| UC-11 | Consultation des événements du club | ✅ Terminé | #16 | `UC-11-consultation-evenements.md` | ❌
| UC-12 | Gestion du planning des événements | 📝 À faire | #39 | `UC-12-consultation-actualites.md` |
| UC-13 | Supprimé
| UC-14 | Accès au planning | 📝 À faire | #41 | `UC-14-AccesPlanning.md` |
| UC-15 | Ajout d'articles au stock | 📝 À faire | #42 | `UC-15-Ajout-Articles-stock.md` |
| UC-16 | Décrémentation d'articles au stock buvette | 📝 À faire | #43 | `UC-16-Decrementation-Articles-stock.md` |
| UC-17 | Accès aux recettes financières du club | ❌ Fermé | #44 | `UC-17-Acces-recettes-financieres-club.md` |
| UC-18 | Vérification de l'ordre des cotisations | 📝 À faire | #45 | `UC-18-Verification-ordre-cotisations.md` |
| UC-19 | Relance des parents/joueurs pour cotisations | 📝 À faire | #46  `UC-19-Relance-Parents/Joueurs-cotisations.md` |
| UC-20 | À été supprimé de la liste | | | | ❌ Fermé | 
| UC-21 | À été supprimé de la liste | | | | ❌ Fermé | 
| UC-22 | Gestion des présences | 📝 À faire | #52 |  `UC-22-Gestion-présences.md` |
| UC-23 | Gestion des horaires et réservation des terrains | 📝 À faire | #53 |  `UC-23-Gestion-horraire&reservation-terrain.md` |
| UC-24 | Canal de communication Coach-Joueurs | ❌ Fermé | #54 |  `UC-24-Canal-Communication-CoachJoueurs.md` |
| UC-25 | Visionner les statistiques des joueurs | 📝 À faire | #55 |  `UC-25-Visionner-Stats-Joueurs.md` |
| UC-26 | Modification du planning des événements par l'Event Manager | 📝 À faire | #63 |  `ShemaUC-26-ModificationPlanningEvenement-EVENTMANAGER.md` |
| UC-27 | Planification logistique d'un événement par l'Event Manager | 📝 À faire | #64 |  `SchemaUC-27-PlanificationLogistiqueEvenement-EVENTMANAGER.md` |
| UC-28 | Traitement des modifications critiques de planning par le Responsable | 📝 À faire | #65 |  `SchemaUC-28-TraitementModificationsCritiquesPlanning-RESPONSABLE.md` |
| UC-29 | Modification du horaires des coachs par le Coordinateur | 📝 À faire | #66 |  `SchemaUC-29-ModificationsHorrairesCoach-COORDINATEUR.md` |
| UC-30 |  Ajouter des bénévoles au planning | 📝 À faire | #67 |  `SchemaUC-30-AjoutBenevolesPlanning.md` |


---
## À ajouter

...

## À modifier
Fichier à vérifier, UC-03 non complet et mis dans  "closed" => pourquoi ? 
Est ce que l'on garde le UC ? Est ce qu'on doit le renommer ? Le supprimer ? 

## Comment ajouter un nouveau Use Case ?

1.  Vérifiez le **prochain numéro disponible** en haut de ce fichier (actuellement UC-30).
2.  Créez une nouvelle Issue avec le titre `[Use Case] UC-XX : Titre`.
3.  Une fois l'UC rédigé et validé, ajoutez une ligne dans le tableau ci-dessus.
4.  Mettez à jour le **prochain numéro disponible** en haut du fichier.

---

## Historique des mises à jour

| Date | Modification |
| :--- | :--- |
| 01/10/2026 | Création de l'index avec les UC-01 à UC-32 |
| 06/10/2026 | Modification de la numérotation des UC de 1 à 11 + suppression des issues doublons mais non traités + liaison en doulon des issues liées et traitées.
| 21/10/2026 | Modification des UC qui n'étaient plus à jour + Suppression des UC hors scope + ajouts des UC de 12 à 25 + Mise en attente de 17 & du 24 |
| 28/10/2026 | Ajouts des derniers UC venant de la liste : `Liste  création ISSUES à vérifier`. |