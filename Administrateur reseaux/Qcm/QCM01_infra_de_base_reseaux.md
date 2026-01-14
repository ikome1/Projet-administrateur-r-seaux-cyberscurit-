## QCM 01 – Infrastructure réseau de base (niveau difficile)

### Consignes
- 20 questions à choix multiples.  
- Une seule bonne réponse par question (sauf indication contraire).  
- Niveau : administrateur réseau confirmé.

---

**1. Sur un commutateur géré, quel est l’intérêt principal de configurer des VLAN 802.1Q ?**  
A. Augmenter le débit physique des ports  
B. Segmenter logiquement le réseau de niveau 2 pour isoler les domaines de broadcast  
C. Chiffrer le trafic entre les postes clients  
D. Remplacer la nécessité d’un routage de niveau 3  

**2. Sur un lien trunk 802.1Q entre deux switches, que se passe-t-il si les VLAN configurés ne correspondent pas de part et d’autre ?**  
A. Le lien se met automatiquement en mode access  
B. Seuls les VLAN communs configurés de part et d’autre passeront correctement  
C. Tous les VLAN seront transportés sans distinction  
D. Le trunk sera automatiquement désactivé  

**3. Dans un plan d’adressage IPv4, quel est le principal avantage d’utiliser un masque /30 sur un lien point à point entre deux routeurs ?**  
A. Maximiser le nombre d’adresses utilisables sur le lien  
B. Réduire le nombre d’adresses utilisables pour limiter le gaspillage  
C. Permettre le multicast natif  
D. Autoriser le VLSM uniquement sur ce lien  

**4. Quelle affirmation décrit le mieux la différence entre une adresse IP privée RFC1918 et une adresse IP publique ?**  
A. Une adresse privée ne peut jamais être routée  
B. Une adresse privée doit être traduite (NAT) pour être atteignable sur Internet  
C. Une adresse publique n’a pas besoin de passer par un routeur  
D. Une adresse publique est toujours statique  

**5. Dans un réseau d’entreprise, quel est l’impact principal d’un trop grand domaine de broadcast (trop de machines dans le même VLAN) ?**  
A. Augmentation de la latence due aux collisions CSMA/CD  
B. Saturation de la table ARP et du trafic de broadcast, pouvant impacter les performances  
C. Impossibilité de faire du routage inter-VLAN  
D. Blocage des trames DHCP Discover  

**6. Sur un switch moderne en full‑duplex, quel type de problème les collisions provoquées par CSMA/CD causent-elles ?**  
A. De fortes pertes de paquets sur tous les ports  
B. Aucune, CSMA/CD n’est plus utilisé en full‑duplex  
C. Un redémarrage automatique du switch  
D. Une désactivation du spanning‑tree  

**7. Dans une topologie avec plusieurs switches redondants, quel est le rôle principal du protocole Spanning Tree (STP/RSTP) ?**  
A. Équilibrer la charge sur tous les liens  
B. Éviter les boucles de niveau 2 en bloquant certains ports tout en maintenant la redondance  
C. Chiffrer les trames entre les commutateurs  
D. Attribuer dynamiquement des adresses IP aux hôtes  

**8. Lorsqu’un poste client envoie une requête ARP “Who has 192.168.10.1 ?”, quelle est la réponse correcte d’un routeur configuré comme passerelle par défaut sur ce réseau ?**  
A. Il ignore toujours les requêtes ARP  
B. Il répond avec sa propre adresse IP  
C. Il répond avec son adresse MAC associée à 192.168.10.1  
D. Il envoie une redirection ICMP vers un autre routeur  

**9. Sur un réseau IPv4, lequel des éléments suivants est indispensable pour qu’un hôte puisse joindre un réseau distant (autre sous‑réseau) ?**  
A. Une adresse MAC statique  
B. Une passerelle par défaut correctement configurée  
C. Un DNS secondaire  
D. Un serveur NTP  

