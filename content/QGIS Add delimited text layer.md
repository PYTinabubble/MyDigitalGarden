---
title: Import XLSX et CSV dans Qgis
draft: 
tags:
  - qgis
---
## Créer un CSV du fichier Excel

Il est possible que l'encodage empêche de récupérer les lettres accentuées.
Pour palier à ce problème, 2 solutions.

### Google Sheet 
Ouvrir le fichier Excel au préalable sur Google Sheet et le télécharger en CSV depuis Google Sheet.

### Notepad
Sur Excel enregistrer le .xlsx en Unicode Texte puis :
- Ouvrir le .txt avec Notepad
- Remplace toutes les tabulations par des point-virgules.
- Sélectionner une tabulation entre 2 colonnes → ctrl+c
- Ouvrir “edition → remplacer” (ctrl+h)
- coller la tabulation et remplacer par “;”
- Fichier → Enregistrer sous
	- Changer l’encodage (encoding) en utf-8
	- Changer l’extension du fichier en .csv
	- Sauvegarder

## Dans Qgis add layer > delimited text layer

Attention de bien choisir le séparateur utilisé dans le CSV.
Semicolon = ;
colon = : 
comma = ,

Attention de préciser si, dans le tableau, les décimaux sont séparés par des virgule : *"decimal separator is comma"*

## Préciser les coordonnées x et y

### WGS84 (4326)
longitude = X (environ 3 dans le Nord)
Latitude = Y (environ 50 dans le Nord)

### Lambert93 (2154)
X environ 600 000 dans le Nord
Y environ 7 000 000 dans le Nord
