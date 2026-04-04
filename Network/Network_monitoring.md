## 📡 Network Monitoring avec Zabbix

Dans cette partie, nous avons intégré **Zabbix** au sein de notre architecture réseau afin d’assurer une supervision centralisée, en temps réel, des différents équipements. Cette solution permet de détecter rapidement les anomalies, d’anticiper les pannes et d’améliorer la disponibilité ainsi que la sécurité globale de l’infrastructure.

---

### 🏗️ Intégration de Zabbix

Cette figure illustre l’intégration du serveur Zabbix dans l’architecture réseau.

![Intégration Zabbix](../images/network_monitoring/Intégration_du_serveur_Zabbix_dans_architecture_reseau.png)  
*Figure 1 : Intégration du serveur Zabbix dans l’architecture réseau*

---

### 🔌 Supervision des commutateurs

Après la configuration du protocole SNMP sur le commutateur ESW4, nous avons vérifié l’état du service afin de valider son bon fonctionnement.

![SNMP Switch](../images/network_monitoring/Etat_du_protocole_SNMP_sur_le_commutateur.png)  
*Figure 2 : État du protocole SNMP sur le commutateur*

Le commutateur a ensuite été ajouté au serveur Zabbix pour assurer sa supervision.

![Ajout Switch](../images/network_monitoring/Ajout_du_commutateur_au_serveur_Zabbix.png)  
*Figure 3 : Ajout du commutateur au serveur Zabbix*

Les figures suivantes illustrent la supervision des commutateurs via SNMP dans Zabbix.

![Switches 1-3](../images/network_monitoring/switches_1_3.png)  
*Figure 4 : Surveillance des commutateurs ESW1, ESW2, ESW3*

![Switches 4-6](../images/network_monitoring/switches_4_6.png)  
*Figure 5 : Surveillance des commutateurs ESW4, ESW5, ESW6*

Les figures ci-dessous présentent la surveillance du trafic des interfaces du commutateur ESW4.

![Interfaces 0-1](../images/network_monitoring/interfaces_01.png)  
*Figure 6 : Interfaces Gi0/0 et Gi0/1*

![Interfaces 2-3](../images/network_monitoring/interfaces_23.png)  
*Figure 7 : Interfaces Gi0/2 et Gi0/3*

---

### 🌐 Supervision des routeurs

Le protocole SNMP a été configuré sur le routeur R1 afin de permettre l’envoi de traps vers Zabbix.

![SNMP Router](../images/network_monitoring/snmp_router.png)  
*Figure 8 : État du service SNMP sur le routeur*

Le routeur a ensuite été intégré dans Zabbix pour assurer sa supervision.

![Ajout Router](../images/network_monitoring/add_router.png)  
*Figure 9 : Ajout du routeur au serveur Zabbix*

Cette figure montre la supervision des routeurs via SNMP.

![Monitoring Router](../images/network_monitoring/router_monitoring.png)  
*Figure 10 : Surveillance des routeurs R1 et R2*

---

### 🔐 Supervision des pare-feux

Les pare-feux **pfSense** ont été configurés pour la supervision SNMP avec Zabbix, permettant la collecte des métriques et la réception des traps.

![SNMP pfSense1](../images/network_monitoring/pfsense1_snmp.png)  
*Figure 11 : Configuration SNMP de pfSense1*

![SNMP pfSense2](../images/network_monitoring/pfsense2_snmp.png)  
*Figure 12 : Configuration SNMP de pfSense2*

Les pare-feux ont ensuite été ajoutés à Zabbix.

![Ajout pfSense1](../images/network_monitoring/add_pfsense1.png)  
*Figure 13 : Ajout de pfSense1*

![Ajout pfSense2](../images/network_monitoring/add_pfsense2.png)  
*Figure 14 : Ajout de pfSense2*

Cette figure illustre la supervision active des pare-feux.

![Monitoring pfSense](../images/network_monitoring/pfsense_monitoring.png)  
*Figure 15 : Surveillance des pare-feux*

---

### 💻 Supervision des machines virtuelles

Les machines **Ubuntu Server** et **Windows 10** ont été supervisées via le déploiement de l’agent Zabbix.

#### 🐧 Ubuntu Server

![Agent Ubuntu](../images/network_monitoring/agent_ubuntu_status.png)  
*Figure 16 : État de l’agent Zabbix sur Ubuntu*

![Integration Agent](../images/network_monitoring/agent_integration.png)  
*Figure 17 : Intégration de l’agent avec le serveur*

![Ajout Ubuntu](../images/network_monitoring/add_ubuntu.png)  
*Figure 18 : Ajout de la VM Ubuntu*

![Monitoring Ubuntu](../images/network_monitoring/monitoring_ubuntu.png)  
*Figure 19 : Supervision du serveur Ubuntu*

---

#### 🪟 Windows 10

![Config Agent Windows](../images/network_monitoring/agent_windows_config.png)  
*Figure 20 : Configuration de l’agent Zabbix sur Windows*

![Ajout Windows](../images/network_monitoring/add_windows.png)  
*Figure 21 : Ajout de la VM Windows*

![Monitoring Windows](../images/network_monitoring/monitoring_windows.png)  
*Figure 22 : Supervision du système Windows*
