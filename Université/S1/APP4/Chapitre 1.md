### 1.1 Contraintes et déformations

Quand il y a une force, il y a des contraintes à l'intérieur du matériel. Aux contraintes sont associés des déformations. 

Les déformations peuvent être élastique: la pièce revient à elle même lorsqu'il n'y a plus de contrainte ou plastique: la pièce est déformée de manière permanente lorsqu'il n'y a plus de contrainte.

#### 1.1.1 Traction simple

Une traction simple est quand des forces colinéaires de signes opposés sont appliquées sur un objet et que la ligne d'action passe par l'axe de l'objet.

![[Pasted image 20241008091914.png|300]]
Si le corps est coupé par un plan perpendiculaire à l'axe de traction, il est possible de le maintenir en équilibre en exerçant un série de force $dF$ dont la somme est égale à $F$ sur la surface de coupe $S$. On dit alors que le plan est soumis à une *contrainte* de tension $\sigma$ définie par: $$\sigma = \frac{dF}{dS}$$
d'où: $$F=\int{\sigma dS}$$

![[Pasted image 20241008092643.png|300]]

Dans le cas d'une traction simple, la contrainte est la même sur toute la surface alors: $$\sigma = \frac{F}{S}$$
Lorsqu'un objet subit une traction simple sur l'axe $z$, le corps s'allonge et subit un *déformation* $\varepsilon$ et le rapport d'allongement est de: $$\varepsilon_x = \frac{du}{u}$$
$$\varepsilon_y = \frac{dv}{v}$$
$$\varepsilon_z = \frac{dw}{w}$$
Dans un traction simple, même si le corps ne subit aucune contrainte sur l'axe des $x$ et l'axe des $z$, il y a quand même des déformations dans ces axes. Les trois déformations sont liées par le *coefficient de Poisson* $\nu$: $$\varepsilon_z = -\frac{\varepsilon_x}{\nu} = -\frac{\varepsilon_y}{\nu}$$
Si les déformations n'entrainent pas de changement de volume, $\nu = 0.5$, si $\nu < 0.5$, les matériaux augmente légèrement de volume. 

##### Loi de Hooke

La contrainte $\sigma_z$ est proportionnelle à la déformation $\varepsilon_z$ selon la loi de Hooke et la constante de proportionnalité $E$ est le *module d'Young*: $$E=\frac{\sigma_z}{\varepsilon_z}$$
En combinant les deux équations précédente, on obtient l'équation suivante: $$\varepsilon_z = -\frac{\varepsilon_x}{\nu} = -\frac{\varepsilon_y}{\nu} = \frac{\sigma_z}{E}$$
Le module d'Young $E$ est une propriété fondamentale des matériaux, sa grandeur dépend de l'intensité des liaisons atomiques.
#### 1.1.2 Torsion simple

Si on applique un couple $C$ aux extrémités d'un cylindre, celui-ci est en torsion. Comme des forces parallèles agissent sur des faces et la contrainte qui est résulte est une *scission*: $$\tau_{zy} = \frac{dT_{zy}}{uv}$$
*Les contraintes de tensions $\sigma$ agissent perpendiculairement à une surface alors que les contraintes de scission $\tau$ agissent parallèlement à une surface.*

![[Pasted image 20241008095850.png]]

Lorsque l'élément se déforme, le point $B$ se déplace en $B'$ d'une valeur $dv$. On appelle ça un *cisaillement* $\gamma$: $$\gamma_{zy} = \frac{dv}{w}$$
À une contrainte de tension $\sigma$ correspond un allongement $\varepsilon$ et à une contrainte de torsion $\tau$ correspond un cisaillement $\gamma$.
Le cisaillement est relié à la scission par la constante d'élasticité appelée *module de cisaillement* ou *module de Coulomb*: $$\tau_{zy} = G\gamma_{zy}$$
#### 1.1.3 Cas général

Le module d'Young, le module de Coulomb et le coefficient de Poisson sont liés entre eux par la relation suivante: $$G=\frac{E}{2(1+\nu)}$$
### 1.2 Caractérisation des propriétés mécaniques 

