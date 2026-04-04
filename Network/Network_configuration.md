### 🌐 Déploiement de l'infrastructure réseau

Nous avons mis en œuvre l’infrastructure réseau cible basée sur l’architecture définie en phase de conception, avec des VLANs, des routeurs, des commutateurs et des pare-feux **pfSense** en haute disponibilité (HA).  
pfSense est utilisé pour le contrôle central des flux réseau, le filtrage, l’application des politiques d’accès et la prévention d’intrusions (IDS/IPS).

---

### 📸 Architecture

Cette figure illustre l’architecture réseau cible mise en place dans notre environnement.

![Architecture réseau cible](../images/network_configuration/Architecture_Reseau.png)  
*Figure 1 : Architecture réseau cible*

---

### 📊 Plan d'adressage

Cette figure présente la répartition des sous-réseaux et l’affectation des adresses IP au sein de l’architecture.

![Plan d'adressage](../images/network_configuration/Plan_d'adressage.png)  
*Figure 2 : Répartition des sous-réseaux et IP*

---

### 🔌 Validation de connectivité

Cette section présente les tests de connectivité réalisés afin de valider l’accès aux ressources internes et externes.

Cette figure montre le test de connectivité entre PC1 et PC3, confirmant le bon fonctionnement de la communication inter-VLAN.

![PC1 vers PC3](../images/network_configuration/Connection_PC1_vers_PC3.png)  
*Figure 3 : PC1 vers PC3*

Cette figure illustre le test de connectivité entre PC4 et PC2, validant la configuration réseau mise en place.

![PC4 vers PC2](../images/network_configuration/Connection_de_PC4_vers_PC2.png)  
*Figure 4 : PC4 vers PC2*

---

### 🔐 Haute disponibilité (HA)

Cette figure présente le statut du pare-feu pfSense1 configuré en tant que nœud principal (Master) dans la solution de haute disponibilité.

![pfSense1 Master](../images/network_configuration/PfSense1_comme_Master.png)  
*Figure 5 : pfSense1 → Master*

Cette figure montre le pare-feu pfSense2 configuré en tant que nœud secondaire (Backup) dans la configuration HA.

![pfSense2 Backup](../images/network_configuration/pfSense2_comme_Backup.png)  
*Figure 6 : pfSense2 → Backup*

---

### 🌐 Connectivité vers serveurs et Internet

Cette figure illustre la connectivité entre PC1 et le serveur Ubuntu, confirmant l’accessibilité entre les VLANs.

![PC1 vers Ubuntu Server](../images/network_configuration/Connexion_de_PC1_à_Ubuntu_Server.png)  
*Figure 7 : PC1 vers Ubuntu Server*

Cette figure montre la réussite de la connexion de PC1 vers Internet.

![PC1 vers Internet](../images/network_configuration/Connection_PC1_de_VLAN_10_à_internet.png)  
*Figure 8 : PC1 vers Internet*

Cette figure illustre l’accès à Internet depuis PC3, validant la configuration réseau pour le VLAN 20.

![PC3 vers Internet](../images/network_configuration/Connection_de_PC3_de_VLAN20_à_internet.png)  
*Figure 9 : PC3 vers Internet*

Cette figure présente la connectivité du serveur Ubuntu vers Internet, confirmant le bon fonctionnement de la passerelle réseau.

![Ubuntu Server vers Internet](../images/network_configuration/Connexion_de_Ubuntu_Server_à_Internet.png)  
*Figure 10 : Ubuntu Server vers Internet*
