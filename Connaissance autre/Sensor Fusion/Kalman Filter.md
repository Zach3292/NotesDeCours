### Connaissance de base préalable
#### État caché
Un *état caché* représente l'état réel du système qu'on ne peut pas mesurer avec des capteurs. Par exemple, si on calcule la masse d'une personne avec une balance, on obtient plusieurs résultats différent à cause de l'imprécision de la balance. *L'état caché* du système est la masse réelle de la personne. Dans cette exemple, la personne est le *système* et la masse est *l'état du système*.
#### Variance et écart type
La variance représente les écarts entre une différente population et l'écart type représente la racine carré de la variance. L'écart type se note $\sigma$ et la variance $\sigma^2$. On peut estimer la variance sans connaitre la population au complet à l'aide d'un échantillonnage et du [Théorème central limite](../../Collégial/4e%20session/Statistiques/L'estimation.md#Théorème%20central%20limite). Si on calcule la variance d'un échantillon, on ne divise par par le nombre de personne dans l'échantillon mais par le nombre de personne moins un à cause de la [Correction de Bessel](https://en.wikipedia.org/wiki/Bessel%27s_correction).
#### La distribution normale
Encore une fois, la plupart des phénomènes naturels peuvent être représenté par une distribution normal selon le [Théorème central limite](../../Collégial/4e%20session/Statistiques/L'estimation.md#Théorème%20central%20limite). Cette loi normale aura la forme [suivante](../../Collégial/4e%20session/Statistiques/Loi%20normale%20et%20variables%20continues.md#Forme%20générale).

#### Variable aléatoire
L'état caché du système est une *variable aléatoire*, celle-ci est décrit par un fonction de densité de probabilité.
#### Estimation, précision et exactitude
Une *estimation* essaye d'évalue l'état caché du système. La *précision* est lorsque nos estimés n'ont pas un grande incertitude. L'*exactitude* est lorsque nos estimés sont proches de la valeur réelle. Un système avec une basse exactitude est dit *biaisé*.
### Filtre $\alpha- \beta - \gamma$ à une dimension
#### Première équation du filtre Kalman
Estimation de l'état présent = La valeur prédit de l'état + un facteur fois (la mesure - la prédiction de l'état)

Le facteur est représenté par $K_n$ et s'appelle le gain Kalman.

On arrive à cette fonction appelé la fonction de changement d'état:$$\hat{\phi}_{n,n}=\hat{\phi}_{n, n-1} + \alpha\cdot \left[z_n+\hat{\phi}_{n, n-1}\right]$$
La différence entre la mesure et l'état prédit s'appelle *l'innovation*.

Le processus d'estimation avec ce filtre peut être représenté par [ce canvas](Procédé%20d'estimation.canvas).
#### Deuxième équation du filtre de Kalman

Lorsque le système n'est pas dans un état statique, il faut pouvoir représenter les lois dynamiques qui le régissent. Avec ces équations, il est possible de prédire le prochaine état du système s'il n'y aurait pas de changement à son comportement. Ce système d'équation représente les deuxièmes équations du filtre Kalman et s'appelle *les équations d'extrapolation de l'état* ou *équations de transition* ou encore *équations de prédiction*.

Les équations de transition dépendent du système et change dépendant du problème. Il existe une forme matricielle générale **qui sera vu plus tard**

#### Calcul du gain de Kalman
Le gain de Kalman est un calcul conceptuellement simple: $$K_n=\frac{\Delta\hat{\phi}_{n,n}}{\Delta\hat{\phi}_{n,n}+\Delta z_n}$$
Où $\Delta$ représente l'incertitude ou l'erreur sur la mesure.

L'erreur sur l'estimation peut être calculé de la manière suivante: $$\Delta\hat{\phi}_{n,n}=(1-K_n)\Delta\hat{\phi}_{n,n-1}$$ 
Dans un filtre Kalman, il faut connaitre ou assumer toutes les variables initiales.

### FIltre Kalman multidimensionnelle
#### La matrice d'état
Elle représente l'état actuelle du système, souvent en coordonnées et en vitesse. Elle est souvent représenté comme suit: $$X = 
\begin{bmatrix} 
x \\
y \\
z \\
\dot{x} \\
\dot{y} \\
\dot{z} \\
\end{bmatrix}$$
#### La prédiction de l'état
Pour prédire l'état du système $x_k$, le filtre Kalman utilise un équation: $$x_k=Ax_{k-1}+Bu_k+w_k$$
Où A et B sont des matrices déterminées à partir de la dynamique du système, $u_k$ est ;a matrice variable de contrôle
### Filtre Kalman étendu