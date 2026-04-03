## 🌐 Déploiement de l'infrastructure réseau

Nous avons mis en œuvre l’infrastructure réseau cible basée sur l’architecture définie en phase de conception, avec des VLANs, des routeurs, des commutateurs et des pare-feux **pfSense** en haute disponibilité (HA).  
pfSense est utilisé pour le contrôle central des flux réseau, le filtrage, l’application des politiques d’accès et la prévention d’intrusions (IDS/IPS).

📸 Architecture

![Architecture réseau cible](images/network_configuration/Architecture_Reseau.png)  
*Figure 1 : Architecture réseau cible*

### 📊 Plan d'adressage


<img width="668" height="842" alt="Plan d&#39;adressage" src="https://github.com/user-attachments/assets/a731eaaa-f17a-4f02-a788-7ec0b15f8c88" />

*Figure 2 : Répartition des sous-réseaux et IP*

Tests réalisés pour vérifier la communication entre VLANs et l’accès Internet

<img width="746" height="385" alt="Connection PC1 vers PC3" src="https://github.com/user-attachments/assets/707c3c81-3e51-4755-9993-c0693d13f120" />

*Figure 3 : PC1 vers PC3*

<img width="746" height="522" alt="Connection de PC4 vers PC2" src="https://github.com/user-attachments/assets/f9a7f431-0fc6-4476-8e35-bf302f29455e" />

*Figure 4 : PC4 vers PC2*

### 🔐 Haute disponibilité (HA)

<img width="1297" height="737" alt="PfSense1 comme Master" src="https://github.com/user-attachments/assets/a29b9bdd-14b9-4139-9d39-4bfbafa7528f" />

 *Figure 5 : pfSense1 Master* 

 <img width="1315" height="791" alt="pfSense2 comme Backup" src="https://github.com/user-attachments/assets/6db8fdc5-e181-4707-bfc9-ad66c95ff61a" />

*Figure 6 : pfSense2 Backup*

### 🌐 Connectivité vers serveurs et Internet

<img width="738" height="517" alt="Connection PC1 de VLAN 10 vers un PC de vlan 77" src="https://github.com/user-attachments/assets/86e9ef8d-aa58-400f-93f6-e32e55a1b7a4" />

*Figure 7 : PC1 vers Ubuntu Server*

<img width="747" height="518" alt="Connection PC1 de VLAN 10 sur internet " src="https://github.com/user-attachments/assets/f1efe4e0-907e-457f-b536-c352c768084f" /> 

*Figure 8 : PC1 vers Internet*  

<img width="746" height="521" alt="Connection de PC3 de VLAN20 sur internet" src="https://github.com/user-attachments/assets/20b847de-68d4-4539-980f-1675789e0647" />

 *Figure 9 : PC3 vers Internet*

<img width="982" height="677" alt="Ping ubuntu vers Internet " src="https://github.com/user-attachments/assets/03109aec-322d-48f8-9683-7ba46b743e47" />

*Figure 10 : Ubuntu Server vers Internet*
