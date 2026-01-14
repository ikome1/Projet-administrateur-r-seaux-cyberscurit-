## QCM 04 – VPN site à site et accès distant (niveau difficile)

### Consignes
- 20 questions à choix multiples.  
- Une seule bonne réponse par question (sauf indication contraire).  
- Niveau : administrateur réseau confirmé.

---

**1. Quel est l’avantage principal d’un VPN IPSec site à site par rapport à un simple tunnel GRE non chiffré ?**  
A. IPSec est plus simple à configurer  
B. IPSec fournit chiffrement, intégrité et authentification des paquets  
C. GRE ne permet pas d’encapsuler du trafic multicast  
D. IPSec ne consomme aucune ressource CPU  

**2. Dans une architecture IPSec, quelle combinaison de protocoles est typiquement utilisée pour transporter le trafic chiffré en mode tunnel ?**  
A. TCP 443 uniquement  
B. ESP (protocole 50) et éventuellement AH  
C. ICMP et ARP  
D. HTTP et HTTPS  

**3. Quelle est la différence principale entre un VPN SSL pour accès distant et un VPN IPSec site à site classique ?**  
A. Le VPN SSL ne peut pas fonctionner derrière un NAT  
B. Le VPN SSL est généralement orienté accès utilisateur distant via navigateur ou client, IPSec site à site relie deux réseaux entiers  
C. IPSec est obligatoirement en mode split‑tunnel  
D. Le VPN SSL ne chiffre pas réellement les données  

**4. Dans une configuration IPSec, à quoi sert la Phase 1 (IKEv2/IKEv1) ?**  
A. À chiffrer directement le trafic utilisateur  
B. À établir un canal sécurisé (SA IKE) pour négocier les paramètres de la Phase 2  
C. À configurer les routes statiques  
D. À gérer le DNS  

**5. Quel est l’avantage principal de l’authentification par certificats (PKI) plutôt que par pre‑shared key (PSK) pour un grand nombre de tunnels VPN ?**  
A. Moins de charge CPU sur les firewalls  
B. Meilleure scalabilité et gestion centralisée des identités, révocation plus fine  
C. Nécessité de moins de ports ouverts  
D. Pas besoin de gérer les dates d’expiration  

**6. Dans un scénario d’accès distant, qu’est‑ce que le “split‑tunneling” ?**  
A. Forcer tout le trafic (Internet + entreprise) dans le tunnel VPN  
B. Envoyer uniquement le trafic destiné au réseau de l’entreprise dans le tunnel, le reste allant directement vers Internet  
C. Créer deux tunnels simultanés vers le même site  
D. Chiffrer le trafic uniquement côté serveur  

**7. Quel risque de sécurité peut introduire le split‑tunneling mal maîtrisé pour un VPN d’accès distant ?**  
A. Une augmentation du débit disponible pour l’utilisateur  
B. Un poste client compromis peut servir de pont entre Internet et le réseau interne  
C. L’impossibilité d’utiliser le DNS interne  
D. La saturation automatique du lien VPN  

**8. Dans une architecture VPN multi‑sites, quel est l’avantage principal d’utiliser un hub‑and‑spoke plutôt qu’un full‑mesh complet ?**  
A. Suppression du besoin de routage  
B. Réduction du nombre de tunnels à configurer et à maintenir  
C. Aucune dépendance au site central  
D. Possibilité de se passer de chiffrement  

**9. Quel mécanisme est le plus approprié pour transporter dynamiquement les routes à travers un tunnel IPSec entre deux firewalls ?**  
A. Utiliser uniquement des routes statiques  
B. Utiliser un protocole de routage dynamique (OSPF, BGP) au-dessus du tunnel  
C. Utiliser ARP  
D. Utiliser DHCP  

**10. Pour un VPN SSL d’accès distant, pourquoi est-il recommandé d’intégrer l’authentification au système central (AD/LDAP, MFA) plutôt que d’utiliser des comptes locaux au firewall ?**  
A. Pour rendre la configuration plus compliquée  
B. Pour centraliser la gestion des identités, appliquer des politiques de mot de passe cohérentes et faciliter les révocations  
C. Pour empêcher toute journalisation  
D. Pour éviter d’utiliser du chiffrement fort  

