## Projet 04 – VPN site-à-site et accès distant pour télétravail

### 1. Contexte
L’entreprise possède désormais deux sites géographiques (Site A : siège, Site B : agence).  
Les deux sites doivent échanger des données de manière **sécurisée** via Internet.  
De plus, certains employés sont en **télétravail** et doivent accéder au réseau interne depuis l’extérieur.

### 2. Objectifs de l’épreuve
- Mettre en place un **VPN site-à-site** entre deux routeurs/pare-feux.  
- Mettre en place un **VPN accès distant** pour les utilisateurs nomades.  
- Tester et documenter la connectivité et la sécurité (chiffrement, authentification).

### 3. Environnement et prérequis
- Deux routeurs (ou pare-feux) :
  - Matériel réel ou virtuel (Cisco, Mikrotik, pfSense, etc.)
  - Ou via un simulateur (GNS3, Eve-NG).
- Une machine « client télétravail » (PC externe).
- Connaissances de base :
  - Routage IP
  - Notions de chiffrement et de tunnels VPN (IPSec, OpenVPN, WireGuard…).

### 4. Cahier des charges technique
- **VPN site-à-site** :
  - Reliant le réseau du Site A (ex : `192.168.10.0/24`) au Site B (ex : `192.168.20.0/24`).
  - Chiffrement IPSec (ou équivalent).
  - Authentification par pré-partage de clé (PSK) ou certificats.
- **VPN client distant** :
  - Permet à un utilisateur externe de se connecter au Site A.
  - Authentification par login/mot de passe et/ou certificat.
- **Sécurité** :
  - Interdire l’accès direct non chiffré entre les sites via Internet.
  - Filtrer les flux si nécessaire (firewall).

### 5. Travaux à réaliser
- **Étape 1 – Conception**
  - Définir les deux sous-réseaux locaux (Site A et Site B).
  - Déterminer les adresses publiques/externes simulées des routeurs.
  - Dessiner un schéma global incluant le client télétravail.

- **Étape 2 – Mise en place du VPN site-à-site**
  - Configurer les politiques VPN (phase 1/phase 2 si IPSec).
  - Spécifier :
    - Les réseaux locaux de chaque côté
    - Les algorithmes de chiffrement et d’authentification.
  - Vérifier l’établissement du tunnel (statut, logs).
  - Tester la connectivité (ping, accès aux services) entre `192.168.10.0/24` et `192.168.20.0/24`.

- **Étape 3 – Mise en place du VPN d’accès distant**
  - Mettre en place un serveur VPN pour les clients distants (OpenVPN, WireGuard, ou équivalent via le routeur).
  - Créer au moins 1 profil utilisateur.
  - Configurer un client VPN sur un poste externe.
  - Tester l’accès aux ressources internes du Site A.

- **Étape 4 – Tests de sécurité**
  - Vérifier que sans VPN, le client externe ne peut pas accéder au LAN.
  - Vérifier que les flux passent bien dans le tunnel chiffré (route, table de routage).

### 6. Livrables attendus
- `README.md` décrivant :
  - La topologie complète
  - Le type de VPN choisi (IPSec, OpenVPN, WireGuard…)
  - Les grandes étapes de configuration.
- Schéma réseau détaillé (`schema_VPN.png` ou `.drawio`).  
- Export ou captures de :
  - La configuration VPN des routeurs/pare-feux
  - Le client VPN (capture d’écran de la connexion).
- Captures d’écran des tests (ping croisé, accès ressources).

### 7. Critères d’évaluation
- Fonctionnement du **VPN site-à-site** (connectivité transparente entre les deux LAN).  
- Fonctionnement du **VPN d’accès distant** (connexion du client externe et accès au LAN).  
- Qualité de la **configuration de sécurité** (pas d’accès non chiffré).  
- Clarté et précision de la **documentation**.

