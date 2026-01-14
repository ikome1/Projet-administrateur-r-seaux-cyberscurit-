## Projet 05 – Détection d’intrusion réseau (IDS/IPS avec Suricata/Snort)

### 1. Contexte
L’entreprise veut surveiller son trafic réseau pour détecter des attaques (scan, exploitation, exfiltration).  
Elle souhaite déployer un **IDS/IPS open source** pour analyser le trafic et générer des alertes.

### 2. Objectifs pédagogiques
- Déployer un **IDS/IPS** (Suricata ou Snort) dans un environnement de lab.  
- Configurer des **règles de détection** (signatures + détection de comportements).  
- Intégrer les alertes dans un outil de visualisation ou SIEM léger.

### 3. Livrables attendus
- Documentation du déploiement (architecture, interfaces, mode IDS/IPS).  
- Fichiers de règles personnalisées (quelques signatures écrites par vous).  
- Captures d’écran ou exports d’alertes générées suite à des attaques simulées.

### 4. Travaux à réaliser
- **Étape 1 – Architecture**
  - Concevoir un lab avec au moins :
    - Une machine attaquante  
    - Une machine victime  
    - Une sonde IDS/IPS écoutant le trafic.  

- **Étape 2 – Installation de l’IDS/IPS**
  - Installer Suricata ou Snort sur une VM dédiée.  
  - Configurer l’interface d’écoute et le mode de fonctionnement (IDS ou IPS).

- **Étape 3 – Règles de détection**
  - Charger les règles communautaires.  
  - Écrire au moins 3 à 5 règles personnalisées (scan Nmap, tentative d’auth brute-force, etc.).  
  - Tester ces règles avec des attaques simulées.

- **Étape 4 – Visualisation**
  - Intégrer les logs/alertes dans :
    - Un SIEM léger, ou  
    - Un dashboard (Kibana, Graylog, etc.), ou  
    - À défaut, des rapports texte bien présentés.  

### 5. Critères d’évaluation
- Qualité de la **mise en place de la sonde**.  
- Pertinence et bon fonctionnement des **règles personnalisées**.  
- Capacité à **interpréter les alertes** générées.  
- Qualité de la documentation technique.

