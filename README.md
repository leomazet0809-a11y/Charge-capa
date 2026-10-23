# Charge Capa – Guide utilisateur

**Charge Capa** sert à gérer la charge et la capacité des activités de la Logistique Aval.
L'application s'ouvre dans **Google Chrome** ou **Microsoft Edge** sur PC et fonctionne **sans connexion internet**.

---

## 1. Installer l'application

1. Sur la page GitHub du projet, cliquez sur **Code › Download ZIP**.
2. Décompressez le ZIP dans un dossier Windows de votre choix (par exemple `C:\Outils\Charge Capa`).
3. Gardez **tous les fichiers ensemble** : `index.html` a besoin des dossiers `lib` et `fonts`.
4. Double-cliquez sur `index.html`. Si le fichier s'ouvre dans un autre navigateur, faites un clic droit › **Ouvrir avec** › Chrome ou Edge.

> Astuce : créez un raccourci de `index.html` sur le bureau ou épinglez l'onglet dans le navigateur.

L'application est aussi disponible en ligne sur GitHub Pages ; elle fonctionne alors de la même façon.

## 2. Le ruban (en haut de l'écran)

| Élément | Rôle | Raccourci |
|---|---|---|
| Logo + nom en gras | Nom du classeur projet ouvert | – |
| Pastille d'état | ✔ vert : enregistré · ● orange : modifications non enregistrées · ⟳ : enregistrement en cours · ⚠ rouge : échec | – |
| Flèche retour | Annule la dernière modification | Ctrl + Z |
| Disquette | Enregistre le projet | Ctrl + S |
| Cadre | Plein écran (re-cliquer pour quitter) | Ctrl + Maj + F |
| Engrenage | Ouvre les Paramètres | Ctrl + , |

