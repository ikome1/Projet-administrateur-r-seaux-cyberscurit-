## Projet 10 – Sauvegardes chiffrées et Plan de Reprise d’Activité (PRA)

### 1. Contexte
L’entreprise commence à produire des données critiques (bases de données clients, documents financiers, etc.).  
Actuellement, les sauvegardes sont ponctuelles, non testées, parfois stockées sur les mêmes machines.  
La direction veut un **vrai plan de sauvegarde** et un **PRA** (Plan de Reprise d’Activité) documenté, en cas :
- De panne matérielle
- De ransomware
- D’erreur humaine majeure.

### 2. Objectifs de l’épreuve
- Mettre en place une **stratégie de sauvegarde** automatique, chiffrée, vers un stockage séparé.  
- Tester la **restauration** des données pour vérifier la fiabilité des sauvegardes.  
- Rédiger un **Plan de Reprise d’Activité** simple mais concret.

### 3. Environnement et prérequis
- Un ou plusieurs serveurs ou dossiers à sauvegarder.  
- Une solution de backup au choix :
  - rsync + chiffrement (gpg), BorgBackup, Restic, Veeam, etc.  
- Un espace de stockage de sauvegarde :
  - Autre serveur, NAS, disque externe, etc.

### 4. Cahier des charges technique
- **Périmètre des sauvegardes** :
  - Au moins :
    - Un dossier de données critiques (ex : `/srv/data`)
    - Une base de données ou équivalent (dump régulier).
- **Stratégie** :
  - Sauvegarde quotidienne (ou fréquence adaptée) automatique.
  - Sauvegardes chiffrées (en transit et/ou au repos).
  - Conservation d’historiques (ex : 7 jours, 4 semaines…).
- **Stockage** :
  - Support distinct du serveur source (pas sur le même disque).

### 5. Travaux à réaliser
- **Étape 1 – Analyse des besoins**
  - Identifier les données critiques à protéger.
  - Évaluer la taille approximative des données.

- **Étape 2 – Choix et mise en place de l’outil de sauvegarde**
  - Choisir la solution (rsync, Borg, Veeam, etc.) et justifier le choix.
  - Installer et configurer l’outil.

- **Étape 3 – Chiffrement et automatisation**
  - Mettre en place le chiffrement des données sauvegardées (clé, mot de passe, certificats…).
  - Créer un script ou une tâche planifiée (cron, planificateur Windows…).
  - Vérifier que la sauvegarde se lance automatiquement.

- **Étape 4 – Test de restauration**
  - Simuler une perte de données sur un répertoire test.
  - Restaurer depuis la sauvegarde.
  - Vérifier l’intégrité des données restaurées.

- **Étape 5 – Rédaction du PRA**
  - Définir plusieurs scénarios de sinistre :
    - Panne disque serveur
    - Crypto-ransomware
    - Suppression accidentelle d’un dossier critique.
  - Pour chaque scénario, décrire :
    - Les étapes de reprise
    - Les responsables
    - Le temps estimé pour revenir à un état opérationnel.

### 6. Livrables attendus
- `README.md` décrivant la stratégie de sauvegarde :
  - Données sauvegardées
  - Fréquence
  - Outil utilisé
  - Localisation des sauvegardes.  
- Script(s) de sauvegarde et de restauration.  
- Captures d’écran / logs montrant :
  - L’exécution des sauvegardes
  - Un test de restauration réussi.  
- Document PRA (`PRA.md` ou `.pdf`) décrivant les scénarios et procédures.

### 7. Critères d’évaluation
- Réalisme et robustesse de la **stratégie de sauvegarde**.  
- Capacité à **restaurer réellement** les données (preuve par test).  
- Qualité du **PRA** (clarté, exhaustivité, réalisme des délais).  
- Niveau de **sécurité** (chiffrement, séparation des supports).

