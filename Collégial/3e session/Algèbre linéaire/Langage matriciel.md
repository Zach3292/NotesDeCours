**Matrice**: un tableau
**Équation linéaire**: $a_1x_1 + a_2x_2 + a_nx_n = b$ où $a_n$ et $b$ sont des nombres réels et $x_n$ des variables
**Système d'équation linéaire**: plusieurs équations linéaires avec les mêmes variables
**Matrice de coefficient**: $$\begin{bmatrix} a_1 & a_2 & a_n \\ a_3 & a_4 & a_m \end{bmatrix}$$
$A_{m\times n}$: Matrice de $m$ lignes et $n$ colonnes
$1\times n$: Matrice ligne
$m \times 1$: Matrice colonne
$A = \left[a_{ij}\right]_{m\times n}$ i: indice de ligne, j: indice de colonne -> Matrice complète vs $a_{ij}$ qui représente seulement un élément d'une matrice

$A_{n\times n}$: Matrice carré d'ordre $n$
**Trace**: somme des éléments de la diagonale d'une matrice carré
$$\mathrm{Tr}\left(A\right) = \sum^n_{i=1}{a_{ii}}$$
Deux matrices sont égales si elles sont identiques, même format et mêmes éléments
**Matrice nulle**: rempli de zéro
**Matrice triangulaire**: matrice carré dont les éléments au dessus au en dessous de la diagonale sont nuls. Peut être inférieur $\left(i>j=0\right)$ ou supérieur$\left(i<j=0\right)$
**Matrice diagonale**: matrice triangulaire inférieur et supérieur en même temps
**Matrice scalaire**: matrice diagonale dont tous les éléments sont identiques
**Matrice identité**: matrice scalaire dont tous les éléments sont 1
**Matrice carré symétrique**: $a_{ij} = a_{ji}$ et $A = A^{ \mathrm{ T } }$
**Matrice carré asymétrique**:  $a_{ij} = -a_{ji}$ et $A = -A^{ \mathrm{ T } }$
- Trace est toujours nulle
**Matrice échelonnée**:
- Toutes les lignes non-nulles sont au-dessus de toues les lignes nulles
- Le pivot d'une ligne (premier élément non-nul) se trouve dans une colonne à droite de celle du pivot de la ligne au dessus d'elle vaut 1
- Tous les coefficients sous un pivot sont nuls
**Matrice échelonnée réduite**:
- Les pivots sont les seuls éléments non-nuls de leur colonne
$$\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
\begin{vmatrix}
a & b \\
c & d
\end{vmatrix} \ A^{ \mathrm{ T } } \ \mathrm{ det }A$$