## QCM 06 – Hardening et sécurisation des serveurs (niveau difficile)

### Consignes
- 20 questions à choix multiples.  
- Une seule bonne réponse par question (sauf indication contraire).  
- Niveau : administrateur systèmes et réseaux confirmé.

---

**1. Quel est l’objectif principal du hardening d’un serveur ?**  
A. Augmenter les performances graphiques  
B. Réduire la surface d’attaque en limitant les services, ports et composants inutiles  
C. Simplifier la configuration réseau  
D. Supprimer le besoin de supervision  

**2. Quelle bonne pratique de base s’applique à tous les comptes administrateurs locaux sur les serveurs ?**  
A. Utiliser le même mot de passe partout pour simplifier  
B. Désactiver les comptes inutilisés et appliquer des mots de passe forts, distincts et renouvelés  
C. Partager le mot de passe dans l’équipe sur un fichier texte  
D. Ne jamais activer la journalisation des connexions  

**3. Sur un serveur Linux exposé, pourquoi est‑il recommandé de désactiver l’authentification par mot de passe SSH au profit des clés ?**  
A. Pour empêcher l’accès root  
B. Pour réduire significativement le risque de réussite des attaques par brute force et vol de mot de passe  
C. Pour accélérer la connexion graphique  
D. Pour ne plus avoir besoin de firewall  

**4. Dans une politique de hardening, quel est l’intérêt principal de limiter au maximum les services écoutant sur des interfaces réseau publiques ?**  
A. Réduire la latence  
B. Diminuer la surface d’exposition aux attaques à distance  
C. Empêcher les sauvegardes réseau  
D. Simplifier le routage  

**5. Sur un serveur Windows membre d’un domaine, quel outil ou mécanisme est le plus utilisé pour appliquer un durcissement cohérent à grande échelle ?**  
A. Les stratégies de groupe (GPO)  
B. Un fichier texte partagé  
C. Un script batch isolé  
D. Le panneau de configuration uniquement  

**6. Pourquoi est-il important de segmenter les rôles (ex : serveur AD, serveur web, serveur base de données) plutôt que de tout regrouper sur un seul serveur ?**  
A. Pour augmenter la consommation de licences  
B. Pour limiter l’impact en cas de compromission et faciliter l’application de politiques de sécurité spécifiques à chaque rôle  
C. Pour rendre le dépannage plus difficile  
D. Pour empêcher les sauvegardes cohérentes  

**7. Quel est l’intérêt principal d’un mécanisme de journalisation centralisée (SIEM ou équivalent) pour le hardening des serveurs ?**  
A. Désactiver les logs locaux  
B. Corréler les événements de sécurité, détecter des comportements anormaux et disposer de preuves en cas d’incident  
C. Supprimer la nécessité de mises à jour  
D. Empêcher les redémarrages planifiés  

**8. Sur un serveur web, quel en‑tête HTTP est couramment utilisé pour réduire certains risques liés au contenu exécuté côté client (XSS, clickjacking, etc.) ?**  
A. `Server: Apache`  
B. `Content-Security-Policy`  
C. `Host`  
D. `User-Agent`  

**9. Dans une démarche de hardening, que signifie le principe du “moindre privilège” ?**  
A. Donner les droits administrateurs à tout le monde pour limiter les incidents de droits  
B. Accorder à chaque compte/service uniquement les permissions strictement nécessaires à sa fonction  
C. Supprimer tous les comptes non‑administrateurs  
D. Interdire l’utilisation de l’authentification forte  

**10. Pourquoi est‑il dangereux de travailler régulièrement avec le compte root (ou Administrator) directement sur un serveur en production ?**  
A. Parce que ces comptes ne fonctionnent pas à distance  
B. Parce que toute erreur peut avoir un impact global, et qu’il est plus difficile de tracer précisément qui a fait quoi  
C. Parce que cela empêche l’utilisation de SSH  
D. Parce que ces comptes ne peuvent pas changer de mot de passe  