**10. Sur une infrastructure de commutation, à quoi sert principalement la table CAM (MAC address table) d’un switch ?**  
A. À router les paquets IP  
B. À associer les adresses MAC aux ports physiques pour commuter les trames de façon ciblée  
C. À mémoriser les noms de domaine des machines  
D. À stocker les ACL de sécurité  

**11. Si un switch ne connaît pas l’adresse MAC de destination d’une trame unicast, que fait-il ?**  
A. Il la supprime  
B. Il l’envoie uniquement sur le port de la passerelle par défaut  
C. Il la flood sur tous les ports du VLAN concerné sauf le port d’origine  
D. Il lance une requête ARP  

**12. Dans une architecture réseau d’entreprise, quel est l’avantage principal de séparer les VLAN utilisateurs, serveurs et management ?**  
A. Réduire le nombre de routeurs nécessaires  
B. Appliquer des politiques de sécurité et de QoS différentes selon les types de flux  
C. Rendre inutile la supervision réseau  
D. Simplifier la numérotation des ports physiques  

**13. Quelle est la fonction principale d’un serveur DHCP dans une infrastructure réseau de base ?**  
A. Fournir uniquement l’adresse IP au client  
B. Fournir dynamiquement des paramètres réseau (IP, masque, passerelle, DNS, etc.) aux clients  
C. Chiffrer le trafic entre le client et le routeur  
D. Remplacer le rôle du DNS  

**14. Dans un environnement avec plusieurs VLAN, où place-t-on généralement le service DHCP pour une architecture propre et scalable ?**  
A. Sur chaque poste client  
B. Sur un commutateur non géré  
C. Sur un serveur central ou un routeur/pare-feu, avec relais DHCP (IP helper) sur les VLAN distants  
D. Sur le même switch que le routeur mais sans configuration particulière  

**15. Quel est le rôle principal d’un routeur dans une infrastructure réseau de base ?**  
A. Connecter des segments de niveau 2 identiques  
B. Router les paquets IP entre des réseaux ou sous‑réseaux différents  
C. Convertir les trames Ethernet en trames Wi‑Fi  
D. Fournir des adresses MAC aux équipements  

**16. Lorsqu’un hôte envoie un paquet à une machine d’un autre réseau, comment le paquet est-il transmis au niveau 2 sur le premier saut ?**  
A. Avec l’adresse MAC de destination de la machine distante  
B. Avec l’adresse MAC de destination de la passerelle par défaut  
C. Avec une adresse MAC de broadcast  
D. Avec une adresse MAC nulle  

**17. Dans la conception d’une infrastructure réseau de base, pourquoi est-il recommandé d’utiliser un adressage structuré par VLAN/site/service (ex : 10.10.X.Y) ?**  
A. Pour rendre les IP plus jolies à lire  
B. Pour faciliter le résumé de routes, la supervision et le dépannage  
C. Pour éviter complètement les collisions  
D. Pour se passer de documentation  

**18. Quel est l’objectif principal du NAT dans un réseau d’entreprise connecté à Internet ?**  
A. Remplacer le routage interne  
B. Permettre à plusieurs adresses privées de partager une ou plusieurs adresses publiques  
C. Augmenter la bande passante sur le lien opérateur  
D. Chiffrer toutes les communications  

**19. Dans une architecture classique à trois couches (accès, distribution, cœur), quel est l’intérêt principal de cette hiérarchisation ?**  
A. Réduire le nombre de VLAN possibles  
B. Améliorer l’évolutivité, la redondance et la maîtrise des domaines de panne  
C. Se passer de routage inter‑VLAN  
D. Simplifier la configuration des postes utilisateurs  

**20. Lors de la mise en place d’une nouvelle infrastructure réseau de base, quelle bonne pratique est la plus pertinente parmi les suivantes ?**  
A. Utiliser un seul VLAN pour tous les équipements pour simplifier  
B. Documenter le plan d’adressage, les VLAN, les rôles des équipements et les liaisons physiques  
C. Ne rien documenter pour éviter les fuites d’informations  
D. Désactiver STP pour gagner en performance  

