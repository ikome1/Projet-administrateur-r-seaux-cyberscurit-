## QCM 05 – Sécurité applicative Web (niveau intermédiaire/avancé)

### Consignes
- 20 questions, difficulté intermédiaire/avancée.  
- Une seule bonne réponse.

---

**1. L’OWASP Top 10 est :**  
A. Une liste de protocoles réseaux  
B. Un classement des 10 vulnérabilités web les plus critiques  
C. Un standard de chiffrement  
D. Une norme ISO  

**2. Une injection SQL permet à un attaquant de :**  
A. Chiffrer la base de données  
B. Exécuter des requêtes SQL non prévues par l’application  
C. Modifier le mot de passe root du système  
D. Changer l’adresse IP du serveur  

**3. Un XSS (Cross-Site Scripting) réfléchi se produit quand :**  
A. Le script malveillant est stocké dans la base de données  
B. Le script est renvoyé directement dans la réponse à partir des paramètres de la requête  
C. Le script est exécuté côté serveur  
D. Le script modifie la configuration du pare-feu  

**4. Pour se protéger des injections SQL, la bonne pratique est :**  
A. Construire les requêtes avec de la concaténation de chaînes  
B. Utiliser des requêtes préparées (requêtes paramétrées)  
C. Désactiver la base de données  
D. Chiffrer tout le code source  

**5. Le CSRF (Cross-Site Request Forgery) exploite :**  
A. La confiance de l’utilisateur dans un site malveillant  
B. La confiance du site dans le navigateur de l’utilisateur (sessions, cookies)  
C. Les faiblesses du protocole TLS  
D. Les faiblesses du DNS  

**6. Une bonne protection contre CSRF est :**  
A. Un simple chiffrement de la base de données  
B. L’utilisation de tokens CSRF uniques par session/formulaire  
C. L’utilisation d’IPv6  
D. Le changement de port HTTP  

**7. L’en-tête HTTP `Content-Security-Policy` (CSP) sert principalement à :**  
A. Forcer le chiffrement du trafic  
B. Limiter les sources autorisées de scripts, styles, images, etc.  
C. Gérer la mise en cache  
D. Configurer les cookies de session  

**8. Un cookie de session sécurisé doit au minimum être :**  
A. Non chiffré et accessible par JavaScript  
B. Marqué `HttpOnly` et `Secure` (si HTTPS)  
C. Partagé entre plusieurs domaines non liés  
D. Stocké côté client en clair dans un fichier texte  

**9. Une mauvaise gestion des identités et des accès (Broken Access Control) permet :**  
A. De ralentir l’application  
B. À un utilisateur d’accéder à des ressources qu’il ne devrait pas voir  
C. De casser TLS  
D. De saturer le CPU  

**10. Dans une architecture REST, l’authentification par token (JWT) mal implémentée peut mener à :**  
A. Des problèmes de routage  
B. Des détournements de session et escalades de privilèges  
C. Un simple bug d’affichage  
D. Une baisse du débit réseau  

**11. Le stockage de mots de passe en base doit se faire :**  
A. En clair pour simplifier la récupération  
B. Sous forme de hash forts avec salt et éventuellement “pepper”  
C. Dans un Excel sur le serveur  
D. Dans les logs applicatifs  

**12. Une exposition d’API non documentée (Shadow API) peut :**  
A. Ne jamais être exploitée  
B. Exposer des fonctions sensibles sans contrôles suffisants  
C. Accélérer l’application  
D. Améliorer la supervision  

**13. La désérialisation non sécurisée (Insecure Deserialization) permet souvent :**  
A. De chiffrer les logs  
B. D’exécuter du code arbitraire côté serveur  
C. De bloquer les sauvegardes  
D. De corrompre uniquement l’interface graphique  

**14. L’énumération d’identifiants utilisateurs est possible si :**  
A. L’appli renvoie des messages d’erreur différents selon que l’utilisateur existe ou non  
B. Les mots de passe sont chiffrés  
C. Tous les comptes sont désactivés  
D. Les sessions expirent  

**15. Un scanner DAST (Dynamic Application Security Testing) agit :**  
A. Sur le code source directement  
B. Sur l’application en cours d’exécution, en envoyant des requêtes malveillantes  
C. Sur le réseau uniquement  
D. Sur le système d’exploitation  

**16. Un scanner SAST (Static Application Security Testing) agit :**  
A. Sur le réseau  
B. Sur l’application en boîte noire  
C. Sur le code source ou bytecode sans exécution  
D. Sur les logs  

**17. Les secrets (clés API, mots de passe…) dans le code source doivent être :**  
A. Commités dans GitHub mais en branch privée  
B. Stockés dans un gestionnaire de secrets dédié  
C. Envoyés par e‑mail à l’équipe  
D. Ignorés car ils sont chiffrés par défaut  

**18. Un “IDOR” (Insecure Direct Object Reference) survient lorsque :**  
A. On utilise TLS 1.3  
B. L’appli permet d’accéder à des objets via un identifiant non suffisamment contrôlé  
C. Le serveur redémarre  
D. Le pare-feu est configuré  

**19. L’exfiltration de données via une API est facilitée si :**  
A. Les quotas, limites de débit et contrôles d’accès sont faibles ou absents  
B. Les logs sont activés  
C. Les certificats sont valides  
D. Les sauvegardes sont régulières  

**20. Une bonne politique de “Security by Design” impose :**  
A. De penser à la sécurité uniquement en phase de test  
B. D’intégrer la sécurité dès la conception et tout au long du cycle de vie  
C. De gérer la sécurité uniquement par le RSSI  
D. D’ignorer les retours d’audit externes  

