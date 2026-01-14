## Projet 10 – Exercice Red Team / Blue Team (simulation d’attaque-défense)

### 1. Contexte
Afin de tester la maturité globale de l’organisation, un exercice “attaque/défense” est organisé :  
- Une équipe **Red Team** simule des attaques contrôlées.  
- Une équipe **Blue Team** surveille, détecte et réagit.

### 2. Objectifs pédagogiques
- Concevoir un **scénario d’exercice réaliste** mais contrôlé.  
- Mettre en œuvre des **tactiques d’attaque** (Red) et des **mécanismes de défense** (Blue) dans un lab.  
- Produire un **retour d’expérience détaillé** des deux côtés.

### 3. Livrables attendus
- Description complète du scénario (objectifs, règles du jeu, périmètre, contraintes).  
- Journal des actions Red Team (tactiques, techniques, procédures – TTP).  
- Journal des actions Blue Team (détections, investigations, remédiations).  
- Rapport de synthèse croisant les deux visions (tableau MITRE ATT&CK possible).

### 4. Travaux à réaliser
- **Étape 1 – Conception du lab**
  - Construire une petite infrastructure cible (serveur web, base de données, postes clients, AD ou équivalent).  
  - Définir les outils d’attaque autorisés (Red) et les moyens de détection (Blue : SIEM, IDS, EDR, logs).

- **Étape 2 – Scénario Red Team**
  - Définir les objectifs : vol de données, persistance, mouvement latéral, etc.  
  - Planifier une chaîne d’attaque (phases : reco, initial access, execution, privilege escalation, etc.).  
  - Documenter toutes les actions réalisées.

- **Étape 3 – Scénario Blue Team**
  - Paramétrer la collecte de logs et les alertes.  
  - Durant l’exercice, noter :
    - Les événements détectés  
    - Les analyses menées  
    - Les actions de remédiation.

- **Étape 4 – Debrief et RETEX**
  - Croiser les journaux Red et Blue pour voir ce qui a été vu ou manqué.  
  - Cartographier les TTP dans une matrice MITRE ATT&CK (même simplifiée).  
  - Proposer des améliorations côté détection, durcissement, procédures.

### 5. Critères d’évaluation
- Réalisme et cadrage du **scénario d’exercice**.  
- Rigueur des journaux d’actions (Red et Blue).  
- Qualité du **retour d’expérience** (leçons apprises concrètes).  
- Capacité à relier l’exercice à des cadres comme **MITRE ATT&CK**.

