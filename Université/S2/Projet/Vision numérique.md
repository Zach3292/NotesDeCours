### Application
#### Inspection
- Trouver des défauts sur la surface 
- Vérifier la forme, la couleur, la présence d’un élément 
- Mesurer (souvent avec backlight et lentille télécentrique)
#### Positionnement
- Ajouter un ‘sens’ (vision) à un robot pour du pick and place
#### Tirer, compter
Faire le trie automatique des pièces

### Avantages et défis
#### Avantages
- Cadence d’inspection 
- Répétabilité
- Inspection de pièces
#### Défis
- Adaptation à la variabilité des pièces 
- Définition précise d’une pièce normale VS anormale 
- Procédé d’inspection prévu VS réel
### Étapes
#### Acquisition
Avec une caméra, une lentille et un éclairage. Certaines caméras font du traitement on board et d'autres seulement de l'acquisition

Le type d'éclairage impacte beaucoup:
- grosseur, angle de lumière 
- Position de l’éclairage (caméra VS objet VS éclairage) 
- Réflectivité matériau 
- Ombrage
#### Traitement
Principe de base: *shit in, shit out*

##### Bonnes pratiques
- ‘Ancrage’ sur image 
- Prise images avec caméra puis configuration offline
- Acquisition: faire attention à l’environnement (ex : variation d’éclairage)

##### Utilisation des données
- Définir vos paramètres à mesurer 
- Configurer les limites d’acceptabilité 
- Tester 
- Redéfinir les paramètres au besoin 
- Revalider les limites au besoin