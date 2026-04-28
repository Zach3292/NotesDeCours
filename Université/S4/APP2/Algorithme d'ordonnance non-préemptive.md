Il existe plusieurs manières d'ordonner des tâches de manière non-prédictive et on peut les regrouper en cinq grandes catégories. Pour chaque catégorie, dès que du temps de processeur est libre, une tâche sera exécutée jusqu'à complétion.

### Ordonnance en ligne du temps (timeline scheduling)
Pour $n$ tâches, il existe $n!$ manières différentes de les ordonner. Le *Timeline scheduling* consiste à avoir un humain trier les tâches et décider l'ordre d'exécution. Il est facile de comprendre pourquoi cette méthode n'est pas réalisable dans un vrai scénario.

### Premier arrivé, premier servi
Le fonctionnement de cette méthode est très bein résumé dans son nom. Les tâches sont exécutées dans l'ordre qu'elles arrivent dans la liste d'attente. Il s'agit d'un algorithme dit *juste*. Dans un système en temps réel, la première tâche n'est pas nécessairement celle qui doit s'exécuter en priorité, c'est pourquoi cette méthode ne fonctionne pas en temps réel.
### Tâche la plus court en premier (shortest job next)
Cette méthode aussi est assez simple à comprendre. En exécutant toujours la tâche la plus courte, on minimise le temps d'attente moyen de chaque tâche. Il s'agit aussi d'un algorithme dit *juste*, puisqu'il bénéficie toutes les tâches de la liste. Cette méthode peut être bonne pour un système standard mais, en temps réel, elle n'empêche pas certaines tâches de dépasser leur limite de temps. Cette méthode est donc inapplicable en temps réel.

### Date limite la plus proche
Cette méthode consiste à exécuter la tâche qui a la date limite la plus proche. S'il existe une manière d'exécuter toutes les tâches en respectant leur date limite, cette méthode va permettre d'y arriver.

### Moins de temps libre
Cette méthode consiste à exécuter les tâches qui ont le moins de temps libre avant de devoir commencer leur exécution pour ne pas manquer leur date limite. Elle ressemble beaucoup à la méthode précédente. Comme elle, s'il existe une manière d'exécuter toutes les tâches sans dépasser leur date limite, cette méthode va la trouver.