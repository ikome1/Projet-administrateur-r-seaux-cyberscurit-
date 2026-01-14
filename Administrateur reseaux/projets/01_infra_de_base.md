## Projet 01 – Infrastructure réseau de base (VLAN, DHCP, DNS)

### 1. Contexte
Une petite entreprise fictive dispose d’un seul switch et d’un routeur, avec une vingtaine d’employés.  
Actuellement, tout le monde est dans le même réseau, sans séparation ni services centralisés.  
La direction souhaite :
- Séparer le réseau par services (Administration, Utilisateurs, Invités)
- Fournir automatiquement des adresses IP
- Mettre en place un serveur DNS interne

### 2. Objectifs de l’épreuve
- **Concevoir et déployer** une infrastructure réseau simple mais réaliste.  
- **Mettre en place des VLAN** et le routage inter-VLAN.  
- **Configurer un serveur DHCP** par VLAN.  
- **Configurer un serveur DNS interne** pour la résolution des noms des machines internes.  
- **Documenter** clairement l’architecture et la configuration.

### 3. Environnement et prérequis
- Outil de simulation (au choix) :
  - Cisco Packet Tracer, ou
  - GNS3, ou
  - Eve-NG, ou
  - Matériel réel si disponible.
- Connaissances de base :
  - Adressage IP, masque, passerelle
  - Notions de VLAN et de routage
  - Bases de la configuration de routeurs/switchs (Cisco, Mikrotik, etc.)

### 4. Cahier des charges technique
- **Nombre de VLAN** :
  - VLAN 10 : `ADMIN` (5 hôtes max)
  - VLAN 20 : `USERS` (30 hôtes max)
  - VLAN 30 : `GUEST` (30 hôtes max)
- **Plan d’adressage (exemple)** :
  - VLAN 10 : `192.168.10.0/24`
  - VLAN 20 : `192.168.20.0/24`
  - VLAN 30 : `192.168.30.0/24`
- **Services** :
  - Un serveur `DHCP` (centralisé ou par interface)
  - Un serveur `DNS` interne (par exemple : `srv-dns.local`)
- **Routage** :
  - Routage inter-VLAN fonctionnel (tous les VLAN peuvent au minimum joindre le serveur DNS et le serveur DHCP)

### 5. Travaux à réaliser
- **Étape 1 – Conception**
  - Définir le plan d’adressage complet (réseau, masque, passerelle, pool DHCP).
  - Déterminer le rôle de chaque équipement (routeur, switch, serveur).
  - Faire un schéma réseau clair avec :
    - Les VLAN
    - Les liens entre équipements
    - Les adresses IP des interfaces.

- **Étape 2 – Configuration des VLAN et du routage**
  - Créer les VLAN 10, 20, 30 sur le switch.
  - Affecter les ports du switch aux VLAN correspondants.
  - Configurer le routage inter-VLAN :
    - Soit via des sous-interfaces sur un routeur (Router-on-a-Stick),
    - Soit via un switch de niveau 3.

- **Étape 3 – Mise en place du DHCP**
  - Créer un pool DHCP par VLAN.
  - Configurer les options nécessaires :
    - Passerelle par défaut (gateway)
    - DNS (le serveur interne)
  - Vérifier que chaque PC reçoit une IP correcte selon son VLAN.

- **Étape 4 – Mise en place du DNS interne**
  - Installer et configurer un serveur DNS (Linux Bind, Windows DNS, ou autre).
  - Créer au minimum :
    - Un enregistrement `A` pour le serveur DNS lui-même.
    - Quelques enregistrements pour les PCs ou serveurs importants.
  - Tester la résolution de noms depuis chaque VLAN.

- **Étape 5 – Tests et validation**
  - Vérifier la connectivité :
    - Ping entre les VLAN
    - Ping vers le serveur DNS
  - Tester :
    - Attribution d’IP automatique dans chaque VLAN
    - Résolution de noms (nslookup/ping par nom)

### 6. Livrables attendus
- **Dossier de projet** contenant :
  - `README.md` : résumé du projet, outils utilisés, étapes principales.
  - `schema_reseau.png` ou `.drawio` : schéma de l’architecture.
  - `plan_adressage.xlsx` ou `.md` : plan d’adressage détaillé.
  - Fichiers de configuration des équipements (routeur, switch, DHCP, DNS).
  - Captures d’écran des tests (DHCP, ping inter-VLAN, résolution DNS).

### 7. Critères d’évaluation
- Cohérence et propreté du **plan d’adressage**.  
- Fonctionnalité :
  - Chaque VLAN reçoit bien des IP via DHCP.
  - Le routage inter-VLAN fonctionne.
  - Le DNS interne est opérationnel.
- Qualité de la **documentation** (clarté, structure, orthographe).  
- Capacité à **expliquer les choix techniques** (oralement ou par écrit).

