---
title: Formation revit
draft: false
tags:
  - revit
  - autodesk
  - formation
---
# Famille

![[Revit_familles.excalidraw]]

**Type** : je modifie les caractéristiques propres à l'objet.
**Catégorie** : je modifie les caracteristiques de tous les objets de la même catégorie

**Différentes familles** :
- Familles système : livrées avec le logiciel (murs, plafonds, ...), il faut les dupliquer pour en créer d'autres
- Familles chargeable (.rfa) : familles que l'on peut trouver sur internet et charger dan,s le logiciel.
- Famille in situ : familles créées pour le projet en cours, "in situ". Il s'agit vraiment de choses spécifiques.

>[!warning] 
>Assigner une catégorie au famille que l'on crée !

La liste des catégories possibles est exhaustive dans Revit, mais il existe une catégorie fourre-tout

Extensions fichiers Revit : 
.rvt : projet
.rfa : Famille
.rte : Gabarit de projet
.rft : Gabarit de famille

# Interface de Revit
- Projet :
	- Nouveau : appeller un gabarit (préconfig différentes selon gabarit)
	- Ouvrir : va chercher un projet
- Famille :
	- Nouveau : Ouvre le gabarit de famille pour créer une famille
	- Ouvrir : Ouvre le dossier où se trouve toutes les familles

>[!danger] Mise à jour
>Il faut faire les mise à jour

Il faut installer les version des logiciels antérieurs pour pouvoir enregistrer en version antérieures

## Le logiciel

Onglets de "architecture" à "système" c'est de la 3D
Annoter n'est que de la 2D
_Tout ce qui est annotatif est propre à la vue dans laquelle on est lorsqu'on crée l'annotation_
Une côte sur une vue ne se trouveras pas sur une autre vue.

Pour la topo : demander aux géomètre des plans autoCAD avec le Z comme attribut géométrique; pas juste annoté.

Onglet "complément" pour e-transmit (ou Formit = sketchup autodesk)

Barre d'accés rapide (la mettre sous le ruban pour pouvoir y ajouter des outils)

En barre de la fenêtre (à gauche) barre de mofification de vue

Dans option : régler les couleurs, les alertes sauvegarde, les raccourcis si besoin

Zoom to : raccourci **ZA** ou double-clique molette
Orbital : Shift + molette **si on sélectionne un objet il devient pivot de la caméra**
Pan : Molette seule
ViewCube : Clique droit dessus **quand la vue est dévérouillée** :
- changer perspective ou ortho (perspective déformée)
- Selectionner une vue d'orientation 
>[!Warning] Dupliquer la vue avant de changer des réglage puis verrouiller la vue (barre de tâche en bas à gauche, cliquer sur la maison avec le cadenas)
>

Pour faire une cube en 3D se servir du cube qui entoure le projet, s'il n'est pas affiché :
En bas a droite cliquer sur l'ampoule pour afficher tous les objets masqués

Pour revenir au modèle 3D dans sa globalité :
Dans propriété de la vue :
- Etendues
	- décocher "zone de coupe"

Barre accès rapide avant dernier bouton sert a fermer tous les onglets de vues ouverts sauf celui en cours (seulement si les vues sont affichées en onglet et non en mosaïque)

## Selection

Comme ACAD
Après une sélection l'icone filtre (entonnoir) apparait et permet de filtrer les objets de la selection en cours.

Quand je survolle un objet et clique sur TAB :
- Sélectionne les autres objets autour
- sélectionne toutes les lignes d'une polyligne
- clique gauche pour sélectionner l'objet trouvé avec TAB

## Vues

>[!Warning] Bien penser à double-cliquer sur la vue dans l'arborescence, un seul clique ne l'ouvre pas et nous n'avons donc pas changé de vue.

### Masquer/isoler

>[!Attention] Dupliquer la vue avant changement

#### Isoler

