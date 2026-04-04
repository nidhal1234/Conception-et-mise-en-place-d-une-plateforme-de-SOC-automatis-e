## 🌐 Déploiement de l'infrastructure réseau

Nous avons mis en œuvre l’infrastructure réseau cible basée sur l’architecture définie en phase de conception, avec des VLANs, des routeurs, des commutateurs et des pare-feux **pfSense** en haute disponibilité (HA).  
pfSense est utilisé pour le contrôle central des flux réseau, le filtrage, l’application des politiques d’accès et la prévention d’intrusions (IDS/IPS).

📸 Architecture

![Architecture réseau cible](../images/network_configuration/Architecture_Reseau.png)  
*Figure 1 : Architecture réseau cible*

### 📊 Plan d'adressage

![Plan d'adressage](../images/network_configuration/Plan_d'adressage.png)


*Figure 2 : Répartition des sous-réseaux et IP*

Tests réalisés pour vérifier la communication entre VLANs et l’accès Internet.

![PC1 vers PC3](../images/network_configuration/Connection_PC1_vers_PC3.png)

*Figure 3 : PC1 vers PC3*

![PC4 vers PC2](../images/network_configuration/Connection_de_PC4_vers_PC2.png)

*Figure 4 : PC4 vers PC2*

### 🔐 Haute disponibilité (HA)

![pfSense1 Master](../images/network_configuration/PfSense1_comme_Master.png)

 *Figure 5 : pfSense1 → Master* 

 ![pfSense2 Backup](../images/network_configuration/pfSense2_comme_Backup.png)

*Figure 6 : pfSense2 → Backup *

### 🌐 Connectivité vers serveurs et Internet

 ![PC1 vers Ubuntu Server](../images/network_configuration/Connexion_de_PC1_à_Ubuntu_Server.png)

*Figure 7 : PC1 vers Ubuntu Server*

 ![PC1 vers Internet](../images/network_configuration/Connection_PC1_de_VLAN_10_à_internet.png)

*Figure 8 : PC1 vers Internet*  

![PC3 vers Internet](..images/network_configuration/Connection_de_PC3_de_VLAN20_à_internet.png)

 *Figure 9 : PC3 vers Internet*

 ![Ubuntu Server vers Internet](../images/network_configuration/Connexion_de_Ubuntu_Server_à_Internet.png)

*Figure 10 : Ubuntu Server vers Internet*


