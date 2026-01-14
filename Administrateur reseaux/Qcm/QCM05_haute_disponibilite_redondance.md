## QCM 05 – Haute disponibilité et redondance (niveau difficile)

### Consignes
- 20 questions à choix multiples.  
- Une seule bonne réponse par question (sauf indication contraire).  
- Niveau : administrateur réseau confirmé.

---

**1. Quelle est la différence principale entre haute disponibilité (HA) et tolérance de panne (fault tolerance) ?**  
A. La haute disponibilité supporte zéro interruption, la tolérance de panne accepte des coupures longues  
B. La tolérance de panne vise un fonctionnement sans interruption perceptible lors d’une panne matérielle, la HA accepte une courte interruption de service  
C. Ce sont deux termes strictement équivalents  
D. La haute disponibilité concerne uniquement le réseau, la tolérance de panne uniquement les serveurs  

**2. Dans une architecture réseau, quel est l’objectif principal de la redondance “N+1” ?**  
A. Doubler systématiquement tous les équipements  
B. Avoir au moins un composant de secours capable de prendre le relais en cas de panne d’un composant actif  
C. Supprimer les SPOF uniquement côté applicatif  
D. Réduire la consommation électrique  

**3. Dans une configuration de bascule de routeur/pare-feu (VRRP/HSRP/CARP), que représente l’adresse IP/ MAC virtuelle ?**  
A. Une adresse inutilisée  
B. Une identité de passerelle partagée qui peut être portée successivement par différents équipements  
C. Une adresse MAC matérielle gravée en usine  
D. Une adresse réservée au management hors bande  

**4. Quel paramètre est critique pour réduire le temps de bascule (failover) dans un cluster de firewalls en HA active/passive ?**  
A. La taille du disque dur  
B. La synchronisation de l’état des sessions et la détection rapide de défaillance (timers, hello)  
C. La présence d’un serveur DHCP  
D. La version du navigateur des administrateurs  

**5. Dans une architecture à deux liens Internet redondants (multi‑homing), quel protocole de routage dynamique est le plus adapté pour une vraie redondance de connectivité publique ?**  
A. OSPF interne uniquement  
B. BGP avec les opérateurs  
C. RIP v1  
D. STP  

**6. Quel est le risque principal d’une redondance mal conçue (boucles, dépendances cachées) ?**  
A. Une réduction automatique de la latence  
B. Une complexité accrue pouvant mener à des pannes globales plus graves qu’avec une architecture simple  
C. Une impossibilité totale de faire du NAT  
D. Un blocage des sauvegardes  

**7. Dans une architecture de haute disponibilité de serveurs applicatifs, quel élément est indispensable pour éviter un SPOF côté stockage ?**  
A. Un unique NAS très puissant sans redondance interne  
B. Un stockage redondé (RAID, double contrôleur, multi‑chemins, réplication)  
C. Un disque dur externe USB  
D. Un partage de fichiers non sauvegardé  

**8. Concernant le RAID, quelle affirmation est correcte ?**  
A. Le RAID remplace entièrement les sauvegardes  
B. Le RAID améliore la disponibilité et/ou les performances, mais ne protège pas contre la suppression logique ou la corruption globale des données  
C. Le RAID empêche toute panne disque  
D. Le RAID est inutile en production  

**9. Dans une architecture à trois couches réseau, où place‑t‑on en général la redondance la plus critique ?**  
A. Au niveau des postes utilisateurs uniquement  
B. Au niveau du cœur et de la distribution, avec liens redondants et équipements doublés  
C. Uniquement sur les switches d’accès  
D. Uniquement sur les imprimantes réseau  

**10. Quel indicateur représente le mieux la disponibilité d’un service sur une année (en %) ?**  
A. Le MTBF uniquement  
B. Le pourcentage de temps de fonctionnement (ex : 99,9 %, 99,99 %) dérivé du temps total de panne  
C. Le débit maximal théorique du lien  
D. Le nombre de tickets ouverts au support  

