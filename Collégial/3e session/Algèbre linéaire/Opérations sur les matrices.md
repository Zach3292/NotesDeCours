### Opération de base
**Addition**: additionner chaque terme avec son équivalent
- Seulement des matrices de même dimension
- Commutative
**Multiplication scalaire**: 
- Commutative
**Transposition**: $A^{ \mathrm{ T } }$  $\left(a_{ij}\right)^\mathrm{T} = a_{ji}$ 

### Propriétés sur les opérations
$$\begin{align}
A + B & = B + A \\
(A+B) + C & = A+(B+C) \\
A + 0_{m\times n} & = A \\
A - A & = 0_{m\times n} \\
k(A+B) & = kA+kB \\
kr(A) & = k(rA) \\
1A & = A \\
0A & = 0_{m\times n} \\
\left(A^{ \mathrm{ T } }\right)^{ \mathrm{ T } } & = A\\
\left(kA\right)^{ \mathrm{T}} & = kA^{ \mathrm{ T } } \\
\left(A + B\right)^{ \mathrm{ T } } & = A^{ \mathrm{ T } } + B^{ \mathrm{ T }}
\end{align}$$
### Multiplication de matrice
$A_{m\times n}B_{n\times p} = C_{m\times p}$
$$C_{ij} = \sum^n_{k=i}{a_{ik}b_{kj}}$$
**Opération non-commutative**
**Matrice idempotente**: $A^2 = A$
**Matrice nilpotente**: $A^k = 0_{m\times n}$
**Indice de nilpotence**: le plus petit $k$ qui  rend la matrice nilpotente

#### Propriétés de la multiplication de matrice
$$\begin{align}
AB & \neq BA \\
(AB)C & = A(BC) \\
r(AB) & = (rA)B \\
AI_n = A & \ \ \ \ \ I_nB = B \\
A(B+C) & = AB + AC \\
(D+E)F & = DF + DE \\
(AB)^{ \mathrm{ T } } & = B^{ \mathrm{ T } }A^{ \mathrm{ T } } \\
AB = AC & \rightarrow B \neq C
\end{align}$$