---
title: GoogleSheet =QUERY
draft: false
tags:
  - GoogleSheet
---
# GoogleSheet =Query

Sources :

- https://coefficient.io/how-to-google-sheets-query-function https://www.sheets-pratique.com/fr/query/introduction
- [How to Create a Dashboard in Google Sheets (10 steps) - Query Formula](https://www.youtube.com/watch?v=1JkvHfzIL0Y "Youtube video")
- [How to Create Dropdown Filters on Google Sheets Dashboard Using QUERY Formula (ADVANCED TRICK)](https://www.youtube.com/watch?v=XGvCT3IeYdA "Youtube Video")

Pour enlever les cellules vides :
"SELECT D,F,E,G WHERE D <> ' '"
"SELECT D,F,E,G WHERE D is not null”

Changer le label :
```
"SELECT D,F,E,G WHERE D <> '' LABEL D 'ID', F 'NOM', E 'PHASE', G 'Puiss -5°C'"
```
Ne pas répéter Label et juste une virgule entre les "colonnes labels"
Penser à mettre "-1" dans le 3e argument afin de ne pas récupérer les noms de colonnes de la base de données en plus.

Les différentes “clauses” possibles doivent être mises dans l’ordre :

> SELECT > WHERE > GROUP BY > PIVOT > ORDER BY > LIMIT > OFFSET > LABEL > FORMAT

On ne met pas de virgules entre les “clauses” mais entre les éléments d’une même “clause”

L’écrire en passant des lignes à chaque “clauses” en tapant ALT+ENTRÉE pour aller à la ligne dans la formule : 
```
“
SELECT D,F,E,G 
WHERE D is not null
LABEL D ‘ID’, F ‘NOM’, E ‘PHASE’, G ‘PUISS -5°C
”
```
Permet de repérer où mettre des virgules et où ne pas en mettre

Pour faire référence à une autre cellule: 
```
=query('Feuille 1'!A1:R10000; "SELECT C, SUM(D)
WHERE E ='"&(B1)&"' AND G = "&(B2)&"
GROUP BY C
ORDER BY C ASC")
```
Ici B1 est du texte et B2 est un nombre. </br>
Pour faire référence à la cellule : **“&cell&”** et s’il s’agit de texte : **‘“&cell&”’**

#GoogleSheet
