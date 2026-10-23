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

## 5. Onglets à venir

- **Fichiers sources** : choix des fichiers Excel/CSV servant de base de données pour chaque activité.
- **Temps gammes** : temps des tâches par activité (Forfait, Ligne, Quantité, Calcul).
- **Prépa OF** : liste des OF à préparer et temps de préparation.

---

### Informations techniques

- Une page `index.html` en HTML/CSS/JavaScript, sans framework.
- `lib/xlsx.full.min.js` : lecture/écriture des fichiers Excel (SheetJS, licence Apache 2.0), embarquée pour fonctionner hors connexion.
- `fonts/inter.woff2` : police Inter (licence SIL OFL), embarquée.
- Les fichiers choisis sont mémorisés par le navigateur (aucune donnée n'est envoyée sur internet).
