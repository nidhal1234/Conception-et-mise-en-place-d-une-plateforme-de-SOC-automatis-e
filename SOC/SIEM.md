Dans cette phase, nous avons procédé au déploiement des agents Wazuh sur deux machines virtuelles de notre maquette réseau, à savoir Ubuntu Server et Windows 10. Cette opération a permis d’assurer la collecte, la remontée et la centralisation des journaux d’activité et des événements de sécurité générés par ces hôtes, en les rattachant au serveur Wazuh principal pour un suivi en temps réel.

Cette figure présente la liste des agents visibles depuis l’interface de gestion Wazuh, confirmant leur ajout réussi et leur communication active avec le serveur.

Figure 1 : [Agents de Wazuh](../images/SOC/Agents%20de%20Wazuh.png)

La figure qui suit nous montre que le serveur Wazuh commence à intercepter les journaux et les alertes des différents niveau à partir de l’agent Windows.

Figure 2 : [Les logs de la machine Windows](../images/SOC/Les%20logs%20de%20la%20machine%20Windows.png)
