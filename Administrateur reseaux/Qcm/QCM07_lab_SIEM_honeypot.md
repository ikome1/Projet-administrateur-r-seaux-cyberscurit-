## QCM 07 – Lab SIEM et honeypot (niveau difficile)

### Consignes
- 20 questions à choix multiples.  
- Une seule bonne réponse par question (sauf indication contraire).  
- Niveau : administrateur réseau / sécurité confirmé.

---

**1. Quel est l’objectif principal d’un SIEM dans une infrastructure d’entreprise ?**  
A. Héberger les bases de données métier  
B. Centraliser, corréler et analyser les événements de sécurité pour détecter des incidents et y répondre plus vite  
C. Remplacer le firewall périmétrique  
D. Gérer les adresses IP des serveurs  

**2. Dans un SIEM, que représente le plus souvent une “corrélation de règles” (correlation rule) ?**  
A. Une sauvegarde automatique  
B. Une logique qui combine plusieurs événements ou conditions pour générer une alerte plus significative qu’un log isolé  
C. Un mécanisme de chiffrement des logs  
D. Un outil de supervision de la température des serveurs  

**3. Quel est le rôle principal d’un honeypot dans un lab de sécurité ?**  
A. Héberger la production  
B. Attirer et analyser les attaques pour mieux comprendre les techniques adverses et améliorer la détection  
C. Fournir un service de backup  
D. Remplacer les serveurs web réels  

**4. Pourquoi est‑il fortement déconseillé de connecter un honeypot non maîtrisé au même segment réseau que les systèmes de production sans isolation ?**  
A. Parce qu’il ne produira pas de logs  
B. Parce qu’un honeypot compromis peut servir de pivot pour attaquer la production  
C. Parce que cela empêche les sauvegardes  
D. Parce que cela casse le DNS  

**5. Dans un lab SIEM, pourquoi est‑il important de normaliser les logs provenant de différentes sources (firewalls, OS, applications) ?**  
A. Pour remplir plus vite la base de données  
B. Pour pouvoir effectuer des recherches et corrélations cohérentes sur des champs communs (IP source, user, action, etc.)  
C. Pour réduire la granularité des événements  
D. Pour supprimer les informations de contexte  

**6. Quel protocole est couramment utilisé pour envoyer des logs depuis un équipement réseau vers un SIEM ou un collecteur de logs ?**  
A. SNMP Trap  
B. Syslog  
C. FTP  
D. IMAP  

**7. Dans un scénario de détection, quel type de règle SIEM est le plus adapté pour repérer un scan de port agressif depuis une même adresse IP ?**  
A. Une règle qui ignore tout trafic provenant d’Internet  
B. Une règle qui compte un nombre élevé de tentatives de connexion sur de multiples ports dans une fenêtre de temps réduite  
C. Une règle basée uniquement sur la taille des paquets  
D. Une règle regardant uniquement les erreurs disque sur les serveurs  

**8. Quel est l’intérêt principal de disposer de timestamps synchronisés (NTP) sur toutes les sources de logs dans un contexte SIEM ?**  
A. Économiser de la bande passante  
B. Permettre une corrélation temporelle fiable entre événements issus de systèmes différents  
C. Accélérer les mises à jour  
D. Supprimer le besoin de filtrage  

**9. Dans un lab honeypot, pourquoi est‑il intéressant de déployer à la fois des honeypots de bas interaction et de haute interaction ?**  
A. Pour compliquer la facturation  
B. Pour combiner volume de collecte (bas interaction) et profondeur d’analyse (haute interaction)  
C. Pour empêcher la collecte de malwares  
D. Pour remplacer le SIEM  

**10. Quel est le risque principal si les flux de logs vers le SIEM ne sont pas chiffrés ni authentifiés sur un réseau potentiellement hostile ?**  
A. Une baisse des performances du SIEM  
B. Un attaquant peut intercepter ou injecter de faux événements, compromettant l’intégrité et la confidentialité des logs  
C. Un blocage des sauvegardes  
D. Une impossibilité de consulter les tableaux de bord  

