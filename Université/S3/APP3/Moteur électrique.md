### Moteur à balais
Un moteur qui utilise des balais et un commutateur pour faire changer le sens du courant et le faire tourner. 
![moteur à balai](Images/Pasted%20image%2020250603070647.png)

#### Ondulation de couple
Ce genre de moteur souffre d'un phénomène appelé *ondulation de couple* puisque la force engendrée par le champ magnétique varie selon la position de la bobine par rapport aux aimants. Par contre, avec 5 bobines, l'ondulation de couple est inférieur à 5% et avec 12 bobines elle est inférieur à 1%.
![ondulation](Images/Pasted%20image%2020250603070914.png)
#### Couple
En se basant sur l'équation de [la force magnétique](../../../Collégial/4e%20session/Physique/La%20force%20magnétique.md), il est possible d'obtenir la formule suivante pour le couple d'un moteur:
$$\tau = K_ti$$
Où $K_t$ est une constante en $Nm/A$ et $i$ est le courant en $A$. On appelle cette constante la *constante de couple d'un moteur*.
#### Niveau électrique
Quand on regarde la tension au borne du moteur, on peut utiliser la [loi de Faraday](Courant%20alternatif.md#Inductance%20et%20circuits%20à%20courant%20alternatif) pour décrire le moteur comme une inductance et un résistance et obtenir l'équation suivante:
$$v = Ri+L\frac{di}{dt}+K_e\omega$$
**En régime permanent**, l'équation devient:
$$v=Ri+K_e\omega$$
Et en réarrangeant:
$$\omega=\frac{v-Ri}{K_e}$$
Où $K_e$ est la *constante électrique d'un moteur* en $V/rad/s$.

Si on part de l'équation de l'équilibre énergétique en régime permanent, on peut faire une preuve intéressante:
$$\begin{align}
vi&=Ri^2+\tau\omega \\
v&=Ri+\frac{\tau}{i}\omega \\
v&=Ri+K_t\omega
\end{align}$$
On arrive ainsi à la même forme vu précédemment et on peut ainsi affirmer que:
$$K_t=K_e$$
En fait, les constantes de moteur mesurent toutes la même chose *mais dans des unités différentes!*

### Moteur sans balais
Un moteur avec balai s'use avec le temps. De plus, le rotor a une grande inertie ce qui limite ses performances. Le moteur sans balais vient régler ces problèmes. Les bobines sont installées sur le stator et l'aimant permanent et lui sur le rotor ce qui réduit grandement l'inertie du rotor. Pour contrôler le moteur, il faut faire commuter le courant dans les diférrentes bobines selon un ordre logique.
![](Images/Pasted%20image%2020250603074046.png)
Il peut ainsi y avoir des moteurs ou le rotor est relié à la coque du moteur et celle-ci tourne aussi:
![](Images/Pasted%20image%2020250603074134.png)

Ces moteurs utilisent souvent des capteur à effet de Hall pour mesurer la vitesse/position du rotor et ainsi diriger la commutation des bobines.

### Moteur pas à pas
Il s'agit de moteur donc l'angle de rotation varie discrètement. 
![](Images/Pasted%20image%2020250603074823.png)


En variant quels électroaimants sont actif ainsi que leur direction, on peut faire bouger le rotor d'une position à l'autre. Normalement, on utilise toutes les bobines pour faire un mouvement ce qui laisse quatre positions possible pour le moteur vu plus haut. Cependant, en utilisant la moitié des bobines pour chaque mouvement, on obtient de *demi-pas*. Le moteur a alors huit positions possible mais la moitié du couple dans les positions intermédiaires.
#### Problèmes du moteur
Le premier problème est la perte de pas, si on essaye de faire tournée le moteur trop vite, il n'a pas le temps d'atteindre son pas avant de se faire appeler au prochain, il va ainsi *sauter* des pas.

Le deuxième problème du moteur est sa [[fréquence de résonance]] généralement faible et il est possible de l'exciter dans le fonctionnement normal du moteur. Celui-ci va donc se mettre à tourner et vibrer de manière erratique.