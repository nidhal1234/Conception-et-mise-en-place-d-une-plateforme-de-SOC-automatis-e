
Pour automatiser notre architecture, nous avons besoin d’intégrer la partie SOAR. À cet effet, les différents composants de la solution ont été déployés sur un serveur Ubuntu, déjà intégré à notre architecture réseau au niveau du VLAN 77.

Pour la mise en place de MISP nous avons créé un fichier Docker Compose décrivant une architecture multi-services destinée au déploiement de la plateforme MISP.
Afin de créer et lancer les conteneurs, nous avons utilisé la commande docker compose up, permettant le déploiement des services en arrière-plan.

Voila l’interface graphique de la plateforme MISP est accessible via un navigateur web, comme illustré dans la figure suivante, confirmant ainsi le bon déploiement du service.

Figure 1 : [Interface graphique de MISP](../images/SOC/Interface%20graphique%20de%20MISP.png)

Nous avons ensuite créé un compte utilisateur que nous avons configuré avec des privilèges administratifs pour l’organisation, assurant ainsi une gestion complète de la plateforme, comme illustré dans la figure suivante.


Figure 2 : [Création d’un utilisateur au niveau de MISP](../images/SOC/Création%20d’un%20utilisateur%20au%20niveau%20de%20MISP.png)

Nous avons intégré, dans le fichier Docker Compose, la configuration du conteneur Cortex ainsi que celle de son moteur de données Elasticsearch, afin d’assurer un déploiement cohérent et fonctionnel de l’environnement SOAR.

L’accès à l’interface graphique de Cortex a été configuré avec succès et est désormais disponible via un navigateur web sur le port 9001, comme présenté dans la figure suivante.

Figure 3 : [Interface graphique de Cortex](../images/SOC/Interface%20graphique%20de%20Cortex.png)

L’étape suivante a consisté à créer un utilisateur au niveau de Cortex, puis à lui attribuer les permissions requises afin d’assurer une gestion complète de la plateforme, comme illustré dans la figure suivante.

Figure 4 : [Création d’un utilisateur au niveau de Cortex](../images/SOC/Création%20d’un%20utilisateur%20au%20niveau%20de%20Cortex.png)



