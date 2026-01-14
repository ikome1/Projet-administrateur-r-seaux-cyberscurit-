## Projet 03 – Plateforme de supervision réseau (Nagios, Zabbix, Centreon, etc.)

### 1. Contexte
L’infrastructure de l’entreprise commence à se complexifier : plusieurs serveurs, routeurs, switchs, points d’accès Wi-Fi.  
Les incidents sont gérés de manière **réactive** (on attend que les utilisateurs se plaignent).  
La DSI veut mettre en place une **supervision centralisée** pour surveiller l’état des équipements et des services.

### 2. Objectifs de l’épreuve
- Déployer une **solution de supervision** réseau et systèmes.  
- Superviser au minimum :
  - La disponibilité des équipements (ping)
  - L’état de quelques services réseau (HTTP, SSH, DNS, etc.)
  - Les ressources système (CPU, RAM, disque) d’au moins 2 serveurs.  
- Mettre en place des **alertes** et un **tableau de bord** de suivi.

### 3. Environnement et prérequis
- Plateforme de supervision au choix :
  - Nagios, Zabbix, Centreon, Icinga, ou équivalent.
- Une ou plusieurs machines cibles à superviser :
  - Routeurs / Switchs
  - Serveurs Linux/Windows
  - Services (web, DNS, etc.)

### 4. Cahier des charges technique
- **Serveur de supervision** :
  - Machine dédiée (VM ou physique).
  - Accès réseau aux machines supervisées.
- **Objets supervisés** (minimum) :
  - 3 à 5 équipements réseau (routeurs, switchs, AP, etc.)
  - 2 serveurs (Linux/Windows)
  - 3 services réseau (par ex : HTTP, SSH, DNS, DHCP).
- **Fonctionnalités** :
  - Vue globale de l’état (OK / Warning / Critical)
  - Envoi d’alertes (mail, notification interne, etc. même simulée)
  - Historique des événements.

### 5. Travaux à réaliser
- **Étape 1 – Installation de la solution de supervision**
  - Installer la solution choisie (tuto officiel recommandé).
  - Configurer les paramètres de base (langue, fuseau horaire, accès web).

- **Étape 2 – Inventaire des équipements à superviser**
  - Lister tous les équipements à inclure dans la supervision.
  - Définir pour chacun :
    - Adresse IP
    - Type d’équipement (serveur, routeur, etc.)
    - Services à surveiller.

- **Étape 3 – Configuration de la supervision**
  - Ajouter les hôtes (hosts) dans l’outil.
  - Ajouter les services à superviser (ping, HTTP, SSH, DNS…).
  - Si nécessaire, installer des agents (ex : Zabbix Agent, NRPE).

- **Étape 4 – Mise en place des alertes**
  - Configurer au moins un canal d’alerte (mail, ou autre).
  - Définir les seuils pour les alertes (CPU > 80 %, disque > 90 %, etc.).

- **Étape 5 – Tableau de bord et rapports**
  - Créer un tableau de bord récapitulatif (synthèse des états).
  - Générer un rapport ou capture d’écran montrant :
    - Les hôtes suivis
    - Les services surveillés
    - Quelques alertes simulées (arrêt volontaire d’un service, par exemple).

### 6. Livrables attendus
- `README.md` expliquant :
  - Le choix de l’outil de supervision
  - L’architecture mise en place
  - La liste des hôtes et services surveillés.
- Captures d’écran :
  - Dashboard global
  - Détail d’un hôte
  - Exemple d’alerte.
- Export éventuel de la configuration (si possible).

### 7. Critères d’évaluation
- Capacité à **installer** et **configurer** correctement la solution.  
- Pertinence du **choix des éléments supervisés**.  
- Visibilité offerte par le **tableau de bord** (clarté, organisation).  
- Capacité à **détecter et interpréter** une alerte (diagnostic de base).