**11. Quel est l’impact principal d’un chiffrement fort (AES‑256, SHA‑2) sur les performances d’un tunnel VPN IPSec ?**  
A. Aucun, le chiffrement est toujours gratuit en ressources  
B. Une consommation CPU plus élevée sur les équipements, pouvant limiter le débit si pas d’accélération matérielle  
C. Une impossibilité de passer à travers les NAT  
D. Un besoin systématique de bande passante supplémentaire  

**12. Dans un VPN IPSec, que permet le mode “Perfect Forward Secrecy” (PFS) ?**  
A. Réduire le temps de négociation  
B. Garantir que la compromission d’une clé à long terme ne permette pas de déchiffrer les sessions passées  
C. Supprimer la nécessité de certificats  
D. Éviter les attaques par déni de service  

**13. Quel est l’intérêt principal de journaliser finement les connexions VPN (qui, quand, d’où, vers quoi) ?**  
A. Générer plus de stockage inutile  
B. Permettre les audits, la traçabilité, les enquêtes en cas d’incident et la détection d’anomalies  
C. Se passer de supervision réseau  
D. Remplacer les sauvegardes  

**14. Dans un scénario où des utilisateurs itinérants se connectent à un VPN d’accès distant, quelle bonne pratique réseau améliore la sécurité globale ?**  
A. Autoriser tout trafic “any‑any” une fois connecté  
B. Appliquer le principe du moindre privilège avec des ACL par groupe d’utilisateurs, et éventuellement une inspection du poste (posture check)  
C. Ne pas journaliser les connexions  
D. Désactiver l’authentification forte  

**15. Quel protocole est souvent utilisé pour encapsuler le trafic d’accès distant au-dessus de TLS afin de traverser plus facilement les pare-feux et proxys ?**  
A. L2TP seul  
B. OpenVPN ou équivalent utilisant TCP/UDP 443  
C. Telnet  
D. FTP  

**16. Dans une liaison VPN site à site entre deux firewalls, que faut‑il vérifier en priorité si le tunnel monte mais que les réseaux distants ne se pinguent pas ?**  
A. Le fuseau horaire des utilisateurs  
B. Les routes et les politiques de sécurité (ACL/Policy) de part et d’autre  
C. La version de l’antivirus des postes clients  
D. Le mot de passe Wi‑Fi  

**17. Quel est l’avantage principal d’un client VPN “always‑on” intégré au poste (par exemple via GPO) par rapport à une connexion manuelle de l’utilisateur ?**  
A. Plus de consommation de batterie  
B. Assurer que la machine est protégée et jointe au SI dès le démarrage, sans dépendre de l’action de l’utilisateur  
C. Impossibilité de déconnecter le VPN  
D. Nécessité de plusieurs comptes locaux  

**18. Dans une entreprise multi‑sites utilisant des VPN, pourquoi est-il important de réfléchir au routage asymétrique et aux chemins de retour ?**  
A. Pour augmenter le temps de convergence  
B. Car certains firewalls ou IPS peuvent bloquer des flux dont le chemin retour ne repasse pas par le même équipement, générant des comportements inattendus  
C. Pour réduire la sécurité du VPN  
D. Pour désactiver le chiffrement IPSec  

**19. Quel mécanisme de haute disponibilité est souvent utilisé pour assurer la continuité d’un service VPN sur deux firewalls en cluster ?**  
A. VRRP/HSRP/CARP ou cluster propriétaire avec partage d’état de session  
B. Un simple ping  
C. Un serveur FTP redondant  
D. Un cache DNS local  

**20. Lors de la mise en place d’une nouvelle infrastructure VPN (site à site + accès distant), quelle bonne pratique est la plus pertinente parmi les suivantes ?**  
A. Utiliser les valeurs par défaut sans revue de sécurité  
B. Documenter précisément la topologie, les paramètres cryptographiques, les règles d’accès, l’authentification et les procédures de dépannage  
C. Partager la même clé pré‑partagée pour tous les tunnels et tous les utilisateurs  
D. Désactiver les journaux pour gagner en performances  

