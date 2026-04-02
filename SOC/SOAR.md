
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

* Intégration de Cortex et MISP

Nous avons choisi MISP comme analyseur principal pour nos IOCs et configuré son intégrationvia la clé API et l’URL du serveur, assurant ainsi une communication sécurisée entre les plateformes.
La configuration est présentée dans la figure suivante.

Figure 5 : [Intégration de Cortex et MISP](../images/SOC/Intégration%20de%20Cortex%20et%20MISP.png)

* Intégration de VirusTotal dans Cortex
  
VirusTotal est un service en ligne permettant d’analyser des fichiers et des URL afin de détecter différents types de menaces, tels que les virus, vers et chevaux de Troie, en s’appuyant sur plusieurs moteurs antivirus. Il permet également d’identifier d’éventuels faux positifs. Dans ce contexte, son intégration au sein de la plateforme Cortex permet d’enrichir les capacités d’analyse et de détection. Afin de mettre en œuvre cette intégration, il est nécessaire de configurer les paramètres requis et d’ajouter la clé API correspondante afin d’activer l’intégration, comme illustré dans la figure suivante.

Figure 6 : [Ajout de l’analyseur VirusTotal](../images/SOC/Ajout%20de%20l’analyseur%20VirusTotal.png)

* Intégration de AbuseIPDB dans Cortex
  
AbuseIPDB est une plateforme dédiée à la lutte contre les activités malveillantes sur Internet, telles que les attaques de pirates, le spam et autres comportements abusifs. Elle permet de signaler une adresse IP associée à une activité suspecte, ainsi que de vérifier la réputation d’une adresse IP via son moteur de recherche. L’intégration de ce service au sein de la plateforme Cortex est présentée dans la figure suivante.

Figure 7 : [Ajout de l’analyseur AbuseIPDB](../images/SOC/Ajout%20de%20l’analyseur%20AbuseIPDB.png)

Après l’ajout des analyseurs avec succès, nous avons procédé à un test d’analyse afin de vérifier leur bon fonctionnement. Les résultats obtenus ont été correctement générés et enregistrés dans l’historique des tâches (Job History) de Cortex, comme le montre la figure suivante.


Figure 8 : [Test des analyseurs](../images/SOC/Test%20des%20analyseurs.jpg)

Nous avons intégré dans notre fichier Docker Compose la configuration des conteneurs requis pour assurer un déploiement optimal de la plateforme TheHive et de ses services associés.
L’interface Web de TheHive est désormais accessible via le port 9000, comme illustré dans la figure suivante.


Figure 9 : [Interface graphique de TheHive](../images/SOC/Interface%20graphique%20de%20TheHive.png)

L’étape suivante a consisté à créer un compte administrateur associé à l’organisation précédemment configurée, comme illustré dans cette figure.

Figure 10 : [Création d’un utilisateur au niveau de TheHive](../images/SOC/Création%20d’un%20utilisateur%20au%20niveau%20de%20TheHive.png)

* Intégration de TheHive avec Cortex et MISP

L’intégration de TheHive avec Cortex a été préalablement définie lors de la configuration du conteneur TheHive, en spécifiant les paramètres nécessaires à la communication, notamment le port d’écoute et la clé API de Cortex, comme illustré dans la figure suivante.

Figure 11 : [Intégration de TheHive et Cortex](../images/SOC/Intégration%20de%20TheHive%20et%20Cortex.jpg)

Pour intégrer TheHive avec MISP, un répertoire de configuration spécifique a été créé, contenant l’URL du serveur MISP, la clé API et l’identifiant de l’organisation. Ce répertoire a ensuite été monté dans le conteneur TheHive, assurant une intégration fluide et sécurisée. La figure suivante illustre cette configuration.

Figure 12 : [Répertoire d’intégration de TheHive et MISP](../images/SOC/Répertoire%20d’intégration%20de%20TheHive%20et%20MISP.jpg)

Nous avons monté le répertoire de configuration dans le conteneur TheHive afin d’établir l’intégration avec la plateforme MISP, comme le montre la figure suivante.

Figure 13 : [Intégration de TheHive et MISP](../images/SOC/Intégration%20de%20TheHive%20et%20MISP.jpg)

