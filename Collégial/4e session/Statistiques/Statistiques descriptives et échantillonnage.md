Les graphiques ou les nombres permettent de résumer ou de tirer l'important d'un ensemble de données

### Graphiques
#### Données catégoriques ou discrètes
1. Arborescent
2. À bande
3. Sectoriel

Dans R: 
```r
stem(data) # Arborescent
ggplot(data, aes(x=continent, y=gdpPercap, fill=continent)) +
  geom_col() +
  labs(x="Continents", y="PIB", title = "PIB en fonction du continent")+
  theme(axis.text.x = element_blank())
  
```
#### Données continues
1. Histogramme
2. Polygone de fréquence
3. Nuage de point

Dans R:
```r
ggplot(data, aes(x = pop)) +
  geom_histogram(binwidth=0.25, color="black", fill="dodgerblue")  + 
  labs(x="Population", y="",title="Histogramme 2002", subtitle="Zach et LP")+
  scale_x_log10()
ggplot(data, aes(x = pop, y = lifeExp, color = continent, size=gdpPercap)) +
  geom_point() +
  scale_x_log10() 

#A histogramme triché
data <- data.frame(
  probDiabete=c(loiBinomiale(0.35, 11, 0:11)),
  nbDiabete=c(0:11)
)
ggplot(data, aes(x = nbDiabete, y = probDiabete)) +
  geom_bar(stat="identity",color="black", fill="dodgerblue")  + 
  labs(x="label x", y="label y",title="title")

```
### Nombres
#### Tendance centrale
1. Moyenne (µ pour population, x avec une barre au dessus pour un échantillon) *aussi appelé espérance*
2. Médiane: valeur du milieu
3. Mode: valeur qui revient le plus souvent

Dans R:
```r
mean(x)
median(x)
mode(x)
```
#### Mesures de position
1. Quartiles (q1, q2, q3) q2 est aussi la médiane
2. Centiles
Dans R:
```r
quantile(data, 1:10/10) # Déciles
quantile(data, 1:4/4) # Quartiles
```
#### Mesures de dispersion
1. Écart-type (sigma minuscule pour une population et s pour échantillon)
2. Variance: écart-type au carré
3. Étendue: valeur max-valeur min
4. Coefficient de variation: écart-type sur moyenne multiplié par 100

Dans R:
```r
sd(data) # Écart type
var(data) # Variance
summary(data) # Amalgame de données
ggplot(data, aes(x=continent, y = lifeExp, )) + # Graphique boites et moustaches
  geom_boxplot() +
  ggtitle("Espérance de vie en fonction du continent en 2007") +
  labs(y="Espérence de vie", x = "Continent")
```
### Échantillonnage
Meilleur approche: aléatoire simple
Sinon: 
1. Aléatoire en grappe (endroit)
2. Aléatoire en strates (ex: 10 par programmes)
3. Aléatoire systématique (à chaque 12 j'en prend un)
Manière non-aléatoire:
1. Pratique: premier disponible
2. Volontariat