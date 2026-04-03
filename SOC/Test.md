Notre architecture est désormais en place, avec l’ensemble des outils correctement configurés et intégrés. Afin d’évaluer l’efficacité de la solution mise en oeuvre, nous avons procédé à une série de tests visant à vérifier la détection, la remontée et le traitement des événements de sécurité dans divers scénarios.

* Scénario de test 1 : Attaque par force brute
  
Pour simuler une attaque par force brute, la machine PC1 a été temporairement remplacée par une machine Kali Linux. Celle-ci a permis de réaliser des tests de pénétration ciblés dans un environnement contrôlé, en respectant la segmentation réseau de la maquette. La figure suivante illustre l’intégration de Kali Linux au sein de notre architecture réseau.

Figure 1 : [Intégration de la machine Kali Linux dans la maquette](../images/Test/Intégration%20de%20la%20machine%20Kali%20Linux%20dans%20la%20maquette.jpg)

Après l’intégration de la machine Kali Linux en tant que poste d’attaque au sein du VLAN 10, nous avons procédé à une simulation d’attaque par force brute ciblant le serveur Ubuntu placé dans le VLAN 77. Pour ce test, l’outil Hydra a été utilisé afin de tenter des connexions SSH en s’appuyant sur deux dictionnaires : l’un contenant une liste d’identifiants users.txt et l’autre une série de mots de passe passwords.txt, comme le montre la figure suivante.

Figure 2 : [Attaque par force brute](../images/Test/Attaque%20par%20force%20brute.png)

Suite au lancement réussi de l’attaque par force brute, une alerte a été immédiatement générée et reçue sur la plateforme Wazuh. Cette alerte détaille notamment l’adresse IP de la machine cible ainsi que celle de la machine attaquante, ainsi que le port réseau exploité lors de l’attaque, comme l’illustre la figure suivante.

Figure 3 : [Attaque par force brute](../images/Test/Alerte%20d’attaque%20sur%20Wazuh.png)

Dès la détection de l’alerte par Wazuh, une alerte correspondante a été automatiquement créée dans TheHive, comme indiqué dans la figure suivante.

Figure 4 : [Alerte de l’attaque par force brute créée](../images/Test/Alerte%20de%20l’attaque%20par%20force%20brute%20créée.jpg)

Une fois l’alerte transmise à TheHive, nous l’avons ouverte afin d’en analyser les éléments
contextuels.

La figure suivante illustre les informations générales associées à cette attaque telles qu’affichées dans l’interface de TheHive.

Figure 5 : [Aperçu de l’alerte de force brute](../images/Test/Aperçu%20de%20l’alerte%20de%20force%20brute.png)

Le cas comporte l’observable créé, où les résultats des analyseurs de Cortex sont accessibles, comme représenté dans la figure suivante.

Figure 6 : [Observables de l’attaque par force brute](../images/Test/Observables%20de%20l’attaque%20par%20force%20brute.jpg)

L’analyseur Cortex a traité l’artefact et généré un rapport d’analyse, dont les résultats sont présentés dans les figures suivantes.

Figure 7 : [Rapport sur Cortex](../images/Test/Rapport%20sur%20Cortex.jpg)

Figure 8 : [Rapport sur TheHive](../images/Test/Rapport%20sur%20TheHive.jpg)

* Scénario de test 2 : Fichier malveillant

Dans ce scénario, un fichier malveillant de type Trojan a été téléchargé sur la machine Ubuntu
Server afin de tester l’efficacité de la solution mise en place. Ce test avait pour but de vérifier la capacité
du système à détecter une menace réelle et à générer les alertes nécessaires pour initier une réponse
appropriée.
Pour initier ce scénario de test, nous avons téléchargé le fichier malveillant au niveau machine Ubuntu Server de notre réseau de test, comme le montre la figure suivante.

Figure 9 : [Téléchargement de fichier malveillant](../images/Test/Téléchargement%20de%20fichier%20malveillant.jpg)

Une alerte a été immédiatement générée par Wazuh dans la section File Integrity Monitoring, signalant une modification non autorisée du système de fichiers.
Cette alerte indiquait l’ajout d’un fichier malveillant de type Trojan sur la machine Ubuntu ciblée, comme le montre la figure suivante.

Figure 10 : [Détection du fichier malveillant via Wazuh](../images/Test/Détection%20du%20fichier%20malveillant%20via%20Wazuh.jpg)

Cette figure présente une vue détaillée de l’alerte émise par Wazuh, mettant en évidence les informations critiques relatives à l’ajout du fichier malveillant détecté sur la machine.

Figure 11 : [Rapport d’alerte Wazuh](../images/Test/Rapport%20d’alerte%20Wazuh.jpg)

Suite à la détection de l’alerte par Wazuh, une alerte liée au fichier malveillant détecté a été automatiquement générée dans TheHive, comme présenté dans la figure suivante.

Figure 12 : [Déclenchement d’une alerte dans TheHive](../images/Test/Déclenchement%20d’une%20alerte%20dans%20TheHive.jpg) 

Dès la réception de l’alerte dans TheHive, nous avons procédé à son ouverture pour examiner en détail les informations contextuelles, comme le montre la figure suivante.

Figure 13 : [Vue détaillée de l’alerte dans TheHive](../images/Test/Vue%20détaillée%20de%20l’alerte%20dans%20TheHive.jpg) 

L’analyse de l’artefact par Cortex a abouti à la génération d’un rapport détaillé, dont les résultats sont illustrés dans les figures suivantes.

Figure 14 : [Rapport d’analyse Cortex](../images/Test/Rapport%20d’analyse%20Cortex.jpg) 


Figure 15 : [Suite de rapport d’analyse Cortex](../images/Test/Suite%20de%20rapport%20d’analyse%20Cortex.jpg) 


