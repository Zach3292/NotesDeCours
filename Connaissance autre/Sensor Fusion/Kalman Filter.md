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
### Filtre $\alpha- \beta - \gamma$
#### Première équation du filtre Kalman
Estimation de l'état présent = La valeur prédit de l'état + un facteur fois (la mesure - la prédiction de l'état)

Le facteur est représenté par $K_n$ et s'appelle le gain Kalman.

On arrive à cette fonction appelé la fonction de changement d'état:$$\hat{\phi}_{n,n}=\hat{\phi}_{n, n-1} + \alpha\cdot \left[z_n+\hat{\phi}_{n, n-1}\right]$$
La différence entre la mesure et l'état prédit s'appelle *l'innovation*.

Le processus d'estimation avec ce filtre peut être représenté par 
### Filtre Kalman étendu