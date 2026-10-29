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
| Période (Du → Au) | Plage de dates commune à toutes les activités ; à l'ouverture : J – 15 à J + 30 | – |
| Flèche retour | Annule la dernière modification | Ctrl + Z |
| Flèche avant | **Rétablit** la dernière action annulée (annuler une annulation, comme Excel). Toute nouvelle modification vide la liste des actions à rétablir | Ctrl + Y |
| Actualiser (deux flèches, à gauche de la disquette) | Recharge les fichiers sources. **Noir** : les données chargées correspondent exactement aux fichiers sur le disque ; **orange** : au moins un fichier est à actualiser (non chargé, lecture à autoriser après une actualisation de la page, modifié depuis son chargement, ou erreur) — la bulle détaille lesquels. Le clic ne relit que les fichiers concernés (ou tous si tout est à jour) et redemande l'accès au navigateur si besoin. Les fichiers ne sont jamais rechargés automatiquement, sauf à l'ouverture de l'application | F9 |
| Disquette | Enregistre le projet. **Noire** : tout est enregistré ; **orange** : modifications non enregistrées, pas encore de classeur ou dernier enregistrement en échec (la bulle précise le cas) | Ctrl + S |
| Cadre | Plein écran (re-cliquer pour quitter) | Ctrl + Maj + F |
| Engrenage | Ouvre les Paramètres | Ctrl + , |