Sélectionner l'objet
- icone "Lunettes" en bas à droite
	- isoler l'élément 
	- Isoler la catégorie
		- On se retrouve dans une fenêtre temporaire
			- On peut restaurer une fois la tâche terminée
			- On peut appliquer pour créer une vue de l'objet isolé par exemple

#### Masquer

Sélectionner l'objet
- Icone "lunettes" icone "Lunettes" en bas à droite
	- masquer l'élément
	- masquer la catégorie
		- restauré
- Clique droit sur l'objet
	- masquer dans la vue 
		- Element
		- Catégorie
			- Pour restaurer : barre modifications de vue en bas à gauche : ampoule 

Ampoule :
Tout ce qui est en magenta est actuellement masqué 
Selectionner l'objet :
- clique droit sur l'objet 
	- afficher dans la vue 
		- élement
		- catégorie

Si on perd la vue {3D} dans l'arborescence :
- Onglet vue
	- vue 3D
		- vue 3D par défaut

## Coupes

Aller dans l'onglet VUE, cliquer sur "Coupes" (que sur les vues en plan et en élévation)

Coupe brisée : Séléectionner la coupe et dans le ruban : "scinder la coupe"

Dans propriété de la coupe on peut décider à quelle échelle le trait de coupe s'affiche ou non

On peut dupliquer une vue pour avoir plusieurs échelles (les échelles sont en bas à gauche de la vue)

## Styles

Changer les épaisseurs de ligne :
Dans onglet "Gérer"
	Paramètres supplémentaires
		épaisseur de ligne 
("le 6 fera un trait d'épaisseur de 1.4 à 1:10 et xxx à 1:500, ...")

**afficher les épaisseurs** : sur la barre d'accès rapide 
En affichant les épaisseurs on voit ce que l'on aura à l'impression

On peut changer le style d'un objet quelque soit la vue, ou dans une vue uniquement

Pour régler le style d'un objet (sur toutes les vues)
- onglet "gérer"
	- style d'objet

Pour changer que dans la vue en cours
- Onglet "vue"
	- Visibilité et graphisme : raccourci **VV**
		- je cherche lélément et clique sur remplacer dans la colonne de ce que je veux remplacer
Le réglage par vue passe au dessus du style dans la vue **concernée**

Pour enlever un réglage de vue :
- retourner dans VV
	- remplacer
		- "pas de remplacement"

On peut changer le style par élément 
Cela permet de changer le remplissage par exemple

- Sélectionner l'éléement
	- clique-droit
		- "remplacer les graphismes dans la vue"
			- par élément
			- par catégorie

Attention que le premier plan ne cache pas l'arrière plan

Arrêtes cachée / Lignes cachées :
- onglet "vue"
	- "afficher les lignes cachées"
		1- Sélectionner l'élément "qui cache"
		2 - Sélectionner l'élément "qui est caché" (possibilité de faire une sélection mutiple, il faut cocher la case "sélection multiple" qui apparait sous le ruban)

Pour supprimer les lignes cachées même manips mais depuis :
- onglet "vue"
	- "supprimer les lignes cachées"

Possibilité de changer le style des lignes cachées dans VV

# Créer des lignes 

- Gerer
	- Parametre supplémentaire 
		- Style de ligne
			- Possibilité de créer un style de ligne : "Nouvelle", on crée une sous catégorie dans la catégorie "ligne"

- Annoter
	- **Ligne de détail**
		- Tout à droite sous "style de ligne"
			- Choisir son style de ligne

>[!warning] tout ce que l'on annote est lié à la vue dans laquelle on la trace contrairement aux éléments 3D

>[!danger]  si on supprime une vue ou même un axe de coupe on perd les annotations de la vue

**Ligne de modèle**
Ligne de modèle permet de dessiner une ligne dans la 3D en choisissant (sous le ruban) le plan sur lequel dessiner la ligne (niveau 1, ...)
Permet d'avoir une ligne dans la 3D pour s'accrocher par exemple

On peut convertir une ligne de modèle en ligne de détail et inversement
- sélectionner la ligne 
	- Dans ruban " convertir les lignes" seulement si l'on est en vue en plan

