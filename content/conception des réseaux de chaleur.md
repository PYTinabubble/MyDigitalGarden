---
title: Conception réseau de chaleur
draft: false
tags:
  - dalkia
---
**Besoins thermiques : détermination des puissances**
coefficient de déperdition global noté G qui s’exprime en W / °C/ m3 chauffés. L’intérêt de ce coefficient est de quantifier la puissance de chauffage requise afin de maintenir une température intérieure pour une température extérieure donnée. Ainsi, **pour un bâtiment de 3 000 m3** de G connu (0,8 W/°C/m3), qui a une température de non chauffage (TNC) de 21°C alors qu’il fait 5°C à l’extérieur, i l faut une puissance utile de chauffage de : Pour 5°C extérieur, P [en Watt]=G [en W/°C/m3] * V [m3] *(TNC [°C] – T extérieure [°C]) P=0,8*3 000*(21-5)=38 400 W P=38,4 kW

**Le besoin utile d’ECS** pourra aussi s’exprimer : Becs = Vecs [m3] *Cpeau [kWh/t/°C]* ( θecs [°C] - θville [°C]) Avec Cpeau [kWh/t/°C] la capacité calorifique de l’eau p rise égale à 1,16 kWh / t / °C (pour une densité de 1 donc pour 1 tonne occupant 1 m3) θecs[°C] la température de puisage de l’ECS θville [°C] la température de l’eau du réseau d’eau de ville

La détermination des besoins consiste :
- au recensement du type de besoins : chauffage, ECS, autres besoins,
- à la détermination des puissances appelées (chauffage, ECS, non climatiques)
- à la détermination des consommations mensuelles et annuelles,
- à la détermination de la température de départ secondaire nécessaire, 
- à la détermination de la température de retour secondaire.

Les consommations mensuelles utiles d’un bâtiment peuvent être modélisées par une droite de régression linéaire. La régression linéaire est de type :
y = a . x + b18
où
y : MWh vendus/mois,
x : DJU de la période considérée,
a : pente de chauffage en MWh / DJU,
b18 : ordonnée à l’origine en MWh/mois

**Nombre de tubes Il dépend du fluide chauffant : 
- dans le cas de vapeur avec condensat non récupéré, il y a un seul tube calorifugé, 
- si le condensat est récupéré, il y a deux tubes, le tube de retour du condensat étant de diamètre sensiblement plus faible que celui de vapeur ; 
- dans le cas d’eau chaude ou d’eau surchauffée, il y a deux tubes calorifugés de même diamètre.
Il a été également réalisé des réseaux à trois tubes : 
- un aller et un retour pour le fonctionnement d’hiver à pleine puissance, et un aller de diamètre réduit afin de diminuer les pertes thermiques (proportionnelles à la surface des tubes) lors du fonctionnement à faible puissance. Le retour sur investissement pour ce troisième tube est difficile à obtenir. 
- Un troisième tube peut aussi être installé en secours pour des sites sensibles, notamment les centres hospitaliers.
Si la production d’eau chaude sanitaire est centralisée (situation rare), sa distribution nécessite deux tubes supplémentaires, et l’on doit alors réaliser en général un réseau à quatre tubes.

**Dilatation**
Allongement du tube sous l’effet de la température
Tout matériau s’allonge et dilate sous l’effet de la chaleur.
L’allongement libre est donné par la formule suivante : **ε = α.L.∆T** 
Avec
- L la longueur de tube considéré à la température de pose,
- α le coefficient de dilatation,
- ∆T la variation de température entre les températures de service te de pose,
- ε l’allongement de la tuyauterie sous l’effet de la variation de température,
Nous l’avons vu, le transport du fluide s'effectue au sein de tubes caloporteurs, en général en acier.
L’acier est sujet à de fortes dilatations, dès lors qu'il subit une augmentation de température.
**Le coefficient de dilatation pour de l’acier est de 0,012 mm / (m . K).

