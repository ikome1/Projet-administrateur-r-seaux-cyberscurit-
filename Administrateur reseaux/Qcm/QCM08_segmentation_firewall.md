## QCM 08 – Segmentation réseau et firewalling (niveau difficile)

### Consignes
- 20 questions à choix multiples.  
- Une seule bonne réponse par question (sauf indication contraire).  
- Niveau : administrateur réseau / sécurité confirmé.

---

**1. Quel est l’objectif principal de la segmentation réseau dans une entreprise ?**  
A. Augmenter le nombre total d’adresses IP disponibles  
B. Limiter les mouvements latéraux d’un attaquant et réduire l’impact d’un incident de sécurité  
C. Supprimer le besoin de routage  
D. Simplifier le plan d’adressage  

**2. Entre les différents types de zones réseau ci‑dessous, laquelle illustre le mieux une architecture raisonnable pour une application web exposée ?**  
A. Tout dans un seul VLAN interne  
B. Zone DMZ pour le frontal web, zone interne applicative, zone base de données, chacune filtrée par firewall  
C. Serveur web directement sur Internet sans firewall  
D. Serveur de base de données dans la DMZ  

**3. Dans une politique de firewall, que signifie concrètement le principe “deny by default” (ou whitelisting) ?**  
A. Tout est autorisé sauf quelques flux explicitement bloqués  
B. Tout est bloqué par défaut, seuls les flux explicitement autorisés sont permis  
C. Seuls les flux sortants sont bloqués  
D. Seuls les flux entrants sont bloqués  

**4. Quel est le risque principal d’une politique firewall trop permissive (any‑any) entre VLAN internes ?**  
A. Une baisse de la latence  
B. Un attaquant ou un malware peut se déplacer librement entre segments et accéder à des ressources critiques  
C. Une impossibilité d’utiliser SNMP  
D. Une panne immédiate du réseau  

**5. Dans une architecture moderne de segmentation, que signifie le concept de “micro‑segmentation” ?**  
A. Créer un VLAN par utilisateur  
B. Appliquer des politiques de contrôle d’accès très fines au niveau workload/VM/conteneur, pas seulement par sous‑réseau  
C. Supprimer tous les firewalls périmétriques  
D. Utiliser uniquement des routeurs sans ACL  

**6. Quel type de règle firewall est le plus adapté pour autoriser un serveur applicatif interne à interroger un serveur de base de données sur un port précis ?**  
A. Source : any / Destination : any / Port : any / Action : allow  
B. Source : IP serveur applicatif / Destination : IP base de données / Port : TCP spécifique / Action : allow  
C. Source : any / Destination : IP base de données / Port : any / Action : allow  
D. Source : IP base de données / Destination : IP serveur applicatif / Port : any / Action : allow  

**7. Pourquoi est‑il important de documenter les règles de firewall (justification, propriétaire, application concernée) ?**  
A. Pour allonger la documentation inutilement  
B. Pour pouvoir maintenir, auditer, nettoyer les règles obsolètes et comprendre l’impact de tout changement  
C. Pour désactiver la supervision  
D. Pour supprimer les sauvegardes de configuration  

**8. Dans une architecture multi‑tiers, quel rôle joue principalement un firewall applicatif (WAF) par rapport à un firewall traditionnel de couche 3/4 ?**  
A. Il remplace complètement le firewall réseau  
B. Il inspecte les requêtes HTTP/HTTPS au niveau applicatif (couche 7) pour détecter des attaques (XSS, SQLi, etc.)  
C. Il gère uniquement le NAT  
D. Il sert de serveur DNS  

**9. Quel est le risque d’un inter‑VLAN routing réalisé sur un switch de niveau 3 sans aucune ACL ni politique de sécurité ?**  
A. Aucun risque particulier  
B. Tous les VLAN peuvent communiquer librement, annulant la logique de segmentation  
C. Le spanning‑tree est désactivé  
D. Le DHCP ne fonctionne plus  