Pour obtenir des caractéristiques de matériaux, on fait des essais mécaniques, des tests. Les essais doivent:
* Mettre en jeux des contraintes connus et simples
* Pouvoir être interprété facilement de manière non équivoque
* Être reproductible
Des organisations se chargent de normaliser les essais.

#### 1.2.1 Essai de traction

Consiste à soumettre une éprouvette du matériau à étudier à une traction et mesurer l'allongement $\Delta l$. 

Il existe trois comportements à une traction:
1. Un comportement **fragile:** le matériau n'a pas de domaine plastique, la rupture sue produit alors que les déformations sont purement élastiques
2. Un comportement **ductile**: une déformation plastique permanente accompagnée généralement d'un durcissement du matériau suit la déformation élastique
3. un comportement **élastique non-linéaire**: la déformation élastique n'est pas proportionnelle à la charge qui la provoque

![[Pasted image 20241008103746.png]]

Pour étudier les courbes de traction, on évalue la contrainte nominale et la déformation nominale: $$\sigma_{nom} = \frac{F}{S_0}$$
$$\varepsilon = \frac{\Delta l}{l_0}$$
*Les contraintes s'expriment en pascals, ou plus généralement en mégapascal. Les déformations sont des grandeurs sans dimensions souvent exprimées en pourcentage*

![[Pasted image 20241008105432.png|400]]

