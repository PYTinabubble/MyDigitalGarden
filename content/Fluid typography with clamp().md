---
title: CSS Clamp()
draft: 
tags:
  - code
source: https://www.smashingmagazine.com/2022/01/modern-fluid-typography-css-clamp/
---
## Définir les tailles de polices 
[typescale](https://typescale.com/) permet de définir des tailles de police selon le *scale*, la taille de base, la police choisie, le *line-height* ou encore le *letter-spacing*
## Calculer la *preferred value* selon son point de départ et son point d'arrivée 

Imaginons que le designer nous a donné des tailles de police et des breakpoints à appliquer. En tant que développeur nous devons implémenter une typographie fluide selon ces paramètres :

- Minimum font size = `36px` (y1)
- Maximum font size = `52px` (y2)
- Minimum font-size s'arrête à partir d'une largeur de viewport de  `600px` (x1)
- Maximum font-size démarre à partir d'une largeur de viewport de `1400px` (x2)

![[Pasted image 20240707171107.png]]

Prenons ces valeurs et mettons les dans la fonction représentant la typographie fluide
$$y=\frac{v}{100}\times x + r$$

On se retrouve avec 2 équations à 2 inconnues :
- La largeur du viewport `v` 
- La taille relative `r`
$$(1): y1=\frac{v}{100}\times x1 + r$$
$$(2): y2=\frac{v}{100}\times x2 + r$$

On peut prendre la première équation et la transformer comme telle :

$$r=y1 - \frac{v}{100}\times x1$$

on peut remplacer  `r` dans la seconde fonction pour calculer `v` :

$$v=\frac{100\times (y2-y1)}{x2-x1}$$
$$v=\frac{100\times(52-36)}{1400-600}$$
$$v=2$$

on obtient la valeur de largeur du viewport : `2vw`. de la même façon on peut isoler `r` et le calculer en utilisant les paramètres adéquats :

$$r=\frac{x1y2-x2y1}{x1-x2}$$
$$r=\frac{600\times52-1400\times36}{600-1400}$$
$$r=24$$


> [!NOTE] Note
> Cette value est en pixel et les valeurs relatives doivent être exprimées en `rem` donc nous pouvons diviser la valeur en pixel par `16` et obtenir `1.5rem`
> Nous devons également convertir la limite minimale de `36px` et la limite maximale de `52px` en `rem` soit `2.25rem` et `3.25rem`

Maintenant que nous avons obtenu ces valeurs, nous pouvons les ajouter à la fonction clamp() dans le css

```css
font-size: clamp(2.25rem, 2vw + 1.5rem, 3.25rem);
```

Nous pouvons faire le graphique de cette fonction pour confirmer que les valeurs calculées sont correctes.

![[Pasted image 20240707171503.png]]

Pour résumer, nous pouvons utiliser les 2 fonctions suivantes pour calculer la *preferred value* et ses paramètres `v` (exprimée en `vw`) et `r` (exprimée en `rem`) depuis les les tailles de police et largeurs de viewport choisies
$$v=\frac{100\times (y2-y1)}{x2-x1}$$
$$r=\frac{x1y2-x2y1}{x1-x2}$$

## Utopia
[Utopia](https://utopia.fyi/type/calculator/) Outil permettant de calculer et récupérer chaque *font-size* selon des *breakpoints* choisis.