**Pour une longueur de 100 m, nous avons donc une variation de l’ordre 200 mm.**
Sous l’effet de la température, les tuyauteries se dilatent, et leur allongement, s’il est entravé, entraîne des contraintes qui peuvent aller jusqu’à la rupture après, éventuellement, flambage dans les parties droites. Pour y remédier, on utilise au cours du tracé du réseau des organes de dilatation qui, par leur déformation élastique, compensent l’allongement des tuyauteries. Ces organes sont placés entre des points fixes qui permettent de limiter les dilatations absorbées par ces organes compte tenu de leurs caractéristiques. Ils opposent à la déformation une certaine résistance qui se reporte sur ces points fixes ; ceux-ci doivent donc être calculés en conséquence. Deux méthodes sont utilisées pour la compensation des dilatations : 
- la compensation dite naturelle, qui consiste à utiliser la flexibilité des tubes acier : dans un changement de direction à angle droit, la déformation du tube permet d'admettre un certain allongement de chacune des branches tout en restant dans les limites acceptables de fatigue du métal,
- l'utilisation de compensateurs qui, par leur déformation, absorbent l'allongement des tuyauteries,
**Compensation naturelle**
C’est la méthode la plus utilisée, la plus sûre, et en général la plus économique.
Elle est réalisée en étudiant, lors du tracé, un parcours sinueux du réseau, avec le maximum de changements de direction à angle droit.
On trouve de simples angles droits, des baïonnettes et des lyres de dilatation, ces dernières consistant à créer sur les longs tronçons obligatoirement droits un ensemble d’angles droits en forme de U qui est particulièrement flexible.
![[Coudes lyres baïonnettes.png]]
Chaque organe de dilatation (coude avec ses branches, baïonnette, lyre) a, de par ses dimensions, une capacité d’absorption de dilatation limitée, compte tenu de la nécessité de rester en tout point dans les limites de fatigue acceptables pour le métal des tubes. On en déduit l’écartement extrême des points fixes qui sont placés de part et d’autre de l’organe de dilatation. Dans le cas de **dilatation naturelle**, les réactions sur les points fixes sont relativement de faible importance, la pression ne jouant aucun rôle contrairement à ce qui se passe dans le cas d’utilisation de compensateurs axiaux. Sur le plan pratique, l’étude de la compensation naturelle dans un réseau se mène de la façon suivante : 
- on détermine le tracé du réseau en réalisant le maximum de changements de direction à angle droit en plan et en élévation, compte tenu évidemment des divers impératifs imposés à ce tracé,
- on répartit approximativement les points fixes de part et d'autre des coudes et des baïonnettes, compte tenu de l'expérience acquise en la matière,
- sur les longues parties droites, où il n'y a ni coude ni baïonnette, on place des lyres de dilatation; leur écartement possible dépendra de leurs dimensions, mais en règle générale on ne dépasse pas 100 m,
- à l'aide d'abaques qui donnent l'écartement maximal des points fixes en fonction des dimensions des organes de dilatation, on vérifie pour les coudes et baïonnettes que l'on se trouve au-dessous de cet écartement ; on détermine ensuite les dimensions à donner aux lyres, compte tenu de la position des points fixes entre lesquels elles se trouvent placées. La hauteur dont on dispose pour ces lyres limite leurs dimensions et peut conduire à en faire varier le nombre.
![[Abaque coudes.png]]
![[Abaque Baïonnettes.png]]
![[Abaque Lyres.png]]
**Utilisation de compensateurs**
La compensation naturelle, si elle est souhaitable, n’est pas toujours utilisable dans les réseaux, compte tenu du tracé partiellement ou totalement imposé et de la présence des autres réseaux qui peuvent empêcher l’utilisation de lyres, très encombrantes.
On doit alors utiliser des compensateurs de dilatation, moins encombrants. La fabrication des compensateurs est au point, cependant il survient quelquefois des cassures dans les ondes après un certain temps de fonctionnement.
Le prix de revient des compensateurs est plutôt supérieur à celui des organes de dilatation naturelle ; c’est la raison pour laquelle il convient de ne les utiliser que lorsqu’il n’y a pas possibilité de faire autrement, soit par manque de place, soit par suite du mode d’installation et de calorifugeage des tuyauteries (tuyauteries enterrées en particulier).
Il existe divers types de compensateurs.
![[Compensateurs.png]]

