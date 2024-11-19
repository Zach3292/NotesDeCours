### Introduction
*La variable indépendante* est celle par laquelle sont effectués les dérivées. 

*La variable dépendante* est celle qui est dérivée.

*L'ordre d'une équation différentielle est l'ordre de la dérivée la plus élevée dans l'équation.*

#### Forme générale d'une équation différentielle
Toute équation différentielle peut s'écrire sous la forme suivante: $$F\left(t,y,y',...,y^{(n)}\right)=0$$
Où $y^{(n)}=\frac{d^nyt}{dt^n}$ est la dérivée d'ordre $n$ de $y$ par rapport à $t$.
#### Équation différentielle linéaire
Si la fonction $F\left(t,y,y',...,y^{(n)}\right)$ est linéaire par rapport à chacune des variables $y,y',...,y^{(n)}$, alors l'équation différentielle $$F\left(t,y,y',...,y^{(n)}\right)=0$$ est dite linéaire.

Une équation est dite linéaire si elle peut se mettre sous la forme $$a_0(t)y^{(n)}+a_1(t)y^{(n-1)}+...+a_n(t)y=f(t)$$
où $a_n$ et $t$ sont des fonctions indépendantes des variables $y,y',...,y^{(n)}$.
##### Équation linéaire différentielle à coefficients constants
L'équation différentielle linéaire $$a_0y^{(n)}+a_1y^{(n-1)}+...+a_ny=f(t)$$ est dite à coefficients constants si $a_n$ sont des **constantes** indépendantes de $t$.

#### Modèle d'entrée/sortie
Les équations linéaires différentielles dans le domaine physique peuvent être représenté comme un modèle d'entrée et sortie. L'entrée est $f(t)$ et la sortie est $y(t)$, dans ce modèle les équations respectent la superposition et la proportionnalité. Les coefficients $a_n$ sont les paramètres du système.

#### Solution à une équation différentielle
Dans le cas d'une équation linéaire, une équation différentielle d’ordre $n$ admet une solution comprenant $n$ constantes arbitraires.
##### Solution générale
La solution générale est une fonction comprenant un *nombre de constantes arbitraires égal à l'ordre de l'équation* et satisfaisant l'équation.
##### Solution particulière
Une solution particulière d’une équation différentielle est une fonction comprenant un *nombre de constants arbitraires* **strictement** *inférieurs à l’ordre de l’équation* et satisfaisant l’équation. 

#### Méthode standard de résolution d'équation à coefficients constants

La solution générale d'une équation différentielle linéaire est égal à la **somme** de 
1. La solution **complémentaire** (solution homogène ou réponse naturelle en électronique) si on remplace $f(t)$ par $0$ (équation homogène).
2. N'importe quelle solution **particulière** (réponse forcée en électronique) de l'équation originale

$$y(t) = y_c(t) + y_p(t)$$
où $y_c(t)$ est la solution générale de de l'équation (homogène) $$a_0y^{(n)}+a_1y^{(n-1)}+...+a_ny=0$$
$y_c(t)$ est une équation comprenant $n$ constantes arbitraires et vérifiant
$$a_0y_c^{(n)}+a_1y_c^{(n-1)}+...+a_ny_c=0$$
et $y_p(t)$ est une fonction ne comportant aucune constante arbitraire vérifiant
$$a_0y_p^{(n)}+a_1y_p^{(n-1)}+...+a_ny_p=f(t)$$
Il faut donc trouver une solution complémentaire et une solution particulière et les additionner.

### Méthodes de résolution pour les équations à coefficients constants de premier ordre
On fait les mêmes trois étapes que vu plus haut
#### Recherche de la solution complémentaire
Nous avons deux approches, prenons l'équation $$\tau\frac{dy}{dt} + y = f(t)$$
Nous avons que $$\tau\frac{dy_c}{dt} + y_c = 0$$
##### Approche intuitive
1. On isole la dérivée.
$$\frac{dy_c}{dt} = \frac{-1}{\tau}y_c$$
2. Quelle est la forme de $y_c(t)$ tel que sa dérivé est proportionnelle à la fonction originale? Ça doit être un exponentielle dans ce cas de forme $$y_c=Ae^{\lambda t}$$
3. On substitue l'équation trouver dans l'équation originale et on résout
##### Approche analytique
On résout pour $y_c$ en faisant isolant tous les termes contenant $y_c$ et en calculant l'intégral.
[[calcul intégral]]

#### Recherche d'une solution particulière
Il existe deux méthodes
##### Méthode des coefficients indéterminés
Prenons l'équation $$\tau\frac{dy_p}{dt} + y_p = f(t)$$
On voit que $y_p(t)$ est une combinaison linéaire de $f(t)$ et de ses dérivées. Il faut donc dérivé plusieurs fois $f(t)$ pour trouver une fonction de *base* pour $f(t)$ et ses dérivées successives.

