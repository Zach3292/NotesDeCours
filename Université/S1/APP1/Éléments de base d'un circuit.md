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
- La capacité de dissipation de chaleur du boitier *1/10 W* (jusqu'à 10 watts)
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

### Le potentiomètre

