Dans cette phase, nous avons procédé au déploiement des agents Wazuh sur deux machines virtuelles de notre maquette réseau, à savoir Ubuntu Server et Windows 10. Cette opération a permis d’assurer la collecte, la remontée et la centralisation des journaux d’activité et des événements de sécurité générés par ces hôtes, en les rattachant au serveur Wazuh principal pour un suivi en temps réel.

Cette figure présente la liste des agents visibles depuis l’interface de gestion Wazuh, confirmant leur ajout réussi et leur communication active avec le serveur.

Figure 1 : [Agents de Wazuh](../images/SOC/Agents%20de%20Wazuh.png)

La figure qui suit nous montre que le serveur Wazuh commence à intercepter les journaux et les alertes des différents niveau à partir de l’agent Windows.

Figure 2 : [Les logs de la machine Windows](../images/SOC/Les%20logs%20de%20la%20machine%20Windows.png)

Cette figure nous montre que le serveur Wazuh commence à intercepter les journaux et les alertes des diffèrents niveaux à partir de l’agent Ubuntu.

Figure 3 : [Les logs de la machine Ubuntu](../images/SOC/Les%20logs%20de%20la%20machine%20Ubuntu.png)

La figure qui suit illustre les techniques MITRE ATT&CK associées aux activités observées sur la machine Windows 10.

Figure 4 : [MITRE ATT&CK pour Windows](../images/SOC/MITRE%20ATT&CK%20pour%20Windows.png)

Cette figure illustre les techniques MITRE ATT&CK associées aux activités observées sur la machine Ubuntu.

Figure 4 : [MITRE ATT&CK pour Ubuntu](../images/SOC/MITRE%20ATT&CK%20pour%20Ubuntu.png)

Pour appliquer efficacement la surveillance Wazuh aux pare-feux pfSense, il est impératif de configurer ces derniers afin qu’ils transmettent leurs journaux d’activité au serveur Wazuh. Cette opération repose sur l’activation de l’option de journalisation distante (Remote Logging) dans l’interface d’administration de pfSense, en spécifiant l’adresse IP du serveur Wazuh comme destination. Les logs sont envoyés via le protocole UDP, généralement sur le port 514, ce qui permet au serveur de centraliser et d’analyser les événements de sécurité générés par les pare-feux en temps réel. Cette configuration constitue la première étape essentielle pour une supervision complète et continue de l’activité réseau filtrée par pfSense.

Cette figure montre la surveillance effective de pfSense1 via le serveur Wazuh.




