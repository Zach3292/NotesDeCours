Une interruption est un mécanisme où une appareil signal au processeur qu'il est prêt à transmettre de l'information. Lorsque le processeur reçoit une demande d'interruption, il arrête l'exécution du programme principal pour exécuter la fonction associé à l'interruption. Il existe plusieurs sources d'interruption matériel, ils peuvent venir de l'intérieur du processeur ou d'un appareil externe. 
### Mécanisme d'interruption
Lorsque le processeur reçoit une demande d'interruption, il fait les étapes suivantes:
1. Interrompre le processeur
2. Arrêter l'exécution de la tâche ou fil actuel
3. Exécution du code relier à l'interruption
4. Retour à l'exécution normal des tâches sur le fil

Il existe plusieurs manières d'interrompre le processeur. Il peut y avoir une source pour toutes les appareils ou une source par appareil. Le premier coûte moins cher en matériel mais il est plus dur de déterminer qui à interrompu le processeur.