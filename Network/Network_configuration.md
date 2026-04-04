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

<img width="747" height="518" alt="Connection PC1 de VLAN 10 sur internet " src="https://github.com/user-attachments/assets/f1efe4e0-907e-457f-b536-c352c768084f" /> 

*Figure 8 : PC1 vers Internet*  

<img width="746" height="521" alt="Connection de PC3 de VLAN20 sur internet" src="https://github.com/user-attachments/assets/20b847de-68d4-4539-980f-1675789e0647" />

 *Figure 9 : PC3 vers Internet*

<img width="982" height="677" alt="Ping ubuntu vers Internet " src="https://github.com/user-attachments/assets/03109aec-322d-48f8-9683-7ba46b743e47" />

*Figure 10 : Ubuntu Server vers Internet*


