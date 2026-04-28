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

On représente souvent les pôles et les zéros selon ce graphique en ignorant ceux à l'infini:
![](Images/Pasted%20image%2020260217134445.png)
En général, **un "x" représente un pôle et un "o" représente un zéro**. Le diagramme de pôles-zéros permet, entre autres, de dire si un système est stable ou non et de donner une approximation de la forme de $H(j\omega)$.
### Factorisation
La forme générale d'une fonction de transfert est la suivante:
$$H(s)=\frac{\left(a_ms^m+a_{m-1}s^{m-1}+...+a_1s+a_0\right)}{\left(b_ns^n+b_{n-1}s^{n-1}+...+b_1s+b_0\right)}$$
Cette fonction est d'ordre $m$ au numérateur et $n$ au dénominateur. On définit le **gain $K$** comme le rapport entre le coefficient du terme de plus grand ordre au numérateur $a_m$ et du dénominateur $b_m$:
$$K=\frac{a_m}{b_m}$$
On peut factoriser la fonction de transfert comme suit:
$$H(s)=K\frac{(s-z_1)(s-z_2)...(s-z_{m-1})(s-z_m)}{(s-p_1)(s-p_2)...(s-p_{n-1})(s-p_n)}$$
$$H(s)=K\frac{\prod^m_{k-1}{(s-z_k)}}{\prod^n_{k-1}{(s-p_k)}}$$
Où $z_k$ sont les zéros et $p_k$ les pôles.

### Développement en fractions partielles
Afin de pouvoir repasser dans le domaine temporel, il est souvent nécessaire d'exprimer la fonction de transfert sous forme de termes simples. Si on a la forme suivante:
$$H(s)=K\frac{(s-z_1)(s-z_2)...(s-z_{m-1})(s-z_m)}{(s-p_1)(s-p_2)...(s-p_{n-1})(s-p_n)}$$
#### Cas 1: $m\geq n$ 
Il faut d'abord décomposer $H(s)$ comme la somme d'un polynôme en $s$ et d'une fraction de polynômes tel que $m<n$. En pratique, on effectue cette opération en factorisant le dénominateur au numérateur.
#### Cas 2: pôles réels uniques
Dans la cas où la fonction ne possède pas de pôles complexes conjugués, on peut exprimer la fonction sous la forme:
$$H(s)=\frac{c_1}{s-p_1}+\frac{c_2}{s-p_2}+...+\frac{c_{n-1}}{s-p_{n-1}}+\frac{c_n}{s-p_n}$$
#### Cas 3: pôles complexes conjugués
Dans le cas où la fonction de transfert $H(s)$ possède des pôles complexes conjugués (par exemple $p_1$ et $p_2=p_1^*$), on peut exprimer la fonction de transfert sous la forme:
$$H(s)=\frac{c_1s+c_2}{(s-p_1)(s-p_2)}+...+\frac{c_{n-1}}{s-p_{n-1}}+\frac{c_n}{s-p_n}$$
Dans le cas d’un système physique, la réponse à une impulsion est toujours un signal réel. Dans ce cas, la fonction de transfert possède des pôles complexes conjugués et on se retrouve dans le cas #3. Ensuite, afin de connaître les coefficients $c_i$, il suffit de multiplier les termes de droite et de gauche par $(s-p_i)$ puis d’identifier le terme $c_i$ en regardant la valeur en $s=p_i$.

