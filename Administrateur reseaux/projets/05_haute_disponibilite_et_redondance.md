## Projet 05 – Haute disponibilité et redondance réseau (VRRP/HSRP/CARP)

### 1. Contexte
Le réseau du siège doit rester disponible même en cas de panne d’un routeur/passerelle.  
Actuellement, un seul routeur assure la sortie vers Internet : c’est un **point de défaillance unique** (SPOF).  
L’entreprise souhaite assurer un **service continu**, même si un des routeurs tombe en panne.

### 2. Objectifs de l’épreuve
- Mettre en place une **passerelle redondante** à l’aide d’un protocole de redondance (VRRP, HSRP, CARP…).  
- Tester la **bascule automatique** en cas de panne d’un des routeurs.  
- Mesurer (ou au moins observer) le temps de coupure et le comportement du réseau.

### 3. Environnement et prérequis
- Deux routeurs ou pare-feux pouvant gérer :
  - VRRP, HSRP, ou CARP (Cisco, Mikrotik, pfSense, etc.).
- Un switch et quelques postes clients.  
- Connaissances de base :
  - Routage, passerelle par défaut
  - Adresses IP virtuelles de passerelle.

### 4. Cahier des charges technique
- **Réseau LAN** :
  - Un réseau utilisateur (ex : `192.168.100.0/24`).
  - La passerelle par défaut des clients doit être une **IP virtuelle** gérée par les deux routeurs.
- **Routeurs** :
  - Routeur 1 : `192.168.100.2`
  - Routeur 2 : `192.168.100.3`
  - IP virtuelle : `192.168.100.1` (passerelle pour les clients).
- **Haute disponibilité** :
  - En fonctionnement normal, Routeur 1 est maître (active) et Routeur 2 est backup.
  - En cas de panne de Routeur 1, Routeur 2 prend automatiquement le relais.

### 5. Travaux à réaliser
- **Étape 1 – Conception**
  - Définir le plan d’adressage.
  - Dessiner le schéma réseau (clients, switch, routeurs, sortie Internet simulée).

- **Étape 2 – Configuration de base des routeurs**
  - Configurer les adresses IP sur les interfaces LAN.
  - Configurer la route vers Internet (réelle ou simulée).

- **Étape 3 – Mise en place du protocole de redondance**
  - Activer VRRP/HSRP/CARP sur les deux routeurs.
  - Définir l’adresse IP virtuelle qui servira de passerelle.
  - Configurer les priorités pour désigner le routeur maître.

- **Étape 4 – Configuration des clients**
  - Configurer les clients pour utiliser la passerelle virtuelle.
  - Vérifier la connectivité Internet en fonctionnement normal.

- **Étape 5 – Tests de bascule**
  - Couper ou redémarrer le routeur maître.
  - Observer :
    - La bascule de la passerelle vers le routeur backup.
    - L’impact sur la connectivité (pings en cours, navigation).
  - Noter le temps approximatif de coupure.

### 6. Livrables attendus
- `README.md` expliquant :
  - Le protocole choisi (VRRP, HSRP, CARP)
  - La configuration principale.
- Schéma réseau clair (`schema_HA.png` ou `.drawio`).  
- Export ou copies de la configuration des deux routeurs.  
- Compte-rendu de tests de bascule :
  - Scénario de panne
  - Observations (perte de paquets, temps de coupure).

### 7. Critères d’évaluation
- Configuration correcte de la **passerelle virtuelle** et des priorités.  
- Fonctionnement réel de la **bascule** en cas de panne.  
- Capacité à **analyser le comportement** du réseau pendant la panne.  
- Qualité de la **documentation** et des conclusions.

