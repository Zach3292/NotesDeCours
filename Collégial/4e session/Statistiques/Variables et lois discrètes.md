Loi de probabilité: aussi appelée fonction de masse
* Donne l'ensemble des probabilités pour tous es évènements possible de l'espace d'échantillonnage

Il existe trois manières de l'obtenir:
1. Expérimentalement, avec des données du problèmes
2. Théoriquement, avec des règles du chapitre 2
3. Avec des règles mathématiques propre à un contexte donné

Espérance: moyenne de $X$: $$E(x) = \sum^n_{k=1}{P(x_k)x_k}$$
Variance de $X$: $$var(x) = E(x^2) - \left( E(x) \right)^2$$
Moyenne, écart type et variance pondéré dans R
```r
weightedMean<-weighted.mean(variable,ponderation)
weightedVar <- sum(ponderation * (variable - weightedMean)^2)
weightedStd <- sqrt(weightedVar)
```

### Exemples:
Si on a une situation de ce genre: 4 boules jaunes, 5 noires et 6 rouges et on en tire 5 boules sans remise.

$$P(u) = \frac{C^n_u \ C^{(T-n)}_{(p-u)}}{C^T_p}$$

Dans R:
```r
#A
nbrdeRouge<-9
nbrTotal<-26
nbrPige<-6

probX<-function(nbrX,X,total,pige){
  (combinaison(nbrX,X) * combinaison(total-nbrX,pige-X)) / 
    combinaison(total,pige)
}
probX(nbrdeRouge,0:6,nbrTotal,nbrPige)
#B
probXCumul<-function(nbrX,X,total,pige){
  temp<-0
  for (x in 0:pige) {
    temp<-sum(probX(nbrX,0:x,total,pige))
    print(temp)
  }
}

probXCumul(nbrdeRouge,0:6,nbrTotal,nbrPige)

```

### Lois mathématiques:

#### Loi uniforme
Toujours la même probabilité pour tous les évènements possible

$$P(x)=\frac{1}{n}$$
$$E(x)=\frac{n+1}{2}$$
$$Var(x)=\frac{n^2-1}{12}$$
Dans R:
```r
espLoiUniforme<-function(n)((n+1)/2)
stdLoiUniforme<-function(n)(sqrt((n^2 -1)/12))
```
#### Loi binomiale
n tirage
2 résultats possibles
On connait les probabilité d'avoir chaque résultat et elle est fixe (suit la règle de Bernoulli)

$$P(x=x)=C^n_k \ p^k \ q^{n-k}$$
k = nombre de succès
q = probabilité d'avoir un échec
p = probabilité d'avoir un succès

Dans R:
```r
loiBinomiale<-function(p, n, k){
  combinaison(n,k)*(p^k)*(1-p)^(n-k)
}

loiBinomialeCumul<-function(p, n, k){
  sum(loiBinomiale(p, n, 0:k))
}
# Fonction déjà dans R:
dbinom(k,n,p) # prob d'avoir k succès exact
pbinom(k,n,p) # prob d'avoir k succès cumulatif
```
#### Loi binomiale négative
On veut calculer la probabilité d'avoir un certain nombre d'échec avant d'avoir un nombre donné de succès
n = nombre d'échec
k = nombre de succès
Dans R:
```r
dnbinom(n,k,p) # Exact
pnbinom(n,k,p) # Cumulatif
```
Nombre d'échec pour avoir une probabilité donné d'avoir au moins un succès dans R:
```r
nbEchecAvantnbSucces<-function(probDefect, wantedPercent){
  i<-0
  while (TRUE) {
    if ((1-dbinom(0, i, 1-probDefect)) > wantedPercent){
      break
    }
    i<-i+1
  }
  print(i)
  
}
```

#### Loi de poisson
Variable discrète liée à un élément continu
On connait la valeur moyenne

Dans R:
```r
dpois(x,e) # exact
ppois(x,e) # cumulatif
```

Moyenne pour avoir une certaine probabilité d'obtenir un résultat dans R:
```r
moyennePourProbdeqqc<-function(qqc, wantedPercent){
  i<-qqc
  while (TRUE) {
    if ((1-ppois(qqc, i)) < wantedPercent){
      break
    }
    i<-i-1
  }
  print(i)
}
```