---
title: Liaisonner Google fonts dans Sass
draft: false
tags:
  - code
---
# Liaisonner Google Font dans Sass

## Récupérer les polices

Dans l'```index.html```, dans la balise ```<head>``` (toujours en dessous du title) intégrer une balise
```
<style> @import url('https://fonts.googleapis.com/css2?family=font_name:wght@0,400;0,600;0,700&display=swap');
      </style>
```

dans cet url :
- Remplacer le "font_name" par le nom de la police voulue
- Si on souhaite plusieurs police, séparer les noms par ```|```
- Pour spécifier des épaisseurs précise remplacer les nombres après les ```:```
- Il est possible d'indiquer les noms des épaisseurs ou abbréviations 

par exemple : 
```
https://fonts.googleapis.com/css?family=Cantarell:italic|Droid+Serif:bold
https://fonts.googleapis.com/css?family=Cantarell:i|Droid+Serif:b
https://fonts.googleapis.com/css?family=Cantarell:i|Droid+Serif:700
```
- à la fin ajouter ```&display=swap``` permet de contrôler ce qui se passe lorsque la police est indisponible.

## Intégrer les polices à Sass

Dans le dossier base avoir un fichier ```_fonts.scss```
Dans ce fichier ```_fonts.scss``` 
- créer des variables sass selon les fonts et les épaisseurs par ex ```$primary-font``` 
- dans le dossier base ne pas oublier le fichier ```_index.scss``` ou se trouve ```@forward "fonts";``` 
- dans le fichier principal scss, appelé le dossier base avec ```@use "./base" as *;```