**10. Dans une politique de segmentation, pourquoi est‑il pertinent de séparer les postes utilisateurs, les serveurs, les imprimantes, l’IoT et les équipements d’administration ?**  
A. Pour respecter les recommandations de câblage  
B. Parce que ces types d’équipements ont des profils de risque, de trafic et de sécurité très différents  
C. Pour économiser des adresses IP  
D. Pour augmenter le nombre de VLAN au maximum  

**11. Quel est l’avantage principal d’un firewall de nouvelle génération (NGFW) par rapport à un firewall traditionnel ?**  
A. Il ne fait pas de NAT  
B. Il ajoute l’inspection applicative, le contrôle par utilisateur/groupe, l’IPS, le filtrage URL, etc.  
C. Il remplace le DNS  
D. Il n’a pas besoin de règles  

**12. Dans une architecture de segmentation, pourquoi est‑il essentiel de prendre en compte aussi les flux sortants (egress filtering) ?**  
A. Les flux sortants sont toujours sûrs  
B. Pour empêcher les exfiltrations de données, les communications vers des C2 malveillants et les accès non maîtrisés à Internet  
C. Pour réduire le trafic entrant  
D. Pour économiser des adresses publiques  

**13. Quel mécanisme est généralement utilisé sur les firewalls pour gérer des ensembles d’adresses ou de services réutilisables dans plusieurs règles ?**  
A. Les scripts Bash  
B. Les objets (adresses, groupes, services, groupes de services)  
C. Les fichiers texte externes non référencés  
D. Les clés SSH  

**14. Dans une DMZ bien conçue, où devraient se trouver les bases de données contenant des données sensibles ?**  
A. Dans la DMZ, accessibles directement depuis Internet  
B. Dans un réseau interne sécurisé, accessible uniquement depuis les serveurs applicatifs autorisés  
C. Sur les postes utilisateurs  
D. Sur un stockage cloud public sans contrôle d’accès  

**15. Pourquoi est‑il important de tester régulièrement les règles de firewall (revues, audits, tests de pénétration) ?**  
A. Pour augmenter le nombre de règles  
B. Pour vérifier que la politique implémentée correspond toujours aux besoins métiers et aux exigences de sécurité, et qu’aucune faille majeure n’a été introduite  
C. Pour désactiver les logs  
D. Pour simplifier la topologie réseau  

**16. Dans une politique de firewall, que signifie l’expression “shadow rule” (règle ombrée) ?**  
A. Une règle invisible pour les administrateurs  
B. Une règle qui n’est jamais appliquée car une règle précédente plus large capture déjà tout son trafic  
C. Une règle en maintenance  
D. Une règle chiffrée  

**17. Quel est l’impact principal d’une segmentation réseau insuffisante sur un incident de type ransomware ?**  
A. Aucun impact  
B. Le malware peut se propager très rapidement à un grand nombre de systèmes, augmentant massivement l’ampleur de l’incident  
C. Il empêche le chiffrement des données  
D. Il protège automatiquement les sauvegardes  

**18. Dans une architecture multi‑sites, comment la segmentation réseau peut‑elle aider à limiter les risques ?**  
A. En reliant tous les sites dans un seul VLAN  
B. En définissant des zones par site, par fonction, et en contrôlant strictement les flux inter‑sites via des firewalls et des VPN  
C. En désactivant le routage  
D. En utilisant uniquement des hubs  

**19. Quel est l’intérêt principal de combiner segmentation réseau et contrôle d’accès au niveau poste (agent EDR/NAC) ?**  
A. Aucun, ces deux approches sont redondantes  
B. Renforcer la défense en profondeur : même si un attaquant franchit une barrière, il rencontre des contrôles supplémentaires au niveau endpoint  
C. Supprimer l’utilisation de pare‑feu  
D. Remplacer la supervision réseau  

**20. Lors de la mise en place d’une nouvelle politique de segmentation et de firewalling, quelle bonne pratique est la plus pertinente parmi les suivantes ?**  
A. Tout bloquer brutalement puis voir ce qui casse en production  
B. Cartographier les flux existants, définir des zones et règles cibles, tester progressivement, impliquer les équipes métier et documenter  
C. Configurer une seule règle any‑any pour commencer  
D. Ne pas conserver d’historique des modifications  