**Expansion**
Le réchauffage d’une masse d’eau conduit à une augmentation de son volume. Dans un circuit fermé cette augmentation doit pouvoir être "encaissée" par l'installation : c'est pour cela qu'est mis en place un équipement qui permet d'absorber la dilatation de l'eau. L'augmentation de volume de l'eau entre 0 et 110ºC est de 6%. Ainsi une installation qui contient un volume de 1 m3 devra avoir un dispositif d'expansion lui permettant d'absorber un volume de 60 L.

**pressions**
Répartition des pressions La pression en tous les points d’une installation à eau chaude sous pression doit être comprise entre deux limites :
- une pression maximale qui est celle à laquelle les tuyauteries et appareils doivent pouvoir résister mécaniquement,
- une pression minimale qui est égale à la pression de vapeur de l’eau à la température qu’il y a en ce point (température qui peut être différente suivant les parties de l’installation, Dans toute installation à eau chaude sous pression, une pression bien déterminée (ou tout au moins comprise entre deux limites fixées) se trouve toujours imposée en un point par le dispositif de mise en pression.
- 
À partir de cette pression, on peut déterminer celle qui règne en tous les points en partant du fait que la différence de pression entre deux points quelconques est :
∆p=∆p1 +∆p2
avec
∆p1 différence de pression due à la dénivellation entre les deux points,
∆p2 somme des pertes de charge entre les deux points.

La pression diminue lorsque l’on s’élève et augmente en sens inverse, la variation étant sensiblement de 1 bar par 10 m de dénivellation.

Pertes de charges et hauteur manométrique des pompes qui les compensent s’expriment en mètres de colonne d’eau (sensiblement 1 bar pour 10 m CE).

On peut tracer pour toute installation le diagramme des pressions en tous les points, mais, en pratique, on ne fait que vérifier les pressions aux points où elles risquent d’être trop élevées ou trop basses.

Pour l’étude de la pression maximale pmax , on doit considérer le cas exceptionnel, mais possible, où le robinet général de retour étant fermé, la totalité de la hauteur manométrique p de la **pompe à débit nul** s’exerce sur l’installation : cela revient pratiquement à ajouter aux pressions statiques p ′ et p ′′ (dues au dispositif de mise en pression et aux dénivellations) cette hauteur manométrique et l’on a :
*pmax = p + p ′ + p ′′
P : HMT pompes
P' : Pression statique
P'' : Pression dénivellations*

Les points de pression maximale doivent être recherchés au <u>refoulement des pompes</u> et aux <u>points bas</u>.

On peut être amené, compte tenu de la résistance à la pression des appareils de l’installation, à limiter cette pression pmax et, par là même, p, p ′ et p ′′.
Cela peut conduire à :
- limiter la hauteur manométrique de la pompe en augmentant les diamètres des tuyauteries et, éventuellement, en choisissant un réchauffeur et des appareils d’utilisation à faible perte de charge (quand cela est possible),
- limiter la température de l’eau chaude sous pression qui impose p ′,
- limiter les dénivellations, par exemple en fractionnant l’installation.
 
Pour l’étude des points de pression minimale, on peut être amené à considérer les deux cas de pompe à l’arrêt ou en fonctionnement.
Les points de pression minimale doivent être recherchés à <u>l’aspiration des pompes</u> et aux <u>points les plus élevés</u>. 
Compte tenu des températures régnant dans les diverses parties de l’installation et des dénivellations entre, d’une part, les points les plus élevés de ces différentes parties et, d’autre part, le point où s’exerce le dispositif de mise en pression, on en déduira la pression à créer par ce dernier.

**Organes du réseau (isolement, vidange, purge, chambre de vannes)**
Il est recommandé de positionner régulièrement les vannes de sectionnement sur le tracé du réseau. Une vanne de sectionnement après chaque piquage parait une bonne règle en termes de conception générale.
Il doit être prévu, dans les réseaux, des vannes permettant d’isoler les différents tronçons pour entretien ou réparation en gênant le moins grand nombre possible d’usagers. Les vannes sont placées sur les tronçons principaux, en général aux dérivations qui sont elles-mêmes isolables. Ils doivent être de très bonne qualité et étanches.
L’arrêté du 6/12/82 a introduit la notion de volumes maximaux (500 m3) qui doivent pouvoir être isolés ainsi que l’obligation d’organes d’isolement automatiques ou commandés à distance en cas de baisse de pression ou d’augmentation de vitesse anormales traduisant une fuite.
Dans les réseaux à eau chaude et à eau surchauffée, tous les points bas et points hauts sont munis de robinets.
Dans les réseaux à vapeur, les points bas sont munis de postes de purge, le condensat étant en général envoyé directement dans la tuyauterie de retour.
Tous ces accessoires sont placés évidemment dans des chambres visitables.

**Détermination des pompes réseaux**

Le débit de la pompe de circulation est la somme des débits dans les différents appareils.

Sa hauteur manométrique doit être égale à la somme des pertes de charge dans le circuit d’eau chaude sous pression. Elle s’exprime généralement en mètres de colonne d’eau (CE).

La perte de charge dans le réseau dépend du débit d’eau chaude sous pression dans les différents tronçons et du diamètre des tuyauteries.

Plus la hauteur manométrique d’une pompe est élevée, plus la puissance absorbée (donc la consommation d’énergie électrique) est grande pour un débit donné.

D’un autre côté, plus le diamètre des tuyauteries d’un réseau est élevé, plus ce réseau est coûteux et plus les pertes thermiques sont importantes (quoique l’on puisse, dans une certaine mesure, limiter ces pertes en augmentant l’efficacité de l’isolation, mais alors le prix du réseau augmente encore). On voit donc qu’il y a un choix à faire.

On sera guidé dans ce choix par diverses considérations, parmi lesquelles on peut citer :
- la vitesse dans les tuyauteries de l’ordre de 1 m/s à 3 m/s pour les gros diamètres,
- la durée d’utilisation de l’installation au débit maximal : dans une installation industrielle qui fonctionne à pleine puissance toute l’année, il y a plus d’intérêt à limiter la hauteur manométrique des pompes que dans une installation de chauffage urbain à débit variable, dont le débit maximal n’est atteint que quelques jours par an,
- la pression maximale admissible dans les appareils d’utilisation, qui dépend en partie de cette hauteur manométrique.

Pratiquement, on arrive à des hauteurs manométriques de l’ordre de : 
- 10 à 20 m CE pour les petites installations s’étendant sur quelques centaines de mètres et d’une puissance de quelques milliers de kilowatts,
- 50 à 150 m CE pour les grandes installations de chauffage urbain dont le réseau atteint plusieurs kilomètres de développement.

La courbe caractéristique d’une pompe indique la différence de pression donnée au fluide pour un certain débit. A l’inverse, plus le débit est important, moins la pompe n’est capable de donner de pression à ce fluide. La caractéristique d’une pompe est de la forme de la courbe bleue :
![[Courbe pompe.png]]
On parle aussi bien de pression exprimée en bar qu’en hauteur manométrique totale (HMT), hauteur d’eau correspondant à cette pression.

Le point de fonctionnement est le point d’intersection entre la courbe de la pompe et la courbe du réseau. 
Puissance utile, absorbée, : pertes La puissance utile est la puissance qui est vraiment utile au point de vue de l’utilisateur. C’est la puissance hydraulique fournie au fluide. Dans le cas des pompes centrifuges, utilisées généralement sur les réseaux de chauffage urbain, la puissance hydraulique est donnée par la formule suivante : 

Ph = Q.HMT.9810

Avec : P = Puissance transmise au fluide par la pompe en Watt.
Q = débit en m3/s.
HMT = perte de charge du réseau hydraulique exprimé en m de colonne d’eau.

La puissance absorbée est la puissance électrique consommée pour le fonctionnement de la pompe. La différence représente les pertes, le rapport le rendement de la pompe. Pour les pompes centrifuges, ce rendement est de l’ordre de 75%.

La puissance absorbée et la puissance hydraulique sont proportionnelles au cube de la vitesse (ou du débit) - le carré par les pertes de charge, la proportionnalité par le débit

La pompe équivalente à deux pompes en série est une pompe dont :
	la hauteur manométrique HMT = HMT 1 + HMT 2
	le débit fourni est égale au maximum des débit Q1 et Q2 ; Q = max (Q1 ;Q2)

La pompe équivalente à deux pompes en parallèle est une pompe dont :
	la hauteur manométrique HMT est le maximum des HMT des deux pompes HMT = max (HMT 1 ; HMT 2)
	le débit fourni est égale à la somme des débits Q1 et Q2 ; Q = Q1 + Q2

**Régulation pompes**
Une pompe centrifuge a une courbe caractéristique débit/hauteur manométrique correspondant à chaque vitesse de rotation.

Lorsqu’elle débite sur un réseau, le point de fonctionnement est l’intersection des deux courbes : point A à la vitesse de rotation V.

Lorsque le débit nécessaire aux sous-stations est réduit par suite de la fermeture des vannes 2 voies, le débit dans le réseau diminue, passant par exemple de Q1 (point A) à Q2 (point B).

![[Courbe regulation pompes.png]]

Si l’on maintient en fonctionnement la pompe à la vitesse de rotation V, son point de fonctionnement passera en C, correspondant à un accroissement de hauteur manométrique de H1 à H3 alors que la perte de charge du réseau a été réduite à H2.

Pratiquement, la différence de pression H3 – H2 devrait alors être absorbée par les régulations des sous-stations, ce qui ne faciliterait pas leur fonctionnement et conduirait de plus à une dépense inutile d’énergie électrique.Nous sommes alors dans le cas d’une surconsommation électrique.
Pour rappel, la puissance absorbée varie ainsi en fonction du cube de la vitesse ou du débit.
Pour éviter ces inconvénients, il faut donc changer la courbe caractéristique de la pompe pour qu’elle passe par B. Cela se fait en ramenant sa vitesse de rotation à v : la puissance absorbée passe alors de P3 à P2.

**Mise en place de pompe en parallèle**
Avec deux pompes de circulation en parallèle, on obtient à chaque vitesse une autre courbe caractéristique de pompes, et l’on voit que de cette façon on peut approximativement adapter les caractéristiques des pompes aux débits du réseau en vue d’obtenir la consommation d’énergie électrique minimale.
Pour faire varier la vitesse des pompes, on peut les munir de moteurs à 2 vitesses (1 400 et 950 tr/min le plus souvent) ou de variateurs de vitesse.

**Mise en place de pompes en série**
On peut également monter les pompes en série : ce sont alors leurs hauteurs manométriques qui s’ajoutent. Cette disposition peut être, en particulier, adoptée dans une installation où il y a plusieurs réseaux à pertes de charge assez différentes. On réalise alors avec un groupe de pompes une pression déterminée pour alimenter certains réseaux et on alimente les réseaux à pertes de charge nettement plus élevées avec une pompe ou un groupe de pompes supplémentaires en série.

**Nombre de pompes installées**
Pompes fonctionnant en saison hivernale
Il est recommandé pour les pompes en fonctionnement pendant la période de chauffage de respecter les règles suivantes :
- pour les petits débits inférieurs à 75 m3 /h par exemple, on recommandera l’installation de deux pompes pouvant véhiculer 100% du débit (une pompe en fonctionnement, une autre en secours avec alternance du fonctionnement),
- pour les débits supérieurs, on installera trois pompes pouvant véhiculer la moitié du débit maximum ou quatre pompes pouvant véhiculer le tiers du débit maximal.

**Pompes Eté**
Il est possible pour diminuer les coûts de pompage durant la période estivale correspondant au talon d’eau chaude sanitaire d’installer une pompe dite ETE dédiée à ce fonctionnement.
Il faudra alors comparer l’investissement supplémentaire lié à cet équipement et les économies générées par son fonctionnement. Le retour sur investissement devra être calculé au cas par cas et n’est pas garanti surtout avec l’installation de pompes à vitesse et débit variable.

**Puissance appelée selon t°C extérieure**
a*x* + b
*x* = température de référence (20°C) - température extérieure étudiée 
a = gradient de puissance appelée quand température extérieure varie de 1°C = puissance totale / (20°C-t°C extérieure la plus basse)
b = puissance moyenne appelée par 20°C (ECS)

Ou : x * Ptotale / (20°C-t°C extérieure la plus basse)