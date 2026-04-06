# 🛡️ Conception et mise en place d'une plateforme de SOC automatisée

Ce projet illustre la conception, le déploiement et la supervision d’une **infrastructure réseau sécurisée** intégrant une solution **SOC (Security Operations Center)** complète.  
Il couvre la configuration des équipements réseau, l’intégration des outils de cybersécurité, la collecte et l’analyse des événements, ainsi que la gestion automatisée des incidents.

---

## 📌 Objectifs du projet

- Déployer une **architecture réseau segmentée** avec VLAN, routage sécurisé et isolation des flux critiques.  
- Implémenter une **solution SOC complète** pour la corrélation, la centralisation et l’analyse des événements de sécurité.  
- Automatiser la **gestion des alertes et la réponse aux incidents** via des outils comme **Wazuh**, **TheHive** et **Cortex**.  
- Tester la résilience et la détection face à des scénarios d’attaque réalistes (force brute, fichiers malveillants, compromission de endpoints).

---

## 🏗️ Architecture du projet

### 1. Architecture réseau cible
Représente le réseau opérationnel avant l’intégration des outils SOC.  
La configuration comprend VLAN, sous-réseaux, liaisons inter-switches et interconnexion des routeurs.  
L’ensemble de l’architecture est **entièrement provisionné et opérationnel**.

![Architecture réseau cible](./images/network_configuration/Architecture_Reseau.png)  
*Architecture réseau cible, entièrement*

### 2. Architecture SOC
Solution SOC déployée pour superviser le réseau, détecter les incidents et orchestrer la réponse automatisée.  
Inclut la collecte des logs, l’analyse des événements et la corrélation avec des référentiels comme **MITRE ATT&CK**.

![Architecture SOC](./images/SOC/Architecture_SOC_Proposee.jpg)  
*Architecture SOC intégrée et opérationnelle*

### 3. Architecture réseau avec SOC
Illustration du réseau cible enrichi par l’intégration des composants SOC, mettant en évidence les flux d’information et l’emplacement des agents et serveurs de sécurité.

![Réseau avec SOC](../images/SOC/Architecture_reseau_securisee_avec_SOC.png)  
*Architecture réseau avec intégration des outils SOC*

---

## 🛠️ Outils et technologies

- **Wazuh** : SIEM et détection d’intrusions, collecte et corrélation des événements de sécurité  
- **TheHive** : gestion centralisée des incidents et orchestration des workflows  
- **Cortex** : analyse automatisée des observables et enrichissement des données  
- **Kali Linux** : simulation d’attaques et tests de pénétration  
- **Ubuntu Server & Windows 10** : endpoints surveillés et collecteurs de logs  
- **pfSense** : pare-feux périmétriques avec journalisation centralisée  
- Protocoles et standards : VLAN, SSH, Syslog, Remote Logging, MITRE ATT&CK, FIM (File Integrity Monitoring)  

---

## 🧪 Scénarios de tests et validation

Les tests réalisés valident la capacité du SOC à détecter, remonter et orchestrer la réponse aux incidents.

### Scénario 1 : Attaque par force brute
- Simulation d’attaques SSH sur un serveur Ubuntu avec **Kali Linux** et **Hydra**.  
- Détection des tentatives d’intrusion et génération d’alertes dans **Wazuh**.  
- Transmission et analyse automatisée des alertes via **TheHive** et **Cortex**.

### Scénario 2 : Injection de fichier malveillant
- Téléchargement d’un fichier **Trojan** sur le serveur Ubuntu.  
- Détection d’altération de fichiers via **Wazuh FIM** et génération d’alertes critiques.  
- Enrichissement et analyse des informations dans **TheHive** et **Cortex**.

Ces tests démontrent l’efficacité du SOC pour la **supervision proactive**, la **détection avancée** et la **réponse automatisée aux incidents**.

---

## 📂 Organisation des fichiers
