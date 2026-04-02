
Pour automatiser notre architecture, nous avons besoin d’intégrer la partie SOAR. À cet effet, les différents composants de la solution ont été déployés sur un serveur Ubuntu, déjà intégré à notre architecture réseau au niveau du VLAN 77.

Pour la mise en place de MISP nous avons créé un fichier Docker Compose décrivant une architecture multi-services destinée au déploiement de la plateforme MISP.
Afin de créer et lancer les conteneurs, nous avons utilisé la commande docker compose up, permettant le déploiement des services en arrière-plan.

Voila l’interface graphique de la plateforme MISP est accessible via un navigateur web, comme illustré dans la figure suivante, confirmant ainsi le bon déploiement du service.

Figure 1 : [Interface graphique de MISP](../images/SOC/Interface%20graphique%20de%20MISP.png)

Nous avons ensuite créé un compte utilisateur que nous avons configuré avec des privilèges administratifs pour l’organisation, assurant ainsi une gestion complète de la plateforme, comme illustré dans la figure qui suit.


Figure 1 : [Interface graphique de MISP](../images/SOC/Interface%20graphique%20de%20MISP.png)