**11. Parmi les propositions suivantes, laquelle correspond à un SPOF (Single Point of Failure) typique dans un réseau d’entreprise ?**  
A. Deux firewalls en cluster actif/passif  
B. Un seul switch de cœur sans redondance ni lien alternatif  
C. Un lien fibre vers chaque bâtiment  
D. Deux routeurs BGP vers deux opérateurs différents  

**12. Quel est l’intérêt principal de la redondance géographique (site principal + site de secours) pour un service critique ?**  
A. Réduire la complexité de l’architecture  
B. Se protéger contre les sinistres majeurs affectant un site complet (incendie, inondation, coupure électrique prolongée)  
C. Éviter d’avoir un PRA  
D. Éviter les sauvegardes quotidiennes  

**13. Dans un cluster de load‑balancing de serveurs applicatifs, quel est l’avantage d’utiliser des vérifications de santé applicatives (health checks) avancées ?**  
A. Augmenter la latence des utilisateurs  
B. Sortir automatiquement du pool les nœuds qui ne répondent plus correctement au niveau applicatif (et pas seulement au ping)  
C. Supprimer les journaux d’erreurs  
D. Se passer de supervision  

**14. Quel est le risque principal si la configuration de deux équipements en HA n’est pas strictement synchronisée (firmware, paramètres, licences) ?**  
A. Une augmentation de la disponibilité  
B. Un comportement différent en cas de bascule, avec des règles de sécurité ou de routage incohérentes  
C. Une réduction des besoins en sauvegarde  
D. Une impossibilité d’activer les logs  

**15. Dans une architecture active/active de firewalls, que faut‑il surveiller particulièrement ?**  
A. Le nombre d’imprimantes installées  
B. La répartition de charge, la cohérence de session, les flux asymétriques et la compatibilité des modules de sécurité (IPS, proxy)  
C. La couleur des voyants LED  
D. Le nombre de comptes locaux  

**16. Quel est le rôle principal d’un protocole comme LACP (802.3ad) dans une architecture de redondance de liens ?**  
A. Chiffrer le trafic utilisateur  
B. Agréger plusieurs liens physiques en un lien logique pour la redondance et l’augmentation de bande passante  
C. Remplacer le protocole STP  
D. Fournir des adresses IP virtuelles  

**17. En pratique, pourquoi ne peut‑on pas viser un SLA de 100 % de disponibilité réelle sur un service complexe ?**  
A. Parce que les protocoles réseau ne le permettent pas  
B. Parce qu’il existe toujours des risques résiduels (pannes matérielles, logiciels, humaines, catastrophes) et des besoins de maintenance  
C. Parce que les utilisateurs n’en ont pas besoin  
D. Parce que les SLA sont interdits contractuellement  

**18. Quel est l’objectif principal d’un test de bascule régulier (DR drill) dans une architecture haute disponibilité ?**  
A. Prouver que la documentation est inutile  
B. Vérifier en conditions réelles que les mécanismes de bascule et de reprise fonctionnent comme prévu  
C. Dégrader volontairement la performance  
D. Désactiver les sauvegardes pendant le test  

**19. Dans la conception d’une architecture HA, pourquoi est-il important d’éviter les dépendances cachées (DNS, NTP, authentification, stockage) non redondées ?**  
A. Parce qu’elles augmentent le débit réseau  
B. Parce qu’une panne de ces services peut rendre la HA inopérante malgré la redondance apparente des composants principaux  
C. Parce qu’elles empêchent la supervision  
D. Parce qu’elles bloquent le load‑balancing  

**20. Lors de la mise en place d’une nouvelle architecture de haute disponibilité pour les services réseau, quelle bonne pratique est la plus pertinente parmi les suivantes ?**  
A. Se concentrer uniquement sur la redondance des liens Internet  
B. Cartographier l’ensemble des dépendances, identifier les SPOF, définir des objectifs de disponibilité réalistes et tester régulièrement les scénarios de panne  
C. Désactiver la journalisation pour gagner en performance  
D. Ne pas informer les équipes métier de l’existence du site de secours  

