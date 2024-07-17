## Créer des noms de lignes pour s'aider
Par exemple quand le *content* démarre et quand le *content* termine.
*content-start*
*content-end*

```css
.container {
Display: grid;
grid-template-columns: 1fr [content-start] 1fr [content-end] 1fr;
}
```

Cela crée une ligne nommée entre les colonnes qui font ici 1fr.
## Etirer le contenu sur les colonnes comprises entre *content-start* et *content-end*
```css
.container {
Display: grid;
grid-template-columns: 1fr [content-start] 1fr [content-end] 1fr;
}

.content {
grid-column: content-start / content-end;
/* OU */
grid-column: content;
}
```