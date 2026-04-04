# 📊 Supervision SIEM avec Wazuh

Dans cette section, nous présentons l’intégration de **Wazuh** dans notre maquette réseau pour la collecte, la centralisation et l’analyse des journaux d’activité et des événements de sécurité. Cette solution permet une supervision en temps réel des systèmes et des pare-feux, ainsi qu’une corrélation avec les techniques MITRE ATT&CK.

---

## 🛠️ Déploiement des agents Wazuh

Les agents Wazuh ont été déployés sur deux machines virtuelles : **Ubuntu Server** et **Windows 10**, afin d’assurer la collecte et la remontée des logs vers le serveur principal.

### 🐧 Ubuntu Server

1. **Enregistrement de l’hôte sur le serveur Wazuh**  
   Cette étape permet de générer les clés d’authentification pour établir une communication sécurisée entre l’agent et le serveur.  
   ![Ajout d’agent Ubuntu](../images/siem/agent_ubuntu_add.png)  
   *Figure 1 : Ajout de l’agent Ubuntu sur le serveur Wazuh*

2. **Installation et vérification de l’agent**  
   Après installation, l’état de l’agent est vérifié pour confirmer son bon fonctionnement.  
   ![État Wazuh Agent Ubuntu](../images/siem/agent_ubuntu_status.png)  
   *Figure 2 : État du Wazuh Agent sur Ubuntu Server*

3. **Configuration de l’agent**  
   L’adresse IP du serveur Wazuh est ajoutée dans le fichier de configuration pour établir la connexion.  
   ![Configuration Wazuh Agent Ubuntu](../images/siem/agent_ubuntu_config.png)  
   *Figure 3 : Configuration du Wazuh Agent sur Ubuntu*

---

### 🪟 Windows 10

1. **Enregistrement de l’hôte sur le serveur Wazuh**  
   La machine Windows est enregistrée sur le serveur pour générer les clés d’authentification sécurisées.  
   ![Ajout d’agent Windows](../images/siem/agent_windows_add.png)  
   *Figure 4 : Ajout de l’agent Windows sur le serveur Wazuh*

2. **Installation et vérification de l’agent**  
   L’état de l’agent est vérifié après installation pour confirmer sa communication avec le serveur.  
   ![État Wazuh Agent Windows](../images/siem/agent_windows_status.png)  
   *Figure 5 : État du Wazuh Agent sur Windows 10*

---

### 📋 Liste des agents

Le serveur Wazuh affiche la liste des agents enregistrés, confirmant leur communication active.  
![Agents Wazuh](../images/siem/agents_list.png)  
*Figure 6 : Agents Wazuh actifs sur le serveur*

---

### 📈 Collecte des journaux

#### Windows 10
Le serveur Wazuh intercepte les logs et alertes générés par l’agent Windows.  
![Logs Windows](../images/siem/logs_windows.png)  
*Figure 7 : Journaux et alertes collectés depuis Windows 10*

#### Ubuntu Server
Le serveur Wazuh intercepte également les logs et alertes générés par l’agent Ubuntu.  
![Logs Ubuntu](../images/siem/logs_ubuntu.png)  
*Figure 8 : Journaux et alertes collectés depuis Ubuntu Server*

---

### 🛡️ Analyse MITRE ATT&CK

#### Windows 10
Les activités observées sur la machine Windows sont corrélées avec les techniques MITRE ATT&CK.  
![MITRE ATT&CK Windows](../images/siem/mitre_windows.png)  
*Figure 9 : Techniques MITRE ATT&CK pour Windows 10*

#### Ubuntu Server
Les activités observées sur la machine Ubuntu sont également analysées avec MITRE ATT&CK.  
![MITRE ATT&CK Ubuntu](../images/siem/mitre_ubuntu.png)  
*Figure 10 : Techniques MITRE ATT&CK pour Ubuntu Server*

---

## 🔐 Surveillance des pare-feux pfSense

Pour superviser les pare-feux via Wazuh, il est nécessaire de configurer la **journalisation distante (Remote Logging)**, en indiquant l’adresse IP du serveur Wazuh et en utilisant le port UDP 514.

### pfSense1

1. **Configuration du Syslog**  
   ![Syslog pfSense1](../images/siem/pfsense1_syslog.png)  
   *Figure 11 : Activation de la journalisation distante sur pfSense1*

2. **Surveillance via Wazuh**  
   ![Surveillance pfSense1](../images/siem/pfsense1_monitoring.png)  
   *Figure 12 : Supervision effective de pfSense1 via Wazuh*

### pfSense2

1. **Configuration du Syslog**  
   ![Syslog pfSense2](../images/siem/pfsense2_syslog.png)  
   *Figure 13 : Activation de la journalisation distante sur pfSense2*

2. **Surveillance via Wazuh**  
   ![Surveillance pfSense2](../images/siem/pfsense2_monitoring.png)  
   *Figure 14 : Supervision effective de pfSense2 via Wazuh*

---

Ce document présente une vue complète de la **supervision SIEM** avec Wazuh, incluant le déploiement des agents, la collecte des logs, l’analyse MITRE ATT&CK et la surveillance des pare-feux pfSense.
