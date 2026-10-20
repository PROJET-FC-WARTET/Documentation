# UC-08 : 

**Acteur principal :** Parent ou enfants majeur
**Objectif :** Signaler qu'un joueur sera absent à un entraînement ou un match
**Préconditions :** Être connecté en tant que Parent ou enfant majeur



## Scénario nominal (étapes)
1. L'utilisateur accède au calendrier ou à la liste des événements (matchs/entraînements).
2. L'utilisateur sélectionne le joueur concerné (si le compte gère plusieurs enfants).
3. L'utilisateur sélectionne l'événement concerné.
4. L'utilisateur choisit le statut : Présent ou Absent.
5. (Optionnel) En cas d'absence, l'utilisateur saisit un motif ou un commentaire de justification.
6. L'utilisateur valide son choix.

## Scénarios alternatifs
- **3a. Modification du statut :** L'utilisateur revient sur un événement déjà renseigné et modifie son statut (passe de "Absent" à "Présent").

## Postconditions
- Le statut du joueur pour l'événement est mis à jour en base de données.
- L'entraîneur/coach est notifié de la modification (ou consulte le récapitulatif mis à jour).

## Éléments techniques (Backend) (Pas encore fait)
- **Route(s) :** [Ex: POST /login]
- **Modèle(s) concerné(s) :** [Ex: User]
- **Tables impactées :** [Ex: users]