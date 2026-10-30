# TECHNOVA — Segmentation du réseau Azure

## 1. Objectif

Séparer les ressources de l'entreprise en plusieurs zones réseau afin d'améliorer l'organisation, la sécurité et l'administration de l'infrastructure.

## 2. Plan d'adressage IP

| Sous-réseau | Adresse réseau | Masque | Utilisation |
|---|---|---|---|
| Subnet-Servers | 10.10.1.0/24 | 255.255.255.0 | Serveurs |
| Subnet-Management | 10.10.2.0/24 | 255.255.255.0 | Administration et supervision |
| Subnet-Clients | 10.10.3.0/24 | 255.255.255.0 | Postes utilisateurs |

## 3. Répartition des ressources prévue

### Subnet-Servers
- AZ-DC01 : 10.10.1.10
- AZ-FS01 : 10.10.1.20

### Subnet-Management
- AZ-MGMT01 : 10.10.2.10
- AZ-BACKUP01 : 10.10.2.20

### Subnet-Clients
- AZ-CLIENT01 : 10.10.3.10

Ces adresses sont les adresses privées prévues pour les futures machines virtuelles.

## 4. Pourquoi segmenter le réseau ?

La segmentation permet de séparer les serveurs, les postes clients et les ressources d'administration.

Elle facilite l'application de règles de sécurité spécifiques à chaque zone.

## 5. Résultat

Les trois sous-réseaux ont été créés dans VNet-TECHNOVA.

## 6. Capture d'écran

<img width="951" height="343" alt="image" src="https://github.com/user-attachments/assets/c88df528-07c7-4157-b589-28a6c1edfa60" />


## 7. Compétences acquises

- Création de sous-réseaux.
- Planification d'adressage IPv4.
- Segmentation réseau.
- Préparation d'une infrastructure d'entreprise.