Sous le ruban, les onglets : **Charge globale** (graphique de toutes les activités), puis les activités **Prépa OF** (onglet affiché à l'ouverture) et **Prépa Expéd**. Les réglages (*Général*, *Fichiers sources*, *Temps gammes*) sont regroupés dans **Paramètres**, une **fenêtre flottante** qui s'ouvre avec l'**engrenage** du ruban (ou Ctrl + ,) et se ferme avec ✕, Échap ou un nouveau clic sur l'engrenage. Le ruban (Enregistrer, Annuler, Période…) reste utilisable pendant qu'elle est ouverte.

Les menus et fenêtres s'ouvrent avec une animation courte. Pendant un chargement, une fenêtre indique le fichier, l'étape en cours (lecture, analyse des onglets, calcul des temps) et le temps écoulé.

Laissez la souris **2 secondes** sur n'importe quel élément cliquable (bouton, liste, case, champ, onglet…) pour voir une bulle d'aide indiquant sa fonction (et son raccourci s'il en a un).

**Adaptation à l'écran** : l'application s'ajuste à la taille de la fenêtre (grand écran, portable, tablette). Le tableau de chaque activité occupe toute la hauteur disponible et défile seul ; sur petit écran, le libellé « Période » est masqué, le menu des Paramètres passe au-dessus du contenu, et sur téléphone le logo et le bouton plein écran sont masqués.

## 3. Le classeur projet (.xlsx)

Tout votre paramétrage est enregistré dans un **classeur Excel** dont vous choisissez l'emplacement.

- **Paramètres › Nouveau classeur…** : choisissez un dossier et un nom (par défaut `Charge Capa.xlsx`).
- **Paramètres › Ouvrir un classeur…** : reprenez un classeur projet existant.
- **Paramètres › Enregistrer sous…** : faites une copie sous un autre nom ou dans un autre dossier.
- **Ctrl + S** ou la **disquette** : enregistre dans le classeur en cours. S'il n'y en a pas encore, l'application vous demande où le créer.
- **Sauvegarde automatique** (option de *Paramètres › Général*, décochée par défaut) : le projet est enregistré **toutes les 10 minutes** s'il a été modifié. Le bouton retour (**Ctrl + Z**) et Rétablir (**Ctrl + Y**) restent utilisables après une sauvegarde automatique : pensez seulement à réenregistrer après avoir annulé. Le navigateur exige un premier enregistrement manuel (Ctrl + S) dans la session pour autoriser l'écriture ; tant que ce n'est pas fait, la ligne sous l'option l'indique.

Au lancement suivant, l'application propose de **reprendre le dernier projet** : cliquez sur **Ouvrir** puis acceptez l'autorisation du navigateur (c'est une sécurité de Chrome/Edge, elle est demandée une fois par session).

⚠ **Fermez le classeur projet dans Excel avant d'enregistrer** : Windows bloque l'écriture d'un fichier ouvert dans Excel. La disquette reste alors orange ; fermez Excel et refaites Ctrl + S.

**Rappel d'enregistrement** : si vous quittez l'application (autre onglet, autre fenêtre, navigateur réduit) alors que des modifications ne sont pas enregistrées, une fenêtre **« Modifications non enregistrées »** s'affiche à votre retour :
- **Enregistrer** enregistre dans le classeur projet (ou demande où le créer s'il n'existe pas encore) ;
- **Plus tard** (ou Échap) ferme le rappel ; il reviendra après une nouvelle modification.

Si vous **fermez** l'onglet ou le navigateur avec des modifications non enregistrées, le navigateur affiche son propre avertissement « Quitter le site ? » (les navigateurs n'autorisent pas d'autre fenêtre à ce moment-là) : choisissez *Annuler* puis faites Ctrl + S.

## 4. Paramètres

La fenêtre **Paramètres** (engrenage du ruban ou Ctrl + ,) contient un menu à gauche : **Général**, **Fichiers sources** et **Temps gammes**.

### 4.1 Général

- **Classeur projet** : ouvrir, créer, enregistrer sous, sauvegarde automatique toutes les 10 minutes (voir ci-dessus).
- **Apparence** : thème *Clair*, *Sombre* ou *Comme Windows* (suit le réglage de Windows).
- **Date d'affectation** : pour chaque activité, le nombre de **jours ouvrés** (lundi à vendredi) entre la date d'affectation par défaut et la date due (2 par défaut). Voir « Date affectation » ci-dessous.
- **Polices d'écriture** : choix de la police (Inter, Segoe UI, Aptos, Bahnschrift, Calibri, Arial) et de la taille du texte, avec aperçu.

### 4.2 Fichiers sources

Chaque ligne relie une **activité** (ex. *Prépa OF*) à un **fichier source** Excel (.xlsx, .xls) ou CSV et à une **gamme** de temps.

| Colonne | Rôle |
|---|---|
| Libellé | Nom libre de la source |
| Activité | Activité alimentée par ce fichier, ou « — Base de données » pour un fichier complémentaire (ex. future base des DN) |
| Fichier source | Cliquez pour choisir le fichier dans un dossier Windows |
| Date du fichier | Date de **dernière modification du fichier** sur le disque : elle indique de quand datent les données sources. En orange si le fichier est plus récent que les données chargées |
| Dernier chargement | Date à laquelle l'application a lu le fichier |
| État | *Chargé* (nombre de lignes lues, détail par onglet dans la bulle), **À actualiser** (le fichier a été modifié depuis le chargement : l'application n'affiche pas les dernières données ; cliquez sur le bouton pour recharger), *Autoriser la lecture*, *Erreur* |
| Gamme | Gamme de temps (Paramètres › Temps gammes) appliquée à l'activité |
| Capacité | Groupes et niveaux du fichier de capacité pris en compte pour l'activité (bouton → cases à cocher par groupe, « OK ») |

- Le bouton **⟳** relit un fichier ; **Tout recharger** relit tous les fichiers.
- Au lancement, les fichiers sont relus automatiquement si le navigateur l'autorise ; sinon cliquez sur **Autoriser la lecture**.
- **Un même fichier pour plusieurs activités** (ex. un seul export pour Prépa OF et Prépa Expéd) : il n'est **lu qu'une fois**, même s'il a été choisi séparément sur chaque ligne. Sous l'état, la mention « = *autre source* » indique le partage ; recharger l'une de ces lignes (⟳ ou « À actualiser ») met à jour toutes celles du même fichier.
- Le bouton **Actualiser** du ruban (F9) recharge en un clic tous les fichiers à actualiser ; il est orange tant que les données chargées ne correspondent pas aux fichiers sources.
- La date des fichiers est revérifiée **chaque minute** et à chaque retour sur l'application : un fichier enregistré entre-temps passe **À actualiser**.
- Les données lues restent dans le navigateur : elles **ne sont pas copiées** dans le classeur projet (seuls le nom du fichier et les dates le sont).
- Pour les CSV, le séparateur (`;` ou `,`) et l'encodage (UTF-8 ou ANSI) sont détectés automatiquement.

**Capacité de travail** (encadré sous les sources d'activités) : une **source unique** pour toutes les activités.
- Fichier Excel ou CSV contenant au moins les colonnes **date**, **groupe**, **Niveau** et **Heure productivité** (une ligne par personne et par jour).
- Mêmes boutons que les autres sources (choisir, recharger, retirer) ; l'état indique le nombre de lignes, de groupes/niveaux et la période couverte.
- Les noms mal encodés de l'export (ex. « Pr\u00e9parations ») sont corrigés automatiquement et regroupés avec « Préparations ».
- Dans chaque source d'activité, la colonne **Capacité** permet de cocher un ou plusieurs couples *Groupe › Niveau* (cocher un groupe coche tous ses niveaux).

### 4.3 Temps gammes

Cette page s'ouvre sur un **récapitulatif des gammes par activité** : pour chaque activité, ses gammes (associées dans *Fichiers sources*) avec le fichier source, le nombre de tâches, les totaux Forfait / Ligne / Quantité et les tableaux de calcul. Les gammes qui ne sont associées à aucune activité sont regroupées en bas.

- **Cliquez sur une gamme** pour l'ouvrir et la modifier ; **← Toutes les gammes** ramène au récapitulatif.
- **+ Nouvelle gamme** crée une gamme vide et l'ouvre directement.
- Dans une gamme ouverte : ✎ renommer, 🗑 supprimer.

**Réglages de la gamme**
- *Onglet des lignes* : onglet du fichier source qui contient une ligne par composant (pour Prépa OF : `OF`).
- *Colonne dossier* : colonne qui identifie un dossier (pour Prépa OF : `OF`).
- *Colonne quantité* : quantité de pièces de chaque ligne (pour Prépa OF : `Qté besoin`).
- *Découper par date* (facultatif) : un dossier est découpé en autant de dossiers que de dates différentes dans cette colonne (pour Prépa Expéd : `Date expédition`, un dossier = une commande pour une date).
- *Exclure les lignes dont la colonne… commence par…* (facultatif) : ces lignes ne comptent pas dans le temps (pour Prépa Expéd : colonne `Article`, préfixe `9`). Un dossier sans aucune ligne comptée a un temps de 0.

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

La gamme *Prépa OF* est pré-remplie avec les 13 tâches et le tableau des DN de référence (DN10 à DN200, dont DN125 à 60 s comme DN100), relié à la **Base DN** (voir ci-dessous) ; la gamme *Prépa Expéd* avec ses 17 tâches (la tâche Forfait *RFF* est toujours comptée).

### 4.4 Ressources à affecter

Il n'y a plus de liste à paramétrer : les ressources proposées dans la colonne **Affectation** sont les **personnes du fichier de capacité** (colonne *nom_complet*).
- Pour une activité, ce sont les personnes des **groupes / niveaux de capacité choisis pour cette activité** (*Fichiers sources*, colonne « Capacité ») ; si aucun n'est choisi, toutes les personnes du fichier.
- Une saisie identique à un nom du fichier (majuscules et accents ignorés) reprend l'écriture exacte du nom ; un autre texte reste accepté (texte libre).
- Les projets enregistrés avec l'ancienne liste *Paramètres › Ressources* sont convertis automatiquement : chaque affectation garde le nom de sa ressource.

## 5. Charge globale

Premier onglet, à gauche des activités : **un seul graphique** qui additionne la charge et la capacité de toutes les activités sur la période du ruban.
- **Barres empilées** : charge **soldée** en bleu (en bas) et charge **en cours** en noir grisé (au-dessus), toutes activités additionnées ; la hauteur totale est la charge totale du jour ;
- **Courbe** : capacité des groupes / niveaux choisis pour les activités (un groupe choisi pour deux activités n'est compté qu'une fois) ;
- en haut : charge totale, dont soldée, dont en cours, charge de chaque activité, capacité totale et taux de charge ;
- boutons **Jour / Semaine / Mois / Année**, axe des dates et survol comme le graphique d'une activité ; le survol détaille la charge de chaque activité ;
- chaque activité y compte les lignes affichées dans son tableau : ses **filtres** (En cours, filtres de colonnes) s'appliquent aussi ici (rappelé à côté du titre).

**Base DN** : dans *Fichiers sources*, la ligne **Base DN** (« — Base de données ») attend le fichier des DN par article (onglet unique, colonnes **Article** et **DN**). Choisissez-le une fois : la tâche *Compter et déposer les pièces* de Prépa OF retrouve alors le DN de chaque ligne en reliant *Composant OF* (fichier Prépa OF) à *Article* (base DN), et applique le temps du tableau DN. Un composant absent de la base prend le temps de la ligne « (vide) ». Comme les autres sources, la base reste sur votre poste : seul le lien vers le fichier est enregistré dans le projet.

## 6. Colonnes et taille des tableaux

À droite des boutons rapides de chaque activité :
- le bouton **Colonnes** (icône de tableau) ouvre la liste des colonnes : cochez celles à afficher, décochez celles à masquer (« (Sélectionner tout) » coche ou décoche tout) ; les flèches **↑ ↓** de chaque colonne changent son **ordre** dans le tableau (haut de la liste = gauche du tableau), **Ordre par défaut** remet l'ordre d'origine ; puis **OK**. Au moins une colonne doit rester affichée. Le bouton est bleu quand des colonnes sont masquées. Les colonnes masquées et leur ordre sont mémorisés **sur ce poste**, pour chaque activité ; un filtre posé sur une colonne masquée reste actif (le bouton **Tout** le retire) ;
- **A−** / **A+** réduisent ou agrandissent le texte du tableau (de 50 % à 160 %) ; le bouton du milieu affiche la taille et revient à **100 %** ;
- **Ajuster** choisit la plus grande taille qui fait tenir toutes les colonnes dans la largeur de l'écran.
La taille vaut pour tous les tableaux d'activité et est mémorisée **sur ce poste** (pas dans le classeur projet).

### Date affectation

Chaque activité a une colonne **Date affectation** (juste à droite de la colonne *Affectation*) : c'est le **jour où le dossier est planifié**, en général avant sa date due (Début opé pour Prépa OF, Date expédition pour Prépa Expéd).
- **Par défaut** : date due − *x* jours ouvrés, *x* étant réglé pour chaque activité dans *Paramètres › Général › Date d'affectation* (2 par défaut). Elle s'affiche alors en gris italique et suit la date due si l'export change.
- **Pour avancer un dossier** (par exemple pour lisser un pic), changez sa date dans la case : elle passe en **bleu gras** et est enregistrée dans le classeur projet (onglet *Dates affectation*). Videz la case (ou remettez la date par défaut) pour revenir au calcul automatique.
- Une date **postérieure à la date due** s'affiche en **rouge**, précédée d'un logo **⚠** (la bulle rappelle les deux dates).
- Avec des **lignes cochées**, la date saisie sur l'une d'elles est recopiée sur toutes les lignes cochées (une seule action, annulable par Ctrl + Z).
- La colonne se trie et se filtre comme les autres. La vue **Affectation par capacité** place la charge à la **date d'affectation** (et non à la date due) ; la période du ruban et les autres graphiques restent basés sur la date due.

### Cases à cocher et affectation en masse

Chaque ligne a une **case à cocher** à gauche, comme dans l'Explorateur Windows : elle apparaît au survol de la ligne, et reste visible dès qu'une ligne est cochée.
- **clic sur la case** : coche ou décoche la ligne ;
- **Maj + clic sur la case** : coche toutes les lignes entre la dernière case cliquée et celle-ci ;
- la case de l'**en-tête** coche ou décoche toutes les lignes affichées ;
- un clic sur la ligne elle-même ne coche que cette ligne (Ctrl + clic : ajoute ou retire) ;
- **Échap** décoche tout.
- Dès que **2 dossiers ou plus** sont sélectionnés (cochés, ou Ctrl + clic), une ligne **« Sélection (n …) »** s'ajoute au pied du tableau, sous le Total : elle donne la **somme des Temps (h)** des dossiers sélectionnés et combien sont affectés.

Ensuite, **saisissez l'affectation dans la case Affectation de l'une des lignes cochées** (au clavier ou par la liste ▾) : dès la validation, elle est **recopiée sur toutes les lignes cochées**, puis les cases sont décochées. L'opération compte comme une seule action, annulable par Ctrl + Z. Une saisie sur une ligne non cochée ne concerne que cette ligne.

### Affectation par capacité

Le bouton **Affectation par capacité** (à gauche du bouton Colonnes) ouvre une vue qui glisse depuis la droite, à côté du tableau. **Faites glisser son bord gauche** pour l'élargir ou la réduire (largeur mémorisée sur ce poste).

La vue présente **un histogramme empilé par jour**, les jours les uns sous les autres (faites défiler la vue vers le haut ou le bas). Chaque histogramme a **une barre par ressource de l'activité** ce jour-là :
- les ressources sont les personnes du **fichier de capacité** (colonne *nom_complet*) appartenant aux **groupes / niveaux choisis pour l'activité** (Paramètres › Fichiers sources, colonne « Capacité »), plus toute ressource à qui du temps est affecté ce jour-là ;
- chaque dossier compte au jour de sa **Date affectation** (voir ci-dessus), et non à sa date due ;
- **vert** : temps **affecté** à la ressource ce jour-là (toutes activités confondues ; le survol précise la part des autres activités) ;
- **gris clair** : temps **restant à affecter** = temps disponible sur la journée (*Heure productivité*) – temps déjà affecté ;
- **rouge vif** : **surcharge**, quand le temps affecté dépasse le temps disponible.

Au survol d'une barre, ses valeurs s'affichent immédiatement.

**Glisser-déposer** : faites glisser une ligne du tableau (ou, si elle est cochée, toutes les lignes cochées) et déposez-la dans la vue :
- **sur la barre d'une personne** : les dossiers lui sont affectés **et** leur *Date affectation* devient le jour de ce graphique ;
- **ailleurs dans le graphique d'un jour** (titre, fond) : seule la *Date affectation* change, l'affectation est conservée.

Pendant le glisser, la barre visée est encadrée et une bulle indique « Affecter à … le … ». L'opération compte comme une seule action, annulable par Ctrl + Z. Partez d'une zone de la ligne sans champ de saisie (pas des cases Affectation ou Date affectation). Sous le nom de chaque jour figurent la semaine, la charge **non affectée** de l'activité et le nombre de surcharges. Le total des surcharges de la période s'affiche en haut de la vue et en **pastille rouge** sur le bouton ; la case **Surcharges** ne garde que les ressources en dépassement. Toutes les lignes affectées de la période sont comptées, quels que soient les filtres du tableau.

> Les noms des affectations doivent être les mêmes que ceux de la colonne *nom_complet* du fichier de capacité (majuscules et accents ignorés) ; les noms des personnes sont écrits en petit sous chaque barre. Sans groupe / niveau choisi pour l'activité, la vue affiche toutes les personnes du fichier de capacité.

## 7. Prépa OF

**Graphique charge / capacité** : le bouton de graphique placé à gauche du grand titre *Prépa OF* (dans la page) ouvre un panneau (Échap ou ✕ pour le fermer) :
- **Barres** : charge du jour = somme des *Temps (h)* des OF dont le Début opé tombe ce jour-là, en deux parts : **soldée** en bleu (Statut opé « Soldée » ; pour Prépa Expéd, Soldée = Oui) et **en cours** en noir grisé ; en haut, la charge totale est détaillée « dont soldée / dont en cours » ;
- **Courbe** : capacité du jour = somme des *Heure productivité* des groupes/niveaux choisis pour l'activité ;
- tous les jours de la période du ruban (week-ends grisés) ; le graphique suit aussi les **filtres de colonnes** du tableau ;
- boutons **Jour / Semaine / Mois / Année** (en haut à droite du graphique) : charge et capacité sont additionnées par semaine, mois ou année ; une semaine ou un mois coupé par la période ne compte que les jours de la période (les dates exactes sont rappelées au survol) ;
- sous l'axe : jours, **numéros de semaine** (S44, norme ISO : la semaine commence le lundi) puis **mois et année** ; un trait pointillé sépare les mois (ou les années en vue Mois) ;
- en haut : charge totale, capacité totale, taux de charge ;
- au survol d'une barre ou d'un point de la courbe, les valeurs du jour s'affichent **immédiatement** (charge, capacité, marge ou dépassement).

Liste de tous les OF dont le **Début opé** est dans la plage de dates choisie en haut de l'onglet.

- **Période** : elle se règle dans le ruban, en haut de page, et s'applique à toutes les activités. Par défaut du jour – 15 jours au jour + 30 jours (vraies dates). Modifiez-les librement ; la période par défaut revient à chaque ouverture de l'application.
- **Annuler un filtre** : poser ou retirer un filtre (En cours, Tout, filtre de colonne) s'annule avec **Ctrl + Z** ou la flèche retour du ruban, comme les autres actions. Les filtres ne sont pas enregistrés dans le projet : les annuler ne le marque pas comme modifié.
- **Boutons rapides** à droite du titre *Prépa OF* : **En cours** n'affiche que les OF dont le *Statut opé* n'est pas « Soldée » (re-cliquer pour l'enlever) ; **Tout** retire tous les filtres (En cours et filtres de colonnes). Le bouton actif est mis en évidence.
- **Total** : le pied du tableau donne le nombre d'OF affichés (« filtrés sur N » si un filtre est actif), le total des heures et le nombre d'OF affectés.
- **Tri** : cliquez sur un titre de colonne (re-cliquez pour inverser).
- **Filtres comme dans Excel** : le petit entonnoir à droite de chaque titre ouvre un menu avec le tri, une zone *Rechercher* et la liste des valeurs à cocher (« (Sélectionner tout) », « (Vides) » pour les cases vides). La liste ne montre que les valeurs encore présentes avec les autres filtres. L'entonnoir devient bleu quand un filtre est actif ; le bouton **Tout** (en haut) les supprime tous. La touche **Entrée** valide le menu de filtre (comme **OK**), y compris après une recherche.
- Le tableau se lit dans le fichier source de l'activité *Prépa OF* (onglets `OF` et `OF - Opérations`) : chargez-le d'abord dans **Paramètres › Fichiers sources**.

| Colonne | Origine |
|---|---|
| Atelier | *Lot PF* commençant par **M** → Montage, **U** → Usinage / sous-traitance, sinon vide |
| OF, Commande liée, Article PF, Qté PF, Statut allocation, Palette, Statut opé, Début opé, Type, Fiche suiveuse, Bon de sortie matière | Colonnes du même nom (onglet OF) |
| Début opé (rappel) | Affiché en **pastille rouge** quand la date est antérieure à aujourd'hui (OF en retard) |
| Type palette | **Cryo** si une opération de l'OF contient « degr » (Dégraissage…, majuscules et accents ignorés), sinon **Bois** |
| Manquants | **Oui** si au moins une ligne de l'OF est marquée « Manquant » (ou « Oui » dans l'export), sinon **Non** |
| Date sortie 2 | Plus ancienne *Date sortie 2* de l'OF (onglet OF - Opérations) |
| Temps (h) | Temps de préparation calculé avec la gamme (2 décimales) |
| Affectation | **Colonne de saisie** (elle défile avec les autres colonnes). **Liste déroulante toujours proposée** : dès que vous cliquez dans la case, la liste des personnes du fichier de capacité s'ouvre sous la case (puis les autres textes déjà saisis dans la colonne) ; cliquez sur un nom pour le choisir, ou « — Aucune affectation » pour retirer. Le bouton ▾ (ou **Alt + ↓**) l'ouvre ou la ferme. **Saisie à la main** : tapez le début d'un nom ; la liste se réduit aux noms qui commencent ainsi et l'application **complète** le premier nom : continuez à taper pour l'ignorer, ou validez. **Entrée** ou **↓** valide et passe à la ligne du dessous, **↑** à la ligne du dessus, **Échap** annule la saisie ; videz la case pour retirer l'affectation. Le pied du tableau indique « n / N affectés ». |

**Calcul du Temps (h)** pour un OF = somme des temps *Forfait* + somme des temps *Ligne* × nombre de lignes + somme des temps *Quantité* × total des *Qté besoin* + pour chaque tâche *Calcul* : Σ (Tps de la valeur de la ligne × *Qté besoin* de la ligne).
Laissez la souris 2 s sur un temps pour voir le détail. Un **⚠** signale des lignes dont la valeur n'est pas dans le tableau de calcul (comptées 0 s).

> Sans fichier **Base DN** chargé (Paramètres › Fichiers sources), toutes les lignes prennent le temps « (vide) » du tableau DN (1 s par pièce).

## 8. Prépa Expéd

Liste des commandes à préparer pour l'expédition : **une ligne par commande et par date d'expédition** (une commande livrée à deux dates donne deux lignes). Source : onglet `Commandes ventes` du fichier de l'activité *Prépa Expéd* (Paramètres › Fichiers sources).

Période, tri, filtres Excel, boutons rapides, total, affectation des ressources, graphique et taille du tableau fonctionnent comme pour Prépa OF :
- la période porte sur la **Date expédition** ;
- **En cours** masque les commandes-dates entièrement soldées (Soldée = Oui) ; **Tout** retire tous les filtres.

| Colonne | Origine |
|---|---|
| Commande (rappel) | En **violet** quand la commande est **splitée** : expédiée à plusieurs dates différentes (toutes dates du fichier confondues, même hors période) |
| Commande, Client, Gestionnaire, Mode livraison, Type, Référence commande | Colonnes du même nom ; si les lignes d'une commande-date ont des valeurs différentes, toutes sont affichées, séparées par « / » |
| RFF | En **pastille rouge** si une valeur est « Oui » |
| Validée | En **pastille rouge** si une valeur est « Non » |
| Manquants | **Oui** en rouge si au moins une ligne a des manquants, sinon Non |
| Date expédition | En **pastille rouge** si elle est antérieure à aujourd'hui |
| Adresse livraison | Nom client livraison, Adresse livraison 1, puis Adresse livraison 2, 3, Code postal, Ville et Pays, sur plusieurs lignes en petit |
| Instruction livraison | En petit, sur plusieurs lignes |
| Soldée | **Oui** si tous les articles de la commande-date sont « Soldé », sinon **Non** |
| Temps (h) | Temps de préparation calculé avec la gamme *Prépa Expéd* sur toutes les lignes (soldées comprises), **sauf les articles commençant par 9** ; quantité = *Qté commandée US* |
| Affectation | Liste déroulante des ressources et saisie au clavier avec complétion, comme pour Prépa OF ; enregistrée dans le classeur projet |

---

### Informations techniques

- Une page `index.html` en HTML/CSS/JavaScript, sans framework.
- `lib/xlsx.full.min.js` : lecture/écriture des fichiers Excel (SheetJS, licence Apache 2.0), embarquée pour fonctionner hors connexion.
- `fonts/inter.woff2` : police Inter (licence SIL OFL), embarquée.
- Les fichiers choisis sont mémorisés par le navigateur (aucune donnée n'est envoyée sur internet).