**Exemple**:
- Si $f(t)$ vaut $20$ -> dérivée: $0$ -> fonction de base: $1$ -> forme: $C$
- Si $f(t)$ vaut $t^2$ ->dérivée: $2t, 2$ -> fonction de base: $1,t$ -> forme: $C_1 + C_2t$
- Si $f(t)$ vaut $5\cos{t}$ ->dérivée: $-5\sin{t},-5\cos{t}$ -> fonction de base: $\cos{t},\sin{t}$ -> forme: $C_1\cos{t} + C_2\sin{t}$

Il faut ensuite écrire $y_p(t) = C_1f_1(t) + C_2f_2(t) + C_kf_k(t)$ et substituer $y_p(t)$ dans l'équation originale pour déterminer les coefficients $C_k$ et obtenir $y_p(t)$.

Si $f(t)$ est constant alors $y_p(t) = f(t)$

**Mise en garde**:
Si la solution complémentaire est égale à la forme trouver de $y_p(t)$, la méthode ne fonctionne pas, il faut multiplier la forme de $y_p(t)$ trouver par $t$ et résoudre pour les coefficients.

##### Méthode de variation des paramètres
Une solution particulière peut être obtenu en faisant varier les paramètres de la solution complémentaire. Dans notre cas, on remplace $A$ par $A(t)$ et on substitut dans l'équation originale, on résout pour $A(t)$.

L'**avantage** de cette méthode au premier ordre est qu'elle permet d'obtenir une formule générale pour $y_p(t)$. L'**inconvénient** est qu'elle conduit parfois à des intégrales complexes.

Si la formule est de la forme vu plus haut alors $$y_p(t)=\left[ \int{e^{\frac{t}{\tau}}f(t)dt} \right]e^{-\frac{t}{\tau}}$$

### Résolution complète d'un équation linéaire à coefficients constants de premier ordre

Si on a l'équation
$$\tau\frac{dy}{dt} + y_= f(t)$$
Comme vu plus haut $$y(t) = y_c(t) + y_p(t)$$
En appliquant la méthode des paramètres on obtient la solution générale suivante:
$$y(t) = Ae^{\frac{-t}{\tau}} + \left[ \int{\frac{1}{\tau}e^{\frac{t}{\tau}}f(t)dt} \right]e^{\frac{-t}{\tau}}$$
### Condition initiale et valeur de la constante arbitraire
Pour un solution générale d'une équation de premier ordre, il y a une constante arbitraire. Pour déterminer la valeur de la constante arbitraire, il faut connaître l'état initiale du système ou $y(t)$ à$t =0$. 

