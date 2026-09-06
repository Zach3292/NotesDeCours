### Couche physique de l'Ethernet classique
L'Ethernet classique est normalisé selon la norme IEEE 802.3. À la base l'Ethernet fin avait une longueur maximale de 185m et pouvant desservir seulement 30 appareils. Il fallait utilisé des répéteurs pour augmenter sa porté. Il s'agissait d'un long bus avec des raccordements pour connecter les ordinateurs dessus. 
### Protocole de sous-couche MAC
Voici un exemple de trame Ethernet classique:
![](Images/Pasted%20image%2020260906085758.png)
Le préambule est toujours 10101010 sauf pour le dernier octet qui est 11 dans la norme IEEE 802.3 pour signifier la start of frame. Il y a deux champs pour les adresses. Il est possible de faire de la diffusion multicast et du broadcast. En mettant un 1 au début de l'adresse de destinataire pour faire une adresse de groupe en multicast ou de mettre tous les bits à 1 pour faire du broadcasting. 