**11. Quel type de mécanisme est particulièrement utile pour limiter les dégâts en cas d’exploitation d’une vulnérabilité sur un service (confinement) ?**  
A. Héberger tous les services sur la même machine  
B. Isolation par conteneurs/VM, sandboxing, et séparation stricte des comptes de service  
C. Exécution de tous les services en tant que root  
D. Désactivation de tous les logs  

**12. Concernant les mises à jour de sécurité des serveurs, quelle approche est la plus adaptée en production ?**  
A. Ne jamais mettre à jour pour éviter les changements  
B. Mettre à jour sans aucun test ou créneau de maintenance  
C. Planifier des fenêtres de maintenance, tester sur des environnements de pré‑production et appliquer rapidement les correctifs critiques  
D. Mettre à jour uniquement les serveurs de test  

**13. Sur un serveur de base de données, quelle bonne pratique s’impose en matière d’accès réseaux ?**  
A. Ouvrir le port de la base à Internet pour permettre le télétravail  
B. Restreindre l’accès à des segments réseau spécifiques (applicatifs, administration) via firewall  
C. Ouvrir le port à tout le LAN sans restriction  
D. Utiliser le compte “sa” ou “root” pour toutes les applications  

**14. Pourquoi est‑il recommandé de désactiver ou restreindre fortement les services de bureau à distance (RDP, VNC) exposés sur Internet ?**  
A. Parce qu’ils consomment trop de CPU  
B. Parce qu’ils constituent une cible privilégiée pour les attaques par brute force, ransomwares et exploitation de vulnérabilités  
C. Parce qu’ils ne supportent pas le chiffrement  
D. Parce qu’ils empêchent l’utilisation de VPN  

**15. Dans une politique de mots de passe serveur, quel compromis est le plus raisonnable actuellement ?**  
A. Mots de passe très courts mais changés toutes les semaines  
B. Mots de passe longs et complexes, rotation raisonnable, et MFA quand c’est possible  
C. Mots de passe simples, jamais changés  
D. Mots de passe partagés entre tous les administrateurs  

**16. Quel est l’avantage principal de l’utilisation systématique du chiffrement disque (Full Disk Encryption) sur les serveurs sensibles ?**  
A. Accélérer les performances d’E/S  
B. Protéger les données en cas de vol ou d’accès physique non autorisé aux supports de stockage  
C. Supprimer le besoin de sauvegardes  
D. Rendre inutile l’authentification  

**17. Dans la configuration d’un serveur, pourquoi faut‑il limiter les binaires et scripts pouvant être exécutés avec des privilèges élevés (SUID root, tâches planifiées) ?**  
A. Pour gagner de l’espace disque  
B. Parce qu’ils peuvent être détournés pour escalader les privilèges en cas de vulnérabilité ou mauvaise configuration  
C. Parce que cela empêche l’administration à distance  
D. Parce que cela bloque le DHCP  

**18. Quel est l’objectif principal de la mise en place de bannières légales sur les services d’accès (SSH, RDP, console web) ?**  
A. Décourager les utilisateurs légitimes  
B. Informer clairement sur les conditions d’utilisation, l’enregistrement des activités et fournir un support juridique en cas d’incident  
C. Accélérer la connexion  
D. Remplacer les journaux d’audit  

**19. Dans une démarche de hardening continue, quelle activité est essentielle en complément des guides de configuration sécurisée (CIS, ANSSI, Microsoft Baselines, etc.) ?**  
A. Ignorer les alertes de sécurité  
B. Réaliser régulièrement des scans de vulnérabilité et des audits de configuration  
C. Supprimer les mises à jour automatiques  
D. Désactiver la supervision  

**20. Lors de la mise en place d’une politique de hardening serveurs dans une entreprise, quelle bonne pratique est la plus pertinente parmi les suivantes ?**  
A. Appliquer brutalement un modèle unique à tous les serveurs sans concertation  
B. Définir des standards par rôle, tester sur un périmètre pilote, documenter, former les équipes et intégrer le hardening au cycle de vie des systèmes  
C. Laisser chaque administrateur appliquer ses propres règles au cas par cas  
D. Ne pas impliquer la direction ni les équipes de sécurité  

