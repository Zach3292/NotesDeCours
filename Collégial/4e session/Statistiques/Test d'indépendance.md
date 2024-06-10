---
id: Test d'indépendance
aliases: []
tags: []
---

Lorsqu'on a deux variables et qu'on veut voir si elles sont indépendantes.

Plusieurs niveaux des deux variables (discrète ou qualitatif)

si $p<\alpha$ alors il y a une dépendance

On fait un test avec R

```r
tableau<-matrix(c(15,9,5,43,55,25,7,19,19),ncol=3,byrow=T)
rownames(tableau)<-c("Collégial","Baccalauréat","Études supérieurs")
colnames(tableau)<-c("2-4 semaines","4-6 semaines","6 semaines et plus")
tableau
chisq.test(tableau,correct=F)

```

Loi normale au carré: loi du chi-carré

Tableau de contingence:

```r
tableaucontingence<-table(ferme$Code1,ferme$Code2)
tableaucontingence

chisq.test(tableaucontingence,correct=F)
```

### Avec des proportions:

```r
donnees<-c(55,40,10,72)
p<-c(0.3,0.25,0.15,0.3)
chisq.test(donnees,p=p)
```

### Test de variance et d'écart type:

```r
x <- c(21.90625,31.29040,32.98142,57.82246,31.65926,29.55542,17.86164,30.16141,51.28263,12.35406,25.09217,33.91287,31.65498,54.91335,31.55975)
require(DescTools)
#A
VarTest(x, alternative = "greater", conf.level = 0.99, 
        sigma.squared = 49) #sigma-squared est la valeur attendue de variance
# dans l'hypoth?se nulle
#B
VarTest(x, alternative = "two.sided", conf.level = 0.99, 
        sigma.squared = 49) #sigma-squared est la valeur attendue de variance
# dans l'hypoth?se nulle
```
