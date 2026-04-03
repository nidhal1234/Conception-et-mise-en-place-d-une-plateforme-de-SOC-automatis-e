* Déploiement des agents Wazuh

Dans cette phase, nous avons procédé au déploiement des agents Wazuh sur deux machines virtuelles de notre maquette réseau, à savoir Ubuntu Server et Windows 10. Cette opération a permis d’assurer la collecte, la remontée et la centralisation des journaux d’activité et des événements de sécurité générés par ces hôtes, en les rattachant au serveur Wazuh principal pour un suivi en temps réel.

Pour le déploiement de l’agent Wazuh sur la machine Ubuntu, il est nécessaire d’enregistrer préalablement cet hôte depuis l’interface d’administration du serveur Wazuh. Cette étape permet de générer les clés d’authentification requises pour établir une communication sécurisée entre l’agent et le
serveur, comme illustré dans la figure suivante.

Figure 1 : [Ajout d’agent Ubuntu](../images/SOC/Ajout%20d’agent%20Ubuntu.png)

Ensuite, nous avons procédé à l’installation de l’agent Wazuh sur notre système linux, suivie de la vérification de son état de fonctionnement, comme le montre la figure suivante.

Figure 2 : [État wazuh-agent sur Ubuntu Server](../images/SOC/État%20wazuh-agent%20sur%20Ubuntu%20Server.png)

Puis nous devons ajouter l’adresse IP de notre serveur wazuh dans le fichier de configuration de l’agent, comme le montre la figure suivante.

Figure 3 : [Configuration du wazuh-agent sur Ubuntu](../images/SOC/Configuration%20du%20wazuh-agent%20sur%20Ubuntu.png)

Pour déployer l’agent Wazuh sur la machine Windows, il est nécessaire d’enregistrer l’hôte via l’interface du serveur Wazuh pour établir une communication sécurisée entre l’agent et le serveur, comme illustré dans la figure suivante.

Figure 4 : [Ajout d’agent Windows](../images/SOC/Ajout%20d’agent%20Windows.png)

Nous avons ensuite installé l’agent Wazuh sur notre machine virtuelle Windows, puis vérifié son état de fonctionnement, comme le montre la figure suivante.

Figure 5 : [État wazuh-agent sur Windows 10](../images/SOC/État%20wazuh-agent%20sur%20Windows%2010.png)

Cette figure présente la liste des agents visibles depuis l’interface de gestion de Wazuh, confirmant leur ajout réussi et leur communication active avec le serveur après le déploiement des agents.

Figure 6 : [Agents de Wazuh](../images/SOC/Agents%20de%20Wazuh.png)

La figure suivante nous montre que le serveur Wazuh commence à intercepter les journaux et les alertes des différents niveau à partir de l’agent Windows.

Figure 7 : [Les logs de la machine Windows](../images/SOC/Les%20logs%20de%20la%20machine%20Windows.png)

Cette figure nous montre que le serveur Wazuh commence à intercepter les journaux et les alertes des diffèrents niveaux à partir de l’agent Ubuntu.

Figure 8 : [Les logs de la machine Ubuntu](../images/SOC/Les%20logs%20de%20la%20machine%20Ubuntu.png)

La figure suivante illustre les techniques MITRE ATT&CK associées aux activités observées sur la machine Windows 10.

Figure 9 : [MITRE ATT&CK pour Windows](../images/SOC/MITRE%20ATT&CK%20pour%20Windows.png)

Cette figure illustre les techniques MITRE ATT&CK associées aux activités observées sur la machine Ubuntu.

Figure 10 : [MITRE ATT&CK pour Ubuntu](../images/SOC/MITRE%20ATT&CK%20pour%20Ubuntu.png)

Pour appliquer efficacement la surveillance Wazuh aux pare-feux pfSense, il est impératif de configurer ces derniers afin qu’ils transmettent leurs journaux d’activité au serveur Wazuh. Cette opération repose sur l’activation de l’option de journalisation distante (Remote Logging) dans l’interface d’administration de pfSense, en spécifiant l’adresse IP du serveur Wazuh comme destination. Les logs sont envoyés via le protocole UDP, généralement sur le port 514, ce qui permet au serveur de centraliser et d’analyser les événements de sécurité générés par les pare-feux en temps réel. Cette configuration constitue la première étape essentielle pour une supervision complète et continue de l’activité réseau filtrée par pfSense.

Cette figure montre la surveillance effective de pfSense1 via le serveur Wazuh.

Figure 6 : [Surveillance de pfSense1 via Wazuh](../images/SOC/Surveillance%20de%20pfSense1%20via%20Wazuh.png)

La figure suivante montre la surveillance effective de pfSense2 via le serveur Wazuh.

Figure 7 : [Surveillance de pfSense2 via Wazuh](../images/SOC/Surveillance%20de%20pfSense2%20via%20Wazuh.png)
