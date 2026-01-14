## QCM 10 – Sauvegardes et Plan de Reprise d’Activité (PRA) – niveau difficile

### Consignes
- 20 questions à choix multiples.  
- Une seule bonne réponse par question (sauf indication contraire).  
- Niveau : administrateur systèmes et réseaux confirmé.

---

**1. Quelle est la différence principale entre PRA (Plan de Reprise d’Activité) et PCA (Plan de Continuité d’Activité) ?**  
A. Le PRA vise la continuité sans interruption, le PCA gère le redémarrage après incident  
B. Le PCA vise la continuité ou la dégradation maîtrisée pendant l’incident, le PRA vise le redémarrage/la reconstruction après sinistre  
C. Ils sont strictement identiques  
D. Le PRA est uniquement technique, le PCA uniquement organisationnel  

**2. Que représentent les indicateurs RPO et RTO dans le contexte des plans de sauvegarde et PRA ?**  
A. RPO = temps de redémarrage, RTO = quantité de données perdues  
B. RPO = point de restauration maximal acceptable (perte de données), RTO = temps maximal pour rétablir le service  
C. RPO = nombre d’utilisateurs impactés, RTO = bande passante minimale  
D. RPO = capacité de stockage, RTO = nombre de sauvegardes par jour  

**3. Dans une stratégie de sauvegarde, quelle est l’idée principale de la règle “3‑2‑1” ?**  
A. 3 sauvegardes par jour, 2 sites, 1 type de support  
B. 3 copies des données, sur 2 types de supports différents, dont au moins 1 hors site  
C. 3 années de rétention, 2 mois de rotation, 1 jour de test  
D. 3 administrateurs, 2 serveurs, 1 robot de bandes  

**4. Quel est le risque principal d’avoir des sauvegardes accessibles en écriture depuis les mêmes comptes/serveurs que la production ?**  
A. Aucune conséquence  
B. En cas de ransomware ou de compromission de compte, les sauvegardes peuvent aussi être chiffrées ou supprimées  
C. Une augmentation du temps de sauvegarde  
D. Un blocage des utilisateurs  

**5. Pourquoi les sauvegardes “air‑gapped” (déconnectées ou très isolées du réseau) sont‑elles considérées comme plus robustes contre les ransomwares ?**  
A. Parce qu’elles sont plus rapides  
B. Parce qu’un malware n’a pas de chemin direct pour chiffrer ou manipuler ces copies  
C. Parce qu’elles ne nécessitent pas de supervision  
D. Parce qu’elles ne demandent jamais de maintenance  

**6. Dans une politique de sauvegarde, quelle combinaison illustre le mieux l’usage des sauvegardes complètes, différentielles et incrémentales ?**  
A. Que des complètes tous les jours  
B. Complète hebdo, incrémentales quotidiennes, et éventuellement différentielles intermédiaires selon les besoins  
C. Que des incrémentales sans complète  
D. Que des différentielles sans complète  

**7. Quel est l’objectif principal des tests de restauration réguliers ?**  
A. Vérifier uniquement les temps de sauvegarde  
B. S’assurer que les sauvegardes sont réellement exploitables, complètes, cohérentes et que les procédures fonctionnent  
C. Remplir plus vite l’espace de stockage  
D. Réduire la fréquence des sauvegardes  

**8. Dans un PRA, pourquoi est‑il crucial de définir un ordre de priorité (ordre de redémarrage) des services ?**  
A. Pour redémarrer en même temps tous les services  
B. Pour concentrer les efforts sur les services critiques métier d’abord, en tenant compte des dépendances techniques  
C. Pour se conformer au protocole TCP  
D. Pour réduire la taille des sauvegardes  

**9. Quel est le risque principal si la documentation PRA n’est pas à jour ou pas accessible en cas de crise ?**  
A. Une baisse de la consommation électrique  
B. Un allongement massif des délais de reprise, des erreurs de manipulation et une perte de crédibilité vis‑à‑vis des métiers  
C. Une augmentation automatique de la bande passante  
D. Une suppression des sauvegardes anciennes  

**10. Dans une stratégie de sauvegarde de bases de données, quel élément est souvent nécessaire en plus des fichiers de données pour une restauration point‑dans‑le‑temps ?**  
A. Les fichiers de cache navigateur  
B. Les journaux de transactions (logs) permettant de rejouer les opérations jusqu’à un instant donné  
C. Les fichiers temporaires du système  
D. Les profils utilisateurs  

