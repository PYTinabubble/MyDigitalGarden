---
draft: false
tags:
---
# Paramètre électriques

Pour démarrer une étude élec
1. Plan GC du bâtiment
2. Bilan de puissance pour fixer la puissance de raccordement (Enedis/RTE)
3. En fonction du besoin de puissance, le raccordement pourra être réalisé en BT ou en HT

Puissance apparente "S" en VA ou kVA
Puissance active "P" en W ou kW
Puissance réactive "Q" en VAR ou kVAR

>[!warning] On peut additionner des kW mais pas des kVA

![[Pasted image 20221103183210.png]]

Plus le cosϕ est proche de 1 plus "S" est proche de "C" et donc est bon
Enedis pénalise si cosϕ < 0.92

ex : Pour une toute petite puissance mais avec un mauvais cosϕ, il faut un transfo permettant de répondre à une puissance réactive très grande (mais inutile).

Plus je consomme du réactif plus "Q" augmente et cosϕ baisse 

Les condensateurs sont actifs > ils créent du "réactif négatif" et et permettent donc de baisse "Q" et d'augmenter cosϕ

>[!note] Tous les moteurs sont déphasés et créent du réactif

## Bilan de puissance

Une fois que l'on a le bilan de puissance on sait combien l'on doit demander à Enedis/RTE

RTE : 400 kV (ex: Gravelines) qu'il transforme en 225kV (HTB) puis en :
- 90 kV
- 63 kV
- 150 kV
- 20 kV
Il y a donc 2 transformations

Enedis gère la partie 20 kV

### Raccordement
#### Si la puissance est < 36 kVA

On parle de raccordement à puissance ==limitée== (ancien tarif bleu)
- Raccordement en BT sous 400V : 3P+N en régime de neutre TT (triphasé)
- Raccordement en BT sous 230V : P+N en régime de neutre TT (monophasé)

#### Si la puissance est 36kVA < P < 250kVA :

On parle de raccordement à puissance ==surveillée== (ancien tarif jaune)
- Raccordement en BT sous 400V : 3P+N en régime de neutre TT
non surveillé : tu peux dépasser mais tu n'es pas limité tu paies le surplus 

#### Si la puissance est = 250kVA :

On parle de raccordement à puissance ==surveillée== (ancien tarif jaune ou tarif vert)
- Raccordement en BT sous 400V : 3P+N en régime de neutre TT
- Raccordement en HTA sous 15kV ou 20kV : 3P Obligation de mettre un poste HT et un transformateur.

#### Si la puissance est > ou = 250kVA :

On parle de raccordement à puissance ==surveillée== (ancien tarif vert)
- Raccordement en HTA sous 15 ou 20kV : 3P Obligation de mettre un poste HT et un transformateur.
- Raccordement en HTB si U > à 20kV (RTE)

![[Pasted image 20221103184531.png]]

### Compteur 

Une fois la puissance totale de des appareils pouvant être utilisés simultanément calculée, il est très simple de **savoir quelle puissance de compteur choisir** :
-   un compteur 3 kVA permet de soutirer **3 000 W simultanément** ;
-   un compteur 6 kVA permet de soutirer **6 000 W simultanément** ;
-   un compteur 9 kVA permet de soutirer **9 000 W simultanément** ;
-   un compteur 12 kVA permet de soutirer **12 000 W simultanément** ;
-   un compteur 15 kVA permet de soutirer **15 000 W simultanément** ;

### Tension

La tension "U" s'exprime en V ou kV

### L'intensité

L'intensité "I" s'exprime en A ou kA

>[!conclusion] Une fois la puissance totale de des appareils pouvant être utilisés simultanément calculée, il est très simple de **savoir quelle puissance de compteur choisir** :

### Eloignement du poste de livraison

Si le point de livraison est éloigné de l’installation, il faut privilégier une distribution HT pour les installations à puissance importante.

>[!info] Ce qui coûte le plus cher, c'est le câble

Enedis s'arrête à la limite de propriété 
La question se pose de repartir de là pour tirer un cable BT jusqu'à l'endroit de l'installation ou de tirer un cable HT et mettre un transfo à l'intérieur du bâtiment au plus proche de l'installation.

Ce sont les câbles BT qui sont les plus cher, j'amène donc la HT au plus près de l'installation

- Si Enedis (limite de propriété) est loin, je prévilégie de tirer du câble HT (moins cher) et met mon transfo à l'intérieur : ==Je dois prévoir une loge transfo==
- Si je ne suis pas loin du poste de livraison (Enedis), je fais mon transfo en préfa à la limite de propriété car peu de câble à tirer : ==moins cher en m²==

#### Section de câble

3 critères permettent de déterminer la section de câble :
- La distance
- La puissance
- Le mode de pose

##### Les modes de pose

1>2>3>4
1. Chemin de câbles : Ventilé, refroidi par l'air
2. Dans la terre : T°C terre varie peu; obligation de mettre du cable "armé" (pour empêcher les court-circuits)
3. Dans un fourreau : Réchauffe l'air dans la gaine, monte en température
4. En caniveau soit ventilé soit non

Selon la puissance on peut augmenter la section du cable ==ou== ton nombre de câbles 
Mais la norme oblige à ne jamais dépasser 4 cables par phase

À section égale tu transportes davantage dans du cuivre que dans de l'alu mais le cuivre est beaucoup plus cher

# Régimes de neutre

Le choix du régime de neutre est lié à l’utilisation et au besoin de production.

## Regime TT

- Systématique en raccordement < 250kVA
- Coupure au premier défaut d’isolement
- Obligation d’avoir un dispositif différentiel

![[Pasted image 20221103191031.png]]

## Régime IT

- Possible si transformateur
- Possibilité de fonctionner avec un défaut d’isolement
- Coupure au second défaut d’isolement
- Déconseillé de distribuer le conducteur neutre
- Obligation de protéger le conducteur de neutre par disjoncteur
- Généralement utilisé dans l’industrie

![[Pasted image 20221103191239.png]]

![[Pasted image 20221103191250.png]]

## Régime TN

- Possible si transformateur
- Coupure au premier défaut d’isolement
- Obligation d’avoir un dispositif différentiel pour les locaux à risques particuliers.
- Gain économique avec le régime TNC
- Régime TNC interdit dans les locaux à risques particuliers

![[Pasted image 20221103191419.png]]

![[Pasted image 20221103191426.png]]

![[Pasted image 20221103191436.png]]

# Les symboles électrique

## Le sectionneur

## l'interrupteur

## Le disjoncteur

### Disjoncteur différentiel

## L'interrupteur-sectionneur

## Le fusible

## Contact normalement ouvert

## Contact normalement fermé

## Le transformateur


# Monophasé / Triphasé / Tétraphasé


