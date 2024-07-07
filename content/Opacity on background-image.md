---
title: Opacity on background-image
draft: false
tags:
  - code
---
## Opacité avec background-image

Il n'y a pas d'option d'opacité pour "background-image".
Mais il est possible d'ajouter de l'opacité au container qui a ce "background-image".
Mais l'opacité s'applique à tous les éléments dans le container.

La solution est d'ajouter l'image comme background d'un **pseudo-element** du container.

## Background-image sur le pseudo-element

Tout comme le container lui même, le pseudo-element peut avoir un "background-image" **et** une opacité
Par exemple si le container est le header :

```css
header {

    width: 100%;

    position: relative;

  
header::before {

      content: '';

      position: absolute;

/* taille pseudo-element = taille container */

      top: 0px;

      right: 0px;

      bottom: 0px;

      left: 0px;

      background-image: url(/src/assets/img/image.jpg);

      background-repeat: no-repeat;

      background-size: 125%;

      background-position: 30% 25%;
      
/* ajoute de l'opacité au pseudo-element qui ne comporte que le background-image */

      opacity: 0.25;

/*Pour être certain que le pseudo element est bien en arrière plan du container */

      z-index: -1;

    }
```
