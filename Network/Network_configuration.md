##🌐 Déploiement de l'infrastructure réseau

Nous avons mis en œuvre l’infrastructure réseau cible basée sur l’architecture définie en phase de conception, avec des VLANs, des routeurs, des commutateurs et des pare-feux **pfSense** en haute disponibilité (HA).  
pfSense est utilisé pour le contrôle central des flux réseau, le filtrage, l’application des politiques d’accès et la prévention d’intrusions (IDS/IPS).

📸 Architecture

<img width="1282" height="675" alt="Architecture Réseau" src="https://github.com/user-attachments/assets/16f61617-e3ac-44d1-9434-c9ecd53c6ed8" />

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