Quand on dessine de lignes de détail ou de modèle on a des outils à dispo (rectangle, cercle,...)
On utilise les cotations qui apparaissent lorsque l'on sélectionne un segment pour changer les dimensions

Sous le ruban : "décalage" permet de tracé avec un décalage : en pointillé on voit le tracé de la souris et en décalé de la valeur entrée on voit la ligne

# Dupliquer

**Dupliquer** une vue la duplique **sans détail à savoir sans annotation**
**Dupliquer avec les détails** permet de récupérer également les annotations

Elles ne sont pas pour autant inter-dépendance

>[!warning] dorénavant toutes les annotations créées seront à nouveau propre à la vue 

# Enregistrer sous

Dans la fenêtre d'enregistrement :
- "option..." au dessus de "annuler"
	- Nombre de version de fichier a chaque ctrl+s

# Murs

Mur architectural : Mur non porteur, associé a un niveau et monte vers un niveau supérieur
Mur porteur : mur qui se dirige vers une niveau inférieur
Mur par face : pour habillé un volume (par exemple bardage avec un mur rideau)

>[!note] on peut transformer archi et porteur et inversement en cochant/décochant "structure" dans les propriétés

>[!danger] Toujours tracé dans le sens des aiguilles d'une montre pour ne pas inverser intérieur/extérieur 

Ligne de justification : où va se poser l'**axe du mur** que l'on crée
- Axe du mur : au milieu du mur (toute compo comprise)
- Axe du porteur : au milieu de la couche "porteuse" dans la compo du mur
- Nu fini: extérieur : extérieur du mur complet 
- Nu fini: intérieur : intérieur du mur complet
- Nu porteur: extérieur : extérieur de la couche porteuse
- Nu porteur: intérieur : intérieur de la couche porteuse

>[!important] important pour les dimensions (décalage si on change la composition du mur)

A la création d'un mur on peut utiliser la "ligne verte" dans les outils de tracé pour sélectionner des lignes à suivre par le mur. 
- Sélectionner mur 
	- onglet "modifier / placer mur"
		-  "Choisir des lignes" (Icône ligne verte)
On pose la souris sur la ligne et en glissant la souris on choisit intérieur/extérieur. Si on appuie sur TAB on peut séléctionner tout un tracé.

>[!Important] bien choisir l'axe du mur à prendre en compte avant dans les propriétés

>[!note] Avantage : le mur est dessiné dans le bon sens (sens horaire)

## Modifier le profil 

Sélectionner un mur et cliquer sur "modifier le profil" 
Ne peut se faire qu'en élévation 
Ouvre le mode esquisse et permet de modifier les arrêtes du mur ou ajouter des ouverture avec les outils de dessin (cercle par ex)

# Quadrillages & fils

Ils se trouvent dans architecture

Pour changer l'incrémentation modifier le texte de la bulle **juste après avoir tracé**

Pour afficher sur la vue 3D entrer dans les propriétés de la vue {3D} et cliquer sur "modifier" dans "afficher les quadrillages"

Pour afficher les bulles des 2 côtés, cocher la case après sélection du fil.

Après sélection du fil cliquer sur l'éclair permet d'améliorer l'affichage quand 2 fils sont trop proches et donc bulles sont superposées.

Se dessine comme les lignes de détail

Afficher des fils selon le niveau :
- Dans une élévation
	- Dé-cadenasser le fil que l'on veut descendre sous un niveau
		- Le descendre
			- Il n'apparaît plus sur les plans de niveau au dessus
			- Pour améliorer l'affichage en 2D à savoir ne pas voir le fil modifié a une hauteur différente sur l'élévation 
				- Cliquer sur "3D" pour passer en "2D" et le remonter: il est désormais afficher normalement dans sa vue 2D

## modifier le style

Dans fenêtre propriété du fil séléctionné :
- cliquer sur "modifier le type" 
	- Je duplique pour créé un nouveau type de quadrillage
		- Je renomme et change le style
			- Je peux sélectionner mon nouveau style depuis la fenêtre propriété après avoir sélectionner les fils à changer

