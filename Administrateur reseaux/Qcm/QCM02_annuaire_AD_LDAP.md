## QCM 02 – Annuaire Active Directory / LDAP (niveau difficile)

### Consignes
- 20 questions à choix multiples.  
- Une seule bonne réponse par question (sauf indication contraire).  
- Niveau : administrateur systèmes et réseaux confirmé.

---

**1. Dans une forêt Active Directory, quel est le rôle principal du schéma (Schema) ?**  
A. Stocker les mots de passe des utilisateurs  
B. Définir les classes d’objets et leurs attributs utilisables dans tout le domaine  
C. Gérer les stratégies de groupe (GPO)  
D. Assurer la réplication inter‑sites  

**2. Quelle affirmation décrit le mieux la différence entre LDAP et Active Directory ?**  
A. LDAP est un protocole, Active Directory est une implémentation d’annuaire qui l’utilise  
B. LDAP est un système d’exploitation, Active Directory est un routeur  
C. LDAP remplace Active Directory  
D. LDAP est uniquement utilisé pour le DNS  

**3. Dans un environnement AD, quel contrôleur possède une responsabilité unique et ne peut être détenu que par un seul serveur par forêt ?**  
A. PDC Emulator  
B. RID Master  
C. Domain Naming Master  
D. Infrastructure Master  

**4. Quel est l’intérêt principal de configurer des Sites Active Directory correctement (basés sur les sous-réseaux IP) ?**  
A. Améliorer le temps de réponse DNS  
B. Optimiser la réplication AD et l’authentification en fonction de la topologie réseau physique  
C. Augmenter le nombre maximal d’utilisateurs par domaine  
D. Éviter de devoir utiliser des GPO  

**5. Dans LDAP, quel élément identifie de manière unique un objet dans l’arborescence ?**  
A. Le nom NetBIOS  
B. Le Distinguished Name (DN)  
C. L’adresse IP du contrôleur de domaine  
D. Le nom du site AD  

**6. Quel protocole est couramment utilisé pour sécuriser les communications LDAP entre un client et un serveur ?**  
A. LDAP en clair est toujours sécurisé par défaut  
B. LDAPS (LDAP sur TLS/SSL)  
C. FTPES  
D. Telnet  

**7. Dans Active Directory, quelle est la fonction principale des OU (Organizational Units) ?**  
A. Remplacer les groupes de sécurité  
B. Organiser logiquement les objets et appliquer des GPO de manière ciblée  
C. Créer des sous-réseaux IP  
D. Servir de zones DNS secondaires  

**8. Quel est l’objectif principal des GPO (Group Policy Objects) dans un domaine AD ?**  
A. Distribuer les mises à jour antivirus  
B. Déployer et appliquer des configurations et paramètres de sécurité de façon centralisée  
C. Gérer la réplication entre contrôleurs de domaine  
D. Créer de nouveaux domaines enfants  

**9. Dans un environnement multi‑sites, quel risque entraîne une mauvaise configuration de la réplication entre contrôleurs de domaine ?**  
A. Une montée en charge automatique du stockage  
B. Des divergences de mot de passe, d’appartenance aux groupes et d’objets AD entre sites  
C. L’impossibilité totale de se connecter localement sur les postes  
D. La suppression automatique des anciens DC  

**10. Quel mécanisme AD est le plus adapté pour déléguer certaines tâches d’administration (ex : réinitialisation de mot de passe) à une équipe de support sans leur donner des droits Domain Admin ?**  
A. Ajout systématique au groupe “Administrateurs du domaine”  
B. Délégation de contrôle sur des OU spécifiques  
C. Activation du mode “God mode” AD  
D. Ajout dans le groupe “Schema Admins”  

**11. Dans un annuaire LDAP, quel type d’objet est généralement utilisé pour représenter un groupe de sécurité ?**  
A. `organizationalUnit`  
B. `groupOfNames` ou un équivalent spécifique à l’implémentation (ex : `group` dans AD)  
C. `inetOrgPerson`  
D. `device`  

**12. Quel est l’avantage principal d’utiliser l’authentification centralisée via AD/LDAP pour des services comme VPN, Wi‑Fi d’entreprise ou applications web internes (SSO) ?**  
A. Réduire le nombre de serveurs DNS nécessaires  
B. Centraliser identités et droits, simplifier la gestion des comptes et les révocations  
C. Empêcher toute connexion hors ligne  
D. Supprimer la nécessité de sauvegardes  

**13. Dans Active Directory, à quoi sert le rôle FSMO PDC Emulator ?**  
A. À stocker les schémas d’objets  
B. À gérer la compatibilité avec les anciens domaines NT4, la synchronisation de l’heure et certaines opérations liées aux mots de passe  
C. À créer automatiquement les OU  
D. À chiffrer la base NTDS.dit  

**14. Lors de la conception d’un annuaire AD pour une grande entreprise, quelle bonne pratique parmi les suivantes est la plus pertinente ?**  
A. Créer le plus de domaines possibles pour chaque service  
B. Limiter le nombre de domaines et structurer surtout avec des OU et des groupes  
C. Mettre tous les comptes dans le conteneur “Users” par défaut  
D. Ne jamais documenter la structure logique  

**15. Dans un contexte LDAP, lequel des éléments suivants est le plus critique pour la haute disponibilité de l’authentification ?**  
A. Avoir plusieurs serveurs DHCP  
B. Avoir plusieurs serveurs d’annuaire répliqués et un mécanisme de bascule côté clients/applications  
C. Avoir un seul serveur d’annuaire très puissant  
D. Avoir un serveur web dédié pour la documentation  

**16. Quel type de groupe AD est le plus approprié pour attribuer des permissions à des ressources d’un même domaine (partages, applications) tout en respectant les bonnes pratiques AGDLP ?**  
A. Groupes globaux pour les autorisations, groupes locaux pour les comptes utilisateurs  
B. Groupes globaux pour regrouper les utilisateurs, groupes locaux de domaine pour porter les permissions  
C. Groupes universels uniquement  
D. Groupes de distribution uniquement  

**17. Lorsqu’un poste membre d’un domaine se connecte, quel service AD est principalement utilisé pour authentifier l’utilisateur ?**  
A. DHCP  
B. Kerberos (et éventuellement NTLM en fallback)  
C. SNMP  
D. SMTP  

**18. Quelle est la conséquence principale d’un mauvais paramétrage de l’horloge (NTP) entre les contrôleurs de domaine et les clients ?**  
A. Une baisse des performances réseau  
B. Des échecs d’authentification Kerberos et des erreurs de sécurité  
C. Une corruption de la base DNS  
D. Un arrêt automatique des contrôleurs de domaine  

**19. Dans un environnement AD, pourquoi faut-il limiter au maximum le nombre de comptes ayant des privilèges Domain Admin / Enterprise Admin ?**  
A. Parce que ces comptes ne peuvent pas se connecter sur les serveurs  
B. Parce que ces comptes ne peuvent pas être surveillés  
C. Parce que leur compromission donne un contrôle quasi total sur l’infrastructure  
D. Parce qu’ils ne peuvent pas changer leur mot de passe  

**20. Dans la mise en place d’un nouveau domaine Active Directory, quelle bonne pratique est la plus pertinente parmi les suivantes ?**  
A. Utiliser un nom de domaine interne identique au domaine public externe sans réflexion  
B. Planifier soigneusement le nommage, la structure des OU, la stratégie de groupes et la redondance des DC  
C. Tout mettre dans une seule OU “Entreprise” pour simplifier  
D. Ne pas mettre de sauvegardes spécifiques pour les DC  

