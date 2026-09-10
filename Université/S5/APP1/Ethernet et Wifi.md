## Ethernet
### Couche physique de l'Ethernet classique
L'Ethernet classique est normalisé selon la norme IEEE 802.3. À la base l'Ethernet fin avait une longueur maximale de 185m et pouvant desservir seulement 30 appareils. Il fallait utilisé des répéteurs pour augmenter sa porté. Il s'agissait d'un long bus avec des raccordements pour connecter les ordinateurs dessus. 
### Protocole de sous-couche MAC
Voici un exemple de trame Ethernet classique:
![](Images/Pasted%20image%2020260906085758.png)
Le préambule est toujours 10101010 sauf pour le dernier octet qui est 11 dans la norme IEEE 802.3 pour signifier la start of frame. Il y a deux champs pour les adresses. Il est possible de faire de la diffusion multicast et du broadcast. En mettant un 1 au début de l'adresse de destinataire pour faire une adresse de groupe en multicast ou de mettre tous les bits à 1 pour faire du broadcasting. 

Il peut y avoir des collisions avec l'Ethernet classique. Si deux stations envoient un message en même temps, une d'elle la détecte en premier et envoie un signal de brouillage. Les deux stations attendent donc un tempos aléatoire avant d'essayer d'envoyer le message de nouveau. 

### Ethernet commuté
L'Ethernet classique arrive rapidement à une limite d'appareil de vitesse alors on a inventé l'Ethernet commuté qui est presqu'exclusivement utilisé de nos jours. On ajoute des commutateurs sur la ligne. Chaque appareil est connecté au commutateur au lieu d'être connecté directement au autres par des hubs. Quand un commutateur reçoit une trame, il la transmet seulement sur le cable vers sa destination. Ainsi, les autres appareils ne sont pas conscient de la trame. Ça permet de décongestionner les cables et d'augmenter la vitesse de transmission de l'information. Le commutateur réduit ainsi grandement le risque de collision sur les lignes. Il permet aussi de parler à plusieurs appareils simultanément sans problème. 

## Wifi
### Architecture et pile de protocole de 802.11
Les réseaux Wifi fonctionnent selon deux modes. Le premier est le mode infrastructure où chaque appareil est relié à un point d'accès qui à son tour est relié à un autre réseau. On peut connecter plusieurs point d'accès ensemble pour faire de plus grands réseaux. 

L'autre mode appelé *ad hoc* permet à plusieurs appareils de se parler directement. Il s'agit d'un marginal par rapport au mode infrastructure.

![](Images/Pasted%20image%2020260906092330.png)

