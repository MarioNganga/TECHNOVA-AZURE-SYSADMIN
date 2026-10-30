# 02 — Création du réseau virtuel Azure (Virtual Network)

## 1. Objectif

Dans le cadre du projet TECHNOVA, j'ai créé un réseau virtuel Azure afin de permettre la communication entre les futures machines virtuelles de l'infrastructure.

Le réseau virtuel permet d'isoler et d'organiser les ressources Azure dans un environnement réseau privé.

## 2. Configuration du réseau

| Paramètre | Valeur |
|---|---|
| Nom du réseau | VNet-TECHNOVA |
| Groupe de ressources | RG-TECHNOVA-LAB |
| Région | France Central |
| Espace d'adressage IPv4 | 10.10.0.0/16 |
| Masque de sous-réseau | 255.255.0.0 |

## 3. Architecture réseau

Le réseau virtuel utilise l'espace d'adressage privé `10.10.0.0/16`.

Cet espace permet de créer plusieurs sous-réseaux afin de séparer les différents types de machines de l'infrastructure.

Les sous-réseaux sont destinés à accueillir :

- Les serveurs Windows.
- Les serveurs d'administration et de supervision.
- Les machines clientes.

## 4. Étapes de réalisation

1. Accès au portail Azure.
2. Ouverture du service **Réseaux virtuels (Virtual Networks)**.
3. Création d'un nouveau réseau virtuel.
4. Sélection du groupe de ressources `RG-TECHNOVA-LAB`.
5. Configuration de la région `France Central`.
6. Définition de l'espace d'adressage IPv4 `10.10.0.0/16`.
7. Création du réseau virtuel `VNet-TECHNOVA`.

## 5. Vérification

Après la création, j'ai vérifié les éléments suivants :

- Le réseau virtuel apparaît dans le groupe de ressources.
- Le nom du réseau est correct.
- La région est correcte.
- L'espace d'adressage IPv4 est bien configuré.

## 6. Captures d'écran

<img width="765" height="205" alt="image" src="https://github.com/user-attachments/assets/b5640596-2fbf-49ce-9c79-598b8352f928" />


## 8. Conclusion

Le réseau virtuel `VNet-TECHNOVA` constitue la base réseau de l'infrastructure. Il permettra de connecter les futures machines virtuelles et de segmenter le réseau à l'aide de plusieurs sous-réseaux et groupes de sécurité réseau (NSG).
