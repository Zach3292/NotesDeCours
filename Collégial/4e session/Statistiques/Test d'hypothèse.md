---
id: Test d'hypothèse
aliases: []
tags: []
---

Inférence: alternative aux intervalles de confiance

Étape 1 : On forme deux hypothèses
$h_0$: hypothèse nulle
$h_1$: hypothèse alternative
Étape 2 : On trace un graphique de loi normale avec $h_0$
On regarde si $h_1$ est dans la zone de rejet ou non

```r
x<-c(88,94,96,101,88,95,99,91,92,98)
mu<-90
alpha<-0.01
t.test(x,mu=mu,alternative="greater",conf.level = 1-alpha)
```

### Valeur P
Plus petite valeur de $\alpha$ qui mène au rejet de $h_0$
Mettre h dans la loi normale
Lors d'un test bilatéral, on multiplie par 2

Si n>30 on utilise la loi normale, sinon on prend la loi de Student

### Test sur des proportions

```r
prop.test(102, 1120, p=0.15, alternative = "less", correct = FALSE, conf.level = 0.99)

prop.test(c(673,966),c(1232,3012),correct=FALSE, conf.level=0.99, alternative = "greater")
```

### Test sur des moyennes indépendantes

```r
x<-c(715,819,1543,201,299,767,491,905,477,583)
y<-c(212,985,1871,321,91,421,683,140,369)
t.test(x,y,conf.level = 0.95)

x<-c(126,156,176,87,135,162,132,120)
y<-c(114,112,160,99,129,165,100,88)
t.test(y,x,conf.level = 0.9, alternative = "less", paired =TRUE)
```