Pour ne pas afficher le segment central (que les bulles) et alléger le plan :
- modifier le style du quadrillage (attention à dupliquer si on veut créer un nouveau type)
	- "Segment central"
		- "Aucun"

## Entrer dans le mode esquisse pour faire du quadrillage complexe

Une fois quadrillage sélectionné : cliquer sur "segments multiples"
On entre en mode esquisse (dans le ruban on voit la validation de l'esquisse), le tracé est en rose

On peut utiliser la ligne verte des outils de dessin pour sélectionner avec TAB tous mes murs par exemple.

# modifier tous les objets dans même type dans un projet

Clique droit sur un élément du type puis "sélectionner toutes les occurrences"

# Outils de modification

Utiliser le ruban d'option pour :
- contraindre
- détacher
- copier
- change le centre de rotation (raccourci espace)
- ....

**Prolonger/ajuster** 
Je dis "jusqu'où je prolonge" d'abord et l'objet "à prolonger" ensuite
Ajuster je clique sur la limite et je choisis la partie que **"je veux garder"**

**Aligner**
J'aligne sur
1. La face que je veux attendre
2. L'objet à aligner

**Symétrie**
On séléctionne l'élément à projeter puis l'axe de symétrie
Si on a pas d'axe on sélectionne l'élément d'abord puis "symétrie - dessiner l'axe", puis on dessine l'axe de symétrie.

**scinder**
Je coupe avec le cutter et scinde, si je coche "supprimer le segment interne" et clique à 2 endroits je supprime la partie entre les 2 coupures.
Je peux "recoller" en étirant le mur vers l'autre

Pour créer un espace "scinder avec espace"

>[!attention] l'espace devient une contrainte de côte, l'espacement restera même lorsque l'on bouge les éléments

Pour recoller le mur il faut :
1. Supprimer la contrainte de côte (ouvrir le cadenas)
2. Cliquer sur le "T" autorisant la jonction 
3. Étirer une partie vers l'autre

# Contraintes

Afficher les contraintes en rouge :
- barre de modification de vue (en bas à gauche)
	- icône de cotation avec cadenas

Permet de voir toutes les contraintes présentes dans la vue et de les modifier ou comprendre le comportement des objets.

## Réseau

Travailler avec le ruban d'option
Linéaire ou radiale : comme son nom l'indique
Cocher/décocher "regrouper et associer" : par défaut coché
Nombre d'éléments : y compris l'élément de départ
"2ème" : On dessine l'écart entre le premier et le 2e et cet écart est mis entre chacun des éléments
Dernier : On clique à l'endroit du dernier et revit distribue le nombre d'objet dans l'intervalle entre l'objet et le clique.

Changer le nombre :
_"2ème"_ : Ajoute des éléments et garde le même intervalle
_"Dernier"_ : Diminue l'intervalle pour intégrer les nouveaux éléments entre le premier et le dernier

Changer l'intervalle :
_"2ème"_ : sélectionner un élément du réseau
- cliquer sur "activer les contrôles et cotes" dans le ruban (côte avec punaise)
	- On voit les côtes on change l'intervalle
		- Les éléments sont écartés/resserés selon le nouvel intervalle
_"Dernier"_ : fais la même chose que "2ème" mais garde la contrainte du nombre (si je change le nombre, Revit ajoute les nouveaux élément entre le premier et le dernier et l'intervalle est modifié)

Si je dois modifier un paramètre d'un objet du réseau, je dois rentrer dans le groupe 
- Sélectionner le groupe
	- Dans ruban "modifier le groupe"
		- Dans la fenêtre "d'esquisse" je sélectionne une élément du groupe
			- Je modifie le paramètre (par exemple hauteur du mur ou section : inclinée, angle :5°)
				- Je valide mon esquisse et tous les murs du réseau sont modifiés

# Modifier une [[REVIT_Famille|famille]]

**Annotations** : il faut ouvrir la famille dans Revit
**Objet** : 
- Double cliquer sur l'objet dans le projet
- Clique droit dans l'arborescence 
	- "Edition"
**Familles système** : changer le type

# Les côtes 

Onglet "Annotation"

>[!note] pour changer une côte sélectionner le mur qui lui est perpendiculaire

**Alignée**
Face du mur : côte depuis la face extérieur du mur
Axe du mur : depuis l'axe du mur
Murs entiers : tout le mur
Références individuelles : démarre une côte depuis une arrête du mur

**Options** : quand murs entiers choisir si on veut côter aussi les ouvertures dans le mur (axe de l'ouverture ou de bord à bord), si on veut coté les intersections ou juste l'intérieur du mur

on peut "modifier les lignes d'attaches" pour en ajouter en cliquant sur un élément à côter (cliquant dans l'espace au delà pour terminer), Ou en enlever en répliquant sur un élément déjà côté.

> Quand les murs ne sont pas à 90°, il faut utiliser TAB pour trouver le coin (essai sur une pièce triangle)
>Après avoir sélectionner "côte alignée" poser la souris sur le coin (du triangle par ex) et TAB donne dans l'ordre :
>- mur adjacent
>- Exterieur
>- épaisseur du mur
>- Axe du mur
>- Axe mur adjacent
>- **Coin**
>Je clique pour attacher la ligne d'attache à ce qui m'intéresse 

Isoler l'objet peut permettre de côter plus facilement (pour les dessins complexes)

### modifier le type de côte

>[!warning] Dupliquer le type !

"Distance de l'accrochage à la ligne de côte" = intéressant pour que les côtes soient toutes à la même distance (créé un accrochage)(mettre 10mm par ex)

Format des unités : soit du projet ou propre à ce type de côte
Pour modifier les paramètre du projet :
- Onglet "gérer"
	- "unités"

On peut se servir des "unités alternatives" pour mettre une valeur dans 2 unités différentes (au dessus et en dessous de la ligne par ex) 

On ne peut pas modifier le texte d'une côte par du numérique (on ne peux pas tricher)

On peut ajouter du texte à une côte en double cliquant sur la valeur
Ou pour tout un type de côte en ajoutant un préfixe dans modifier le type 

**Longueur d'arc**

3 temps :
1. Je sélectionne le coté d'arc, intérieur ou extérieur
2. Je sélectionne la ligne de départ
3. Je séléctionne la ligne d'arrivée
(Possibilité d'utiliser TAB pour trouver le coin)

**Côtes d'élévation**

On peut changer la base relative de la côte (x depuis le niveau y ou x' par rapport au niveau Z)
Pour ça changer le type (dupliquer !) Et "Référence de l'élévation" et passer de "point de base du projet" à "relative"
Choisir ensuite dans les propriétés la base relative 
(Pour indiquer du texte devant, dans modifier le type > unités principales > entrer le texte dans indicateur

# Hachurage : Zone de pochage / Zone de masquage

Ne se voit que dans la vue où elle a été créée 
Ne se voit pas en 3D

Annoter > zone > zone de pochage/zone de masquage

On entre dans l'esquisse pour tracer notre zone de hachures

>[!note] Pour ne pas voir le contour de la zone de masquage mettre type de ligne invisible
>Si l'ont veut qu'une partie du contour, scinder le contour en plusieurs parties et changer le type de ligne de chaque partie (invisible ou non)

# Point de base du projet et point topo

De base que dans la vue plan masse
Réaffirmer soit par l'ampoule soit par **VV**

Point de base du dessin (0,0) du projet.

---

# [[REVIT_2022-10-25#Les côtes|Côtes]] de mur 

Lorsque l'on fait une côte du mur entier il faut "jouer" avec la côte : Revit changera la côte selon l'endroit où elle est (extérieur à intérieur, intérieur à intérieur, etc..)

Comment bien gérer les côtes temporaires pour redimensionner :
>[!hint] Je sélectionne le mur que je veux bouger et qui est "perpendiculaire" au mur que je veux modifier (celui que j'agrandis ou rétréci) > la côte temporaire "utile" apparaît 

---
# Elevation

En plan : sélectionner un symbôle d'élévation pour choisir le cadre de visibilité
>[!warning] bouger le symbole élévation avec l'outil déplacer sinon le cadre de vue bouge avec

## Créer une élévation

onglet "vue" > Elevation
Dans arborescence d'élévation une nouvelle vue apparaît 

>[!Important] si je ne vois pas un objet depuis une vue élévation j'ai sûrement mal placé le cadre de vue de l'élévation dans la vue en plan

---

# Les sols

Onglet "Architecture" > Sol 

Dalle architecturale : juste un sol
Plancher : structurel, porteur (pas de différence majeur avec la dalle archi)
Sol par face : habille un sol

On se retrouve en mode esquisse

- on peut choisir le type de dalle dans les propriétés
- Dans les outils de dessin on a **"choisir des murs"** (permet de bouger la dalle quand on bouge les murs)
	- Nue intérieur/extérieur poser la souris sur l'arrête intérieure ou extérieure du mur (verifier les pointillés pour savoir)
		- TAB pour séléctionner le contour de murs entier

Si je veux un décalage par rapport au nu extérieur > dans le ruban outil je rentre le décalage :
- négatif pour intérieur
- Positif pour extérieur

Après avoir séléctionner le sol, je peux "modifier la limite" pour retourner dans l'esquisse
Pour créer des ouvertures par exemple

En bas à droite de la fenêtre "activer/désactiver la sélection par face" permet de sélectionner les murs ou sol en cliquant sur leur faces

---

# Création d'un niveau

Ne fonctionne qu'en élévation
Onglet "architecture" > "Niveau"
- Ruban outil : choisir le type de vue à créer avec les niveaux
	- Créé un niveau avec sa vue en plan, de plafond et structurel

Je peux copier un niveau existant (plus intuitif) mais je crois recréer les vues :
- outil copier après avoir sélectionner le niveau
	- Les niveaux sont noirs et non bleu ce qui veut dire qu'ils n'ont pas de vues associées de créées 
		- Onglet "Vue"
			- Nouveau plan d'étage, faux plafond, étage

---

# Monter un niveau

Dans la vue en plan d'un niveau supérieur, on voit en fond le niveau inférieur
- on peut changer ça dans les propriétés de la vue
	- "Niveau en fond de plan"
		- Plage: niveau de base

On peut copier/coller un autre niveau (du moins les objet copier)
- Après avoir sélectionner les objets (avec TAB par exemple)
	- Dans ruban "presse papier"
		- "Copier"
			- Dérouler l'option "Coller"
				- "Aligner sur les niveaux sélectionnés"
					- Choisir le niveau de destination

---

# Créer un toit

Le toit est attaché au niveau supérieur même si les murs ne sont pas contraints au niveau supérieur

## Toit par tracé

- dans la vue en plan du niveau sup
	- Lance l'esquisse
		- On peut changer décocher l'inclinaison des côtés que l'on a sélectionné
		- Le débordement est sous le niveau bas
			- Je peux rattacher les murs au toit :
				- je sélectionne les murs (TAB)
					- Je choisis "haut" car je veux sélectionner le haut des murs 
						- Je clique sur le toit

En vue en plan on ne voit pas le toit entièrement, c'est à cause du réglage de la plage de la vue.
C'est un réglage dans les propriétés de la vue.
Plage de vue > modifé
- cliquer sur "affichage" pour voir le schéma explicatif

**Plan de coupe** : par défaut à 1,20m 
- il s'agit de la hauteur à laquelle revit arrête d'afficher les éléments dans la **vue en plan**

## Toit par extrusion

On dessine une ligne et c'est cette ligne qui va s'extruder

Chaque mur est potentiellement un "plan" pour l'extrusion = c'est le mur par lequel part l'extrusion

On trace la ligne (juste une ligne non bouclée) et on valide

Reste a "attacher" les murs au toit :
>[!Note] séléctionner tous les murs > "attacher haut/bas" et séléctionner le toit

---

# Les menuiseries

>[!hint] passer par onglet "insérer" > famille autodesk : bibliothèque de famille

Onglet "architecture"
Pour changer la façade d'une porte ou fenêtre (placer la fenêtre sur une autre façade)
>[!danger] Décocher "contrainte" et cocher "détacher"

---

# Cage d'escalier


Onglet "architecture" > Cage

Mode esquisse pour tracer la cage et la contraindre en niveau bas et niveau haut (traverse tous les étages)

## Créer un escalier

Ruban d'options 
Ligne de justification, on choisit où se place l'escalier par rapport à son support
Attention de bien finir les 16 marches sans quoi l'escalier n'atteint pas le niveau supérieur

"modifier le type"
- Je peux modifier le type de volée de marche dans les propriétés du type
	- Je peux cocher/décocher les marches contremarches pour créer un escalier sans contremarches
- Modifier le palier (identique à la marche ou non)
	- Je décoche identique pour le configurer
- Les supports (limons) peuvent être modifiés de la même façon
	- "Support intermédiaire" : cocher/décocher pour créer un limon intermédiaire

Une [[REVIT_Famille|famille]] est çoncu pour s'intégrer à un élément (mur, toit,... par exemple)
Peut également être inséré sur un plan de construction

![[REVIT_Escalier.excalidraw]]

Créer une zone de coupe autour de la séléction :
- séléctionner les objets 
	- "Zone de séléction" raccourci **BX**
		- Pour l'enlever et la réinitialiser : **décocher zone de coupe dans les propriétés de la vue et la recocher pour la réinitialiser**
		- Permet également de créer une vue de la séléction pour communiquer

On peut créer un escalier en esquisse :
- Sélectionner l'escalier 
	- Modifier l'escalier
		- Prendre la volée ou palier et cliquer sur convertir
			- modifier l'esquisse

>[!danger] irréversible

Il faut une limite (lignes vertes) mais **pas autour** juste sur les côtés
En créant des arcs (lignes vertes) au lieu de lignes droites on créé des courbes 
Aligner les lignes de marches aux limites ensuite 

Profil de marche modifiable par familles de profil

---

# Les gardes corps

Onglet "Architecture" > "gardes-corps"

Dérouler :
 - Placer sur l'escalier / Rampe : permet de remettre un garde corps sur l'escalier (si on l'a supprimé par erreur)
	- esquisser la trajectoire : 
		- En mode esquisse
			- Utiliser les outils de dessin (comme ligne verte pour coller à des contours)
				- Penser à attacher le garde corps à l'élément (la dalle par exemple). Il est attaché au niveau par défaut
					- Séléctionner le garde corps > choisir un nouvel hôte (par exemple un mur et il suivra le haut du mur)
					- 
		- Toutes les parties du gardes corps sont modifiables par logique
		- Chaque parties du garde-corps (poteaux, traverses, ...) est modifiable ou chargeable via une famille (par exemple charger la famille poteaux fonte, changer la famille de profil de traverse,..)

---

# Composition des murs

>[!warning] Dupliquer le type

Dans les propriétés du type du mur :
- structure > "modifier"
	- Insérer des couches
	- Monter/descendre les couches
- Les couches limites en gris délimite ce qui est structurel
	- Colonne fonction : fonction de la couche, finition 2 : intérieur, finition 1 : extérieur, couche membrane (invisible) : étancheité
		- L'indice entre parenthèse : niveau de priorités, pour attacher la géométrie, les porteurs ensembles, les finitions ensembles...
	- Colonne matériau

Modifier les matériaux des murs.
>[!warning] Dupliquer/créer un nouveau matériau

Pour chaque couche 
Si visible : 
- onglet "graphique" : onglet graphique : changer les motifs de surface et de coupe 
- Onglet "apparence" : mettre une image pour le matériau
Si invisible :
- onglet "graphique" : changer motif de coupe

Dans composition du mur : en bas a droite "vue" : 
- coupe : permet d'avoir les boutons de modifications verticales
	- Cela permet de modifier verticalement chaque couche du mur (par exemple l'enduit qui irait au dessus de la dalle)
		- Cliquer sur modifier 
			- Choisir la limite de la couche (trait de contour)
				- Décadenasser 
				- Une flêche pour étirer l'enduit apparaît sur les murs 
	- Permet de créer un soubassement :
		- Je "scinde la couche" : je clique avec le cutter sur le trait exterieur
		- Pour changer la hauteur je clique "modifier" et cliquer sur le trait de scission pour changer la côte
		- Ma couche a une épaisseur "variable"
			- J'"insère une couche" 
			- >[! Danger] je ne change pas son epaisseur
				- je change son matériau
					- Je clique sur attribuer couche et je clique sur l'apercu sur le contour de la couche a laquelle je dois l'attribuer
	- Fusionner après une scission
		- Cliquer sur "fusionner" puis sur le trait de scission 

## modifier matériau Dalle

Attacher les géométries 
- Attacher le mur sup à la dalle
- Attacher le mur inf à la dalle
- Attacher le mur sup au mur inf

## Incliner des sols

Au moment de l'esquisse (création de la dalle)
- outil "flêche d'inclinaison"
	- Flêche à intégrer à l'intérieur de l'esquisse
		- Dans les propriétés soit je modifie le niveau au bas de la flêche, le niveau du bout de la flêche, le décalage du bas de la flêche par rapport au niveau bas (décalage en hauteur)
		- Si je fais pas inclinaison attention de mettre le décalage à 0 pour que la face haute de la dalle parte a 0 sinon démarrage dalle 30 com au dessus du niveau

## Rampes

Création d'un niveau dédié au départ de la rampe
On donne le niveau de départ et d'arrivée
Ayant choisi le type de rampe (10,12 ou 15% par exemple) la longueur est défini 
Fonctionne alors comme les escaliers : Revit nous donne le nombre de m (comme les marches) il nous reste à tracer.

Dans les propriétés de type on peut changer la longueur maximale de l'inclinaison = au bout de combien de m d'inclinaison il crée un palier.

>[!note] les rampes n'ont pas de composition en couche, pour créer une rampe avec plusieurs couches de matériaux il vaut mieux utiliser une dalle inclinée

A la différence des familles, comme toutes familles système, les murs ne sont pas chargeable dans un autre projet. Pour ça il faut ouvrir les 2 projet (celui où sont les murs et celui dans lequel on veut transférer) > Onglet "gérer" > "transférer les normes du projet" dans la partie "paramètre" du ruban "gérer"

---

# Les poteaux

Poser les poteaux, indiquer le niveau bas et le niveau haut. Les éventuels décalages.
Rentrer dans les propriétés de type pour changer la largeur/diamètre

---

# les éléments de détail

Élément 2D représentant de la 3D

Onglet "Annoter" 
- Composants
	- Composants de détail

>[!note] ne fonctionne qu'en 2D et ne s'affiche que sur la vue où il a été ajouté

Avec plusieurs éléments de détail je peux créer un groupe
Ce "groupe de détail" se retrouve dans l'arborescence dans groupes > détail
Ce qui me permet de le réutiliser

---

# Annotation générique 

Onglet "annoter" > "Symbole" au bout du ruban
Charger le dossier "annotation"

---

# Vue de détail

A partir d'une vue :
- onglet "vue" > "Repère"
	- Encadré le détail à créer
		- On retrouve la vue dans l'arborescence au même endroit que la vue dans laquelle on l'a crée

---

# Vue de légende

Créer une légendre

Dans arborescence, légende > Clique droit : nouvelle légende
- Ouvre une page blanche
	- Annoter : composants > composant de légende
		- Ruban d'option : liste des composants dans le projet
			- Choix de la représentation (en élévation ou en plan)
	- On peut créer tableaux, mises en page, à partir de ligne de détail, textes, ...
