### 3.1 Symétries
Il y a trois types de symétrie en physique:
1. symétrie de rotation
2. symétrie de réflexion
3. symétrie de translation
Le champ électrique possède les mêmes symétries que l'objet chargé

La surface de Gauss choisie doit aussi avoir les mêmes symétriques que l'objet évalué

### 3.2 Flux électrique
Définition: quantité de quelque chose traversant une surface

Pour calculer le flux traversant une surface simple, on peut utiliser l'équation suivante:
Le flux électrique $\Phi$ est égal au produit scalaire du champ électrique $\vec{E}$ et de l'air de la surface $\vec{A}$ où le vecteur est normale à la surface comme suit: $$\Phi = \vec{E} \cdot \vec{A}$$
### 3.3 Théorème de Gauss
Pour évaluer le flux de différentes surfaces non-standards, on utilise une surface de Gauss fictive. Le flux ne dépend pas de la surface choisi et il peut être calculé comme cela:$$\Phi = \oint{\vec{E}\cdot d\vec{A}} = \frac{Q_{int}}{\epsilon_{0}}$$
### 3.4 Le théorème de Gauss en action
Il est possible de faire de la mécanique à l'aide du théorème de Gauss puisque $\vec{F} = m\vec{a}$, et que $\vec{F} = q\vec{E}$, alors $q\vec{E}= m\vec{a}$ ou $\vec{a} = \frac{q\vec{E}}{m}$. Il est ainsi possible de calculer des sommes de forces sur des charges. 

Pour une surface de Gausse sphérique de rayon $r$ et un objet chargé de rayon $R$, le champ électrique peut être résumé en deux situations:
1. Si $r > R$ alors $$\vec{E} = \frac{kQ}{r^2}\hat{r}$$
2. Si $R>r$ alors$$\vec{E} = \frac{kQr}{R^3}\hat{r}$$
### 3.5 Conducteur en équilibre électrostatique
Si un conducteur est à l'intérieur d'un champ, il y aura un champ induit à l'intérieur du conducteur. Dans un conducteur $\vec{E}_{ind} + \vec{E}_{ext} = \vec{0}$. 

Comme les charges se dispersent à la surface du conducteur, le champ vaut $\vec{E} = \frac{\sigma}{\epsilon_0}$.

Il y a cinq règles pour décrire le comportement des conducteurs:
1. À l'intérieur d'un conducteur, le champ est nul
2. Si il y a présence de charges excédentaires dans le conducteur, celle-ci vont se répartir sur les parois
3. À l'extérieur du conducteur, le champ vaut $\vec{E} = \frac{\sigma}{\epsilon_0}$ avec une orientation radiale au conducteur
4. Si le conducteur à une cavité, le champ est nul dans celle-ci et elle isole des champs extérieurs, il s'agit d'une cage de Faraday
5. S'il y a une charge dans la cavité, il y a de l'induction sur la paroi intérieur de la cavité et une charge va se former sur celle-ci

### 3.6 Diélectriques (isolants)

Pour un isolant: le champ électrique résultant à l'intérieur ne sera pas nul. Il peut plutôt être décrit par l'équation si-dessous où $K$ appelée kappa est une constante pour chaque matériau:$$\vec{E}_{res} = \frac{\vec{E}_{ext}}{K}$$
Ainsi, le flux peut être décrit par cette équation pour un diélectrique:$$\Phi = \oint{K\vec{E}\cdot d\vec{A}}=\frac{Q_{int}}{\epsilon_0}$$
