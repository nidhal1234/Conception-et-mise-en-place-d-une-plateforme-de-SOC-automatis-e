Dans cette partie, nous procédons à la mise en oeuvre de l’infrastructure réseau cible, telle
qu’elle a été définie lors de la phase de conception. Cette étape vise à concrétiser l’architecture théorique
en déployant une infrastructure opérationnelle, structurée autour d’équipements réseau configurés selon
les exigences de performance, de disponibilité et de sécurité. Elle constitue la base technique du projet
et garantit un environnement stable, évolutif et conforme aux objectifs fixés.
Un élément fondamental de cette infrastructure est le pare-feu pfSense, une solution open-source
de nouvelle génération, largement adoptée dans les environnements professionnels pour ses capacités
avancées de filtrage, de routage et de sécurité. Dans le cadre de ce projet, pfSense joue un rôle
stratégique en tant que point central de contrôle des flux réseau. Il permet la mise en place de règles
de filtrage granulaires, l’application de politiques d’accès rigoureuses, et l’intégration de mécanismes
de détection et de prévention des intrusions (IDS/IPS) grâce à des modules tels que Snort ou Suricata.
Sa flexibilité, sa stabilité et sa capacité à s’adapter à des architectures complexes en font un choix
particulièrement pertinent pour renforcer la posture de sécurité de l’infrastructure.

Cette figure présente l’architecture détaillée de la maquette réseau cible, servant de base à la
phase de déploiement et de configuration. Cette illustration met en évidence les équipements clés, leurs
interconnexions, ainsi que la segmentation du réseau prévue pour garantir performance et sécurité.
Nous détaillerons ensuite les composants principaux et les configurations associées pour assurer la
conformité aux objectifs du projet.

Figure 1 : Architecture réseau réseau cible

[Architecture Réseau](../images/network_configuration/Architecture%20Réseau.png)

Après la réalisation et la configuration de notre maquette, la validation fonctionnelle vise à s’assurer que l’architecture réseau conçue répond aux objectifs attendus en matière de connectivité, de segmentation logique, et de communication entre les différents équipements. Elle constitue une étape essentielle permettant de vérifier que la configuration des routeurs, commutateurs, pare-feux et machines virtuelles a été correctement appliquée, et que les liaisons établies entre les composants assurent un fonctionnement cohérent et stable. Cette validation repose sur une série de vérifications de base avant les tests approfondis, notamment la connectivité IP, la reconnaissance des VLANs, la disponibilité des services réseau essentiels et la conformité des adresses IP selon le plan d’adressage défini.

Ces figures illustrent respectivement le déroulement et les résultats de ce test de connectivité, confirmant le bon fonctionnement des liens et des configurations réseau en place.

Figure 2 : Test de connectivité de PC1 vers PC3

[Test de connectivité de PC1 vers PC3](../images/network_configuration/Connection%20PC1%20vers%20PC3.png)

Figure 3 : Test de connectivité de PC4 vers PC2

[Test de connectivité de PC4 vers PC2](../images/network_configuration/Connection%20de%20PC4%20vers%20PC2.png)

Cette figure illustre clairement que pfSense1 est correctement configuré et opérationnel en tant que pare-feu maître Master.

Figure 4 : Statut Master du pfSense1 dans la configuration HA

[Statut Master du pfSense1 dans la configuration HA](../images/network_configuration/PfSense1%20comme%20Master.png)

Contrairement à pfSense1, le pare-feu pfSense2 est correctement configuré en tant que noeud secondaire Backup dans la solution de haute disponibilité, comme illustré dans la figure qui suit.

Figure 5 : Statut Backup du pfSense2 dans la configuration HA

[Statut Backup du pfSense2 dans la configuration HA](../images/network_configuration/pfSense2%20comme%20Backup.png)

Cette figure illustre le succès de la connectivité établie entre un hôte du VLAN 10 et un hôte du VLAN 77, confirmant ainsi l’efficacité de la configuration mise en place.

Figure 6 : Connexion de PC1 à Ubuntu Server

[Connexion de PC1 à Ubuntu Server](../images/network_configuration/Connexion%20de%20PC1%20à%20Ubuntu%20Server.png)

La figure qui suit illustre le succès de la connectivité depuis un hôte du VLAN 10 PC1 vers internet.

Figure 7 : Connexion de PC1 à Internet

[Connexion de PC1 à Internet](../images/network_configuration/Connection%20PC1%20de%20VLAN%2010%20à%20internet.png)

Cette figure illustre le succès de la connectivité depuis un hôte du VLAN 20 PC3 vers internet.

Figure 8 : Connexion de PC3 à Internet

[Connexion de PC3 à Internet](../images/network_configuration/Connection%20de%20PC3%20de%20VLAN20%20à%20internet.png)

Cette figure illustre la réussite de la connectivité de la VM Ubuntu Server vers internet.

Figure 9 : Connexion de Ubuntu Server à Internet

[Connexion de Ubuntu Server à Internet](../images/network_configuration/Connexion%20de%20Ubuntu%20Server%20à%20Internet.png)
