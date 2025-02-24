### Rappel sur les bases vectorielles
Rappel sur les bases [ici](../../../Collégial/3e%20session/Algèbre%20linéaire/Vecteurs%20du%20plan.md#Principe%20de%20base). Dans ce cours, on utilisera les lettres $a,b,c$ pour identifier les bases ainsi que des indices $1,2,3$ pour spécifier les trois axes.

Il est possible d'exprimer un vecteur dans une base en faisant le produit scalaire avec chacun des vecteurs unitaires de la base:
$$r_i^a=\vec{r}\cdot\hat{a}_i\rightarrow\underline{r}^a=\begin{bmatrix}\vec{r}\cdot\hat{a}_1\\ \vec{r}\cdot\hat{a}_2\\ \vec{r}\cdot \hat{a}_3\end{bmatrix}$$
### Transfert d'une équation vectorielle vers un équation matricielle
**Lorsque les vecteurs-colonnes sont tous exprimés dans la même base**, on peut transformer les équations vectorielles avec des vecteurs de position en équations matricielles avec des vecteur-colonnes.
### Calcul de longueur, projections et angles avec les composantes
$$\lVert\vec{r}\rVert^2=\vec{r}\cdot\vec{r}=\underline{r}^T\underline{r}=r_1^2+r_2^2+r_3^2$$
$$\lVert\vec{r}\rVert=\sqrt{\underline{r}^T\underline{r}}$$
$$d=\vec{r}\cdot\hat{n}=\underline{r}^T\underline{n}$$
$$\cos{\angle(\hat{n}_1\hat{n}_2)}=\hat{n}_1\cdot\hat{n}=\hat{\underline{n}}_1^T\hat{\underline{n}}_2$$
### Produit vectoriel
$$\vec{u}=\vec{v}\times\vec{w}\rightarrow\underline{u}=\underline{v}^\times\underline{w}\rightarrow\begin{bmatrix}u_1\\ u_2 \\ u_3\end{bmatrix}=\begin{bmatrix}o&-v_3&v_2 \\ v_3 &0&-v_1\\ -v_2&v_1&0\end{bmatrix}\begin{bmatrix}w_1\\ w_2 \\ w_3\end{bmatrix}$$
L'ordre des multiplication est importante
### Produit tensoriel / produit intérieur