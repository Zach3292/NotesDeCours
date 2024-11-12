### Résumé
Le résumé du gradient est expliqué ici: [](Analyse%20vectorielle.md#Gradient) 
Il s'agit d'un vecteur de dérivée partielle

Exemple: si on a un fonction $f(x,y) = x^2 + y^2$ alors:
$$\nabla f = \left[ \begin{align} & \frac{\partial f}{\partial x} \\ & \frac{\partial f}{\partial y}  \end{align} \right] = \left[\begin{split}
& 2x \\
& 2y
\end{split}\right]$$
Le gradient est un opérateur linéaire alors: $$\begin{align}\nabla(f_1 +f_2) & = \nabla f_1 + \nabla f_2 \\
\nabla(\alpha f) & = \alpha\nabla f
\end{align}$$
On peut utiliser de la superposition grâce à la linéarité. 

Le gradient d'une fonction de température nous indique le chemin le plus rapide pour augmenter en température. 

#### Gradient descent
Le fameux *"gradient descent"* veut tout simplement dire qu'on suit à chaque instant le vecteur de gradient pour pouvoir se retrouver au point maximum du champ scalaire. Il s'agit d'une manière efficace de trouver le *sommet* d'une fonction multi-dimensionnelle. C'est très souvent utilisé en machine learning pour entrainer des intelligences artificielles.
#### Dérivée directionnelle
Une dérivée directionnelle permet de calculer le taux de variation d'une fonction à plusieurs variables selon une certaine direction $\vec{v}$.  Le gradient est un outil qui permet de calculer cette dérivée directionnelle: $$ D_{\vec{v}}\ f = \frac{\vec{v}}{||\vec{v}||}\cdot(\nabla f)$$
#### Potentiel gravitationnel
Le gradient permet de calculer le potentiel gravitationnel $U$ d'un objet dans un champ gravitationnel. Selon les lois de Newton: $$\vec{F} = \frac{-m_1 m_2 G}{r^3}\vec{r} = -\nabla U$$
Et :$$ U = \frac{-m_1 m_2 G}{r}$$
Ainsi, en calculant le gradient de $U$, on obtient le champ gravitationnel entre deux objets.