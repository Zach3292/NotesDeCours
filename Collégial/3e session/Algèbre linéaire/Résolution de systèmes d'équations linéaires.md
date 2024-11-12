Un système est compatible s'il y a une solution et incompatible sinon

Si $\mathrm{det}A = 0$, il y a infinie ou aucune solution s'il y a le même nombre d'inconnus que d'équations

### Règle de Cramer
Soit un système $AX=B$ si $n$ équations et inconnus et que $\mathrm{det}A \neq 0$, On note $\Delta$ le déterminant da la matrice $A$ et $\Delta x_i$ le déterminant qu'on obtient en remplaçany la i-ème colonne de $A$ par la matrice $B$.

Un tel système admet une solution unique: $$x_i = \frac{\Delta x_i}{\Delta}$$
### Méthode de Gauss Jordan
**Opérations élémentaires de ligne**:
- Intervertir 2 lignes
- Multiplier une ligne par un scalaire non-nul
- Remplacer la ligne $i$ par $i+kj$
**Matrice augmenté d'un système d'équations linéaires:**

$$
  \left[\begin{array}{rrr|r}
    a_{11} & a_{12} & a_{1n} & b_1 \\ 
	a_{21} & a_{22} & a_{2n} & b_2 \\ 
	a_{n1} & a_{n2} & a_{nn} & b_3 \\ 
  \end{array}\right]
$$
**Matrices équivalentes**: Matrice augmentée associé à des systèmes ayant le même ensemble de solution

La méthode consiste à obtenir une matrice échelonnée réduite et effectuant des opérations élémentaires de ligne sur une matrice équivalentes au systèmes à résoudre. Les coefficients du système seront dans la colonne augmentée. 

#### Caractérisation d'un système
Rang de la matrice: nombre de ligne non-nulles de la matrice augmentée échelonnée équivalente

Si $AX=B$ est un système d'équations linéaires à $n$ inconnus et équations dont la matrice des coefficients $A$ est une matrice de rang $p$ et que la matrice $[A|B]$ est de rang $q$. Alors le système:
- N'admet aucune solution pour $p<q$
- Admet une infinité de solution si $p=q$ et $p<n$
- Admet une solution unique si $p=q=n$
Si le système admet une infinité de solution, la solution générale comporte $n-q$ inconnues libres.

#### Détermination de l'inverse avec Gauss-Jordan
Si $A^{-1} = B$ alors $[A_n|I_n]$ est équivalent à $[I_n|B_n]$. Il est donc possible d'obtenir l'inverse d'une matrice en l'augmentant de sa matrice identité et en appliquant Gauss-Jordan.