**11. Pourquoi est‑il important de prendre en compte la sauvegarde et la reprise des configurations réseau (firewalls, routeurs, switches) dans un PRA ?**  
A. Parce que ces équipements n’ont pas besoin de configuration  
B. Parce que sans ces configurations, même si les serveurs sont restaurés, le trafic ne pourra pas circuler correctement  
C. Pour augmenter l’espace de stockage utilisé  
D. Pour compliquer la gestion des sauvegardes  

**12. Dans un scénario de catastrophe majeure, quel est l’avantage d’avoir un site de secours “chaud” (hot site) par rapport à un site “froid” (cold site) ?**  
A. Coût plus faible  
B. Temps de reprise beaucoup plus court, car l’infrastructure est déjà en grande partie prête et synchronisée  
C. Aucun, ils sont équivalents  
D. Nécessité d’aucune supervision  

**13. Quel est le risque principal d’une stratégie de sauvegarde qui ne couvre que les serveurs virtuels mais pas les stockages partagés ni les configurations d’hyperviseur ?**  
A. Augmentation des performances de sauvegarde  
B. Impossibilité de reconstruire correctement l’environnement en cas de sinistre complet de l’infrastructure de virtualisation  
C. Doublement automatique des sauvegardes  
D. Problèmes d’adressage IP  

**14. Dans un PRA, que signifie l’expression “mode dégradé” ?**  
A. Un mode où aucun service ne fonctionne  
B. Un mode où certains services sont réduits ou simplifiés, mais qui permet de maintenir un minimum d’activité critique  
C. Un mode réservé uniquement aux tests  
D. Un mode où l’on arrête volontairement les sauvegardes  

**15. Pourquoi la classification des données (confidentielles, sensibles, critiques, etc.) est‑elle importante pour la stratégie de sauvegarde/PRA ?**  
A. Pour augmenter la longueur des étiquettes  
B. Pour adapter la fréquence, la rétention, les moyens de protection et les exigences de reprise selon la criticité  
C. Pour supprimer certaines sauvegardes jugées inutiles  
D. Pour limiter le chiffrement aux données publiques  

**16. Quel est l’intérêt principal de chiffrer les sauvegardes stockées hors site ou dans le cloud ?**  
A. Réduire le temps de sauvegarde  
B. Protéger la confidentialité des données en cas de vol ou d’accès non autorisé au support ou au fournisseur  
C. Supprimer la nécessité d’authentification  
D. Remplacer les contrôles d’accès  

**17. Dans un PRA, pourquoi est‑il important d’inclure aussi les aspects organisationnels (communication, décision, responsabilités) et pas seulement techniques ?**  
A. Parce que la technique n’a aucun rôle  
B. Parce qu’en situation de crise, la coordination, la décision rapide et la communication avec les métiers sont essentielles pour une reprise efficace  
C. Pour compliquer la documentation  
D. Pour réduire le nombre de sauvegardes  

**18. Quel est l’impact principal d’une mauvaise prise en compte de la bande passante disponible entre site de production et site de secours dans une réplication de données ?**  
A. Aucune conséquence  
B. Des retards de réplication, des RPO non respectés et un risque de saturation du lien  
C. Une réduction automatique des données stockées  
D. Une augmentation du débit Internet pour les utilisateurs  

**19. Pourquoi est‑il pertinent de séparer les rôles entre administrateurs de production et administrateurs des sauvegardes/PRA (ou au minimum de séparer les comptes) ?**  
A. Pour compliquer la vie des équipes  
B. Pour limiter l’impact d’une compromission de compte et appliquer le principe du moindre privilège également sur les systèmes de sauvegarde  
C. Pour empêcher les tests de restauration  
D. Pour réduire la fréquence des sauvegardes  

**20. Lors de la mise en place ou la refonte d’une stratégie de sauvegardes et de PRA, quelle bonne pratique est la plus pertinente parmi les suivantes ?**  
A. Se contenter de sauvegarder “au mieux” sans objectifs définis  
B. Définir avec les métiers les RPO/RTO, cartographier les dépendances, choisir les technologies adaptées, tester régulièrement et mettre à jour le plan  
C. Ne pas formaliser le plan pour rester “agile”  
D. Supprimer les anciennes sauvegardes sans contrôle  

