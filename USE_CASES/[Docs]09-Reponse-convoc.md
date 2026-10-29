# UC-09 : Réponse à une convocation

**Acteur principal :** Parent
**Objectif :** Répondre "présent" ou "absent" à une convocation
**Préconditions :** être connecté en tant que parent, avoir reçu une convocation

## Scénario nominal (étapes)
1. Le parent accède à la liste de ses convocations.
2. Il sélectionne une convocation.
3. Le système affiche le détail : événement, date, heure, lieu, équipe.
4. Le parent clique sur « Présent ».
5. Le système enregistre la réponse et affiche un message de confirmation.
6. Le système rend la réponse visible pour le coach.

## Scénarios alternatifs
- **4a. Réponse « Absent » :** Le parent clique sur « Absent ». Le système demande un motif. Le parent le saisit et valide, puis on reprend à l'étape 5.
- **4b. Modification de la réponse :** Le parent rouvre une convocation déjà traitée et change sa réponse. Le système met à jour la réponse et informe le coach.
- **4c. Réponse en retard :** La date limite de réponse est dépassée ou l'événement a déjà eu lieu. Le système affiche « Cette convocation n'est plus modifiable. »
- **4d. Absence de réponse :** Le parent ne répond pas dans le délai prévu (à définir). Le système envoie une relance automatique.
- **2a. Convocation d'un autre enfant :** Un parent ne voit et ne peut répondre qu'aux convocations de ses propres enfants.

## Postconditions
La réponse (présent ou absent +motif) est enregistrée et visible par le coach.

## Éléments techniques (Backend)
- **Route(s) :** [Ex: POST /login]
- **Modèle(s) concerné(s) :** [Ex: User]
- **Tables impactées :** [Ex: users]