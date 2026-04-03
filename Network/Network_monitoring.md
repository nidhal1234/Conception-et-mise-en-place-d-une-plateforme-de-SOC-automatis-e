Dans cette partie, nous avons intégré l’outil de supervision Zabbix dans notre architecture réseau afin de renforcer la sécurité, la disponibilité et la performance de l’infrastructure. Cette solution permet une surveillance centralisée et en temps réel des équipements, facilitant la détection précoce desanomalies, des pannes ou des comportements suspects. Grâce à Zabbix, nous assurons une visibilitécomplète sur l’état du réseau, ce qui permet une réaction rapide face aux incidents et contribue à la résilience globale du système.

La figure qui suit illustre l’amélioration de notre architecture réseau grâce à l’intégration du serveur Zabbix.

Figure 1 : [Intégration du serveur Zabbix dans l’architecture réseau](../images/network_monitoring/Intégration%20du%20serveur%20Zabbix%20dans%20l’architecture%20réseau.png)

* Supervision des commutateurs

Après la configuration du protocole SNMP sur le commutateur ESW4, afin qu’il puisse envoyer ses traps vers le serveur Zabbix, nous avons vérifié l’état du service afin de s’assurer de son bon fonctionnement.
Cette figur présente l’état actuel de SNMP sur le commutateur, confirmant ainsi la prise en compte des paramètres appliqués.

Figure 2 : [État du protocole SNMP sur le commutateur](../images/network_monitoring/État%20du%20protocole%20SNMP%20sur%20le%20commutateur.png)

Ensuite, nous avons ajouté le commutateur ESW4 au serveur Zabbix afin d’assurer sa supervision.

La figure suivante illustre son intégration dans l’interface de surveillance.

Figure 3 : [Ajout du commutateur au serveur Zabbix](../images/network_monitoring/Ajout%20du%20commutateur%20au%20serveur%20Zabbix.png)


Ces figures illustrent la surveillance effective des commutateurs à partir de l’interface Zabbix, réalisée via le protocole SNMP.

Figure 4 : [Surveillance des commutateurs ESW1, ESW2, ESW3 avec Zabbix](../images/network_monitoring/Surveillance%20des%20commutateurs%20ESW1,%20ESW2,%20ESW3%20avec%20Zabbix.png)

Figure 5 : [Surveillance des commutateurs ESW4, ESW5, ESW6 avec Zabbix](../images/network_monitoring/Surveillance%20des%20commutateurs%20ESW4,%20ESW5,%20ESW6%20avec%20Zabbix.png)

Les figures qui suivent présentent la surveillance du trafic réseau des interfaces du commutateur
ESW4 via Zabbix

Figure 6 : [Surveillance des interfaces Gi0/0 et Gi0/1 de commutateur ESW4 avec Zabbix](../images/network_monitoring/Surveillance%20des%20interfaces%20Gi00%20et%20Gi01%20de%20commutateur%20ESW4%20avec%20Zabbix.png)

Figure 7 : [Surveillance des interfaces Gi0/2 et Gi0/3 de commutateur ESW4 avec Zabbix](../images/network_monitoring/Surveillance%20des%20interfaces%20Gi02%20et%20Gi03%20de%20commutateur%20ESW4%20avec%20Zabbix.png)

* Supervision des Routeurs

À cette étape, le protocole SNMP a été configuré sur le routeur R1 afin de permettre l’envoi de traps vers le serveur Zabbix. L’état du service a ensuite été vérifié pour s’assurer de son bon fonctionnement.

Cette figure illustre l’état actuel de SNMP sur le routeur, confirmant que les paramètres ont bien été appliqués.

Figure 8 : [État du service SNMP sur le routeur](../images/network_monitoring/État%20du%20service%20SNMP%20sur%20le%20routeur.png)

Puis, nous avons ajouté le routeur R1 au serveur Zabbix afin d’assurer sa supervision.

La figure suivante illustre son intégration au sein de l’interface de surveillance, confirmant que routeur est désormais pris en charge pour le monitoring SNMP.

Figure 9 : [Ajout du routeur au serveur Zabbix](../images/network_monitoring/Ajout%20du%20routeur%20au%20serveur%20Zabbix.png)

