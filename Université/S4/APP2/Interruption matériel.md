Une interruption est un mécanisme où un appareil signal au processeur qu'il est prêt à transmettre de l'information. Lorsque le processeur reçoit une demande d'interruption, il arrête l'exécution du programme principal pour exécuter la fonction associée à l'interruption. Il existe plusieurs sources d'interruptions matériel, elles peuvent venir de l'intérieur du processeur ou d'un appareil externe. 
### Mécanisme d'interruption
Lorsque le processeur reçoit une demande d'interruption, il fait les étapes suivantes:
1. Interrompre le processeur
2. Arrêter l'exécution de la tâche ou fil actuel
3. Exécution du code relié à l'interruption
4. Retour à l'exécution normale des tâches sur le fil

Il existe plusieurs manières d'interrompre le processeur. Il peut y avoir une source pour tous les appareils ou une source par appareil. Le premier coûte moins cher en matériel, mais il est plus difficile de déterminer la source de l'interruption.

### Caractéristiques des routines d'interruption (ISR)
Voici quelques caractéristiques important pour une *ISR*:
- Permet au système de rapidement retourner à l'exécution normale
- Minimise la possibilité qu'une autre interruption arrive en même temps
- Réduit la probabilité d'un bug de programmation pendant son exécution

### Ignorer des interruptions et interruptions imbriqués
Dans un système en temps réel, rien n'empêche à une interruption d'arriver pendant une autre. Parfois, cette deuxième interruption est plus importante que la première. Il existe deux types d'interruptions:
1. Requête d'interruption
2. Interruption non-masquable

La deuxième ne peut jamais être ignorée, elles nécessitent une réponse immédiate et ne peuvent pas être désactivées non plus.

### Fonctions ré-entrantes
Une fonction qui, pour un ensemble de paramètres donnés, va toujours retourner le même résultat et ça, peu importe quand elle est exécuté et si elle est interrompu. Une fonction d'interruption devrait toujours être ré-entrante *(bonne pratique)*.