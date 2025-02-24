### Définition
Un vecteur propre est un vecteur qui demeure sur la même axe lors d'une transformation linéaire ou d'une rotation. Il peut être réel ou imaginaire. La valeur propre est le scalaire qui multiplie ce vecteur lors de la transformation. Il peut y avoir plusieurs vecteurs propres et valeurs propres pour une matrice de transformation.

Excellente vidéo pour la visualisation: [3Blue1Brown](https://youtu.be/PFDu9oVAE-g?si=GLm007SeqbhfFnW5).
### Application à la rotation
Le vecteur propre d'une matrice de rotation est l'axe de rotation et la valeur propre est 1.

### Calcul des vecteurs propres
$$A\vec{v}=\lambda\vec{v}$$
Où
$A$ est la matrice de transformation, $\vec{v}$ sont les vecteurs propres et $\lambda$ la valeur propre correspondante. On peut réduire l'équation précédente à celle-ci pour simplifier le calcul:
$$(A-\lambda I)\vec{v}=\vec{0}$$
Par contre, on veut un vecteur non nul comme réponse et la seule manière est que:
$$\mathrm{det}(A-\lambda I)=0$$
On trouve ainsi la ou les valeur propre qu'on peut utiliser pour calculer le vecteur propre.