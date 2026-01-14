## QCM 03 – Supervision et métrologie réseau (niveau difficile)

### Consignes
- 20 questions à choix multiples.  
- Une seule bonne réponse par question (sauf indication contraire).  
- Niveau : administrateur réseau confirmé.

---

**1. Quel est l’intérêt principal d’utiliser SNMPv3 plutôt que SNMPv2c pour la supervision réseau ?**  
A. SNMPv3 consomme moins de bande passante  
B. SNMPv3 permet l’authentification et le chiffrement des échanges  
C. SNMPv3 ne nécessite aucune configuration côté équipements  
D. SNMPv3 remplace totalement les syslog  

**2. Dans une architecture de supervision, que représente principalement une “sonde” ou “poller” ?**  
A. Un simple client SSH  
B. Un composant chargé d’interroger périodiquement les équipements (SNMP, ICMP, API, etc.)  
C. Un serveur de sauvegarde  
D. Un routeur BGP  

**3. Quel protocole est le plus souvent utilisé pour la collecte de journaux (logs) réseau centralisés ?**  
A. FTP  
B. Syslog (UDP/TCP 514, parfois TLS)  
C. POP3  
D. TFTP  

**4. Dans une solution de supervision comme Zabbix, Centreon, Nagios ou Prometheus, quel est l’avantage majeur de définir des seuils d’alerte (warning/critical) sur les métriques ?**  
A. Réduire automatiquement la consommation CPU des serveurs  
B. Déclencher des notifications proactives avant l’impact utilisateur  
C. Éviter de devoir historiser les données  
D. Supprimer la nécessité de redondance  

**5. Quel est l’objectif principal d’une vue “topologie réseau” dans un outil de supervision ?**  
A. Gérer les comptes utilisateurs de l’outil  
B. Visualiser graphiquement les liens et dépendances entre équipements pour faciliter le diagnostic  
C. Chiffrer les flux SNMP  
D. Remplacer la documentation réseau  

**6. Dans un système de métrologie, pourquoi est-il crucial d’horodater précisément toutes les mesures (NTP synchronisé) ?**  
A. Pour réduire l’espace disque occupé  
B. Pour pouvoir corréler correctement les événements et les performances à travers plusieurs équipements et outils  
C. Pour se passer de sauvegardes  
D. Pour éviter les pannes matérielles  

**7. Sur une sonde de supervision, quel type de mesure est le plus pertinent pour détecter un début de saturation de lien WAN ?**  
A. Le nombre de sessions SSH  
B. Le pourcentage d’utilisation bande passante (in/out) couplé à la latence et la perte de paquets  
C. Le nombre d’utilisateurs connectés à l’Active Directory  
D. Le nombre de ports ouverts sur le firewall  

**8. Quel est l’avantage principal d’utiliser des templates ou modèles de supervision pour des familles d’équipements (switch Cisco, firewall Fortinet, etc.) ?**  
A. Empêcher toute personnalisation des alertes  
B. Standardiser les métriques, seuils et checks, et accélérer le déploiement sur de nombreux équipements  
C. Réduire les besoins en stockage  
D. Supprimer la nécessité de MIB SNMP  

**9. Concernant SNMP, quel est le rôle principal des MIB (Management Information Base) ?**  
A. Chiffrer les échanges SNMP  
B. Décrire la structure et les OID des objets supervisables sur un équipement  
C. Stocker les logs des utilisateurs  
D. Générer automatiquement des rapports PDF  

**10. Dans un environnement supervisé, quel est le risque majeur de configurer des notifications trop nombreuses ou mal filtrées (alert fatigue) ?**  
A. Surcharge du processeur des routeurs  
B. Les équipes ignorent ou manquent les vraies alertes critiques noyées dans le bruit  
C. Impossibilité d’historiser les données  
D. Blocage automatique des comptes administrateurs  