### Application aux circuits électriques du premier ordre
#### Circuit RC
Comme vu [[Circuit à courant continu#7.7 Circuits RC|ici]]. Les équations sont obtenus avec la résolution d'équations différentielles de premier ordre.
![[Pasted image 20241118095859.png]]
La mise en équation du circuit donne $$RC\frac{dV_C(t)}{dt} + V_C(t) = V_s(t)$$
Il s'agit de la même forme d'équation que vue plus haut où $\tau=RC$, $y_c(t) = V_C(t)$ et $f(t)=V_s(t)$.

#### Circuit RL
![[Pasted image 20241119104221.png|300]]
La mise en équation du circuit donne $$\frac{L}{R}\frac{di(t)}{dt}+i(t)=\frac{1}{R}V_s(t)$$
Il s'agit de la même forme d'équation que vue plus haut où $\tau=\frac{L}{R}$, $y_c(t) = i(t)$ et $f(t)=V_s(t)$.
### Méthodes de résolution des équations différentielles linéaires à coefficients constants du second ordre
Soit l'équation suivante $$a\frac{d^2y}{dt^2}+b\frac{dy}{dt}+y=f(t)$$
où $a\neq0$ et $b$ et $c$ sont des contantes données avec $f(t)$ un fonction quelconque donnée.

Si l'équation provient de la mise en équation d'un circuit RLC, alors $a$, $b$ et $c$ sont positifs et on peut poser que $\alpha=\frac{b}{2a}$, que $\omega^2_o=\frac{c}{a}$ et que $g(t)=\frac{f(t)}{a}$ pour mettre l'équation sous la même forme que le Hambley: $$\frac{d^2y}{dt^2}+2\alpha\frac{dy}{dt}+\omega^2_0y=g(t)$$
Comme vu plus haut: $$y(t)=y_c(t) + y_p(t)$$ et les mêmes conditions s'appliquent
#### Recherche de solution complémentaire
Il faut résoudre l'équation suivante $$a\frac{d^2y_c}{dt^2}+b\frac{dy_c}{dt}+y_c=0$$
Comme vu précédemment, la seule fonction $y_c(t)$ qui peut résoudre cette équation est de la forme suivante: $$y_c(t) = Ae^{\lambda t}$$
Par substitution, on obtient
$$\begin{align} a\frac{d^2Ae^{\lambda t}}{dt^2}+b\frac{dAe^{\lambda t}}{dt}+Ae^{\lambda t}& =f(t) \\
a\lambda^2Ae^{\lambda t}+b\lambda Ae^{\lambda t} +cAe^{\lambda t}& =0 \\
\left(a\lambda^2+b\lambda+c\right)Ae^{\lambda t} & = 0 \\
\mathrm{Donc} \\
a\lambda^2+b\lambda+c & = 0
\end{align}$$
Cette dernière équation est appelée *l'équation caractéristique* ou *auxiliaire*. Pour résoudre cette équation on utilise la méthode du discriminant avec la formule quadratique:$$\begin{align}
&\lambda_1 =\frac{-b+\sqrt{\Delta}}{2a} &\lambda_2=\frac{-b-\sqrt{\Delta}}{2a} \\
&& \Delta = b^2-4ac 
\end{align}$$
On obtient alors la solution complémentaire suivante $$y_c(t)=A_1e^{\lambda_1t}+A_2e^{\lambda_2t}$$
##### Cas où le discriminant est négatif
Si le discriminant est négatif, il faut faire appelle aux nombres complexes pour résoudre le problème
$$y_c(t)=B_1e^{\frac{-b+j\sqrt{-\Delta}}{2a}}+B_2e^{\frac{-b-j\sqrt{-\Delta}}{2a}}$$
pour simplifier l'équation, on utilise $\alpha = \frac{b}{2a}$ et $\beta=\frac{\sqrt{-\Delta}}{2a}$ alors on obtient
$$y_c(t)=B_1e^{-\alpha+j\beta}+B_2e^{-\alpha-j\beta}$$
En séparant les termes de l'exposant et en appliquant la [[Note de cours#Formule d'Euler|formule d'Euler]] on obtient ceci: $$y_c(t)=(B_1+B_2)\cdot e^{-\alpha t}\cos{\beta t} + j(B_1-B_2)\cdot e^{-\alpha t}\sin{\beta t}$$
Comme $y_c(t)$ est une fonction réelle, $B_1$ et $B_2$ doivent être des nombres complexes conjugués pour qu'on puisse dire que $$A_1=B_1+B_2 \ \mathrm{et} \ A_2 = j(B_1-B_2)$$
$A_1$ et $A_2$ sont alors des nombres réels et on peut écrire la solution complémentaire sous sa forme finale: $$y_c(t)=A_1e^{-\alpha t}\cos{\beta t} + A_2e^{-\alpha t}\sin{\beta t}$$
#### Recherche d'une solution particulière
Tout comme le premier ordre, il y a deux méthodes pour trouver une solution particulière
##### Méthode des coefficients indéterminés
Même démarche qu'[[Équations différentielles linéaires du premier et second ordre#Méthodes de résolution pour les équations à coefficients constants de premier ordre#Recherche d'une solution particulière#Méthode des coefficients indéterminés|ici]].
##### Méthode de variation des paramètres
On fait varier les deux constantes arbitraires de $y_c(t)$. Si $y_c(t) = A_1h_1(t)+A_2h_2(t)$ alors $y_p(t) =A_1(t)h_1(t)+A_2(t)h_2(t)$. SI on a que $$a\frac{d^2y_p}{dt^2}+b\frac{dy_p}{dt}+y_p=f(t)$$
On substitut $y_p$ dans l'équation et on résout pour trouver $A_1$ et $A_2$. Il est utile de se servir des propriétés de la solution complémentaire pour s'aider à résoudre l'équation. Cette méthode donne souvent des intégrales comme résultat. 

En faisant le calcul, il est possible d'obtenir une formule générale pour $y_p$ si elle respecte la forme vu plus haut: $$y_p(t)=\left[ -\int{\frac{h_2f(t)}{a(h_1h^{'}_2-h^{'}_1h_2)}dt} \right]h_1(t)+\left[ -\int{\frac{h_1f(t)}{a(h_1h^{'}_2-h^{'}_1h_2)}dt} \right]h_2(t)$$
### Conditions initiales et valeurs des constantes arbitraires
Comme pour le premier ordre, il faut connaitre les valeurs de $y(0)$ et de $y'(0)$.
### Application aux circuits électriques de second ordre
![[Pasted image 20241119123221.png|300]]
#### Tension aux bornes du condensateur
La mise en équation du circuit donne pour la tension aux bornes du condensateur$$LC\frac{d^2V_c(t)}{dt^2}+RC\frac{dV_c(t)}{dt}+V_c(t)=V_s(t)$$
En posant $\alpha=\frac{R}{2L}$, $\omega^2_0=\frac{1}{LC}$ et $f(t)=\frac{V_s(t)}{LC}$ on obtient une équation de la forme voulu $$\frac{d^2y}{dt^2}+2\alpha\frac{dy}{dt}+\omega^2_0y=f(t)$$
où $y(t) = V_c(t)$
#### Courant dans l'inducteur
La mise en équation du circuit donne pour le courant dans l'inducteur$$L\frac{d^2i(t)}{dt^2}+R\frac{di(t)}{dt}+\frac{1}{C}i(t)=\frac{dV_s(t)}{dt}$$En posant $\alpha=\frac{R}{2L}$, $\omega^2_0=\frac{1}{LC}$ et $f(t)=\frac{1}{L}\frac{dV_s(t)}{dt}$ on obtient une équation de la forme voulu $$\frac{d^2y}{dt^2}+2\alpha\frac{dy}{dt}+\omega^2_0y=f(t)$$
où $y(t)=i(t)$.