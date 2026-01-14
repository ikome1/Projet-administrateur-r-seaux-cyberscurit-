## Projet 06 – Sécurité applicative et pipeline DevSecOps

### 1. Contexte
L’entreprise développe en interne plusieurs applications web et APIs.  
Actuellement, la sécurité est traitée uniquement en fin de projet, lors de tests manuels, ce qui entraîne des retards et des failles en production.  
La DSI souhaite intégrer la sécurité **tout au long du cycle de développement** via une démarche DevSecOps.

### 2. Objectifs pédagogiques
- Concevoir et mettre en place un **pipeline CI/CD intégrant des contrôles de sécurité**.  
- Automatiser des analyses SAST, DAST, et de dépendances (Software Composition Analysis).  
- Sensibiliser les développeurs à la **remontée précoce des vulnérabilités**.

### 3. Livrables attendus
- Description de l’architecture DevSecOps proposée (outils, étapes du pipeline).  
- Fichiers de configuration du pipeline (GitHub Actions, GitLab CI, Jenkinsfile, etc. selon choix).  
- Exemple de rapport de vulnérabilités généré automatiquement.  
- Guide “Bonnes pratiques DevSecOps” pour l’équipe de dev.

### 4. Travaux à réaliser
- **Étape 1 – Choix de la stack et du pipeline**
  - Choisir un dépôt de code (GitHub/GitLab local) et un outil CI/CD.  
  - Définir les étapes du pipeline : build, tests, SAST, SCA, DAST, déploiement.

- **Étape 2 – Intégration SAST / SCA**
  - Ajouter un outil SAST (ex : SonarQube, CodeQL, Semgrep…).  
  - Ajouter un outil d’analyse de dépendances (SCA) pour détecter les libs vulnérables.  
  - Configurer l’échec du pipeline en cas de vulnérabilité critique.

- **Étape 3 – Intégration DAST (basique)**
  - Déployer une version de test de l’appli.  
  - Lancer un scan DAST automatisé (ex : OWASP ZAP en mode CI).  
  - Collecter et analyser les résultats.

- **Étape 4 – Documentation et sensibilisation**
  - Rédiger un guide résumant :
    - Où sont intégrés les contrôles sécurité dans le pipeline  
    - Comment les développeurs doivent réagir aux alertes.  
  - Proposer des règles de qualité (ex : pas de merge si score sécurité < seuil).

### 5. Critères d’évaluation
- Intégration réelle d’outils de **sécurité dans le pipeline CI/CD**.  
- Pertinence des règles de blocage / seuils définis.  
- Qualité de la documentation et de la pédagogie pour les développeurs.  
- Compréhension des limites des outils (faux positifs, complémentarité SAST/DAST/SCA).

