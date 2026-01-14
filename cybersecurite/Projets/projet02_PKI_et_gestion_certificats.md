## Projet 02 – PKI d’entreprise et gestion des certificats (niveau avancé)

### 1. Contexte
L’entreprise souhaite sécuriser ses communications internes (HTTPS, VPN, authentification forte) via une **infrastructure de gestion de clés (PKI)**.  
Elle veut maîtriser sa propre autorité de certification interne (CA) pour émettre, renouveler et révoquer des certificats.

### 2. Objectifs pédagogiques
- Concevoir et déployer une **PKI interne** (racine + CA(s) subordonnée(s) si possible).  
- Gérer le **cycle de vie des certificats** (émission, renouvellement, révocation, CRL/OCSP).  
- Intégrer des certificats dans plusieurs usages (HTTPS interne, VPN, authentification machine/utilisateur).

### 3. Livrables attendus
- Documentation technique de la PKI :
  - Architecture (CA racine, CA d’entreprise, serveurs de publication CRL/OCSP).  
  - Procédures de génération, renouvellement, révocation.  
  - Politique de certification simplifiée (CP/CPS light).  
- Scripts ou commandes utilisés (OpenSSL, HashiCorp Vault PKI, Microsoft ADCS, etc.).  
- Exemples de certificats déployés (captures de config, export `.crt` anonymisé, etc.).

### 4. Travaux à réaliser
- **Étape 1 – Conception**
  - Définir le rôle de la PKI (quels usages ? internes seulement ?).  
  - Choisir la techno (OpenSSL, ADCS, autre).  
  - Définir la hiérarchie (CA racine offline, CA d’émission online, etc.).

- **Étape 2 – Mise en place de la CA**
  - Générer la clé et le certificat de la CA racine.  
  - Mettre en place la CA d’entreprise (émission).  
  - Configurer les paramètres de base (algorithmes, durées de validité, etc.).

- **Étape 3 – Cycle de vie des certificats**
  - Émettre un certificat serveur HTTPS pour un site interne.  
  - Émettre un certificat pour un serveur VPN.  
  - Documenter la procédure d’émission pour un utilisateur ou une machine.

- **Étape 4 – Révocation et publication**
  - Mettre en place une CRL (liste de révocation) et/ou OCSP.  
  - Révoquer un certificat de test et vérifier la prise en compte.  
  - Documenter les délais de mise à jour, les risques en cas de non-vérification.

### 5. Critères d’évaluation
- Qualité de la **conception de la PKI** (hiérarchie, usages).  
- Correcte mise en œuvre du **cycle de vie des certificats**.  
- Niveau de détail des procédures (capacité à reproduire).  
- Compréhension des impacts en cas de compromission d’une CA.