#### Exemple
On considère la fonction de transfert suivante:
$$H(s)=\frac{s^4-s^3+s^2+1}{s^3+s}$$
On voit que $m\geq n$ donc on est au cas #1, il faut factoriser le dénominateur au numérateur
$$H(s)=\frac{(s^3+s)(s-1)+s+1}{s^3+s}=(s-1)+\frac{s+1}{s(s+j)(s-j)}$$
La deuxième partie de la fonction peut aussi être définie par ses pôles, ses zéros et son gain:
- Pôles: $p_1=-j$, $p_2=p_1^*=j$, $p_3=0$
- Zéros: $z_1=-1$, $z_2=\infty$
- Gain: $K=1$
Les deux premiers pôles sont des complexes conjugués, on se retrouve au cas #3 et on peut réécrire la fonction sous une autre forme de fractions partielles:
$$H(s)=(s-1)+\frac{c_1s+c_2}{(s-p_1)(s-p_2)}+\frac{c_3}{s-p_3}$$
Pour trouver les valeurs de $c_i$, on multiplie par $(s-p_i)$ les termes de gauche et de droite
$$H(s)(s-p_1)=(s-1)(s-p_1)+\frac{c_1s+c_2}{(s-p_2)}+(s-p_1)\frac{c_3}{s-p_3}$$
Puis on évalue en $s=p_1=-j$ en prenant que $H(s)$ égal la version factoriser plus haut
$$\begin{align}
H(s)(s-p_1)&=0+\frac{c_1p_1+c_2}{p_1-p_2}+0 \\
(s-1)(s-p_1)+\frac{(s+1)(s-p_1)}{s(s+j)(s-j)}&=\frac{c_1p_1+c_2}{p_1-p_2}\\
0+\frac{s+1}{s(s-j)}&=\frac{c_1p_1+c_2}{p_1-p_2}\\
s&=p_1\\
\frac{p_1+1}{p_1(p_1-j)}&=\frac{c_1p_1+c_2}{p_1-p_2}\\
1+j&=-jc_1+c_2
\end{align}$$
On répète mais avec $(s-p_2)$:
$$H(s)(s-p_2)=(s-1)(s-p_2)+\frac{c_1s+c_2}{(s-p_1)}+(s-p_2)\frac{c_3}{s-p_3}$$
Puis on évalue avec $s=p_2=j$:
$$\begin{align}
H(s)(s-p_2)&=0+\frac{c_1p_2+c_2}{p_2-p_1}+0 \\
(s-1)(s-p_2)+\frac{(s+1)(s-p_2)}{s(s+j)(s-j)}&=\frac{c_1p_2+c_2}{p_2-p_1}\\
0+\frac{s+1}{s(s+j)}&=\frac{c_1p_2+c_2}{p_2-p_1}\\
s&=p_2\\
\frac{p_2+1}{p_2(p_2+j)}&=\frac{c_1p_2+c_2}{p_2-p_1}\\
1-j&=-jc_1+c_2
\end{align}$$
On trouve alors que $c_1=-1$ et $c_2=1$

Pour obtenir $c_3$ on fait le même développement
$$H(s)(s-p_3)=(s-1)(s-p_3)+(s-p_3)\frac{c_1s+c_2}{(s-p_1)(s-p_2)}+c_3$$
$$\begin{align}
H(s)(s-p_3)&=(s-1)(s-p_3)+(s-p_3)\frac{c_1p_2+c_2}{p_2-p_1}+c_3 \\
(s-1)(s-p_3)+\frac{(s+1)(s-p_3)}{s(s+j)(s-j)}&=(s-1)(s-p_3)+(s-p_3)\frac{c_1p_2+c_2}{p_2-p_1}+c_3\\
(s-1)(s-p_3)+\frac{(s+1)}{(s+j)(s-j)}&=(s-1)(s-p_3)+(s-p_3)\frac{c_1p_2+c_2}{p_2-p_1}+c_3\\
\frac{(s+1)}{(s+j)(s-j)}&=(s-p_3)\frac{c_1p_2+c_2}{p_2-p_1}+c_3\\
s&=p_3\\
\frac{1}{1}&=c_3\\
1&=c_3
\end{align}$$
On peut donc remplacer les pôles et les coefficients dans la formule originale pour obtenir:
$$H(s)=(s-1)+\frac{-s+1}{(s+j)(s-j)}+\frac{1}{s}$$
À l'aide des tables de transformée de Laplace inverse, on peut trouver la [réponse impulsionnelle](Introduction%20signaux%20et%20systèmes.md#Fonction%20de%20transfert%20et%20réponse%20impulsionnelle) du système:
$$h(t)=\mathcal{L}^{-1}(H(s))=\delta'(t)-\delta(t)-\cos{t}+\sin{t}+u(t)$$
Où $u(t)$ représente la fonction échelon et $\delta(t)$ est [l'impulsion de Dirac](La%20transformée%20de%20Fourier.md#L'impulsion%20de%20Dirac).
### Pôles et zéros avec Matlab
Dans Matlab, la fonction *roots* nous permet d'obtenir les racines d'un polynôme.
## Lien entre les transformées de Laplace et de Fourier
### Définition
Si on restreint que $x(t)$ doit être causal (que pour $t<0$, $x(t)=0$), la transformée de Fourier s'obtient simplement en posant que $s=j\omega$.
### Évaluation de $H(j\omega)$ en fonction des pôles et des zéros
Comme vu plus tôt, on peut exprimer $H(s)$ comme suit:
$$H(s)=K\frac{(s-z_1)(s-z_2)...(s-z_{m-1})(s-z_m)}{(s-p_1)(s-p_2)...(s-p_{n-1})(s-p_n)}$$
On peut donc aussi exprimer la fonction de transfert harmonique:
$$H(j\omega)=K\frac{(j\omega-z_1)(j\omega-z_2)...(j\omega-z_{m-1})(j\omega-z_m)}{(j\omega-p_1)(j\omega-p_2)...(j\omega-p_{n-1})(j\omega-p_n)}$$
On peut aussi calculer le module et la phase de la fonction de transfert harmonique:
$$|H(j\omega)|=|K|\frac{|j\omega-z_1||j\omega-z_2|...|j\omega-z_{m-1}||j\omega-z_m|}{|j\omega-p_1||j\omega-p_2|...|j\omega-p_{n-1}||j\omega-p_n|}$$
$$\angle H(j\omega)=\angle K +(\angle(j\omega-z_1)+...+\angle(j\omega-z_m))-(\angle(j\omega-p_1)+...+\angle(j\omega-p_n))$$
## Réponse impulsionnelle d'un système LTI
### Définition
La réponse impulsionnelle $h(t)$ est par définition la réponse du système lorsque l'entrée est l'impulsion de Dirac. Par définition, la sortie dans le domaine de Laplace est relié à l'entrée par la fonction de transfert $H(s)$. Si l'entrée est une impulsion de Dirac, sa transformée de Laplace est 1 (selon les tables) et donc dans le domaine de Laplace, la transformée de la réponse impulsionnelle est $Y(s)=H(s)$. Mathématiquement, on peut donc exprimer la réponse impulsionnelle d'un système comme la transformée de Laplace inverse de la fonction de transfert $H(s)$:
$$h(t)=\mathcal{L}^{-1}(H(s))$$
### Stabilité d'un système
Le lieu des pôles et des zéros permet aussi de déterminer la stabilité d'un système LTI.

