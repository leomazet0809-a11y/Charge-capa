# Template de prompt : ajouter une activité

Copiez le bloc ci-dessous dans une nouvelle demande à Claude, remplacez les `[…]` et supprimez les lignes inutiles.
Plus les noms d'onglets et de colonnes sont **exacts** (copiés depuis l'export Excel), moins il y aura d'allers-retours.

---

```markdown
Ajoute une nouvelle activité « [Nom affiché, ex. Réception] » dans Charge Capa (index.html),
sur le modèle de « Prépa OF » et « Prépa Expéd » (définition dans ACT_DEFS).

## 1. Identité
- Identifiant : [ex. reception]  (sert pour ACT_DEFS, la source s-[id] et la gamme g-[id])
- Nom de l'onglet / titre : [ex. Réception]
- Position de l'onglet : [après Prépa Expéd / ailleurs]
- Un « dossier » (une ligne du tableau) = [ex. un bon de réception ; une commande par date…]
- Unité affichée (pluriel, ex. « OF », « commande(s) ») : [ex. réception(s)]
- Bulle d'aide de l'onglet : [ex. Affiche les réceptions à traiter et leur temps]

## 2. Fichier source
- Libellé de la source dans Paramètres › Fichiers sources : [ex. Réceptions fournisseurs]
- Même fichier qu'une activité existante ? [non / oui, celui de Prépa OF]
- Onglet(s) et colonnes utilisées (noms exacts) :
  - Onglet « [Nom onglet 1] » : [Col A], [Col B], [Col C], …
  - Onglet « [Nom onglet 2] » (facultatif) : [Col X], [Col Y], …
- Regroupement des lignes en dossiers : [ex. une ligne par valeur de « N° réception » ;
  ou par « Commande » + « Date »]
- Lignes à ignorer : [aucune / ex. Article commençant par 9 / Statut = Annulé]

## 3. Date de la période
- Colonne date filtrée par la période du ruban : [ex. Date réception prévue]
- Afficher en pastille rouge si la date est dépassée : [oui / non]

## 4. Bouton « En cours »
- Un dossier est considéré comme terminé (masqué par « En cours ») quand : [ex. Statut = « Soldé »
  sur toutes les lignes]

## 5. Colonnes du tableau (dans l'ordre)
| Colonne affichée | Origine / règle | Format |
|---|---|---|
| [Ex. Réception] | [colonne « N° réception », en gras] | texte |
| [Ex. Fournisseur] | [colonne « Fournisseur » ; valeurs différentes jointes par « / »] | texte |
| [Ex. Qté] | [somme de « Qté reçue »] | nombre |
| [Ex. Date prévue] | [colonne « Date réception prévue »] | date (rouge si dépassée) |
| [Ex. Urgent] | [Oui si au moins une ligne a « Priorité » = 1] | pastille rouge si Oui |
(Les colonnes Temps (h), Affectation et Date affectation sont ajoutées automatiquement.)

## 6. Gamme de temps (Paramètres › Temps gammes)
- Onglet des lignes : [ex. Réceptions]
- Colonne dossier : [ex. N° réception]
- Colonne quantité : [ex. Qté reçue]
- Découpage par colonne (facultatif) : [aucun / ex. Date réception prévue]
- Exclusion (facultatif) : colonne [ex. Article] commençant par [ex. 9]
- Tâches (type = Forfait | Ligne | Quantité | Calcul, temps en secondes) :
  - Forfait — [Nom de la tâche] — [90] s
  - Ligne — [Nom de la tâche] — [40] s
  - Quantité — [Nom de la tâche] — [5] s
  - Calcul — [Nom] — [colonne / table de valeurs → secondes, si besoin]

## 7. Capacité (facultatif)
- Groupes / niveaux du fichier de capacité à présélectionner : [aucun / ex. Groupe Réception › Niveau 1]

## 8. Consignes
- Les projets .xlsx existants doivent recevoir automatiquement la nouvelle source et la gamme
  (DEFAULT_SOURCES + ensureActivityDefaults), sans toucher aux réglages déjà présents.
- Ajoute une section « [N]. [Nom] » dans le README (même format que Prépa Expéd : description,
  tableau des colonnes, calcul du temps) et mets à jour la phrase listant les onglets.
- Vérifie que la page s'affiche sans erreur console, avec et sans fichier source chargé.
- [Autre précision : couleurs, colonnes masquées par défaut, tri par défaut…]

Si une information manque ou est ambiguë, pose-moi la question avant de coder.
```

---

## Pour aller plus vite

- **Joignez un extrait de l'export** (quelques lignes, données sensibles masquées) ou une capture des en-têtes :
  Claude pourra vérifier les noms de colonnes exacts.
- Le minimum indispensable : **sections 1, 2, 3, 4 et 6**. Sans section 5, Claude proposera des colonnes
  à partir de celles du fichier.
- Pour une activité qui **ressemble à une existante**, il suffit souvent d'écrire :
  « Comme Prépa Expéd, mais avec l'onglet `…`, la date `…` et ces tâches : … ».
