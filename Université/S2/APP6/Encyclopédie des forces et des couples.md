### 12.1 La masse, le poids et la gravité
La masse et le poids ne sont pas la même chose. Le poids est le produit de la masse et de l'accélération gravitationnelle.

### 12.2 Gravité uniforme sur une particule ou un corps
Pour une particule, la force gravitationnelle est [la suivante](../../../Collégial/1ere%20session/Physique/Les%20forces.md#Force%20gravitationnelle) et pour un corps il s'agi de la même chose mais appliquée à son centre de masse.

### 12.6 Friction cinétique et la loi de friction continu
La friction est dur à modélisé parfaitement en raison des nombreuses variables inconnues. On cependant modéliser la force de contact entre des objets comme suit:
$$\vec{F}^{B_A/A_B}=\vec{F}_N+\vec{F}_f$$
Où $\vec{F}_N$ est la force normale et $\vec{F}_f$ est une force perpendiculaire à la normale.

La loi de Coulomb sur la friction cinétique est [la suivante](../../../Collégial/1ere%20session/Physique/Les%20forces.md#Force%20de%20frottement#Cinétique). Par contre, elle peut être difficile à calculer numériquement si la vitesse de l'objet est très faible et qu'une division par zéro est créer pour la direction de la force.

Pour régler ce problème, on utilise la loi de friction continue. Celle-ci peut modéliser des situations où l'objet glisse et aussi où l'objet colle.
$$\vec{F}_f=-\mu_k|\vec{F}_N|\frac{\vec{v}^{B_A/A_B}_{\textrm{tangent}}}{|\vec{v}^{B_A/A_B}_{\textrm{tangent}}|+\epsilon_v}$$
Où $\epsilon_v$ est un nombre positif beaucoup plus petit que la norme de la vitesse.

### 12.7 Ressort en translation
Si le ressort à une constante d'élasticité qui demeure constante peu importe l'étirement du ressort alors la force exercé par le ressort est [la suivante](../../../Collégial/1ere%20session/Physique/Les%20forces.md#Force%20élastique). Dans notre notation c'est plutôt:
$$\vec{F}^{Q/P}=-k*\Delta l*\hat{u}^{Q/P}$$


