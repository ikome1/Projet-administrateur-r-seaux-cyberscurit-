## Projet 01 – Architecture de sécurité d’entreprise (Segmentation, Zero Trust, IAM)

### 1. Contexte
Une entreprise de 500 employés possède plusieurs sites, un data center interne et quelques services dans le cloud.  
L’architecture actuelle s’est construite au fil du temps, sans vision globale de sécurité : réseaux à plat, droits trop larges, pas de stratégie Zero Trust.  
La direction demande une **refonte de l’architecture de sécurité** avec une vision de niveau licence/master.

### 2. Objectifs pédagogiques
- Concevoir une **architecture de sécurité globale** (niveau macro + quelques vues détaillées).  
- Intégrer les principes de **segmentation**, de **Zero Trust**, d’**IAM** (Identity & Access Management).  
- Produire une documentation de **niveau professionnel** (pour un comité de direction et une DSI).

### 3. Livrables attendus
- Dossier d’architecture (`.md` ou `.pdf`) contenant :
  - Cartographie du SI (réseaux, applications, données critiques).  
  - Proposition de segmentation (LAN, DMZ, Admin, utilisateurs, partenaires, cloud, etc.).  
  - Modèle de contrôle d’accès (RBAC / ABAC, MFA, SSO).  
  - Schémas d’architecture (vue logique + vue réseau).  
  - Plan de mise en œuvre (phases, dépendances, priorités).  
- Diaporama de synthèse (10–15 slides) pour la direction.

### 4. Travaux à réaliser
- **Étape 1 – Analyse de l’existant**
  - Identifier les actifs critiques (données, applications, infrastructures).  
  - Cartographier les flux principaux (utilisateurs ↔ applis ↔ données).  
  - Identifier les points faibles (absence de segmentation, comptes à privilèges, etc.).

- **Étape 2 – Définition des objectifs de sécurité**
  - Disponibilité, intégrité, confidentialité, traçabilité.  
  - Contraintes réglementaires (RGPD, secteur d’activité…).  
  - Besoins métiers (télétravail, accès partenaires, mobilité).

- **Étape 3 – Conception de l’architecture cible**
  - Définir les zones réseau et leurs rôles.  
  - Proposer un modèle Zero Trust (authentification forte, vérification continue, moindre privilège).  
  - Définir l’architecture IAM (annuaire, MFA, SSO, gestion des identités à privilèges).  
  - Intégrer les services cloud (accès sécurisé, VPN, CASB éventuel).

- **Étape 4 – Stratégie de déploiement**
  - Prioriser les chantiers (quick wins vs projets lourds).  
  - Estimer les risques si certains chantiers sont retardés.  
  - Proposer des indicateurs de suivi (KPI de sécurité).

### 5. Critères d’évaluation
- Cohérence globale de l’architecture.  
- Pertinence du modèle Zero Trust et de l’IAM proposés.  
- Qualité des schémas et de la documentation (clarté, niveau pro).  
- Capacité à justifier les choix techniques vis-à-vis des risques.

