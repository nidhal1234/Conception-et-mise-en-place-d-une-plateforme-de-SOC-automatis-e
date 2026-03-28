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

[Accéder à l’Architecture Réseau](../images/network_configuration/Architecture%20Réseau.png)

Après la réalisation et la configuration de notre maquette, la validation fonctionnelle vise à s’assurer que l’architecture réseau conçue répond aux objectifs attendus en matière de connectivité, de segmentation logique, et de communication entre les différents équipements. Elle constitue une étape essentielle permettant de vérifier que la configuration des routeurs, commutateurs, pare-feux et machines virtuelles a été correctement appliquée, et que les liaisons établies entre les composants assurent un fonctionnement cohérent et stable. Cette validation repose sur une série de vérifications de base avant les tests approfondis, notamment la connectivité IP, la reconnaissance des VLANs, la disponibilité des services réseau essentiels et la conformité des adresses IP selon le plan d’adressage défini.

Ces figures illustrent respectivement le déroulement et les résultats de ce test de connectivité, confirmant le bon fonctionnement des liens et des configurations réseau en place.

Figure 1 : Architecture réseau réseau cible
[Accéder à l’Architecture Réseau](../images/network_configuration/ConnectionPC1versPC3.png)

