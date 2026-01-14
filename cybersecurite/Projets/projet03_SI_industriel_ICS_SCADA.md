## Projet 03 – Sécurisation d’un SI Industriel (ICS/SCADA)

### 1. Contexte
Une usine dispose d’un réseau industriel (PLC, automates, HMI, SCADA) connecté au SI bureautique pour la supervision et la collecte de données.  
Les industriels sont très sensibles aux arrêts de production et aux attaques type Stuxnet, Industroyer, etc.  
On vous demande de proposer une **architecture de sécurité spécifique ICS**.

### 2. Objectifs pédagogiques
- Comprendre les **spécificités des réseaux industriels** (temps réel, disponibilité, protocoles propriétaires).  
- Proposer une **segmentation adaptée** (zones et conduits, ISA/IEC 62443).  
- Définir des mesures de protection **réalistes** (filtrage, durcissement, supervision).

### 3. Livrables attendus
- Dossier d’architecture de sécurité ICS :
  - Cartographie fonctionnelle (Niveau 0 à 4, modèle Purdue).  
  - Proposition de zones (safety, control, DMZ industrielle, DMZ IT/OT, etc.).  
  - Politiques d’accès entre IT et OT.  
  - Mesures de protection (firewall industriel, jump server, etc.).  
- Fiche de risques principaux et contre-mesures.

### 4. Travaux à réaliser
- **Étape 1 – Cartographie du SI Industriel**
  - Identifier les composants clés : automates, capteurs, SCADA, serveurs d’historisation.  
  - Déterminer les dépendances avec le SI bureautique.

- **Étape 2 – Analyse des risques**
  - Lister les scénarios de menace principaux (sabotage, ransomware, erreur opérateur).  
  - Évaluer l’impact potentiel (sécurité des personnes, pertes financières, etc.).

- **Étape 3 – Conception de l’architecture sécurisée**
  - Appliquer les principes ISA/IEC 62443 et le modèle Purdue.  
  - Segmenter en zones et définir les “conduits” (flux autorisés).  
  - Proposer les équipements de sécurité (firewall L3/L7, IDS OT, bastion).

- **Étape 4 – Plan de mise en œuvre**
  - Prioriser les chantiers de sécurisation (quick wins vs gros projets).  
  - Prévoir les contraintes d’exploitation (fenêtres de maintenance, tests).

### 5. Critères d’évaluation
- Pertinence de la **segmentation IT/OT**.  
- Prise en compte des **contraintes industrielles** (disponibilité, temps réel).  
- Réalisme des mesures (pas uniquement théoriques).  
- Qualité de la documentation produite.

