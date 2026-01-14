## QCM 06 – Forensique et analyse de logs (niveau avancé)

### Consignes
- 20 questions, niveau avancé.  
- Une seule bonne réponse par question.

---

**1. En forensique, la première règle fondamentale lors de la collecte de preuves est :**  
A. Modifier les fichiers pour les comprendre  
B. Ne jamais toucher au système compromis  
C. Préserver l’intégrité des preuves (ne pas les altérer)  
D. Compresser tous les fichiers systèmes  

**2. Le principe de la “chaîne de possession” (chain of custody) sert à :**  
A. Gérer les backups  
B. Documenter qui a eu accès aux preuves et quand  
C. Configurer un pare-feu  
D. Chiffrer les logs  

**3. Une image disque “forensique” doit être :**  
A. Une simple copie de quelques fichiers  
B. Un clonage bit à bit du support, idéalement en lecture seule  
C. Une archive compressée sans vérification  
D. Une liste des répertoires  

**4. Quel format est couramment utilisé pour les journaux d’événements système sous Linux ?**  
A. `.docx`  
B. `journalctl` / fichiers sous `/var/log/`  
C. `.pst`  
D. `.mdb`  

**5. Sous Windows, quel journal contient principalement les événements liés à la sécurité (logons, changements de droits, etc.) ?**  
A. Application  
B. Sécurité (Security)  
C. Système (System)  
D. Setup  

**6. L’analyse de la timeline (chronologie) en forensique consiste à :**  
A. Supprimer les événements anciens  
B. Arranger les événements par ordre alphabétique  
C. Reconstituer les événements dans l’ordre temporel pour comprendre l’attaque  
D. Compresser les logs  

**7. Un IOC (Indicator of Compromise) est :**  
A. Une vulnérabilité non exploitée  
B. Un indice technique suggérant qu’un système a été compromis  
C. Une mise à jour de sécurité  
D. Une politique de mot de passe  

**8. Le fichier `auth.log` sur un système Linux Debian/Ubuntu contient typiquement :**  
A. Les logs d’accès web  
B. Les logs d’authentification (SSH, sudo, etc.)  
C. Les logs de base de données  
D. Les logs de pare-feu matériel  

**9. Dans un environnement SIEM, la “corrélation” d’événements permet de :**  
A. Effacer les doublons  
B. Lier plusieurs événements techniques pour détecter un scénario d’attaque  
C. Chiffrer tous les logs  
D. Modifier les dates des logs  

**10. Un artefact forensique est :**  
A. Un résidu ou trace laissée par une activité sur un système  
B. Un correctif de sécurité  
C. Un script de sauvegarde  
D. Un type de malware  

**11. Lors de l’analyse mémoire (RAM), on peut typiquement trouver :**  
A. Uniquement des logs compressés  
B. Des processus actifs, clés de chiffrement, connexions réseau, etc.  
C. Uniquement les fichiers du disque  
D. Uniquement la configuration BIOS  

**12. L’outil `Volatility` est principalement utilisé pour :**  
A. Scanner des ports  
B. Analyser des images mémoire  
C. Sauvegarder des disques  
D. Gérer des certificats  

**13. La rotation des logs (logrotate, etc.) est importante car :**  
A. Elle efface tous les logs  
B. Elle évite que les disques soient saturés et garde un historique structuré  
C. Elle désactive la journalisation  
D. Elle chiffre les bases de données  

**14. Un horodatage incohérent (problème d’heure, fuseaux, NTP) peut :**  
A. N’avoir aucun impact  
B. Rendre difficile la reconstitution d’un incident et la corrélation avec d’autres sources  
C. Accélérer les systèmes  
D. Supprimer les logs  

**15. Dans une enquête, l’analyse des fichiers “prefetch” sous Windows peut fournir :**  
A. La liste des patchs installés  
B. Des informations sur les programmes exécutés récemment  
C. Les mots de passe des utilisateurs  
D. La configuration réseau  

**16. Le but d’un “journal d’audit” est :**  
A. De sauvegarder les emails  
B. De tracer les opérations sensibles pour des besoins de conformité et d’enquête  
C. De compresser les fichiers temporaires  
D. D’optimiser la mémoire  

**17. Lors d’un incident, isoler un poste du réseau (par exemple en coupant le câble) sert à :**  
A. Effacer le malware  
B. Empêcher la poursuite de l’attaque ou l’exfiltration de données  
C. Améliorer les performances  
D. Mettre à jour l’antivirus  

**18. Un log d’accès web (Apache/Nginx) permet notamment de voir :**  
A. Les mots de passe en clair  
B. Les URL demandées, codes retour HTTP, IP sources, user-agents  
C. La configuration du système  
D. Les clés privées TLS  

**19. Une surcharge de logs non filtrés dans un SIEM peut :**  
A. Améliorer la visibilité sans inconvénient  
B. Saturer le stockage et rendre l’analyse difficile (bruit)  
C. Accélérer les requêtes de recherche  
D. Supprimer les alertes  

**20. Avant de tirer des conclusions en forensique, il est essentiel de :**  
A. Se baser sur une seule preuve  
B. Corréler plusieurs sources de preuves et garder un esprit critique  
C. Fermer immédiatement l’enquête  
D. Réinitialiser tous les systèmes  

