## Projet 07 – Mini SOC : SIEM + Honeypot pour détection d’attaques

### 1. Contexte
Les attaques (scans, tentatives de brute-force, malware) sont de plus en plus fréquentes.  
L’entreprise souhaite **voir ce qui se passe réellement** sur son réseau et disposer d’un début de SOC (Security Operations Center).  
Pour cela, elle veut :
- Centraliser les logs de plusieurs machines
- Déployer un **honeypot** pour attirer les attaquants
- Visualiser les attaques en temps réel.

### 2. Objectifs de l’épreuve
- Mettre en place une **solution de collecte et d’analyse de logs** (SIEM ou équivalent).  
- Déployer un **honeypot** (ex : SSH, web, etc.).  
- Créer des **dashboards** montrant les tentatives d’attaque.  
- Rédiger un **mini rapport** sur les attaques observées.

### 3. Environnement et prérequis
- Une solution de type SIEM au choix :
  - Wazuh, Graylog, ELK (Elasticsearch + Logstash + Kibana), Splunk Free, etc.
- Une ou plusieurs machines sources de logs :
  - Serveur Linux, Windows, routeur, etc.
- Un honeypot au choix :
  - Cowrie (SSH), Dionaea, ou autre.

### 4. Cahier des charges technique
- **Collecte de logs** :
  - Au moins 2 sources différentes (ex: 1 serveur + 1 honeypot).
  - Intégration des logs dans le SIEM.
- **Honeypot** :
  - Accessible depuis un réseau externe ou simulé.
  - Capable de journaliser les tentatives de connexion/attaques.
- **Dashboard** :
  - Vue des événements récents
  - Nombre de tentatives par type (ex: SSH, HTTP)
  - Origine (adresse IP source).

### 5. Travaux à réaliser
- **Étape 1 – Installation du SIEM**
  - Installer la solution choisie (Wazuh, Graylog, ELK, etc.).
  - Configurer le stockage et l’accès au dashboard.

- **Étape 2 – Intégration des premières sources de logs**
  - Ajouter au moins un serveur (Linux/Windows) comme source.
  - Vérifier la remontée des logs dans le SIEM.

- **Étape 3 – Déploiement du honeypot**
  - Installer un honeypot (par ex. Cowrie pour SSH).
  - Configurer l’envoi de ses logs vers le SIEM.
  - Vérifier que les événements du honeypot apparaissent dans le SIEM.

- **Étape 4 – Génération d’événements de test**
  - Simuler des attaques ou scans (ex : nmap, tentatives SSH).
  - Vérifier la bonne collecte et visualisation dans le SIEM.

- **Étape 5 – Dashboard et rapport**
  - Créer un ou plusieurs dashboards :
    - Top IP attaquantes
    - Nombre de tentatives par jour
    - Services les plus attaqués.
  - Rédiger un mini rapport décrivant :
    - Les types d’attaques observées
    - Les IP sources (géolocalisation éventuelle)
    - Des recommandations de sécurité.

### 6. Livrables attendus
- `README.md` expliquant l’architecture SOC (SIEM + honeypot + sources de logs).  
- Schéma logique du flux de logs (`schema_SOC.png` ou `.drawio`).  
- Captures d’écran :
  - Dashboard principal
  - Détail d’un événement (tentative d’attaque).
- Le rapport d’analyse des attaques observées (document `.md`, `.pdf` ou autre).

### 7. Critères d’évaluation
- Capacité à **collecter** et **corréler** des logs depuis plusieurs sources.  
- Bon fonctionnement du **honeypot** (présence d’événements d’attaque).  
- Qualité des **dashboards** (lisibilité, pertinence).  
- Niveau d’**analyse** dans le rapport (compréhension des attaques, recommandations).