*Courbe pour un matériaux ductile*
1. Déformation élastique linéaire
	1. Suit la [[#Loi de Hooke|loi de Hooke]]
2. Déformation plastique homogène
	1. Le *taux de consolidation* $d\sigma/d\varepsilon$ dans le domaine plastique est noté $\eta$ diminue plus la contrainte augmente et devient éventuellement nul à la valeur maximale de la contrainte nominale.
3. Déformation plastique non-homogène
	1. Localisé dans la *zone de striction*. Quand la consolidation du matériau ne peut plus compenser l'augmentation de la contrainte, il y a instabilité et striction.
4. Rupture
	1. Dans la zone de striction

On peut obtenir plusieurs valeurs importantes des caractéristiques mécaniques d'un matériau à l'aide de la courbe: 
* La *limite d'élasticité vraie* $R_e$ (ou *limite de proportionnalité*) 
	* La contrainte où le matériau ne suit plus la loi de Hooke
* La *limite conventionnelle d'élasticité* $R_{e0.2}$
	* Comme la $R_e$ est difficile à évaluer en pratique, on définit $R_{e0.2}$ qui correspond à la contrainte où il y a un déformation plastique (permanente) de $0.2\%$. 
	* La valeur de $R_{e0.2}$ est défini par l'intersection de la courbe et d'une droite parallèle à la pente élastique passant par $0.2\%$.
	* Si le passage d'élastique à plastique est discontinu, alors $R_e = R_{e0.2}$.
	![[Pasted image 20241008111444.png|300]]
	![[Pasted image 20241008124024.png|300]]
* La *résistance à la traction* $R_m$
	* La contrainte maximale atteinte durant l'essai de traction
	* Les matériaux fragiles n'ont pas de domaine plastique, $R_M = R_e$
* L'*allongement à la rupture* A
	* L'allongement maximale atteint après la rupture, calculer comme le $R_{e0.2}$ avec la pente de la partie élastique.
	* Il s'agit d'un mesure de la ductilité
	* Il est nul pour les matériaux fragiles
* La *striction à la rupture* Z
	* La striction est la variation de la section à l'endroit de la rupture
	* Elle est donnée par la relation: $$Z=\frac{S_0-S_f}{S_0}\times 100\%$$
	* Comme $A$, $Z$ donne une mesure de la ductilité d'un matériau
* *L'énergie de déformation*
	* L'aire sous la courbe de traction est homogène à une énergie de déformation par unité de volume.
	* En effet, en se fiant au définition: $$W = \int{\sigma_{nom} \ d\varepsilon} = \int{\frac{F}{S_0}d\left(\frac{\Delta l}{l_0}\right)=}\frac{1}{S_0 \ l_0}\int{Fd(\Delta l)} = \frac{1}{V_0}\int{Fd(\Delta l)}$$
	* Le terme $\int{Fd(\Delta l)}$  de l'équation représente l'énergie dépensée (le travail fait) au cours de l'essai
	* On peut séparé le travail pour la déformation plastique de la déformation élastique: $$W_{él} = \int{\sigma_{nom} \ d\varepsilon_{él}} = \frac{1}{2}\sigma\varepsilon_{él}= \frac{E\varepsilon^2_{él}}{2}=\frac{\sigma^2}{2E}$$

#### 1.2.2 Essai de compression

L'inverse de l'essai de traction
Si l'éprouvette est trop haute par rapport à son diamètre:
1. Il y a risque de *flambage* causé par une instabilité élastique
	1. La charge de flambage est seulement fonction de la géométrie de l'éprouvette et du module d'Young du matériau. 
	2. Pour éviter ce problème, le rapport $h/d$ est maintenu inférieur à 3.
2. Le frottement sur les faces d'appui de l'éprouvette et le plateau s'oppose à l'expansion du diamètre de l'éprouvette causant des déformations hétérogènes résultant à un tonneau

L'essai de compression ne permet pas d'atteindre la rupture sur un matériau ductile.

Ils sont très utiles pour déterminer la contrainte de rupture des matériaux fragiles qui résistent mal à la traction.

Matériau isotrope: même propriété peu importe dans quel axe on évalue.

#### 1.2.3 Essai de flexion

![[Pasted image 20241008131514.png]]
##### Essai à trois points
Pour un essai de flexion à trois points, la contrainte maximale est donnée par l'équation suivante: $$|\sigma_{max}| = \frac{3}{2}\left(\frac{FL}{bh^2}\right)$$
où 
$F$ = charge appliquée en son centre
$b$ = largeur de l'éprouvette
$h$ = hauteur de l'éprouvette
$L$ distance entre les appuis

##### Essai à quatre points
Pour un essai de flexion à trois points, la contrainte maximale est donnée par l'équation suivante: $$|\sigma_{max}| = \frac{3}{2}\left(\frac{F(L-l)}{bh^2}\right)$$où
$l$ = distance entre les points de flexion

Tout comme l'essai de compression, l'essai de flexion ne permet pas nécessairement d'atteindre la rupture des matériaux ductiles. Ils sont souvent utilisés pour tester la résistance à la flexion des matériaux fragiles.

#### 1.2.4 Essai de dureté

La dureté d'un matériau représente sa résistance à la pénétration. Il y a plusieurs tests de dureté différents: 
![[Capture d’écran, le 2024-10-08 à 13.21.12.png|]]

### 4.3 Ténacité
#### 4.3.1 Définition

*Rigidité*: Résistance à la déformation, en fonction de l'intensité des liaisons qui existent entre les atomes ou les molécules constitutifs d'un matériau. On la mesure en partie par le module d'Young $E$. 
*Résistance*: caractérise la contrainte maximal qu'un matériau peut supporter avant de se rompre. 
*Ductilité*: propriété grâce à laquelle un matériau peut se déformer de façon permanente avant de se rompre. 
*Fragilité*: se dit d'un matériau ne pouvant pas se déformer de manière plastique
*Ténacité*: résistance à la propagation brutale de fissures
*Dureté*: résistance à la pénétration
*Malléabilité*: capacité de se déformer plastiquement en compression

### Complément
#### Capacité thermique
Lorsqu'on apporte une chaleur $dQ$ à un matériau et que la température augmente de $dT$, sa capacité thermique $C$ est déterminée par: $$C = \frac{dQ}{dT}$$
Plus $C$ est grand, plus le matériau est difficile à réchauffer
#### Conduction thermique

Caractérise le transfert de chaleur à travers un matériau. Représenté par: $$J= -k\frac{dT}{dx}$$
Où $J$ est le flux de chaleur, ($W/m^2$) et que $dT/dx$ ($C\degree/m$) représente le gradient de température selon la direction x du flux. 

Voir [[Gaz, liquides et solides#Capacité thermique]]
#### Conduction électrique

Voir [[Le courant électrique#6.5 La loi d'Ohm]] pour la résistivité et la conductivité électrique.s