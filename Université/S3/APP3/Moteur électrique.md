### Moteur à balais
Un moteur qui utilise des balais et un commutateur pour faire changer le sens du courant et le faire tourner. 
![moteur à balai](Pasted%20image%2020250603070647.png)

#### Ondulation de couple
Ce genre de moteur souffre d'un phénomène appelé *ondulation de couple* puisque la force engendrée par le champ magnétique varie selon la position de la bobine par rapport aux aimants. Par contre, avec 5 bobines, l'ondulation de couple est inférieur à 5% et avec 12 bobines elle est inférieur à 1%.
![ondulation](Pasted%20image%2020250603070914.png)
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
