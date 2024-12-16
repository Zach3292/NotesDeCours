### 3.1 Conducteur
Un conducteur est composé en séparant deux plaques conductrices par un diélectrique. Lorsque du courant passe au travers d'un condensateur, des charges s'accumulent sur les deux plaques du condensateur. La charge positive sur une plaque est de même norme que la charge négative sur l'autre plaque ce qui rend la charge net du condensateur nulle. 

#### Voltage en terme de charge
La charge emmagasinée est souvent considérée en terme de potentiel selon la relation présenté [ici](Les%20condensateurs.md#5.1%20La%20capacité%20d'un%20condensateur) entre le potentiel, la charge et la capacité d'un condensateur.

#### Courant en terme de voltage
Le courant est la dérivée des charges tel que vu [ici](Le%20courant%20électrique.md#6.1%20Introduction). En remplaçant la charge net par le relation entre le voltage et la capacité on obtient l'équation suivante: $$i=C\frac{dV}{dt}$$
Grâce à cette relation, il est possible de déterminer que lorsque le condensateur est complètement chargé dans un circuit de charge ou complètement déchargé dans un circuit de décharge, le courant passant au travers de ses bornes est nul.
#### Voltage en terme de courant
Comme le courant est la variation de charge, on peut l'intégrer pour obtenir la charge en fonction du courant: $$q(t)=\int^{t_1}_{t_0}{i(t)dt} + q(0)$$
Le voltage est proportionnel à la charge donc nous avons que: $$V(t)=\frac{1}{C}\int^{t_1}_{t_0}{i(t)dt} + \frac{q(0)}{C}=q(t)=\frac{1}{C}\int^{t_1}_{t_0}{i(t)dt} + V(0)$$
#### Énergie emmagasinée dans un condensateur
L'énergie dans un condensateur est donnée par plusieurs équations [ici](Les%20condensateurs.md#5.3%20L'énergie%20emmagasinée%20dans%20un%20condensateur).

### 3.2 Condensateur en parallèle et série
Les condensateurs ont un comportement inverse aux résistances. 
#### En parallèle
Il se combine en parallèle selon l'équation [suivante](Les%20condensateurs#5.4%20Association%20des%20condensateurs#En%20parallèle).
#### En série
Il se combine en série selon l'équation [suivante](Les%20condensateurs#5.4%20Association%20des%20condensateurs#En%20série).
### 3.3 Caractéristiques physiques d'un condensateur
#### Capacité
La capacité d'un condensateur peut être calculé avec les équations [suivantes](Les%20condensateurs.md#5.2%20Types%20de%20condensateur).
#### Condensateurs pratiques
Pour obtenir une capacité utile, un condensateur devrait avoir des plaques beaucoup trop grandes pour l'électronique moderne. On y arrive souvent en alternant les plaques et en les enroulants l'un autour de l'autre. *Les condensateurs réels ont un voltage maximales puisque dans un champ électrique trop fort, les diélectriques deviennent des conducteurs.*
#### Condensateurs électrolytiques
Dans un conducteur électrolytique, une plaque est souvent formé de métal, le diélectrique une couche d'oxydation sur le métal tandis que l'autre plaque est souvent en fait une solution électrolytique. Cela à comme avantage d'avoir un excellent ratio capacité/grandeur mais permet seulement au courant de passer d'un côté. Le condensateur à donc une certaine polarité.
#### Effet parasite
Un condensateur réel ne peut pas être simplement modélisé par une capacité. l faut plutôt utiliser ce circuit:
![250](Pasted%20image%2020241118103707.png)
En plus de la capacité $C$, une certaine résistance $R_s$ existe à cause de la résistivité des plaques. De plus, lorsque du courant circule dans le condensateur, il y a un certain champ magnétique créer qui ajoute une certaine inductance $L_s$. Enfin, aucun diélectrique n'est parfait et un petit courant circule au travers de l'isolant représenté par la résistance en parallèle $R_p$. $R_s$, $L_s$ et $R_p$ sont des éléments parasites du condensateur qui créent des effets parasites.

### 3.4 Les inducteurs
#### Principe de base
Un inducteur est composé de fil enroulé souvent autour d'un coeur magnétique. Selon la [loi de Faraday](Courant%20alternatif.md#Inductance%20et%20circuits%20à%20courant%20alternatif), la variation de courant dans un inducteur produit un champ magnétique qui induit une différence de potentiel au borne de l'inducteur. Pour un inducteur idéal, cette différence est proportionnelle à la variation de courant par la constante de proportionnalité $L$ aussi appelée l'inductance d'un inducteur. L'inductance à comme unité des Henrys $H$ qui sont égaux à des volts seconde par ampère $V\cdot s/A$.
#### Courant en terme de voltage
En réarrangent la loi de Faraday, on obtient $$di=\frac{1}{L} V(t)dt$$
En intégrant de chaque côté de l'équation on obtient $$\int^{i(t)}_{i_0}{di}=\frac{1}{L}\int^{t}_{t_0}{V(t)dt}$$
En réarrangent et intégrant: $$i(t)=\frac{1}{L}\int^{t}_{t_0}{V(t)dt} + i(0)$$
En analysant un peu, on voit que si la tension est finie, le courant peut seulement changer d'une quantité limitée à chaque intervalle de temps. Ainsi, le courant dans un inducteur est continu sans sauts et coupures (discontinuités). L'inducteur limite donc les changements brusques de courant. 
#### Énergie emmagasinée dans un inducteur
Pour obtenir l'énergie dans un inducteur, on doit intégrer sa puissance $$W(t)=\int^{t}_{t_0}{P(t)dt}$$
La puissance d'une composante vaut $P=Vi$ alors $$W(t)=\int^{t}_{t_0}{(V(t)\cdot i(t))dt}$$
On peut ensuite substituer le voltage à l'aide de la loi de Faraday $$W(t)=\int^{t}_{t_0}{L \frac{di}{dt}i(t)dt}$$
Le différentiel de temps s'annule et on peut changer les limites de la borne d'intégral $$W(t)=\int^{i(t)}_{0}{Lidi}$$
En calculant l'intégral, on arrive à $$W(t)=\frac{1}{2}Li^2(t)$$
### 3.5 Inducteur en parallèle et série
Les inducteurs se combinent comme des résistances
#### En parallèle
$$\frac{1}{L} = \frac{1}{L_1} + \frac{1}{L_2} + \frac{1}{L_3}$$
#### En série
$$L = L_1 + L_2 + L_3$$

### 3.6 Inducteur pratique
Un exemple d'utilisation pratique d'un inducteur en circuit DC est pour un *boost converter* qui permet d'augmenter le voltage d'une source. ![Pasted image 20241118130828](Pasted%20image%2020241118130828.png)
Lorsque la switch $S$ est est fermée, la source fait circulé du courant au travers de l'inducteur et lorsqu'elle ferme, l'inducteur force du courant dans la diode. Ce courant charge le condensateur qui commencera à accumuler du potentiel et dépassera rapidement la tension de la source. La switch ouvre et ferme très rapidement. 
#### Effet parasite
![Pasted image 20241118132727](Pasted%20image%2020241118132727.png)
Tout comme les condensateur, les inducteurs ont des effets parasites. Ceux-ci sont inverse puisqu'on recherche une inductance et aucune capacité.
### 3.7 Inductance mutuelle
![Pasted image 20241118133011](Pasted%20image%2020241118133011.png)
Lorsqu'on couple deux inducteurs ensembles, leur champs magnétiques s'aident ou se nuisent et il développe une inductance mutuel. Ce principe peut être utilisé dans plusieurs systèmes différents.
#### Tranformateur
Lorsqu'on a du courant AC, on peut utiliser des inductance mutuelles pour augmenter le voltage en ayant un inducteur avec plus de tour que l'autre.