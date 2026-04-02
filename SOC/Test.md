Notre architecture est désormais en place, avec l’ensemble des outils correctement configurés et intégrés. Afin d’évaluer l’efficacité de la solution mise en oeuvre, nous avons procédé à une série de tests visant à vérifier la détection, la remontée et le traitement des événements de sécurité dans divers scénarios.

* Scénario de test 1 : Attaque par force brute
  
Pour simuler une attaque par force brute, la machine PC1 a été temporairement remplacée par une machine Kali Linux. Celle-ci a permis de réaliser des tests de pénétration ciblés dans un environnement contrôlé, en respectant la segmentation réseau de la maquette. La figure suivante illustre l’intégration de Kali Linux au sein de notre architecture réseau.

Figure 1 : [Intégration de la machine Kali Linux dans la maquette](../images/Test/Intégration%20de%20la%20machine%20Kali%20Linux%20dans%20la%20maquette.jpg)

Après l’intégration de la machine Kali Linux en tant que poste d’attaque au sein du VLAN 10, nous avons procédé à une simulation d’attaque par force brute ciblant le serveur Ubuntu placé dans le VLAN 77. Pour ce test, l’outil Hydra a été utilisé afin de tenter des connexions SSH en s’appuyant sur deux dictionnaires : l’un contenant une liste d’identifiants users.txt et l’autre une série de mots de passe passwords.txt, comme le montre la figure suivante.

Figure 2 : [Attaque par force brute](../images/Test/Attaque%20par%20force%20brute.png)
