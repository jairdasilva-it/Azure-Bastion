# Azure Bastion Lab

## 🎯 Objectif

Déployer et configurer **Azure Bastion** afin d'administrer une machine virtuelle **Windows Server 2025** sans exposer de port **RDP (3389)** ni d'adresse IP publique.

Ce projet a été réalisé dans le cadre de ma préparation à la certification **Microsoft Azure AZ-104** afin de développer mes compétences en administration Cloud, en sécurisation des accès et en gestion des infrastructures Azure.

---

## 💻 Technologies utilisées

- Microsoft Azure
- Azure Bastion
- Windows Server 2025
- Azure Virtual Network (VNet)
- Azure Subnets
- Network Security Groups (NSG)

---

## 🏗️ Architecture

```text
                Internet
                    │
                    ▼
             Azure Bastion
                    │
                    ▼
      Windows Server 2025 VM
        (Adresse IP privée)
```

---

## 🎯 Résultat

Grâce à Azure Bastion :

- aucune adresse IP publique n'est nécessaire sur la machine virtuelle ;
- aucun port RDP n'est exposé sur Internet ;
- l'administration s'effectue directement depuis le portail Azure via une connexion sécurisée.

Cette architecture respecte les bonnes pratiques de sécurisation des machines virtuelles Azure.

---

## 👤 Auteur

**Jair Da Silva**

Technicien Systèmes & Réseaux | Support IT N1/N2 | Microsoft Azure

GitHub : https://github.com/jairdasilva-it

LinkedIn : https://www.linkedin.com/in/jair-da-silva-6b14aa278

---

# 🚀 Étapes du projet

## 1️⃣ Création du réseau virtuel

- Création du Virtual Network
- Création du sous-réseau **vm-subnet**
- Création du sous-réseau **AzureBastionSubnet**

---

## 2️⃣ Déploiement de la machine virtuelle

- Création d'une machine virtuelle Windows Server 2025
- Déploiement dans le sous-réseau **vm-subnet**
- Attribution temporaire d'une adresse IP publique afin d'effectuer les premiers tests

---

## 3️⃣ Déploiement d'Azure Bastion

- Création du service Azure Bastion
- Déploiement dans le sous-réseau **AzureBastionSubnet**
- Attribution d'une adresse IP publique au Bastion

---

## 4️⃣ Sécurisation de la machine virtuelle

- Suppression de l'adresse IP publique de la VM
- Vérification que la machine virtuelle n'est plus accessible directement depuis Internet

---

## 5️⃣ Validation

- Connexion réussie à la machine virtuelle via Azure Bastion
- Ouverture d'une session Windows Server directement depuis le portail Azure
- Validation du fonctionnement sans adresse IP publique sur la machine virtuelle

---

# 📸 Captures d'écran

## 1. Réseau virtuel et sous-réseaux

Création du Virtual Network avec les sous-réseaux **vm-subnet** et **AzureBastionSubnet**.

![Virtual Network](01-vnet-subnets.png)

---

## 2. Azure Bastion

Déploiement du service Azure Bastion dans le sous-réseau dédié.

![Azure Bastion](02-bastion-host.png)

---

## 3. Machine virtuelle (avant sécurisation)

Machine virtuelle Windows Server déployée avant la suppression de son adresse IP publique.

![Machine virtuelle](03-vm-private.png)

---

## 4. Machine virtuelle sans adresse IP publique

Après suppression de l'adresse IP publique, la machine virtuelle n'est plus accessible directement depuis Internet.

![VM sans IP publique](04-vm-no-public-ip.png)

---

## 5. Connexion via Azure Bastion

Connexion sécurisée à la machine virtuelle directement depuis le portail Azure.

![Connexion Bastion](05-connect-via-bastion.png)

---

## 6. Session Windows Server

Ouverture de la session Windows Server via Azure Bastion sans utilisation du protocole RDP sur Internet.

![Windows Server](06-windows-server-session.png)

---

# 💼 Compétences démontrées

- Déploiement d'une infrastructure Microsoft Azure
- Administration de machines virtuelles Azure
- Configuration d'Azure Bastion
- Gestion des Virtual Networks (VNet)
- Gestion des sous-réseaux Azure
- Gestion des adresses IP publiques
- Sécurisation des accès aux machines virtuelles
- Administration Windows Server
- Bonnes pratiques de sécurité Cloud
- Préparation à la certification Microsoft AZ-104
