### Les résistances

Permet de limiter le courant passant dans un circuit. Elle est identifier par la référence R? et il en existe plusieurs types tel que les résistances montées en surface *SMT* et celle avec pattes *through hole*. Les résistances utilisent un code de couleur universel pour déterminer leurs caractéristiques. 

#### Code de couleur

Les résistances les plus communes comportent quatre bandes de couleur. Chaque bande a son rôle:
1. Premier chiffre significatif
2. Deuxième chiffre significatif
3. Multiplicateur
4. Précision

Pour les chiffres significatifs, le code suivant est utilisé:
![[Pasted image 20240830102140.png]]
Pour le multiplicateur, le code suivant est utilisé:
![[Pasted image 20240830102231.png]]
Pour la précision, le code suivant est utilisé:
![[Pasted image 20240830102256.png]]

Cependant certains sites pratiques tel que [Digikey](https://www.digikey.ca/en/resources/conversion-calculators/conversion-calculator-resistor-color-code) permettent de rapidement calculé ces valeurs.

#### Autres infos
Il n'est pas possible de fabriquer toutes les valeurs de résistances existantes, c'Est pourquoi un ensemble de 24 valeurs a été créé. Celui-ci s'appelle le E24 et comporte ces valeurs ainsi que toutes leurs multiplicateurs en base 10: 100 – 110 – 120 – 130 – 150 – 160 – 180 – 200 – 220 – 240 – 270 – 300 330 – 360 – 390 – 430 – 470 – 510 – 560 – 620 – 680 – 750 – 820 - 910

Lorsqu'on fait un *BOM* pour des résistances, on doit inclure l'information suivante:
- La valeur de la résistance *RES 390K OHM* (390 kOhm)
- La capacité de dissipation de chaleur du boitier *1/10 W* (jusqu'à 1/10 watts)
- La précision de a résistance *5%* (plus ou moins 5%)
- La taille de la résistance *0805* (80 millièmes de pouce par 50 millièmes de pouce)

Il faut respecter le format suivant:
**RES 390K OHM 1/10 W 5% 0805**

### Les condensateurs

Comme les condensateurs s'opposent aux variations de tensions, ils sont souvent utilisés pour stabiliser une tension continue. À l'entrée des circuits, ils y a toujours un plus grand condensateur servant de réservoir au cas où la demande de courant augmente soudainement. Sinon, ces demandes auraient pour effet de faire chuter la tension de la source lorsque celle-ci ne pourraient plus fournir. 

#### Condensateur de découplage
Pour chaque circuit intégré, on doit intégré un condensateur de découplage. Ils sont à côté des pièces pour minimiser la longueur des fils et les effets inductifs parasites indésirables. 

Ceux-ci filtrent mieux les variations rapides de courant. Ça permet de stabiliser l'alimentation des circuits intégrés.

Il en existe deux sortes:
- En polyester, plus cher, meilleur précision, utile pour le filtrage de signal
- En céramique, moins cher, moins précis, utile pour le découplage

#### Condensateur polarisé
Certains condensateurs sont dit non-polarisés, c'est à dire que l'orientation de branchement n'a pas d'importance. Par contre, pour certains condensateurs dit polarisés, l'orientation est primordiale. Le condensateur risque d'explosé s'il est mal branché. 

#### Autres infos

Les condensateurs varient en fonction de la température. Il y a un code selon les caractéristiques:
- X8R (−55/+150, ΔC/C0 = ±15%)
- X7R (−55/+125 °C, ΔC/C0 = ±15%)
- X6R (−55/+105 °C, ΔC/C0 = ±15%)
- X5R (−55/+85 °C, ΔC/C0 = ±15%)
- X7S (−55/+125, ΔC/C0 = ±22%)
- Z5U (+10/+85 °C, ΔC/C0 = +22/−56%)
- Y5V (−30/+85 °C, ΔC/C0 = +22/−82%).
- NPO (ne varie pas en fonction de la température)

Dans un *BOM*, la sélection d'un condensateur se caractérise par six éléments. 
- La technologie du condensateur *CAP CER* (céramique)
- La valeur de la capacité *0.1 µF* (0.1 micro farad)
- La précision nominale du condensateur *10%*
- La tension maximale *50V* 
- La stabilité thermique du condensateur *NPO* (ne varie pas en fonction de la température)
- Le format du boitier *RADIAL* (un cylindre)

### Les diodes
#### Diode silicium
La diode sert a rectifié le courant, elle le laisse seulement passer dans un sens jusqu'au sa tension maximale.

#### Diode électroluminescente
Aussi appelé *DEL* ou *LED*. Lorsqu'il y a un tension entre les bornes de *LED*, celle-ci émet de la lumière, la baisse de tension observée dépend de la couleur de la *LED*.

#### Diode infrarouge
Elle fonctionne de la même manière qu'une *LED* mais elle émet de la lumière infrarouge.
### Les potentiomètres

Un potentiomètre est une résistance à valeur variable. Sa valeur indiquée est la valeur maximale de la résistance. Il est possible de l'utiliser comme un diviseur de tension facilement.

### Les alimentations
Pour qu'un circuit fonctionne, il a besoin d'une source d'énergie. C'est le rôle de l'alimentation qui agit en tant que source de tension et de courant. Elle peut être flottante ou non, entre d'autres mots, elle peut être connecter à la mise à la terre ou non.

### Les circuits intégrés

Un circuit intégré est un circuit complet miniaturisé dans un boitier qui peut être *through hole* ou *SMT*. Dans un schéma, il utilise la référence U?. Généralement, la patte 1 du boitier est identifié par un rond blanc sur le boitier ou un gravure. Sur un *PCB*, l'emplacement de la patte 1 est représenté par un carré tandis que toutes les autres pattes sont des ronds. La numérotation des pattes se fait en sens inverse des aiguilles d'une montre. 

Pour faciliter le changement d'un circuit intégré brisé sur un *PCB*, il est recommandé de souder un connecteur tampon *socket* au lieu de souder directement le circuit intégré.

### Le 556

![[Pasted image 20240830151611.png]]
Un 556 est un générateur d'ondes carrées doubles, il regroupe deux 555 qui sont des générateurs d'ondes carrées. Lorsque la tension du *threshold* dépasse un seuil qui correspond aux deux tiers du *VCC*, la sortie *output* sera à 0V. Lorsque le *threshold* retourne à un tension sous le tier du *VCC*, la sorite *output* retourne à la tension d'alimentation. La sortie *discharge* quant à elle est à 0V quand la sortie *output* est à 0V, sinon elle est flottante.

Le 556 comporte deux modes d'alimentations, le mode astable et monostable.

#### Mode astable

Le mode astable est un mode cyclique ou la sortie n'est jamais stable, d'où le nom astable. Il est souvent utilisé afin de réaliser une horloge. Pour ce faire, on tire profit du temps de charge et de décharge d'un [[|circuit RC]]. 
![[Pasted image 20240830152126.png]]

##### Mode de fonctionnement:
Lorsqu'il est mis sous tension, la tension va monter jusqu'à ce que le condensateur atteigne le 2/3 du *VCC* ce qui va fera tomber la sortie *discharge* à 0V. Ainsi, le condensateur va donc se décharger jusqu'à ce que la tension atteigne 1/3 du *VCC*. La sortie *discharge* va donc revenir flottante et le condensateur va recommencer à se charger. La fréquence de ce cycle ainsi que son rapport cyclique dépendent de la valeur des résistances $R_A$ et $R_B$ sur le schéma.

Les ondes créées seront donc carré et les ondes aux bornes du condensateur seront exponentielles.

La fiche technique du 555 indique un mode astable avec un rapport cyclique de 50% (techniquement impossible avec le présent circuit).

#### Le mode monostable

Lorsqu'on utilise le mode monostable, la sortie du 556 demeure stable jusqu'à ce qu'un front descendant arrive à l'entrée *trigger*. À cette instant, le condensateur va se charger jusqu'à ce que la tension atteigne le 2/3 du *VCC*. Ça va donc créer un impulsion dont la durée peut être changée selon les valeurs du condensateurs et de la résistance.

![[Pasted image 20240830153231.png]]

#### Générateur d'ondes carrées basse fréquence

Pour générer des ondes carrés avec un rapport cyclique de 50%, on peut utiliser une modification du mode astable. 
![[Pasted image 20240901095857.png]]

Pour calculer la fréquence d'oscillation, on doit fixer certaines valeurs puisqu'il y a trop d'inconnu autrement. On fixe souvent la valeur du condensateur en premier puisqu'il y a moins de possibilité facilement accessible que de résistance.

### Les portes logiques

Il existe trois types de porte logique *(et, ou, et exclusif)* qui peuvent être agencé ensemble avec des inverseurs pour créer une logique complexe. 

Ces portes sont très sensible au bruit, il est donc recommander de connecter les entrées inutilisées à la masse et de laisser les sorties flottantes.

![[Pasted image 20240901102314.png]]