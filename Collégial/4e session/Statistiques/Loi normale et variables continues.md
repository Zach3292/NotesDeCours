L'intégrale des fonctions de densité donne la probabilité. Si on les intègre de l'infini à moins l'infini, ça va toujours donner 1. 

### La loi normale:

#### Centrée réduite (lorsque $\mu = 0$ et $\sigma = 1$):
$$f(x) = \frac{1}{\sqrt{2\pi}} e^{\frac{-z^2}{2}}$$

#### Forme générale:
$$f(x) = \frac{1}{\sqrt{2\pi\sigma^2}} e^{\frac{-(x-\mu)^2}{2\sigma^2}}$$

Un loi normale est toujours cumulative

Pour transformer en loi centrée réduite:
$$\frac{x-\mu}{\sigma} = z$$

Dans R: 
```r
pnorm(x) # Centrée réduite
pnorm(x,mean=0,sd=0) # Forme générale
```
#### Inverse
Permet de trouver quelle x pour être dans un certain intervalle de probabilité.
Dans R: 
```r
qnorm(prob,mean=0,sd=0)
```
#### Tester la normalité
1. Graphique: histogramme
2. Calcul discret:
$$1 \lt \frac{Q_3-Q_1}{\sigma} \lt 1.6$$
3. Papier loi normale

Dans R:
```r
hist(data)
R<-function(n)((quantile(n, 0.75)-quantile(n,0.25))/sd(n))
#Définir fonction R qui doit être entre 1 et 1.6 pour normalité
R(data) #Devrait être entre 1 et 1.6
qqnorm(data)
abline(mean(data),sd(data)) 
qqline(data)
```
