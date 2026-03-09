## Vis
Il existe deux systèmes de dimensions standards pour des filets sur des vis: le système fin *fine thread UNF* et le système brut *coarse thread UNC*. Le *pitch diameter $d_p$* est le diamètre du cylindre d'un filet parfait où l'épaisseur des filets et des *grooves* sont égales.
![](Images/Pasted%20image%2020260309074859.png)

Le *stress area* est calculé à partir de la moyenne de *pitch* et *root diameters*. On utilise cette aire pour le calcule des contraintes dans les filets. 

Dépendant de l'application, il existe différent grade de vis dépendant de la tolérance qu'on veut de grade 1 à 3 où 3 possède les plus petites tolérances mais est plus cher.

### Types de vis
![](Images/Pasted%20image%2020260309075606.png)

#### Vis et boulons
Les vis et boulons sont de loin les plus communs, leur différence est seulement dans leur intentions d'utilisation. Un boulon est fait pour être utilisé avec un écrou tandis qu'une vis est utilisé dans un trou taraudé. Par fois des vis ont une rondelle incluse sous leur tête pour évité d'oublié d'en installé une. On appelle ces vis des *sems*. 
#### Stud et tiges filetées
Un *stud* est taraudé des deux côtés et est souvent utilsé pour être attaché de façon permanent dans un trou taraudé. Les deux filets peuvent être différent ou identiques. Une tige filetée est le type le moins commun. Elle est souvent utilisé lorsqu'on a besoin d'un membre fileté très long.
### Types de tête de vis
Voici des formats de tête de vis très commun:
![](Images/Pasted%20image%2020260309080138.png)
Une règle général est qu'un boulon peut servir de vis dans un trou fileté avec pour exception le boulon de carrosserie dit *carriage bolt*.

Voici des formats de tête conçus pour ne pas être dévisser:
![](Images/Pasted%20image%2020260309080345.png)

### Matériaux de vis
La plupart des vis sont fait en acier mais dans certain cas, il y en a en aluminium, en bronze, en cuivre, en nickel, en titane etc. Tout dépend du contexte d'utilisation de la vis.

## Tension dans un boulon
Pour la plupart des applications, le vis et boulons devraient être serré pour qu'il y a ait une tension initiale $F_i$ quasiment égale la *charge complète* qui est défini comme le maximum de force de tension une déformation permanente ([limite d'élasticité](../../S1/APP4/Chapitre%201.md#1.2%20Caractérisation%20des%20propriétés%20mécaniques)).

On peut utiliser cette équation pour la déterminer:
$$F_i=K_iA_iS_p$$
Où: $A_i$ est la *stress area* des filets, $S_p$ est la limite d'élasticité et $K_i$ est une constante, souvent autour de 0.9 pour une application statique. La logique derrière cette tension initiale est que pour un chargement en tension, le boulon ne peut pas vraiment s'étirer sans que les membres se sépare et plus la tension initiale est grand, plus ce sera dur. Et pour les chargements en cisaillement, plus la tension initiale est grande, plus la force de friction résistant au cisaillement est grande. 

Il ne faut pas oublié que le boulon subit aussi une contrainte en torsion lorsqu'elle est serrée et elle va souvent se "lousser" un peu au début de son utilisation. La contrainte en torsion dépend aussi de la firction entre les filets et l'écrou.
![](Images/Pasted%20image%2020260309082246.png)

La méthode la plus utilisé pour serrer une vis à la bonne tension est d'utilisé une clé dynamométrique. Cependant, la précision de cette méthode est souvent seulement autour de 30% en raison des différentes frictions présentes.

En remarquant que la tension initiale ressemble à la charge sur [le jack](Vis%20de%20puissance%20et%20filets.md#Vis%20de%20puissance), on peut déduire l'équation suivante qui relie le couple et la tension initiale en assumant un coefficient de friction autour de 0.15 et des filets standards:
$$T=0.2F_id$$
Où $d$ est le diamètre nominal majeur du filet. Il faut toutefois se rappeler qu'il s'agit d'une relation approximative.

## Relâchement des filets et verrou de filet
Un avantage des joints filetés est que dans la plupart des applications ils peuvent être facilement désassemblés. Un des désavantages est que parfois, il se desserre est se désassemble sans qu'on le veuille.

### Facteurs qui affecte le relâchement
- Plus l'angle de l'hélice est grand, plus le relâchement est grand
- Plus la tension initiale est grand, moins le relâchement est grand
- Une surface rugueuse ou molle réduit la tension initiale et donc augmente le relâchement
- Un traitement de surface à tendance à augmenter la friction et donc réduire le relâchement

Pour contrer ce problème, il existe plusieurs solutions comme les *lock-nuts* et des rondelles *(washers)* hélicoïdales.
![](Images/Pasted%20image%2020260309085639.png)
On peut aussi utiliser deux écrous standards pour essayer de produire un effet de verrou.

## Rivets
Les rivets sont des joints permanent qui coute beaucoup moins cher que des vis et sont plus rapide à installer.
![](Images/Pasted%20image%2020260309140811.png)
![](Images/Pasted%20image%2020260309140909.png)
![](Images/Pasted%20image%2020260309140930.png)
## Soudage
Parfois, la soudure est aussi une option à considérer pour lier deux pièces. Il en existe plusieurs types:
- *Stick welding*: On fait fondre une tige de métal traité sur du métal. La tige est consommée.
- *MIG welding*: On utilise un embout qui fournie un gaz comme de l'argon pour de l'aluminium et la tige n'est pas traité. La tige est consommée.
- *TIG welding*: Utilise une tige en tungstène qui n'est pas consommé et un autre fil à part, on utilise de l'hélium ou de l'argon pour protéger et ça permet de souder des métaux non ferreux.
- *Flux core arc welding*: Comme du stick weld sauf que le flux est à l'intérieur de l'électrode au lieu d'être autour. L'électrode est poussé par un moteur.
![](Images/Pasted%20image%2020260309142554.png)

## Brasage et soudure
Comme du soudage sauf que la température en sous la température de fusion des pièces qu'on veut lier. Au dessus de 450C, il s'agit de brasage et en dessous il s'agit de soudure. L'avantage est qu'on peut lieu des pièces de différents types de matériaux ensemble avec ces techniques.
## Adhésif
Les avantages des adhésifs sont qu'ils n'y a pas de trou qui affaiblit la pièce, pas de haute température nécessaire et les contraintes sont souvent réparti sur de plus grande surface. Cependant, les adhésifs sont plus sensibles à la chaleur que les autres types de joints. Il faut aussi que la surface qu'on veut coller soin propre. Les adhésifs sont généralement peu couteux.