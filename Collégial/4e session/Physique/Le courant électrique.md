---
id: Le courant électrique
aliases: []
tags: []
---

### 6.1 Introduction

Pour qu'il y a est un courant électrique, il doit y avoir un mouvement des charges donc il n'y a pas d'équilibre électrostatique.

Par convention, le courant va à l'inverse du mouvement des électrons. Le courant va dans la même direction que le champ électrique alors $i//\vec{E}$ mais il s'agit d'un abut de notation puisque le courant est un scalaire et non pas un vecteur.
$$i = \left|\frac{Q_{net}}{\Delta t}\right| = \left|\frac{dq}{dt}\right| \left[\frac{C}{s}\right] \left[A\right]$$

#### Loi des noeuds:

Lorsqu'il y a un noeud dans un circuit, le courant entrant est égale au courant sortant de ce noeud tel que $i_1 + i_2 = i_3$.

#### Vitesse de dérive

La vitesse de dérive des électrons est très lente. $v_d = \frac{l}{\Delta t} \approx 10^{-6} \ m/s$

Il est possible d'obtenir le courant en fonction de la vitesse de dérive:

1. Pendant $\Delta t$, l'électron parcourt $l=v_d\Delta t$.
2. La densité de charge $n$ vaut $n=\frac{nb_é}{V}$
3. $V = A_S \cdot l$
4. $nb_é = nA_Sl$
5. $q = -e$
6. $Q = -enA_Sl$
7. $i =  \left|\frac{Q_{net}}{\Delta t}\right| = \frac{enA_Sl}{\Delta t} = enA_Sv_d$

#### La densité de courant

La densité de courant $\vec{J}$ vaut $\vec{J} = \frac{i}{A} = en\vec{v_d}$

$$i = \int{\vec{J}\cdot d\vec{A}}$$


### 6.2 Conduction et champs électrique

Sans champ, le mouvement moyen des électrons est nul.

La vitesse des électrons le long du fil vaut $\vec{v} = v_{th} + v_d$
$$v_d = at = \frac{-e\vec{E}\tau}{m}$$

$\tau$ est le temps moyen entre deux collisions

Alors $$\vec{J} = \frac{ne^2\vec{E}\tau}{m}=\sigma\vec{E}=\frac{\vec{E}}{\rho}$$

Plus $\frac{ne^2\tau}{m}$ est grand, meilleur est le conducteur

$$\frac{ne^2\vec{E}\tau}{m} = \sigma$$

#### Loi d'Ohm microscopique

La loi d'Ohm microscopique est la suivante:
$$\vec{J} = \sigma\vec{E}=\frac{\vec{E}}{\rho}
$$


### 6.3 Résistivité et température


Pour un conducteur: si $T°++ \rightarrow \tau -- \rightarrow \rho ++$
Si $T°++ \rightarrow n$ demeure constant

$\rho\ \alpha \ T°$

Pour un semi-conducteur:
Si $T°++\rightarrow n++ \rightarrow \rho--$



Pour un conducteur ou un supra conducteur:

$$\rho = \rho_0\left(1+\alpha\left(T-T_0\right)\right)$$ 

*Voir si un peut mettre une valeur absolue à la température*
$\alpha$ peut être trouver dans le cahier à la page 199 selon les matériaux.

### 6.4 Courant dans les conducteurs

$$\begin{align}
\vec{J} & = \frac{\vec{E}}{\rho} \\
& = \frac{\Delta V}{\rho l} \\
\frac{i}{A} & = \frac{\Delta V}{\rho l} \\
\Delta V & = \frac{i\rho l}{A} \\
R & =\frac{\rho l}{A} \\
\Delta V & = Ri
\end{align}$$

### 6.5 La loi d'Ohm

$$\Delta V = Ri$$

Il y a des conducteurs ohmiques et des conducteurs non-ohmiques.

La résistivité d'un matériau est donné par la relation: $$R=\rho\frac{l}{s}$$
### 6.6 La puissance électrique

La batterie fait un travail électrique: $W =\Delta U_e = q\Delta V$.

La puissance est la dérivée du travail. 

$$\begin{align}
\frac{dW}{dt} & = \frac{dq}{dt}\cdot \Delta V \\ \\
& = i\Delta V
\end{align}$$

La puissance dissipée vaut $i^2R$ ou $\frac{\Delta V^2}{R}$

On appelle ça l'effet Joules -> chaleur. *Recherche à faire*


