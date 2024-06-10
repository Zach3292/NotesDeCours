---
id: Régression
aliases: []
tags: []
---

Droite de régression d'un ensemble de point
Corrélation entre x et y

```r
pointure<-c(6,8,9,6.5,7,7.5,9.5,8,5,6.5,8.5,7)
taille<-c(152,175,173,160,169,165,181,173,157,164,176,170)
frame<-data.frame(pointure,taille) #transformer en donn?es pour ggplot
require(ggplot2)

ggplot(frame,aes(x=pointure,y=taille))+
  geom_point() +
  labs(x="Pointure",y="Taille")

#B
modele<-lm(taille~pointure)
modele #Pour obtenir l'équation de la régression
cor(pointure,taille)^2 
summary(modele)
```

### Coefficient de corrélation (Pearson)
Évalutaion de la corrélation linéaire: r $\rightarrow$ Test de pearson
* Aucune corrélation: $r=0$
* Corrélation parfaite: $r=1$
* Corrélation parfaite négative: $r=-1$

```r
#C
cor.test(pointure,taille, aternative="two-sided",conf.level=0.95)

#D
frame<-data.frame(pointure=6)
predict(modele, frame, interval="prediction",level=0.95)
```

### Coefficient de détermination $R^2$

Toujours positif
Donne la variabilité expliquée par la relation linéaire diviser par la variabilité totale
Pourcentage

```r
#Graphique nuage de points avec droite de r?gression
#Ici intervalle 95%
ggplot(pelican,aes(x=BPC,y=Épaisseur))+
  geom_point() +
  geom_smooth(method="lm",level=0.95)+
  labs(x="BPC",y="Épaisseur")+
  geom_jitter()

#Ajouter la pr?diction (lignes rouges)
model1 <- lm(Épaisseur ~ BPC, data=pelican)
temp_var <- predict(model1, interval="prediction")
new_df <- cbind(pelican, temp_var)
ggplot(new_df, aes(x=BPC, y=Épaisseur))+
  geom_point() +
  geom_line(aes(y=lwr), color = "red", linetype = "dashed")+
  geom_line(aes(y=upr), color = "red", linetype = "dashed")+
  geom_smooth(method=lm, se=TRUE)+
  geom_jitter()+
  labs(x="BPC",y="Épaisseur")
```
### Test avec plusieurs variables:

```r
#A
recettes<-c(80.2,110.1,50.2,130.6,54.8,30.3,79.4,91,135.4,89.3)  # recettes ou revenu du film (le y)
cout<-c(7.3,12.9,5.2,10.7,3.1,3.5,9.2,9,15.1,10.2) # Coût pour faire le film
promo<-c(6.0,5.8,2.1,8.4,2.9,1.2,3.7,7.6,7.7,4.5) # Coût en promotion
ventesl<-c(5.4,8.8,15.1,12.2,10.6,3.5,9.7,5.9,20.8,7.9) # Ventes du livre associé au film
newdata<-cbind(recettes,cout,promo,ventesl)
pairs(newdata)

#B
modele2<-lm(recettes~cout+promo+ventesl)
newdata<-data.frame(cout=12,promo=4,ventesl=6)
predict(modele2,newdata,interval="pred")
```


