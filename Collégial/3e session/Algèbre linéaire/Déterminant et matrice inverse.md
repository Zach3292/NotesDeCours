Le déterminant d'une matrice carré est noté $\mathrm{det}A$ ou $|A|$ 

$A$ est singulière si $\mathrm{det}A = 0$ et régulière sinon. 

Seules les matrices régulières possèdent un inverse
### Calcul du déterminant
#### Règle de Sarrus
![[Pasted image 20241111200008.png]]
#### Méthode classique
**Mineur**: déterminant d'une matrice si on enlève la i-ème ligne et la j-ème colonne noté $M_{ij}$
**Cofacteur d'une matrice**: noté $A_{ij} = {\left(-1 \right)}^{(i+j)}M_{ij}$ 
Calcul du déterminant:
$$\mathrm{det}A = \sum^n_{k=1}{a_{ik}A_{ik}} = \sum^n_{k=1}{a_{kj}A_{kj}}$$
### Propriétés des déterminants
- On peut calculer le déterminant à partir de n'importe quelle ligne ou colonne
- Si $B$ résulte de l'inversion de deux lignes ou colonnes d'une matrice $A$ alors $\mathrm{det}B = -\mathrm{det}A$
- Si $A$ est triangulaire alors $\mathrm{det}A = \prod^n_{k=1}{a_{kk}}$
- $\mathrm{det}\left(A^{\mathrm{T}}\right) = \mathrm{det}A$
- Le déterminant d'une matrice avec ligne et colonne nulle est nulle
- Si $B$ est une matrice obtenue en multipliant une ligne ou colonne de $A$ par une constante $c$ alors $\mathrm{det}B = c\cdot\mathrm{det}A$
- $\mathrm{det}(cA) = c^n\cdot\mathrm{det}A$
- Une matrice carré avec deux lignes ou colonne identique à un déterminant nul
- Si une ligne ou colonne est le multiple d'un autre le déterminant est nul
- Si $B$ est une matrice obtenue en ajoutant un multiple d'une ligne ou colonne d'une matrice $A$ à une autre ligne ou colonne d'une matrice $A$ alors $\mathrm{det}B = \mathrm{det}A$
- $\mathrm{det}(AB) = \mathrm{det}A \cdot \mathrm{det}B$

### Calcul d'une matrice inverse
Matrice de cofacteur associée à une matrice carré $A$ notée $\mathrm{cof}A$
$$\mathrm{cof}A = 
\begin{bmatrix} 
A_{11} & A_{12} & A_{1n} \\ 
A_{21} & A_{22} & A_{2n} \\ 
A_{n1} & A_{n2} & A_{nn} \\ 
\end{bmatrix}$$
Matrice adjointe de $A$ notée $\mathrm{adj}A = \left(\mathrm{cof}\right)^{\mathrm{T}}$

$$A^{-1} = \frac{1}{\mathrm{det}A}\cdot\mathrm{adj}A$$

#### Propriétés des matrices inverses
- Si $AC=D$ et $EB=F$ alors $C=A^{-1}D$ et $E=FB^{-1}$
- Matrice inverse d'une matrice régulière est toujours unique
- $\mathrm{det}(A^{-1})=\frac{1}{\mathrm{det}A}$
- $\left(A^{-1}\right)^{-1} = A$
- $(AB)^{-1} = B^{-1}A^{-1}$
- $(A^\mathrm{T})^{-1} = (A^{-1})^\mathrm{T}$
- $(kA)^{-1} = \frac{1}{k}A^{-1}$
