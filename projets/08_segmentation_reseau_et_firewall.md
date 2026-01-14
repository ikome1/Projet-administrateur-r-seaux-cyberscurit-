## Projet 08 – Segmentation réseau et règles firewall avancées (LAN / DMZ / Invités)

### 1. Contexte
Actuellement, tous les serveurs et postes utilisateurs se trouvent dans un même réseau à plat.  
Un serveur web de l’entreprise est accessible depuis Internet **dans le même LAN** que les postes utilisateurs, ce qui n’est pas acceptable.  
L’objectif est de segmenter le réseau en plusieurs **zones de sécurité** et de filtrer précisément les flux.

### 2. Objectifs de l’épreuve
- Concevoir une **architecture segmentée** avec au minimum :
  - Un LAN interne
  - Une DMZ
  - Un réseau Invités (Wi-Fi invité par exemple).  
- Mettre en place un **pare-feu** central pour contrôler les flux entre ces zones.  
- Documenter toutes les règles dans un tableau lisible.

### 3. Environnement et prérequis
- Un pare-feu (ou routeur avec firewall avancé) :
  - pfSense, OPNsense, Cisco ASA, Mikrotik, etc.
- Des VLANs ou réseaux distincts pour chaque zone.  
- Un serveur web placé en DMZ, quelques postes clients en LAN et en Invités.

### 4. Cahier des charges technique
- **Zones** :
  - LAN interne (`LAN`) : utilisateurs internes, serveurs internes.
  - DMZ : serveur web exposé à Internet.
  - Invités (`GUEST`) : accès Internet uniquement, pas d’accès au LAN interne.
- **Règles firewall (exemples à adapter)** :
  - Internet → DMZ : HTTP/HTTPS autorisés vers le serveur web.
  - DMZ → LAN : interdit, sauf cas très spécifique justifié.
  - LAN → DMZ : autorisé (admin, maintenance) sur certains ports.
  - LAN → Internet : autorisé (HTTP/HTTPS, DNS).
  - GUEST → Internet : autorisé (HTTP/HTTPS, DNS).
  - GUEST → LAN/DMZ : interdit.

### 5. Travaux à réaliser
- **Étape 1 – Conception de l’architecture**
  - Définir les réseaux/VLAN :
    - Exemple : `192.168.10.0/24` (LAN), `192.168.20.0/24` (DMZ), `192.168.30.0/24` (GUEST).
  - Dessiner le schéma incluant pare-feu, switch, serveurs, clients, Internet.

- **Étape 2 – Création des VLANs / sous-réseaux**
  - Configurer les VLANs sur les switchs.
  - Configurer les interfaces/ sous-interfaces sur le pare-feu.

- **Étape 3 – Mise en place du serveur DMZ**
  - Installer un serveur web en DMZ (simple site de test).
  - Lui attribuer une IP spécifique dans le réseau DMZ.
  - Simuler ou configurer une redirection depuis Internet (NAT).

- **Étape 4 – Configuration du pare-feu**
  - Créer les règles suivant le cahier des charges.
  - Documenter chaque règle dans un tableau :
    - Source zone, IP/port source
    - Destination zone, IP/port destination
    - Action (Allow/Deny)
    - Justification.

- **Étape 5 – Tests de validation**
  - Depuis Internet (simulé) :
    - Accéder au serveur web DMZ (HTTP/HTTPS).
  - Depuis le LAN :
    - Accéder au serveur web DMZ.
    - Accéder à Internet.
  - Depuis le réseau GUEST :
    - Accéder à Internet.
    - Vérifier l’impossibilité d’accéder au LAN et à la DMZ.

### 6. Livrables attendus
- `README.md` expliquant :
  - Les zones mises en place
  - Le rôle de chaque zone
  - Les grands principes de filtrage.  
- Schéma réseau (`schema_segmentation.png` ou `.drawio`).  
- Tableau détaillé des règles firewall (format `.md`, `.xlsx`, etc.).  
- Captures d’écran ou tests montrant :
  - Accès autorisés
  - Accès bloqués.

### 7. Critères d’évaluation
- Qualité de la **segmentation** (séparation claire des rôles).  
- Pertinence et rigueur des **règles firewall**.  
- Absence de “trous” évidents (par ex. GUEST qui accède au LAN).  
- Clarté de la **documentation des règles**.

