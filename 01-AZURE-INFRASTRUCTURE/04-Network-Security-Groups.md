# 04 — Création et configuration des Network Security Groups (NSG)

## 1. Objectif

Dans le cadre du projet TECHNOVA, j'ai mis en place des Network Security Groups (NSG) dans Microsoft Azure afin de contrôler les communications réseau entre les différentes parties de mon infrastructure.

Un NSG est un mécanisme de filtrage réseau Azure qui permet d'autoriser ou de refuser le trafic entrant et sortant selon des règles définies.

L'objectif est de renforcer la sécurité du réseau et de séparer les différents environnements de l'entreprise.

## 2. Environnement technique

| Paramètre | Valeur |
|---|---|
| Cloud | Microsoft Azure |
| Groupe de ressources | RG-TECHNOVA-LAB |
| Réseau virtuel | VNet-TECHNOVA |
| Région | France Central |
| Espace d'adressage | 10.10.0.0/16 |

## 3. Création des Network Security Groups

J'ai créé trois groupes de sécurité réseau afin de protéger les différents sous-réseaux de l'infrastructure.

| Nom du NSG | Sous-réseau associé | Rôle |
|---|---|---|
| NSG-TECHNOVA-SERVERS | Subnet-Servers | Protection des serveurs |
| NSG-TECHNOVA-MGMT | Subnet-Management | Protection des serveurs d'administration |
| NSG-TECHNOVA-CLIENTS | Subnet-Clients | Protection des postes clients |

## 4. Rôle des différents NSG

### NSG-TECHNOVA-SERVERS

Ce groupe de sécurité est destiné aux serveurs principaux de l'infrastructure.

Exemples :
- AZ-DC01 : contrôleur de domaine Active Directory et DNS.
- AZ-FS01 : serveur de fichiers Windows.

### NSG-TECHNOVA-MGMT

Ce groupe de sécurité est destiné aux serveurs d'administration et de supervision.

Exemples :
- AZ-MGMT01 : serveur Linux destiné à Zabbix et GLPI.
- AZ-BACKUP01 : serveur de sauvegarde.

### NSG-TECHNOVA-CLIENTS

Ce groupe de sécurité est destiné aux postes clients Windows qui seront intégrés au domaine Active Directory.

Exemple :
- AZ-CLIENT01 : poste client Windows.

## 5. Étapes de réalisation

Pour chaque NSG, j'ai effectué les opérations suivantes :

1. Accès au portail Microsoft Azure.
2. Recherche du service Network Security Groups.
3. Création d'un nouveau groupe de sécurité réseau.
4. Sélection de l'abonnement Azure for Students.
5. Sélection du groupe de ressources RG-TECHNOVA-LAB.
6. Définition du nom du NSG.
7. Sélection de la région France Central.
8. Validation et déploiement de la ressource.

## 6. Association des NSG aux sous-réseaux

Après leur création, les groupes de sécurité réseau ont été associés aux sous-réseaux correspondants du réseau virtuel VNet-TECHNOVA.

Cette association permet d'appliquer les règles de filtrage réseau aux ressources présentes dans chaque sous-réseau.

## 7. Politique de sécurité réseau

Les règles de sécurité seront adaptées aux besoins de communication de l'infrastructure.

Les principes retenus sont :

- Limiter les accès aux ressources nécessaires.
- Ne pas exposer les services d'administration directement à Internet.
- Ne pas exposer SMB (port 445) à Internet.
- Autoriser uniquement les communications nécessaires entre les serveurs et les clients.
- Contrôler les accès d'administration.

Les règles personnalisées seront documentées et testées lors de la configuration des machines virtuelles et d'Active Directory.

## 8. Vérifications

Les vérifications effectuées ou à effectuer :

- Présence des trois NSG dans le groupe de ressources.
- Vérification des noms des NSG.
- Vérification de leur région.
- Vérification de leur association avec les bons sous-réseaux.
- Vérification des règles de sécurité appliquées.

## 9. Captures d'écran

<img width="770" height="352" alt="image" src="https://github.com/user-attachments/assets/f420e032-e8a9-4df9-81a7-06e45f56dc86" />


## 10. Compétences développées

- Création de Network Security Groups dans Azure.
- Compréhension du filtrage réseau.
- Segmentation et sécurisation d'une infrastructure cloud.
- Association des NSG aux sous-réseaux.
- Préparation des règles de sécurité réseau.

## 11. Conclusion

La mise en place des trois Network Security Groups constitue une première étape dans la sécurisation de l'infrastructure TECHNOVA.

Cette organisation permettra de contrôler les communications réseau entre les serveurs, les équipements d'administration et les postes clients.

Les prochaines étapes consisteront à déployer les machines virtuelles Windows Server et à adapter les règles réseau aux services Active Directory, DNS et SMB.
