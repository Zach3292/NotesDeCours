### Définition
Une particule est comme un point, sauf qu'elle possède une masse. Ainsi, comme un point, *elle ne possède pas d'orientation, donc aucune vitesse et accélération angulaire sur elle même*. Elle n'a aussi aucune dimension. Cependant, une particule possède une masse donc elle a d'autre propriété importante.
### Système de particules
Il s'agit d'un ensemble de particule. Pour un système $S$ formé d particule $Qi$.
$$\begin{align}
m^S&\triangleq\sum^n_{i=1}{m^{Q_i}} \\
^N\vec{L}^S&\triangleq\sum^n_{i=1}{^N\vec{L}^{Q_i}}\\
^NK^S&\triangleq\sum^n_{i=1}{^NK^{Q_i}}
\end{align}$$
La masse et le centre masse du système sont décrit [ici](../../S2/APP6/Masse,%20centre%20de%20masse%20et%20centroïde.md).
### Momentum linéaire
Comme décrit [ici](../../../Collégial/1ere%20session/Physique/Quantité%20de%20mouvement.md) et est défini comme suit:
$$^N\vec{L}^Q\triangleq m^Q\cdot {}^N\vec{v}^Q$$
Pour un système de particule:
$$^N\vec{L}^S\triangleq\sum^n_{i=1}{^N\vec{L}^{Q_i}}=\triangleq\sum^n_{i=1}{m^{Q_i}\cdot{}^N\vec{v}^{Q_i}}=m^S\cdot {}^N\vec{v}^{S_{cm}}$$
La somme des forces (force résultante) peut être représenté en fonction du momentum linéaire:
$$\vec{F}^S=\frac{^Nd{}^N\vec{L}^S}{dt}$$
### Momentum angulaire
On peut noter le momentum angulaire d'une particule $Q$ autour d'un point $O$ dans un référentiel $N$ comme:
$$^N\vec{H}^{Q/O}\triangleq\vec{r}^{Q/O}\times{}^N\vec{L}^Q=\vec{r}^{Q/O}\times m^Q{}^N\vec{v}^Q$$
Pour un système de particule $S$:
$$^N\vec{H}^{S/O}\triangleq\sum^n_{i=1}{^N\vec{H}^{Q_i/O}}=\sum^n_{i=1}{\vec{r}^{Q_i/O}\times{}^N\vec{L}^{Q_i}}=\sum^n_{i=1}{\vec{r}^{Q_i/O}\times m^{Q_i}{}^N\vec{v}^{Q_i}}$$
La somme de moment (moment résultant) peut être représenté en fonction du momentum angulaire:
$$\vec{M}^{S/O}=\frac{^Nd{}^N\vec{H}^{S/S_{cm}}}{dt}+\vec{r}^{S_{cm}/O}\times\frac{^Nd{}^N\vec{L}^S}{dt}$$
Il y a aussi un théorème pour changer le point de référence d'un momentum angulaire:
$$^N\vec{H}^{S/P}={}^N\vec{H}^{S/O}+\vec{r}^{O/P}\times{}^N\vec{L}^S = {}^N\vec{H}^{S/O}+\vec{r}^{O/P}\times m^S{}^N\vec{v}^{S_{cm}}$$
### Énergie cinétique d'une particule
Comme un particule possède une masse, elle possède de l'énergie. L'énerie cinétique d'une particule $Q$ est décrite par:
$$^NK^Q\triangleq\frac{1}{2}m^Q\cdot {}^N\vec{V}^Q\cdot{}^N\vec{v}^Q$$
Pour un système de particule $S$:
$$^NK^S\triangleq\sum^n_{i=1}{^NK^{Q}}$$