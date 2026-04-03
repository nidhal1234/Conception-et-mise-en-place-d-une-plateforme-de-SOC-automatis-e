🌐 Déploiement de l'infrastructure réseau

Nous avons mis en œuvre l’infrastructure réseau cible basée sur l’architecture définie en phase de conception, avec des VLANs, des routeurs, des commutateurs et des pare-feux **pfSense** en haute disponibilité (HA).  

pfSense est utilisé pour le contrôle central des flux réseau, le filtrage, l’application des politiques d’accès et la prévention d’intrusions (IDS/IPS).

📸 Architecture

![Architecture Réseau](images/network_configuration/Architecture_Reseau.png)
Après la réalisation et la configuration de notre maquette, la validation fonctionnelle vise à s’assurer que l’architecture réseau conçue répond aux objectifs attendus en matière de connectivité, de segmentation logique, et de communication entre les différents équipements. Elle constitue une étape essentielle permettant de vérifier que la configuration des routeurs, commutateurs, pare-feux et machines virtuelles a été correctement appliquée, et que les liaisons établies entre les composants assurent un fonctionnement cohérent et stable. Cette validation repose sur une série de vérifications de base avant les tests approfondis, notamment la connectivité IP, la reconnaissance des VLANs, la disponibilité des services réseau essentiels et la conformité des adresses IP selon le plan d’adressage défini.

Ce tableau présente la répartition des sous-réseaux et l’affectation des adresses aux différents équipements de la maquette.

Figure 2 : [Plan d'adressage de l'architecture réseau](../images/network_configuration/Plan%20d'adressage.png)

Ces figures illustrent respectivement le déroulement et les résultats de ce test de connectivité, confirmant le bon fonctionnement des liens et des configurations réseau en place.

Figure 3 : [Test de connectivité de PC1 vers PC3](../images/network_configuration/Connection%20PC1%20vers%20PC3.png)

Figure 4 : [Test de connectivité de PC4 vers PC2](../images/network_configuration/Connection%20de%20PC4%20vers%20PC2.png)

Cette figure illustre clairement que pfSense1 est correctement configuré et opérationnel en tant que pare-feu maître Master.

Figure 5 : [Statut Master du pfSense1 dans la configuration HA](../images/network_configuration/PfSense1%20comme%20Master.png)

Contrairement à pfSense1, le pare-feu pfSense2 est correctement configuré en tant que noeud secondaire Backup dans la solution de haute disponibilité, comme illustré dans la figure qui suit.

Figure 6 : [Statut Backup du pfSense2 dans la configuration HA](../images/network_configuration/pfSense2%20comme%20Backup.png)

Cette figure illustre le succès de la connectivité établie entre un hôte du VLAN 10 et un hôte du VLAN 77, confirmant ainsi l’efficacité de la configuration mise en place.

Figure 7 : [Connexion de PC1 à Ubuntu Server](../images/network_configuration/Connexion%20de%20PC1%20à%20Ubuntu%20Server.png)

La figure qui suit illustre le succès de la connectivité depuis un hôte du VLAN 10 PC1 vers internet.

Figure 8 : [Connexion de PC1 à Internet](../images/network_configuration/Connection%20PC1%20de%20VLAN%2010%20à%20internet.png)

Cette figure illustre le succès de la connectivité depuis un hôte du VLAN 20 PC3 vers internet.

Figure 9 : [Connexion de PC3 à Internet](../images/network_configuration/Connection%20de%20PC3%20de%20VLAN20%20à%20internet.png)

Cette figure illustre la réussite de la connectivité de la VM Ubuntu Server vers internet.

Figure 10 : [Connexion de Ubuntu Server à Internet](../images/network_configuration/Connexion%20de%20Ubuntu%20Server%20à%20Internet.png)


