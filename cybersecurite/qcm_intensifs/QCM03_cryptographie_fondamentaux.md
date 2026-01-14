## QCM 03 – Cryptographie : fondamentaux (niveau intermédiaire)

### Consignes
- 20 questions, difficulté légèrement supérieure.  
- Une seule bonne réponse par question.

---

**1. La cryptographie symétrique utilise :**  
A. Une clé publique uniquement  
B. Une clé privée uniquement  
C. Une même clé pour chiffrer et déchiffrer  
D. Aucune clé  

**2. La cryptographie asymétrique utilise :**  
A. Deux clés différentes mais liées mathématiquement  
B. Deux mots de passe identiques  
C. Aucun mathématiques complexes  
D. Un seul secret partagé  

**3. Parmi ces algorithmes, lequel est typiquement symétrique ?**  
A. RSA  
B. AES  
C. Diffie-Hellman  
D. DSA  

**4. Parmi ces algorithmes, lequel est typiquement asymétrique ?**  
A. AES  
B. ChaCha20  
C. RSA  
D. 3DES  

**5. Un “hash” cryptographique doit être :**  
A. Réversible  
B. Lent et très compressible  
C. À sens unique et résistant aux collisions  
D. Identique pour toutes les entrées  

**6. Quel algorithme de hash est aujourd’hui considéré comme cassé ou obsolète pour la sécurité ?**  
A. SHA‑256  
B. SHA‑3  
C. MD5  
D. BLAKE3  

**7. La fonction de dérivation de mot de passe (PBKDF2, bcrypt, Argon2…) sert à :**  
A. Accélérer les connexions  
B. Rendre plus difficile l’attaque par bruteforce sur des mots de passe hashés  
C. Chiffrer le trafic réseau  
D. Sauvegarder des fichiers  

**8. La signature numérique permet de garantir :**  
A. La disponibilité uniquement  
B. La confidentialité uniquement  
C. L’authenticité et l’intégrité d’un message  
D. La vitesse de transmission  

**9. Dans un protocole TLS, la cryptographie asymétrique est principalement utilisée pour :**  
A. Chiffrer tout le trafic de bout en bout  
B. L’authentification et l’échange de clé de session  
C. Compresser les paquets  
D. Gérer les VLANs  

**10. Diffie-Hellman sert principalement à :**  
A. Signer des documents  
B. Échanger une clé secrète sur un canal non sûr  
C. Chiffrer directement les fichiers  
D. Gérer les comptes utilisateurs  

**11. Le “salt” ajouté à un mot de passe avant hashage sert à :**  
A. Le rendre plus lisible  
B. Éviter l’utilisation efficace de tables arc-en-ciel (rainbow tables)  
C. Accélérer le calcul du hash  
D. Remplacer le mot de passe  

**12. Chiffrer un disque dur complet permet principalement de :**  
A. Protéger les données contre un vol physique de la machine  
B. Accélérer l’accès aux fichiers  
C. Bloquer les virus  
D. Supprimer les logs système  

**13. Une PKI (Public Key Infrastructure) sert à :**  
A. Gérer les VLANs  
B. Gérer les clés et certificats pour l’authentification et le chiffrement  
C. Superviser les routeurs  
D. Sauvegarder les logs  

**14. Un certificat X.509 contient typiquement :**  
A. Un mot de passe en clair  
B. Une clé publique, un sujet, un émetteur, une durée de validité, etc.  
C. Un hash de la base de données  
D. Un compte administrateur  

**15. Quel principe est faux concernant la sécurité des algorithmes ?**  
A. On doit pouvoir publier l’algorithme sans compromettre la sécurité  
B. C’est la clé qui doit rester secrète, pas l’algorithme  
C. La sécurité par l’obscurité ne doit pas être la seule défense  
D. Il faut garder l’algorithme secret pour qu’il soit sécurisé  

**16. Le mode CBC, GCM, CTR sont des :**  
A. Types de certificats  
B. Modes de fonctionnement de chiffrements par bloc  
C. Protocoles de routage  
D. Méthodes de compression  

**17. Une collision de hash correspond à :**  
A. Plusieurs clés publiques identiques  
B. Deux entrées différentes produisant le même hash  
C. Deux certificats expirant le même jour  
D. Deux VLANs partageant le même ID  

**18. Le chiffrement de bout en bout (E2EE) garantit que :**  
A. Seuls les serveurs peuvent lire les messages  
B. Seuls les intermédiaires peuvent lire les messages  
C. Seuls l’émetteur et le destinataire final peuvent lire les messages  
D. Les messages ne sont jamais chiffrés  

**19. Dans une attaque de type “replay”, l’attaquant :**  
A. Modifie le code source d’un logiciel  
B. Réinjecte des messages valides capturés précédemment  
C. Exploite une faille dans le hash  
D. Submerge le réseau de paquets  

**20. Le stockage sécurisé de clés privées doit :**  
A. Se faire en clair sur un partage réseau  
B. Se faire dans des modules sécurisés (HSM, TPM, coffre chiffré)  
C. Être envoyé par mail à l’équipe  
D. Être copié dans un fichier texte sur le bureau  