**11. Quel type d’outil est le plus adapté pour centraliser et analyser de grands volumes de logs réseau et systèmes (recherches, corrélations, tableaux de bord) ?**  
A. Un serveur DHCP  
B. Une stack de type ELK/Opensearch, Graylog ou équivalent  
C. Un serveur FTP  
D. Un proxy web  

**12. Dans une architecture de supervision distribuée, pourquoi déployer plusieurs pollers/satellites proches des sites distants ?**  
A. Pour consommer plus de licences  
B. Pour réduire la latence des interrogations et limiter la dépendance au WAN  
C. Pour remplacer les routeurs distants  
D. Pour se passer de chiffrement  

**13. Quel est l’objectif principal de la “capacity planning” (planification de capacité) basée sur les données de métrologie ?**  
A. Désactiver les alertes non critiques  
B. Anticiper les besoins d’augmentation de bande passante, CPU, RAM, stockage avant saturation  
C. Réduire le nombre de switches dans l’infrastructure  
D. Simplifier le plan d’adressage IP  

**14. Sur un outil de supervision moderne, quel est l’intérêt de disposer d’un système de tags/labels sur les métriques et hôtes (par site, par rôle, par criticité) ?**  
A. Rendre les noms d’hôtes plus longs  
B. Filtrer, agréger et construire des tableaux de bord dynamiques adaptés aux différents besoins (réseau, systèmes, sécurité, métier)  
C. Empêcher la suppression d’anciens hôtes  
D. Chiffrer les données de métrologie  

**15. Quel mécanisme de supervision est le plus pertinent pour vérifier la disponibilité d’un site web d’entreprise ?**  
A. Ping ICMP uniquement sur l’adresse IP du serveur  
B. Un check applicatif HTTP/HTTPS simulant une vraie requête et vérifiant le code de retour et le contenu  
C. Un simple traceroute  
D. Une requête SNMP sur le switch d’accès  

**16. Dans la chaîne de traitement d’une alerte réseau, quelle étape est la plus critique pour réduire le temps moyen de résolution (MTTR) ?**  
A. Générer un rapport mensuel PDF  
B. Déclencher une notification claire, contextualisée et orientée action vers les bonnes équipes  
C. Augmenter le nombre de seuils sur toutes les métriques  
D. Rebooter systématiquement les équipements concernés  

**17. Pourquoi est-il pertinent de superviser non seulement l’infrastructure (switches, routeurs, firewalls) mais aussi les services critiques (DNS, DHCP, LDAP, applicatifs) ?**  
A. Pour remplacer les tests utilisateurs  
B. Pour avoir une vision de bout en bout de la chaîne de service et détecter les impacts métiers  
C. Pour se passer de documentation  
D. Pour éviter de sécuriser les accès administrateurs  

**18. Quel est le risque principal de faire tourner la plateforme de supervision sur une seule machine virtuelle sans redondance ni sauvegarde ?**  
A. Aucune, la supervision n’est jamais critique  
B. Perte de visibilité sur l’infrastructure en cas de panne, perte d’historique et de capacité de diagnostic  
C. Augmentation des performances réseau  
D. Suppression automatique des anciennes alertes  

**19. Dans un contexte d’ITIL/gestion de services, à quoi sert principalement la corrélation entre incidents, changements et données de supervision ?**  
A. À augmenter la complexité du système  
B. À comprendre l’impact des changements, identifier les causes racines et améliorer en continu l’infrastructure  
C. À remplacer les sauvegardes  
D. À bloquer les utilisateurs non techniques  

**20. Lors de la mise en place d’un nouveau système de supervision réseau, quelle bonne pratique est la plus pertinente parmi les suivantes ?**  
A. Activer toutes les métriques et toutes les alertes par défaut sur tous les équipements  
B. Définir une stratégie progressive : périmètre prioritaire, criticité, seuils adaptés, tests, documentation et formation des équipes  
C. Limiter la supervision aux seuls liens Internet  
D. Ne jamais mettre à jour la solution de supervision une fois installée  

