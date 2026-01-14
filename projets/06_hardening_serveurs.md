## Projet 06 – Durcissement (Hardening) de serveurs Linux/Windows

### 1. Contexte
Plusieurs serveurs de l’entreprise (web, fichiers, DNS, etc.) sont exposés sur le réseau interne et/ou Internet.  
Ils ont été installés rapidement avec une configuration par défaut, ce qui présente des **risques de sécurité**.  
La DSI souhaite appliquer des bonnes pratiques de **hardening** pour réduire la surface d’attaque.

### 2. Objectifs de l’épreuve
- Mettre en œuvre des **mesures de sécurité** sur un ou plusieurs serveurs (Linux et/ou Windows).  
- Désactiver les services inutiles et renforcer les services critiques (SSH, RDP, etc.).  
- Mettre en place un **pare-feu**, la **journalisation** et un début de **surveillance des logs**.  
- Rédiger une **checklist de sécurité** réutilisable.

### 3. Environnement et prérequis
- Un ou plusieurs serveurs :
  - Linux (Debian, Ubuntu, CentOS, etc.)
  - Et/ou Windows Server.
- Connaissances de base :
  - Services système (systemd, services Windows)
  - Pare-feu (iptables, ufw, firewalld, Windows Firewall)
  - Comptes utilisateurs et permissions.

### 4. Cahier des charges technique
- **Gestion des comptes** :
  - Supprimer ou désactiver les comptes inutiles.
  - Appliquer une politique de mot de passe forte.
- **Services** :
  - Inventorier les services actifs.
  - Désactiver ceux qui ne sont pas nécessaires.
- **Accès à distance** :
  - Sécuriser SSH (Linux) : clé SSH, port, bannière, etc.
  - Sécuriser RDP (Windows) si utilisé.
- **Pare-feu** :
  - N’autoriser que les ports nécessaires.
  - Bloquer le reste par défaut.
- **Logs** :
  - Activer/paramétrer la journalisation (syslog, journald, Event Viewer).
  - Mettre en place une rotation des logs (logrotate ou équivalent).

### 5. Travaux à réaliser
- **Étape 1 – Inventaire de l’état initial**
  - Lister les comptes utilisateurs existants.
  - Lister les services actifs et ports ouverts.
  - Lister les règles de pare-feu existantes.

- **Étape 2 – Politique de comptes et mots de passe**
  - Mettre en place une politique de mot de passe minimale :
    - Longueur minimale
    - Complexité
    - Durée de validité
  - Désactiver les comptes inutiles ou par défaut.

- **Étape 3 – Durcissement des services**
  - Pour Linux :
    - Sécuriser SSH (clé publique, désactiver root distant si possible, etc.).
  - Pour Windows :
    - Vérifier les paramètres RDP, utilisateurs autorisés, etc.
  - Désactiver les services non utilisés (FTP, Telnet, etc.).

- **Étape 4 – Configuration du pare-feu**
  - Définir les ports à autoriser (SSH, HTTP, DNS, etc. selon le rôle du serveur).
  - Bloquer le reste.
  - Tester depuis un autre poste (ports ouverts/fermés).

- **Étape 5 – Journalisation et rotation des logs**
  - Vérifier la bonne collecte des logs système et sécurité.
  - Mettre en place (ou vérifier) la rotation des logs.
  - Proposer un début de stratégie de conservation des logs.

### 6. Livrables attendus
- `README.md` présentant :
  - L’état initial
  - Les actions de hardening menées
  - Les résultats obtenus.
- Fichiers de configuration modifiés (pare-feu, SSH, etc.).  
- Captures d’écran ou extraits de commandes montrant :
  - Les ports ouverts avant/après
  - La liste des services avant/après.
- Une **checklist de durcissement** réutilisable pour d’autres serveurs.

### 7. Critères d’évaluation
- Pertinence des **mesures de sécurité** appliquées.  
- Réduction visible de la **surface d’attaque** (moins de ports/services exposés).  
- Capacité à **ne pas casser le service** (les services utiles restent accessibles).  
- Qualité de la **checklist** et de la documentation.

