## QCM 08 – Sécurité Cloud et conteneurs (niveau avancé+)

### Consignes
- 20 questions, niveau avancé+.  
- Une seule bonne réponse par question.

---

**1. Le modèle de “responsabilité partagée” en Cloud signifie que :**  
A. Le fournisseur Cloud est responsable de tout  
B. Le client est responsable de tout  
C. Certaines couches sont gérées par le fournisseur, d’autres par le client  
D. Personne n’est responsable en cas d’incident  

**2. Dans un modèle IaaS, le client est typiquement responsable de :**  
A. La sécurité physique du datacenter  
B. Le matériel et l’hyperviseur  
C. Les OS, middleware, applications et données  
D. Les fibres optiques entre data centers  

**3. Un bucket de stockage (ex : S3) mal configuré peut exposer :**  
A. Uniquement des logs internes  
B. Des données sensibles publiquement sur Internet  
C. Seulement des métadonnées inoffensives  
D. Rien d’important  

**4. Les rôles IAM larges de type `*:*` (full admin) sont problématiques car :**  
A. Ils simplifient trop l’administration  
B. Ils violent le principe du moindre privilège et augmentent le risque de compromission  
C. Ils bloquent l’accès aux ressources  
D. Ils ne sont acceptés que pour des comptes de service  

**5. Un Security Group (AWS) ou NSG (Azure) sert à :**  
A. Gérer les comptes utilisateurs  
B. Filtrer les flux réseau (pare-feu de niveau VM/service)  
C. Chiffrer les disques  
D. Gérer les licences logicielles  

**6. Dans Kubernetes, un “namespace” permet :**  
A. De créer un cluster physique séparé  
B. De segmenter logiquement et isoler des ressources au sein d’un cluster  
C. De chiffrer les secrets  
D. De gérer le stockage  

**7. Les “secrets” Kubernetes devraient être :**  
A. Stockés en clair dans les manifestes YAML commités dans Git  
B. Chiffrés et gérés via un gestionnaire de secrets (KMS, Vault, etc.)  
C. Envoyés par e‑mail aux développeurs  
D. Partagés sur un chat d’équipe  

**8. Dans un environnement conteneurisé, une image Docker contenant des vulnérabilités doit être :**  
A. Ignorée si l’appli fonctionne  
B. Scannée (SCA) et corrigée (mise à jour des dépendances, base images)  
C. Déployée uniquement en test  
D. Protégée par un antivirus classique  

**9. Une mauvaise isolation des conteneurs peut permettre :**  
A. Une meilleure performance  
B. Des évasions de conteneur (container escape) vers l’hôte  
C. Une meilleure journalisation  
D. Une réduction des coûts  

**10. L’utilisation de rôles IAM attachés aux machines (instance profiles) plutôt qu’à des clés statiques dans le code permet :**  
A. De simplifier les attaques  
B. De réduire le risque de fuite de clés dans le code  
C. D’empêcher l’authentification  
D. D’augmenter la latence  

**11. L’outil “CloudTrail” (AWS) ou équivalent sert principalement à :**  
A. Gérer le stockage  
B. Journaliser les appels d’API et actions d’administration  
C. Gérer les DNS  
D. Chiffrer les buckets  

**12. Dans un cluster Kubernetes, l’accès à l’API Server doit être :**  
A. Ouvert à tous sur Internet  
B. Restreint et protégé (auth forte, réseau, RBAC)  
C. Désactivé  
D. Protégé uniquement par mot de passe faible  

**13. Le principe d’immutabilité des infrastructures (Infrastructure as Code + images immuables) contribue à la sécurité car :**  
A. Il facilite les accès non contrôlés  
B. Il permet de recréer à l’identique des environnements propres et contrôlés  
C. Il empêche toute mise à jour  
D. Il rend les logs inutiles  

**14. Un “pod security policy” ou équivalent (Pod Security Standards) sert à :**  
A. Gérer la QoS  
B. Limiter ce que les pods peuvent faire (privilèges, volumes, hostNetwork, etc.)  
C. Configurer le load balancing  
D. Gérer les quotas CPU  

**15. Les métadonnées d’instance (ex: `169.254.169.254` sur AWS) sont sensibles car :**  
A. Elles ne contiennent jamais d’info utile  
B. Elles peuvent contenir des tokens/infos d’auth pour les services Cloud  
C. Elles sont toujours chiffrées  
D. Elles sont inaccessibles depuis les VMs  

**16. Une fuite de clé d’accès Cloud avec plein de droits peut mener à :**  
A. Rien, les logs protègent  
B. La prise de contrôle des ressources Cloud, exfiltration données, minage crypto, etc.  
C. Un simple avertissement  
D. Un redémarrage automatique des VM  

**17. L’isolation réseau entre “tiers” (web / app / DB) dans le Cloud doit être :**  
A. Ignorée car les services sont managés  
B. Réalisée via VPC, sous-réseaux, Security Groups/NSG, pare-feux  
C. Remplacée par un seul gros réseau à plat  
D. Gérée uniquement par DNS  

**18. Un registre d’images privé (Container Registry) doit être :**  
A. Public pour faciliter le déploiement  
B. Restreint (auth, droits finement gérés) et scanner les images  
C. Non journalisé  
D. Utilisé uniquement en dev  

**19. Les “serverless functions” (FaaS) présentent des risques si :**  
A. On configure bien les permissions par fonction  
B. On utilise des permissions globales et peu de journalisation  
C. On les déploie derrière une API Gateway  
D. On active les logs d’exécution  

**20. Une bonne stratégie de sécurité multi-Cloud inclut :**  
A. Des configurations différentes et non documentées sur chaque Cloud  
B. Des politiques IAM cohérentes, une gouvernance et des contrôles homogènes  
C. Aucun contrôle centralisé  
D. Une désactivation de tous les logs  

