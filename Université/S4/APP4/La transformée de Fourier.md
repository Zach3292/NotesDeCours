## Limite de la série de Fourier
Comme vu [ici](Série%20de%20Fourier.md), il est possible de remplacer un signal périodique par une somme d'harmoniques. Cependant, qu'arrive-t-il quand le signal original n'est pas périodique?

Si on prend une onde carrée et qu'on ajoute une zone de silence de plus en plus grande entre chaque pulsation, on se rapproche de plus en plus d'une fonction qui n'est pas périodique et qui devient une simple pulsation. 
![](Images/Pasted%20image%2020260216092959.png)Ici l'axe des fréquences représentes $k/T$ et non $k$. Si on fait tendre la période $T\rightarrow\infty$ et qu'on multiplie les coefficients de Fourier par la période $T$, on obtient **l'enveloppe spectral**, la courbe par laquelle passent tous les points des spectres précédents. Il s'agit de la définition de la **transformée de Fourier**.
![](Images/Pasted%20image%2020260216093343.png)
## Définition de la transformée de Fourier
### Expression mathématique
Lorsqu'on fait tendre $T$ vers l'infini, la pulsation fondamentale $\omega_0$ tend vers zéro, plus précisément vers un élément différentiel $d\omega$. Ainsi la pulsation discrète $k\omega_0$ devient une pulsation continue $\omega$. Si on part de la définition des [coefficients de Fourier](Série%20de%20Fourier.md#Définition) et qu'on fait tendre $T$ vers l'infini, on obtient la **transformée de Fourier** noté comme suit:
$$X(\omega) = \mathcal{F}\left(x(t)\right)=\int^{+\infty}_{-\infty}{x(t)e^{-j\omega t}dt}$$

De la même manière, il est possible d'écrire l'équation de synthèse de la **transformée de Fourier inverse** de $X(\omega)$. On note celle-ci comme suit:
$$x(t)=\mathcal{F}\left(X(\omega)\right)=\frac{1}{2\pi}\int^{+\infty}_{-\infty}{X(\omega)e^{j\omega t}d\omega}$$
### Comparaison avec la série de Fourier
![](Images/Pasted%20image%2020260216094408.png)
## Relation 