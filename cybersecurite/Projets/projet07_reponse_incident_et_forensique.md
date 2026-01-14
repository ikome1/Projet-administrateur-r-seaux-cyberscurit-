## Projet 07 – Réponse à incident et analyse forensique (niveau licence/master)

### 1. Contexte
Un poste utilisateur et un serveur semblent compromis (comportement anormal, alertes antivirus, connexions suspectes).  
L’entreprise doit réagir rapidement tout en **préservant les preuves** pour comprendre l’attaque et s’en protéger à l’avenir.

### 2. Objectifs pédagogiques
- Mettre en œuvre un **processus de réponse à incident** (préparation, détection, confinement, éradication, rétablissement, retour d’expérience).  
- Réaliser une **analyse forensique de base** sur un poste ou un serveur compromis (disque, mémoire, logs).  
- Produire un **rapport d’incident** structuré pour la direction et la technique.

### 3. Livrables attendus
- Plan de réponse à incident simplifié (RACI, procédures, contacts).  
- Dossier d’analyse forensique :
  - Chronologie de l’incident  
  - Indicateurs de compromission trouvés  
  - Hypothèse de scénario d’attaque.  
- Rapport final (technique + exécutif) avec recommandations.

### 4. Travaux à réaliser
- **Étape 1 – Préparation**
  - Définir les rôles (équipe IR, référent métier, DSI…).  
  - Lister les outils et sources de preuves disponibles (SIEM, EDR, logs, images disques).

- **Étape 2 – Scénario d’incident**
  - Construire ou utiliser un scénario de compromission contrôlé (lab).  
  - Recueillir les premiers indices : alertes, logs, comportement utilisateur.

- **Étape 3 – Collecte et analyse des preuves**
  - Identifier les traces sur le système :  
    - Journalisation (Windows Event Logs, journald, fichiers logs).  
    - Fichiers suspects, clés de registre, tâches planifiées.  
  - Reconstituer la ligne de temps de l’attaque.

- **Étape 4 – Mesures de remédiation**
  - Proposer les actions de confinement, d’éradication et de restauration.  
  - Identifier les failles qui ont permis l’attaque (techniques, organisationnelles).

- **Étape 5 – Retour d’expérience (RETEX)**
  - Rédiger les leçons apprises.  
  - Proposer des améliorations de processus et de contrôles techniques.

### 5. Critères d’évaluation
- Structure et réalisme du **plan de réponse à incident**.  
- Rigueur dans la **collecte et l’analyse des preuves**.  
- Qualité du rapport (compréhensible pour direction + technique).  
- Capacité à proposer des **actions préventives** pertinentes.