Un système est stable si sa réponse impulsionnelle tend vers 0 lorsque $t$ tend vers l'infini.

De façon général, la réponse impulsionnelle sera à énergie finie si et seulement si tous les pôles $p_i$ de la fonction de transfert sont dans le demi plan gauche tel que:
$$Re(p_i)<0$$
S'il existe un pôle sur l'axe des imaginaires pur ($Re(p_i)=0$), on dit que le système est marginalement stable.
### Évaluation de réponse impulsionnelle en fonction des pôles et des zéros
Avec la position des pôles et des zéros dans le plan complexe, on peut également deviner rapidement la forme de la réponse impulsionnelle.
- Plus un pôle s'approche de l'axe imaginaire, plus le système est résonnant à cette fréquence. Ceci se traduit par un pic étroit dans le domaine fréquentiel et un longue réponse dans le domaine temporel.
- La position verticale des pôles à un impact direct sur la fréquence de résonance du système. Plus les pôles sont éloignés de l'axe horizontal, plus la fréquence de résonance sera grande.
## Propriétés de la transformée de Laplace
### Opération générale
Les propriétés de la transformée de Laplace sont très similaire au [propriétés de la transformée de Fourier](La%20transformée%20de%20Fourier.md#Propriétés%20de%20la%20transformée%20de%20Fourier), sauf qu'on remplace $j\omega$ par $s$. Voici un cours résumé:
- Ces transformées (Laplace et Fourier) sont linéaires; 
	- La transformée d’une dérivée est égale à la transformée du signal avant dérivation, multipliée par l’élément fréquentiel $s$ (pour Laplace) ou $j\omega$ (pour Fourier); 
	- La transformée d’une intégrale est égale à la transformée du signal avant intégration, divisée par l’élément fréquentiel $s$ (pour Laplace) ou $j\omega$ (pour Fourier);
	- Un décalage temporel de $\tau$ introduit le facteur $e^{-s\tau}$ (pour Laplace) et $e^{lj\omega\tau}$ (pour Fourier); 
	- Multiplier par une sinusoïde a l’effet de décaler le spectre d’origine, et de le centrer à la fréquence de la sinusoïde (la porteuse), à la fois dans les fréquences positives et négatives.
### Cas avec des conditions initiales
Dans le cas général, la transformée de Laplace de la dérivée d'une fonction est donnée par:
$$\mathcal{L}(x'(t))=s\mathcal{L}(x(t))-x(0)$$
De même que:
$$\mathcal{L}(x''(t))=s^2\mathcal{L}(x(t))-sx(0)-x'(0)$$
