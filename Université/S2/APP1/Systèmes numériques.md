### Signaux analogiques et numériques
**Un signal analogique** représente de l'information continue avec un nombre infini de valeurs possibles à l'intérieur d'une plage. Un signal numériques sont à la fois **discrétisés**, ils ont un nombre fini de valeurs possible, et **échantillonnés** à une certaine fréquence.

### Conversion analogique à numérique
Un convertisseur analogique à numérique *ADC* traduit le signal analogique en signal numérique selon un certain **niveaux de quantification** *N*. Ce niveau est exprimé en bit. Un bit comporte deux états, 0 ou 1. On peut en utilisé plusieurs pour enregistrer plus d'information. Il est donc possible d'avoir une meilleur **résolution**. Voir [la quantification](../../../Collégial/4e%20session/Calcul%203/Note%20de%20cours.md#Quantification) pour plus de détail sur la discrétisation. Le **pas de discrétisation** peut aussi se calculer ainsi lors d'un petit niveau de quantification: $$\Delta V=\frac{V_{max}-V_{min}}{N-1}$$
Lors de la conversion, il y a aussi un [échantillonnage](../../../Collégial/4e%20session/Calcul%203/Note%20de%20cours.md#Échantillonnage) puisqu'on ne peut pas enregistrer un nombre infinie de donné par unité de temps.

### Systèmes numériques combinatoires et séquentiels

Les systèmes numériques peuvent être classé en deux grandes catégories: **les systèmes combinatoires** qui ne dépendent que de l'information actuelle et **les systèmes séquentiels** qui dépendent de l'information actuelle mais aussi de l'information passée enregistrée en mémoire. 

**Les mathématiques discrètes** définissent les règles de logique des systèmes numériques.

### Systèmes séquentiels synchrones et asynchrones
**Les systèmes synchrones** sont des systèmes où il y a une horloge, la mémoire est mise à jour à chaque signaux d'horloge. **Les systèmes asynchrones** ne disposent pas d'horloge et la mémoire est mise à jour dès qu'il y a de la nouvelle information.