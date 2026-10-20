# FITENY_corpus — organisation

Les fichiers sont rangés simplement ; ce sont les tableaux de `tableaux/` qui relient chaque audio à son texte, son item, sa variété et son locuteur.

## Dossiers
- `tableaux/` : `items_T1.csv` (207 mots, rempli), `items_T2.csv` (300 phrases, traductions à remplir), `items_T4.csv` (images, à remplir), `enregistrements.csv` (1 ligne par audio), `locuteurs.csv` (1 ligne par locuteur, anonyme).
- `T1/audio/`, `T2/audio/`, `T4/audio/` : un sous-dossier par variété : `mer_merina`, `bet_betsileo`, `bzc_betsimisaraka_sud`, `tdx_antandroy`.
- `T4/images/` : `T4-001.jpg`, `T4-002.jpg`…  `T4/references/` : descriptions merina existantes (AfriVoice, WAXAL), par exemple `T4-001_merina_afrivoice_26832.wav` + `.txt`.

## Codes des variétés
`mer` merina · `bet` betsileo · `bzc` betsimisaraka du Sud · `tdx` antandroy. (Le betsileo n'a pas de code ISO propre et partage `plt` avec le merina : on utilise donc ces codes courts.)

## Noms de fichiers
- Enregistrement FITENY : `<variété>-<locuteur>-<tâche>-<item>.wav` + `.txt` du même nom (transcription de ce qui a été dit).
  - T1 : un fichier par locuteur d'abord (`bzc-LOC003-T1.wav`), découpé ensuite en `bzc-LOC003-T1-001.wav` … `-207.wav`.
  - T2 : `bzc-LOC003-T2-051.wav`.  T4 : `bzc-LOC003-T4-001.wav`.
- Jamais de prénom dans un nom de fichier.

## Règles
- T1 et T2 sont parallèles (même item dans chaque variété) ; T4 ne l'est pas (description libre, on transcrit).
- Les items T2-001 à T2-050 sont réservés au test ; jamais de texte WAXAL ni biblique dans le test.
- Chaque audio a sa ligne dans `enregistrements.csv`, chaque locuteur dans `locuteurs.csv`.

## Références de Serva pour T1 (`tableaux/references/`)
- `serva_T1_large.csv` : les 207 mots × les 60 parlers de Serva & Pasquini (2020), une colonne par parler, rangés de A à Z.
- `serva_T1_long.csv` : la même chose en une ligne par mot et par parler (12 420 lignes), avec la variété, la localité, le groupe (A à D, calculé par FITENY sur la matrice de distances), la distance au merina et `identique_merina` (oui/non). Pratique pour filtrer dans un tableur.
- Source : Serva, M. & Pasquini, M. (2020). Dialects of Madagascar. PLoS ONE 15(10): e0240170. Licence CC BY 4.0, citation obligatoire.
- Ce sont des **références publiées**, pas nos données : les colonnes `forme_<variété>_retenue` de `items_T1.csv` ne se remplissent qu'avec ce que disent **nos** locuteurs.