La figure suivante illustre la surveillance effective des routeurs à partir de l’interface Zabbix, réalisée
via le protocole SNMP.

Figure 10 : [Surveillance des routeurs R1 et R2 avec Zabbix](../images/network_monitoring/Surveillance%20des%20routeurs%20R1%20et%20R2%20avec%20Zabbix.png)

* Supervision des pare-feux
  
Les pare-feux pfSense ont été configurés pour la supervision via SNMP avec Zabbix, permettant la collecte en temps réel des métriques (interfaces, ressources, trafic) et l’envoi de traps SNMP pour détecter les événements critiques. Les deux figures suivantes montrent la configuration des pare-feux pfSense1 et pfSense2.

Figure 11 : [Configuration SNMP de pfSense1](../images/network_monitoring/Configuration%20SNMP%20de%20pfSense1.png)

Figure 12 : [Configuration SNMP de pfSense2](../images/network_monitoring/Configuration%20SNMP%20de%20pfSense2.png)

Nous avons désormais ajouté les deux pare-feux, pfSense1 et pfSense2, au serveur Zabbix afin d’assurer leur supervision.

Ces figures illustrent cette intégration au sein de l’interface de surveillance.


Figure 13 : [Ajout du pfSense1 au serveur Zabbix](../images/network_monitoring/Ajout%20du%20pfSense1%20au%20serveur%20Zabbix.png)

Figure 14 : [Ajout du pfSense2 au serveur Zabbix](../images/network_monitoring/Ajout%20du%20pfSense2%20au%20serveur%20Zabbix.png)

La figure suivante illustre avec succès l’état de la surveillance, confirmant la réception et l’analyse des traps SNMP émis par les dispositifs pfSense.

Figure 15 : [Surveillance des pare-feux avec Zabbix](../images/network_monitoring/Surveillance%20des%20pare-feux%20avec%20Zabbix.png)

* Supervision des machines virtuelles

Dans cette étape, nous avons procédé à la configuration avancée de la supervision des machines virtuelles Ubuntu Server et Windows 10 en déployant et intégrant l’agent Zabbix sur chaque hôte. Cette configuration permet la remontée granulaire d’indicateurs clés tels que l’utilisation des ressources système (CPU, mémoire, disque), l’état des processus critiques ainsi que la disponibilité des services.

Après l’installation de l’agent Zabbix sur la machine Ubuntu Server, nous avons vérifié son état de fonctionnement afin de nous assurer qu’il est actif et opérationnel.
Cette figure présente le statut du service Zabbix Agent sur le système.

Figure 16 : [État de l’agent Zabbix sur Ubuntu Server](../images/network_monitoring/État%20de%20l’agent%20Zabbix%20sur%20Ubuntu%20Server.png)

La figure suivante illustre l’intégration de l’agent Zabbix avec le serveur Zabbix, confirmant ainsi l’établissement d’une communication entre les deux.

Figure 17 : [Intégration de l’agent Zabbix avec le serveur](../images/network_monitoring/Intégration%20de%20l’agent%20Zabbix%20avec%20le%20serveur.png)

Ensuite, nous avons ajouté la machine virtuelle Ubuntu Server au serveur Zabbix afin d’assurer sa supervision, comme le montre la figure suivante.

Figure 18 : [Ajout de Vm Ubuntu au serveur Zabbix](../images/network_monitoring/Ajout%20de%20Vm%20Ubuntu%20au%20serveur%20Zabbix.png)

Le résultat de la supervision réalisée via Zabbix met en évidence l’évolution de l’utilisation de l’espace disque sur la machine virtuelle Ubuntu Server, offrant un suivi précis de la consommation des ressources de stockage et facilitant l’anticipation des besoins futurs, comme le montre la figure qui suit.


Figure 8 : [Supervision du serveur Ubuntu](../images/network_monitoring/Monitoring%20du%20Serveur%20Ubuntu.png)

Cette figure illustre le résultat de la supervision réalisée via Zabbix sur la machine virtuelle Windows 10.

Figure 9 : [Supervision du système Windows 10](../images/network_monitoring/Monitoring%20du%20système%20Windows%2010.png)


