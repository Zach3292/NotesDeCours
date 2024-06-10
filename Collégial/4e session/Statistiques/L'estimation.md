---
id: L'estimation
aliases: []
tags: []
---

Probabilité: population connue
Statistiques: population inconnue

On veut passer d'un échantillon à un epopulation à l'aide de l'Estimation

Si on a $S$ qui est l'écart type de la population réelle ou estimée et $n$ le nombre d'échantillon. Il est possible de trouver $\sigma$ qui est l'écart type des échanitllons:
$$\sigma = \frac{S}{\sqrt{n}}$$

### Théorème central limite
Si $n>30$ alors peu importe la distribution de la population, la distributions des échantillons sera normale. Les paquets de 30 et plus suivent la distribtuion normale.

### Intervalles de confiance

Signifier par un seuil de confiance

#### Population normale et écart type connu:

$$E=\frac{S}{\sqrt{n}}Z\left(\frac{\alpha}{2}\right)$$

#### Population normale avec $n<30$
Loi de student
Degrées de liberté: $n-1$

$$E=\frac{S}{\sqrt{n}}T\left(\frac{\alpha}{2}\right)$$

```r
x<-c(420,380,560,670,500,888,705,470)
t.test(x,conf.level=0.95)
```

#### Population quelconque avec $n>30$

$$E=\frac{S}{\sqrt{n}}Z\left(\frac{\alpha}{2}\right)$$

### Proportion

$$\sigma = \sqrt{\frac{pq}{n}}$$

$$E=\sigma Z\left(\frac{\alpha}{2}\right)$$

Tois conditions à respecter:
1. $n>=30$
2. $np >= 5$
3. $nq >= 5$

```r
conditionChecker<-function(n,p){
  if(n >= 30 & n*p>=5 & n*(1-p)>=5){
    print("Check passed")
  } else{
    print("Check failed")
  }
}
conditionChecker(n,p)

p<-1190
n<-2000
binom.test(p,n,conf.level=0.90)
```

### Déterminer la taille d'un échantillon si E est connu

```r
n0<-50
s<-2.4
e<-0.5
alpha<-0.1

n<-(e/(qnorm(alpha/2)*s))^(-2)
print(n)
print(n-n0)
```

