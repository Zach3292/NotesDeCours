## Introduction
La transformée de Laplace est une forme plus général de la transformée de Fourier. Il est aussi possible d'obtenir très facilement une approximation de [fonction de transfert harmonique](Fonction%20de%20transfert%20harmonique.md) à partir de la fonction de transfert $H(s)$. De façon formelle, on exprime la relation entre l'entrée,  la sortie et la fonction de transfert d'un signal comme suit:
$$Y(s) = H(s)X(s)$$
$$Y(\omega)=H(j\omega)X(\omega)$$
Il existe cependant des signaux pour lesquels la transformée de Fourier n'existe pas. Il faut donc utiliser la forme plus générale: la **transformée de Laplace**.
## La transformée de Laplace
### Formalisation
La transformée de Laplace $X(s)$ unilatérale d'un signal $x(t)$ se définit comme suit:
$$X(s)=\int^{+\infty}_0{x(t)e^{-st}dt}$$
On appelle cette forme la forme unilatérale puisque l'intégral évalue seulement les valeurs positives de $t$. Ça revient à considérer que les signaux $x(t)$ sont nuls pour $t<0$.
Comme pour les fonctions de transfert harmonique, la fonction de transfert $H(s)$ se trouvent en isolant $Y(s)/X(s)$. En posant $s=j\omega$ il est possible de directement la fonction de transfert harmonique à partir de $H(s)$. 

### Convergence
Comme la transformé de Laplace est une fonction de la variable $s$, on pourrait supposé que comme la variable, la fonction est défini sur tout le plan complexe. En effet, l'intégrale ne converge pas sur toutes les valeurs de $s$. La région du plan où l'intégrale de $X(s)$ converge s'appelle le **domaine de convergence**. À l'extérieur de la région de convergence, la transformée de Laplace n'existe pas.

## Fonction de transfert $H(s)$
### Pôles et zéros
La fonction de transfert pour un système LTI est de forme de fraction de polynômes. Elle peut donc être décrite par ses pôles et ses zéros:
- **Les pôles sont les racines du dénominateur de $H(s)$**, les valeurs de $s$ pour lesquelles $H(s)\rightarrow\infty$
- **Les zéros sont les racines du numérateur de $H(s)$**, les valeurs de $s$ pour lesquelles $H(s)\rightarrow 0$
Une fonction caractéristique d'une fonction de transfert donc la réponse d'un système est réelle est que **les pôles et les zéros complexes doivent apparaître en paires conjuguées**. Seul les pôles ou zéro réels n'ont pas à obéir à cette contrainte.