Sous le ruban, les onglets : **Prépa OF** à gauche (onglet affiché à l'ouverture) ; **Fichiers sources**, **Temps gammes** et **Paramètres** à droite.

Laissez la souris **2 secondes** sur un bouton pour voir une bulle d'aide (nom, rôle, raccourci).

## 3. Le classeur projet (.xlsx)

Tout votre paramétrage est enregistré dans un **classeur Excel** dont vous choisissez l'emplacement.

- **Paramètres › Nouveau classeur…** : choisissez un dossier et un nom (par défaut `Charge Capa.xlsx`).
- **Paramètres › Ouvrir un classeur…** : reprenez un classeur projet existant.
- **Paramètres › Enregistrer sous…** : faites une copie sous un autre nom ou dans un autre dossier.
- **Ctrl + S** ou la **disquette** : enregistre dans le classeur en cours. S'il n'y en a pas encore, l'application vous demande où le créer.

Au lancement suivant, l'application propose de **reprendre le dernier projet** : cliquez sur **Ouvrir** puis acceptez l'autorisation du navigateur (c'est une sécurité de Chrome/Edge, elle est demandée une fois par session).

⚠ **Fermez le classeur projet dans Excel avant d'enregistrer** : Windows bloque l'écriture d'un fichier ouvert dans Excel. La pastille d'état passe alors en rouge ; fermez Excel et refaites Ctrl + S.

Si vous fermez l'onglet avec des modifications non enregistrées, le navigateur vous prévient.

## 4. Paramètres

- **Classeur projet** : ouvrir, créer, enregistrer sous (voir ci-dessus).
- **Apparence** : thème *Clair*, *Sombre* ou *Comme Windows* (suit le réglage de Windows).
- **Polices d'écriture** : choix de la police (Inter, Segoe UI, Aptos, Bahnschrift, Calibri, Arial) et de la taille du texte, avec aperçu.

## 5. Fichiers sources

Chaque ligne relie une **activité** (ex. *Prépa OF*) à un **fichier source** Excel (.xlsx, .xls) ou CSV et à une **gamme** de temps.

| Colonne | Rôle |
|---|---|
| Libellé | Nom libre de la source |
| Activité | Activité alimentée par ce fichier, ou « — Base de données » pour un fichier complémentaire (ex. future base des DN) |
| Fichier source | Cliquez pour choisir le fichier dans un dossier Windows |
| Date du fichier | Date de dernière modification du fichier |
| Dernier chargement | Date à laquelle l'application a lu le fichier |
| État | *Chargé* (nombre de lignes lues, détail par onglet dans la bulle), *Modifié* (le fichier a changé : cliquez sur Recharger), *Autoriser la lecture*, *Erreur* |
| Gamme | Gamme de temps (onglet Temps gammes) appliquée à l'activité |

- Le bouton **⟳** relit un fichier ; **Tout recharger** relit tous les fichiers.
- Au lancement, les fichiers sont relus automatiquement si le navigateur l'autorise ; sinon cliquez sur **Autoriser la lecture**.
- Les données lues restent dans le navigateur : elles **ne sont pas copiées** dans le classeur projet (seuls le nom du fichier et les dates le sont).
- Pour les CSV, le séparateur (`;` ou `,`) et l'encodage (UTF-8 ou ANSI) sont détectés automatiquement.

## 6. Temps gammes

L'onglet s'ouvre sur un **récapitulatif des gammes par activité** : pour chaque activité, ses gammes (associées dans *Fichiers sources*) avec le fichier source, le nombre de tâches, les totaux Forfait / Ligne / Quantité et les tableaux de calcul. Les gammes qui ne sont associées à aucune activité sont regroupées en bas.

- **Cliquez sur une gamme** pour l'ouvrir et la modifier ; **← Toutes les gammes** ramène au récapitulatif.
- **+ Nouvelle gamme** crée une gamme vide et l'ouvre directement.
- Dans une gamme ouverte : ✎ renommer, 🗑 supprimer.

**Réglages de la gamme**
- *Onglet des lignes* : onglet du fichier source qui contient une ligne par composant (pour Prépa OF : `OF`).
- *Colonne dossier* : colonne qui identifie un dossier (pour Prépa OF : `OF`).
- *Colonne quantité* : quantité de pièces de chaque ligne (pour Prépa OF : `Qté besoin`).

**Tableau des tâches** : pour chaque tâche, l'affectation, la description et le temps en secondes. Les flèches changent l'ordre.

| Affectation | Calcul du temps |
|---|---|
| Forfait | Compté **1 fois par dossier** (par OF) |
| Ligne | Multiplié par le **nombre de lignes** du dossier |
| Quantité | Multiplié par la **somme des quantités** du dossier |
| Calcul | Selon un **tableau de valeurs** (voir ci-dessous) ; la colonne Tps affiche « cf tableau » |

Les totaux Forfait / Ligne / Quantité s'affichent sous le tableau.

**Tableau de calcul** (un par tâche « Calcul ») :
1. Donnez un *libellé* (ex. `DN`).
2. Choisissez le *fichier source*, l'*onglet* et la *colonne des valeurs*.
   Si ce fichier n'est pas celui de l'activité (ex. base des DN), indiquez les deux colonnes de *liaison* (ex. `Composant OF` ↔ `Article`).
3. **Importer les valeurs de la colonne** ajoute les valeurs trouvées (doublons supprimés) avec un temps de 0 s ; les temps déjà saisis ne sont jamais écrasés.
4. Saisissez le **Tps (sec)** de chaque valeur. La ligne **(vide)** s'applique aux lignes sans valeur.

Temps de la tâche pour une ligne = Tps (sec) de sa valeur × quantité de la ligne.
Exemple : 3 lignes de 5 pièces en DN10 (1 s) → 1 × 5 × 3 = 15 s.

La gamme *Prépa OF* est pré-remplie avec les 13 tâches et le tableau des DN de référence.

## 7. Prépa OF

Liste de tous les OF dont le **Début opé** est dans la plage de dates choisie en haut de l'onglet.

- **Plage de dates** : par défaut du jour – 15 jours au jour + 30 jours (vraies dates). Modifiez-les librement ; **Plage par défaut** les remet.
- **Résumé** (à droite) : nombre d'OF, total d'heures, nombre d'OF avec manquants.
- **Tri** : cliquez sur un titre de colonne (re-cliquez pour inverser).
- **Filtres comme dans Excel** : le petit entonnoir à droite de chaque titre ouvre un menu avec le tri, une zone *Rechercher* et la liste des valeurs à cocher (« (Sélectionner tout) », « (Vides) » pour les cases vides). La liste ne montre que les valeurs encore présentes avec les autres filtres. L'entonnoir devient bleu quand un filtre est actif ; **Effacer les filtres** (en haut) les supprime tous. Le résumé indique alors « n OF (filtrés sur N) ».
- Le tableau se lit dans le fichier source de l'activité *Prépa OF* (onglets `OF` et `OF - Opérations`) : chargez-le d'abord dans **Fichiers sources**.

| Colonne | Origine |
|---|---|
| Atelier | *Lot PF* commençant par **M** → Montage, **U** → Usinage / sous-traitance, sinon vide |
| OF, Commande liée, Article PF, Qté PF, Statut allocation, Palette, Statut opé, Début opé, Type, Fiche suiveuse, Bon de sortie matière | Colonnes du même nom (onglet OF) |
| Type palette | **Cryo** si une opération de l'OF contient « degr » (Dégraissage…, majuscules et accents ignorés), sinon **Bois** |
| Manquants | **Oui** si au moins une ligne de l'OF est marquée « Manquant » (ou « Oui » dans l'export), sinon **Non** |
| Date sortie 2 | Plus ancienne *Date sortie 2* de l'OF (onglet OF - Opérations) |
| Temps (h) | Temps de préparation calculé avec la gamme (2 décimales) |

**Calcul du Temps (h)** pour un OF = somme des temps *Forfait* + somme des temps *Ligne* × nombre de lignes + somme des temps *Quantité* × total des *Qté besoin* + pour chaque tâche *Calcul* : Σ (Tps de la valeur de la ligne × *Qté besoin* de la ligne).
Laissez la souris 2 s sur un temps pour voir le détail. Un **⚠** signale des lignes dont la valeur n'est pas dans le tableau de calcul (comptées 0 s).

> En attendant la base des DN, toutes les lignes prennent le temps « (vide) » du tableau DN (1 s par pièce).

---

### Informations techniques

- Une page `index.html` en HTML/CSS/JavaScript, sans framework.
- `lib/xlsx.full.min.js` : lecture/écriture des fichiers Excel (SheetJS, licence Apache 2.0), embarquée pour fonctionner hors connexion.
- `fonts/inter.woff2` : police Inter (licence SIL OFL), embarquée.
- Les fichiers choisis sont mémorisés par le navigateur (aucune donnée n'est envoyée sur internet).
