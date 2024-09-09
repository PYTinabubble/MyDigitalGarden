---
title: Quelques règles pour les base de données
draft: 
source: https://www.codeproject.com/articles/359654/11-important-database-designing-rules-which-i-fo-2 https://www.astera.com/fr/knowledge-center/oltp-and-olap/#:~:text=Structure%20de%20donn%C3%A9es%20normalis%C3%A9e%20%3A%20Les%20bases%20de,un%20stockage%20et%20une%20r%C3%A9cup%C3%A9ration%20efficaces%20des%20donn%C3%A9es.
---
## 1 - Choix de la base de donnée

Réfléchir d'abord à l'utilisation de la donnée
Différence entre données normalisées et données dénormalisées.
Différence entre [[OLTP]] et [[OLAP]]

### Normalisées (OLTP)
La donnée normalisée permet de faire des ajouts, modification ou suppression rapidement et sans se prendre la tête. 
En gros, on ajoute des lignes et on en supprime quand on en a besoin.

Nom | Adresse |
------ | ------|
PYT | France|
PYT | Japon
Julien | France|
Julien | Belgique |

### Dénormalisées (OLAP)

La donnée sert à l'analyse complexe, permet de comprendre ou prendre des décisions

Nom | Adresse 1 | Adresse 2 |
| --- | ------ | --------- |
PYT | France | Japon |
Julien | France | Belgique |

## 2 - Séparer la donnée en parties logiques

Il faut se simplifier la vie pour les futures requêtes.
Si on se retrouve à devoir faire des requêtes à rallonge où l'on utilise des *substring*, des *left')* ou *right()* c'est que déjà cette règle aurait dû être appliquée.

### Ne pas faire
| SST | Puissances | 
|----|-------------|
|SST01|appelée : 200 <br /> souscrite : 500 <br /> installée : 300| 

### À faire
| SST | Puissances appelée | Puissance souscrite| Puissance installée |
|----|:---------------------:|:--------------------:| :---------:|
|SST01|200|500|300|

## 3 - Ne pas abuser de la règle 2

Décomposer c'est bien mais il ne faut pas tout décomposer au point de complexifier l'analyse.

### Ne pas faire 

| Code région | Code département | Code commune | Code client |
| :--------------:| :------------:| :--------: | :--------:|
| 03 | 00 | 00 | 00-00 |

### À faire

| Nom | Téléphone      |
| :-: | :------------- |
| PYT | 03-00-00-00-00 |

## 4 - Définir des règles d'homogénéité cohérentes
Définir en amont des règles pour la donnée permet d'éviter des erreurs de duplication

Erreurs possibles :

| ID    | Nom        | Puissance |
| ----- | ---------- | --------- |
| SST01 | Bâtiment 1 | 1 200     |
| SST02 | Bâtiment 2 | 500       |
| SST3  | Bâtiment 3 | 1500      |
| SST03 | Bâtiment 3 | 1500      |


### Homogène
Le format d'un attribut doit-être identique partout
- soit des espaces soit non
- soit une unité soit non
- soit vide soit false soit non
- soit oui soit yes soit true

### Cohérente
Le formatage d'un attribut ne se fait pas dans le base de donnée, la base de donnée est **brute**
- ne pas mettre de séparateur de milliers dans les chiffres

### Les ID
Les id doivent être unique et **courts**


## Ne pas multiplier la donnée bêtement

facultatif

| SST | nbre de Lgts | Puissance | Moy par Logement |
| :-----: | :-----------: | :-----------: | :--------------: |
|SST 01 | 30 | 2400 | 80 |
|SST 02 | 50 | 3000 | 60 |
|SST 03 | 10 | 1000 | 100 |

Ici l'attribut moyenne par logement est peut-être inutile ? 
Une requête simple nous permettra de la retrouver

| SST | Zone Nord | Zone Sud |
| :---: | :--------: | :-------: |
|SST 01 | TRUE | FALSE |
|SST 02 | TRUE | FALSE |
|SST 03 | FALSE | TRUE |

Ici, l'une des 2 zones est inutiles et peut-être remplacée par :

|  SST   | Zone |
| :----: | :--: |
| SST 01 | NORD |
| SST 02 | NORD |
| SST 03 | SUD  |


## Définir la valeur *null*

La valeur *null* peut vouloir dire *inconnue*, *manquante* ou encore non applicable.
Une fois que l'on a défini chaque colonne de notre base de donnée, il faut définir pour chaque colonne si elle acceptent la valeur *null* et si oui à quoi elle correspond.

>Note
> La valeur null ne peut pas être admise dans la colonne *ID*


