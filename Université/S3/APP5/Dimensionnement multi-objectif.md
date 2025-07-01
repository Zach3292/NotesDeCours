### Élaboration du cahier des charges
En général, il faut inclure les éléments suivants:
- Tension
- Volume
- Poids
- Coût
- Énergie
- Puissance
- Température
- Durée de vie

Pour chaque élément, dire la valeur minimale ou maximale ainsi que les unités. 

#### Hypothèses de conception
Les hypothèses de conception servent à simplifier le choix de conception. Elles sont à faire au choix selon les priorités du système. 

On peut par exemple supposer que la tension des cellules est parfaitement balancé.

### Calcul des spécifications de conception
#### Estimation du volume
Selon le nombre de cellule, on peut faire une approximation rapide du volume de la batterie.
$$V_{sae}=n_sn_pl(D+2e)^2$$
Où
- $n_s$: nombre de cellule en série
- $n_p$: nombre de cellule en parallèle
- $l$: longueur d'une cellule
- $D$: diamètre d'une cellule
- $e$: épaisseur de la paroi des cellules

On peut réécrire l'équation:
$$n_s\leq\frac{V_{sae}{n_p$$
#### Estimation de la masse
$$m_{sae}=n_sn_p(m_{cell}+m_{pcm})$$
Où
- $m_{cell}$: Masse d'une cellule
- $m_{pcm}$: Masse du système de refroidissement