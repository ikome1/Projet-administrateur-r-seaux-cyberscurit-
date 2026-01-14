## Projet 02 – Annuaire d’entreprise (Active Directory ou LDAP)

### 1. Contexte
L’entreprise grandit et compte maintenant plusieurs services (RH, Finance, Support, Direction).  
La gestion manuelle des comptes utilisateurs sur chaque poste devient trop lourde et peu sécurisée.  
La DSI décide de mettre en place un **annuaire centralisé** pour :
- Centraliser l’authentification
- Gérer les groupes et les droits
- Préparer l’automatisation (scripts, GPO, etc.)

### 2. Objectifs de l’épreuve
- Installer et configurer un **annuaire d’entreprise** (Active Directory ou OpenLDAP).  
- Organiser les utilisateurs et groupes dans une **arborescence logique** (OU, groupes).  
- Mettre en place des **stratégies simples** (sécurité, partage réseau, etc.).  
- Documenter la procédure d’intégration d’un nouveau poste et d’un nouvel utilisateur.

### 3. Environnement et prérequis
- Plateforme au choix :
  - Windows Server (Active Directory), ou
  - Linux (OpenLDAP + outils associés).
- Connaissances de base :
  - DNS interne
  - Comptes utilisateurs et groupes
  - Notions de domaine, d’OU, de GPO (si AD).

### 4. Cahier des charges technique
- **Structure de l’annuaire** :
  - Un domaine (ex : `entreprise.local`)
  - Des OU par service :
    - `OU=RH`
    - `OU=Finance`
    - `OU=Support`
    - `OU=Direction`
  - Un OU `Ordinateurs` ou équivalent.
- **Utilisateurs** :
  - Créer au moins 2 utilisateurs par service.
  - Utiliser une convention de nommage (ex : `prenom.nom`).
- **Groupes** :
  - Créer des groupes de sécurité par service (ex : `GG_RH`, `GG_Finance`).
  - Associer les utilisateurs aux bons groupes.

### 5. Travaux à réaliser
- **Étape 1 – Installation de l’annuaire**
  - Installer le serveur (Windows ou Linux).
  - Configurer le nom de domaine de l’entreprise (ex : `entreprise.local`).
  - Vérifier la résolution DNS pour le domaine.

- **Étape 2 – Conception de l’OU et des groupes**
  - Définir la structure logique des OU (services, ordinateurs).
  - Créer la structure dans l’annuaire.
  - Définir les groupes nécessaires (par service, par rôle).

- **Étape 3 – Création des utilisateurs**
  - Créer au moins :
    - 2 comptes Direction
    - 2 comptes RH
    - 2 comptes Finance
    - 2 comptes Support
  - Documenter la convention de nommage choisie.

- **Étape 4 – Stratégies simples (GPO ou équivalent)**
  - Mettre en place des politiques de mot de passe :
    - Longueur minimale
    - Complexité
    - Durée de validité
  - Mettre en place 1 ou 2 règles simples :
    - Par exemple : afficher un fond d’écran commun, mapper un lecteur réseau, interdire le panneau de configuration pour certains groupes.

- **Étape 5 – Intégration de postes clients**
  - Joindre au moins 2 machines clients au domaine.
  - Tester la connexion avec différents utilisateurs.
  - Vérifier que les stratégies s’appliquent bien aux bons comptes.

### 6. Livrables attendus
- `README.md` décrivant :
  - Le choix de la techno (AD ou LDAP)
  - L’architecture retenue
  - Les grandes étapes d’installation.
- Export ou captures :
  - De la structure des OU
  - Des groupes
  - D’exemples d’utilisateurs.
- Captures d’écran :
  - Connexion d’un poste client
  - Application d’une GPO ou d’une politique.

### 7. Critères d’évaluation
- Qualité de la **structure de l’annuaire** (logique, claire, maintenable).  
- Respect du cahier des charges (OU, groupes, utilisateurs).  
- Fonctionnement réel :
  - Authentification via l’annuaire
  - Application des politiques.  
- Qualité de la **documentation** et capacité à réinstaller/reproduire la solution.

