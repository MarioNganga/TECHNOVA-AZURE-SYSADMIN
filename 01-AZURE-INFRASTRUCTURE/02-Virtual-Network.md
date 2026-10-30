# TECHNOVA — Configuration du réseau virtuel Azure

## 1. Objectif

Créer un réseau virtuel Azure afin de permettre aux futurs serveurs et postes clients de communiquer au sein d'un réseau privé.

## 2. Configuration réseau

| Paramètre | Valeur |
|---|---|
| Nom | VNet-TECHNOVA |
| Groupe de ressources | RG-TECHNOVA-LAB |
| Région | France Central |
| Adresse réseau | 10.10.0.0/16 |
| Masque | 255.255.0.0 |

## 3. Rôle du réseau virtuel

Le réseau virtuel Azure permet d'isoler logiquement les ressources du laboratoire et de contrôler leurs communications.

Il constitue la base réseau de l'infrastructure TECHNOVA.

## 4. Architecture prévue

Le réseau accueillera trois zones :

- Subnet-Servers : serveurs Windows.
- Subnet-Management : administration, supervision et sauvegarde.
- Subnet-Clients : postes utilisateurs.

## 5. Résultat

Le réseau virtuel VNet-TECHNOVA a été créé dans Azure.

## 6. Capture d'écran

<img width="1059" height="237" alt="image" src="https://github.com/user-attachments/assets/9a130187-6c8b-4258-89a7-695bd7779f88" />

## 7. Compétences acquises

- Création d'un réseau virtuel Azure.
- Configuration d'un espace d'adressage IPv4.
- Compréhension de la segmentation réseau.
