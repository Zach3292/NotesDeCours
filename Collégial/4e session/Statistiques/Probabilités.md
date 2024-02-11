### Définition
Valeur entre 0 et 1
Probabilité de a:$$P(a)$$
Probabilité de tout sauf a:$$P'(a)$$
$$P(a) = 1 - P'(a)$$
Les probabilités peuvent être représenté en diagramme de Venn lorsque qu'elles sont mutuellement exclusives ou en diagramme en arbre lorsqu'elles sont séquentielles

### Calculs
Lorsque qu'on parle de la probabilité de quelque chose **ou** quelque chose d'autre, on calcule une somme *souvent utile avec des probabilités mutuellement exclusives*$$P(a)+P(b)-P(a \; et \; b) = P(a \; ou \; b)$$
Lorsqu'on parle de probabilité de quelque chose **et** quelque chose d'autre, on calcule un produit *souvent utile avec des probabilités séquentielles* $$P(a)*P(b) = P(a \; et \; b)$$
### Dénombrement

Il y a quatre types de dénombrement:
1. Celui pas de nom:
	Le nombre de possibilité est égale au produit des embranchements dans le diagrammes en arbres
2. Arrangement:
	Calcul factoriel selon le nombres de possibilités pour avoir tous les arrangements différents *page 82*
3. Permutations:
	Sous-groupe donc l'ordre est important. Exemple: pigé les positions au jeu du trou de cul$$ P^n_k = \frac{n!}{(n-k)!}$$
		n: nombre de personne total
		k: nombre de personne dans le sous-groupe
4. Combinaisons:
	Sous-groupe donc l'ordre n'est pas important$$ C^n_k = \frac{n!}{k!(n-k)!}$$
### Théorème de Bays
Il s'agit en quelque sorte d'un calcul à l'envers
P(A|B) est égale à la probabilité qu'on est A si on a B$$ P(A|B) = \frac{P(B|A)*P(A)}{\sum_{i=1}^{k} P(B|A_i)*P(A_i)}$$
*Exemple, Yves et Jean font des mitaines selon différentes proportions, chacun font des rouges et des bleues selon différentes proportions. Si on choisi une mitaine bleue, quelles sont les probabilités qu'elle est été faite par Yves. Ici le créateur est représenté par A et la couleur est représentée B*