**11. Dans un lab SIEM, quel type de données complémentaire aux logs bruts améliore fortement les capacités de détection avancée ?**  
A. La météo du jour  
B. Les flux de NetFlow/sFlow, les données de threat intelligence (IoC, listes noires), les inventaires d’actifs  
C. Les historiques de navigation personnelle des administrateurs  
D. Les mots de passe en clair des utilisateurs  

**12. Quel est l’objectif principal de la rétention à long terme des logs de sécurité dans un SIEM ?**  
A. Remplir le stockage au maximum  
B. Permettre des analyses forensiques, la conformité réglementaire et l’étude des tendances sur des périodes longues  
C. Augmenter le nombre d’alertes inutiles  
D. Remplacer les sauvegardes de bases de données  

**13. Dans un lab honeypot, pourquoi est‑il important de séparer fortement l’environnement de capture et l’environnement d’analyse ?**  
A. Pour compliquer l’administration  
B. Pour réduire le risque que des artefacts malveillants capturés dans le honeypot compromettent aussi les outils d’analyse  
C. Pour diminuer la quantité de logs  
D. Pour empêcher la corrélation avec le SIEM  

**14. Quel est l’intérêt principal de rejouer dans un SIEM des journaux d’attaques observés sur un honeypot ?**  
A. Tester et améliorer les règles de détection, les tableaux de bord et les scénarios de réponse à incident  
B. Réduire l’espace disque  
C. Supprimer les anciennes règles de corrélation  
D. Tester la bande passante du réseau  

**15. Dans un environnement SIEM de production, pourquoi faut‑il limiter l’accès aux dashboards et requêtes sensibles (contenant des données personnelles ou critiques) ?**  
A. Pour réduire le nombre d’utilisateurs  
B. Pour respecter le principe du moindre privilège, la confidentialité et la conformité réglementaire  
C. Pour empêcher toute investigation  
D. Pour simplifier la configuration des alertes  

**16. Quel est l’impact principal d’une mauvaise gestion de la volumétrie de logs (trop ou pas assez) sur un SIEM ?**  
A. Aucun impact significatif  
B. Soit saturation de la plateforme et perte d’événements, soit trous dans la visibilité empêchant une détection fiable  
C. Une augmentation automatique de la puissance de calcul  
D. Une suppression magique des faux positifs  

**17. Dans un lab SIEM, quel type d’exercice permet de tester l’efficacité globale de la chaîne de détection et de réponse ?**  
A. Un simple test de ping  
B. Un exercice de type purple team/red team, injectant des scénarios d’attaque réalistes et observant la détection/réponse  
C. Un envoi massif d’e‑mails légitimes  
D. Un redémarrage des serveurs de logs  

**18. Pourquoi est‑il intéressant de déployer un honeypot “high‑value” simulant un contrôleur de domaine ou un serveur de base de données critique ?**  
A. Pour héberger les données réelles de production  
B. Pour attirer des attaquants plus avancés et observer des techniques plus sophistiquées  
C. Pour remplacer l’AD réel  
D. Pour désactiver le firewall  

**19. Dans un SIEM, quel est l’avantage principal d’utiliser des tableaux de bord dédiés par rôle (réseau, systèmes, sécurité, métier) ?**  
A. Multiplier les écrans inutiles  
B. Fournir à chaque équipe les vues les plus pertinentes pour son périmètre, sans noyer les utilisateurs sous des informations hors sujet  
C. Empêcher le partage d’informations entre équipes  
D. Remplacer la documentation  

**20. Lors de la mise en place d’un lab SIEM et honeypot pour la formation et l’expérimentation, quelle bonne pratique est la plus pertinente parmi les suivantes ?**  
A. Le connecter directement en production sans filtrage  
B. Isoler l’environnement, documenter les scénarios, collecter et analyser les données, et intégrer les leçons apprises dans la production  
C. Désactiver la journalisation pour ne pas remplir le disque  
D. Utiliser des comptes administrateurs de production dans le lab  

