## Projet 09 – Sécurité Cloud (AWS / Azure / GCP) et revue de configuration

### 1. Contexte
L’entreprise migre progressivement des services dans le cloud public (IaaS, PaaS, SaaS).  
Elle craint les **mauvaises configurations** (S3 publics, clés exposées, droits trop larges, etc.).  
On vous demande de réaliser une **revue de sécurité Cloud** et de proposer une base de bonnes pratiques.

### 2. Objectifs pédagogiques
- Comprendre les **principes de responsabilité partagée** en Cloud.  
- Auditer et durcir la configuration de base d’un tenant ou d’un compte Cloud.  
- Mettre en place quelques **contrôles techniques** (IAM, logs, alertes, chiffrement).

### 3. Livrables attendus
- Rapport d’audit de configuration Cloud :  
  - Inventaire des ressources  
  - Principales non-conformités / risques  
  - Recommandations détaillées.  
- Checklists de bonnes pratiques (IAM, stockage, réseau, journaux, clés, etc.).

### 4. Travaux à réaliser
- **Étape 1 – Contexte et périmètre**
  - Choisir un fournisseur (AWS, Azure, GCP) et un périmètre (compte/tenant de lab).  
  - Documenter les services utilisés (VM, stockage, DB, fonctions, etc.).

- **Étape 2 – Audit de configuration**
  - Examiner :
    - Les rôles et politiques IAM  
    - Les règles réseau (Security Groups, NSG, FW)  
    - La configuration des stockages (public/privé, chiffrement).  
  - Identifier les écarts avec les bonnes pratiques.

- **Étape 3 – Durcissement**
  - Proposer et/ou appliquer :  
    - Principe de moindre privilège IAM  
    - Activations des logs (CloudTrail, Monitor, etc.).  
    - Chiffrement des données au repos et en transit.

- **Étape 4 – Surveillance et alertes**
  - Mettre en place quelques alertes (accès depuis pays non attendus, création de ressources sensibles, etc.).  
  - Décrire comment ces alertes seraient traitées par l’équipe sécurité.

### 5. Critères d’évaluation
- Compréhension des **spécificités Cloud** vs on-premise.  
- Pertinence de l’**audit de configuration** et des recommandations.  
- Qualité des checklists et de la documentation.  
- Capacité à prioriser les actions de sécurisation.

