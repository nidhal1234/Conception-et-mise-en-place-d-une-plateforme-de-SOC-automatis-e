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


La figure suivante illustre la surveillance effective des routeurs à partir de l’interface Zabbix, réalisée
via le protocole SNMP.

Figure 6 : [Surveillance des routeurs R1 et R2 avec Zabbix](../images/network_monitoring/Surveillance%20des%20routeurs%20R1%20et%20R2%20avec%20Zabbix.png)

Dans cette phase, nous avons mis en oeuvre la configuration nécessaire pour permettre la supervision des pare-feux pfSense au moyen du protocole SNMP. Cette configuration a établi un lien de communication fiable entre ces équipements de sécurité et le serveur Zabbix, permettant la collecte en temps réel d’indicateurs essentiels tels que l’état des interfaces, le niveau d’utilisation des ressources, et les statistiques de trafic.

La figure qui suit illustre avec succès l’état de la surveillance, confirmant la réception et l’analyse
des traps SNMP émis par les dispositifs pfSense.

Figure 7 : [Surveillance des pare-feux avec Zabbix](../images/network_monitoring/Surveillance%20des%20pare-feux%20avec%20Zabbix.png)


Dans cette étape, nous avons procédé à la configuration avancée de la supervision des machines virtuelles Ubuntu Server et Windows 10 en déployant et intégrant l’agent Zabbix sur chaque hôte. 
Network Monitor
Cette configuration permet la remontée granulaire d’indicateurs clés tels que l’utilisation des ressources système (CPU, mémoire, disque), l’état des processus critiques ainsi que la disponibilité des services.


Le résultat de la supervision réalisée via Zabbix met en évidence l’évolution de l’utilisation de l’espace disque sur la machine virtuelle Ubuntu Server, offrant un suivi précis de la consommation des ressources de stockage et facilitant l’anticipation des besoins futurs, comme le montre la figure qui suit.


Figure 8 : [Supervision du serveur Ubuntu](../images/network_monitoring/Monitoring%20du%20Serveur%20Ubuntu.png)

Cette figure illustre le résultat de la supervision réalisée via Zabbix sur la machine virtuelle Windows 10.

Figure 9 : [Supervision du système Windows 10](../images/network_monitoring/Monitoring%20du%20système%20Windows%2010.png)


