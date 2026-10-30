# 03 — Création des sous-réseaux Azure (Subnets)

## 1. Objectif

Dans le cadre du projet TECHNOVA, j'ai divisé le réseau virtuel `VNet-TECHNOVA` en plusieurs sous-réseaux.

Cette segmentation permet de séparer les serveurs, les machines d'administration et les postes clients.

Elle facilite l'organisation du réseau et la mise en place de règles de sécurité adaptées à chaque environnement.

## 2. Configuration générale

| Paramètre | Valeur |
|---|---|
| Réseau virtuel | VNet-TECHNOVA |
| Espace d'adressage | 10.10.0.0/16 |
| Groupe de ressources | RG-TECHNOVA-LAB |

## 3. Liste des sous-réseaux

| Nom du sous-réseau | Adresse réseau | Masque |
|---|---|---|
| Subnet-Servers | 10.10.1.0/24 | 255.255.255.0 |
| Subnet-Management | 10.10.2.0/24 | 255.255.255.0 |
| Subnet-Clients | 10.10.3.0/24 | 255.255.255.0 |

## 4. Rôle de chaque sous-réseau

### Subnet-Servers

Plage : `10.10.1.0/24`

Ce sous-réseau est destiné aux serveurs principaux de l'entreprise :

- AZ-DC01 : serveur Active Directory et DNS (IP prévue : 10.10.1.10).
- AZ-FS01 : serveur de fichiers (IP prévue : 10.10.1.20).

### Subnet-Management

Plage : `10.10.2.0/24`

Ce sous-réseau est destiné aux serveurs d'administration, de supervision et de sauvegarde :

- AZ-MGMT01 : serveur Linux de supervision (IP prévue : 10.10.2.10).
- AZ-BACKUP01 : serveur de sauvegarde (IP prévue : 10.10.2.20).

### Subnet-Clients

Plage : `10.10.3.0/24`

Ce sous-réseau est destiné aux postes clients de l'entreprise :

- AZ-CLIENT01 : poste client Windows (IP prévue : 10.10.3.10).

## 5. Étapes de réalisation

1. Accès au réseau virtuel `VNet-TECHNOVA`.
2. Ouverture de la section **Subnets**.
3. Création du sous-réseau `Subnet-Servers`.
4. Configuration de l'adresse `10.10.1.0/24`.
5. Création du sous-réseau `Subnet-Management`.
6. Configuration de l'adresse `10.10.2.0/24`.
7. Création du sous-réseau `Subnet-Clients`.
8. Configuration de l'adresse `10.10.3.0/24`.
9. Vérification des trois sous-réseaux dans Azure Portal.

## 6. Vérifications

Les vérifications à effectuer :

- Les trois sous-réseaux sont présents dans `VNet-TECHNOVA`.
- Chaque sous-réseau possède la bonne plage IPv4.
- Les plages ne se chevauchent pas.
- Les sous-réseaux appartiennent au bon réseau virtuel.

## 7. Captures d'écran

<img width="976" height="371" alt="image" src="https://github.com/user-attachments/assets/d728eaf8-c4ba-44ce-9b10-29531a35b2a3" />


## 8. Compétences développées

- Segmentation d'un réseau virtuel.
- Configuration des plages IPv4.
- Organisation des serveurs et des postes clients.
- Préparation d'une architecture réseau sécurisée.
- Planification de l'adressage IP.

## 9. Conclusion

La segmentation du réseau `VNet-TECHNOVA` permet de séparer logiquement les serveurs, les équipements d'administration et les postes clients.

Cette organisation facilitera l'application des règles de sécurité réseau avec les Network Security Groups (NSG).
