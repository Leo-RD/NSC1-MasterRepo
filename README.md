# Projet Porte Sécurisée via NFC

Ce dépôt est le **dépôt principal (MASTER)** regroupant l’ensemble des composants du projet de porte sécurisée connectée utilisant la technologie **NFC**.  
Il intègre à la fois la partie physique (Raspberry + lecteur NFC), l’infrastructure logicielle (API, base de données), les interfaces web et mobiles, ainsi que les outils de gestion.

---

## 📌 Architecture globale

Le système est composé de 4 blocs principaux :

1. **Mobile / Web**  
   - Application web déployée sur **Vercel**  
   - Application mobile développée avec **Flutter (Dart)**  
   - Interaction avec l’API pour ouvrir/fermer la porte et consulter les accès

2. **Physique**  
   - **Porte sécurisée** connectée  
   - **Raspberry Pi** gérant les signaux d’ouverture/fermeture  
   - **Lecteur NFC** pour authentification locale  
   - Communication via **Wi-Fi** et **MQTT**

3. **Infrastructure**  
   - **API centrale** exposant les fonctionnalités du système  
   - Base de données pour la gestion des utilisateurs, des accès et des logs

4. **Gestion**  
   - Application de gestion développée en **C#**  
   - Permet la supervision, l’administration et la configuration des accès

---

## 🛠️ Technologies utilisées

- **Frontend :** HTML, CSS, JavaScript (hébergé sur [Vercel](https://nsc-1-door-2.vercel.app/homepage.html))  
- **Mobile :** .NET MAUI  
- **Backend :** API REST (PhpSlim, SlimSkeleton)  
- **Matériel :** Raspberry Pi, module NFC, communication Wi-Fi et MQTT
- **Base de données :** SQL  
- **Gestion :** Application C# de monitoring et administration  

---

## 📂 Structure des dépôts associés

- 🌐 [NSC1-WebRepo](https://github.com/Leo-RD/NSC1_DOOR_2) → site web (accueil, login, inscription)  
- 📱 [Mobile App (Flutter)](https://github.com/Leo-RD/nsc1_mobileapp) → dans ce dépôt MASTER et celui dédié (lien)
- ⚙️ API + Base de données → dans ce dépôt MASTER et celui dédié
- 🔒 Code embarqué (Raspberry + NFC) → dans ce dépôt MASTER  
- 🖥️ [Outil de gestion C#](https://github.com/fuxau/gestionappNSC1_securedoor.git) → dans ce dépôt MASTER et celui dédié (lien) 

---

## 📊 Schéma d’architecture

![Architecture du projet](./docs/SYNOPTIQUE_NSC1.png)  
*(Le schéma ci-dessus illustre les interactions entre les différents blocs : mobile/web, physique, infrastructure et gestion.)*

---

## 🚀 Installation & Lancement

### 1. Cloner le dépôt

```bash
git clone https://github.com/Leo-RD/NSC1-MasterRepo.git
```

### 2. Web

Voir instructions dans le dépôt NSC1-WebRepo

### 3. Mobile

Ouvrir le projet .NET MAUI dans Visual Studio

Lancer sur un émulateur ou un appareil réel

### 4. API & Backend

Ouvrir le projet backend dans Visual Studio

Configurer la base de données (script SQL fourni dans /db/)

Lancer l’API localement ou via un hébergement

### 5. Raspberry Pi

Déployer le code embarqué (C/C++ ou Python selon le module utilisé)

Connecter le lecteur NFC

Configurer la communication réseau (Wi-Fi / LoRaWAN)

### 6. Application de gestion

Ouvrir le projet C# dans Visual Studio

Lancer l’application pour gérer utilisateurs et accès

### 🔒 Fonctionnalités principales

- Authentification via carte NFC

- Ouverture/fermeture de la porte à distance via API

- Suivi des accès en temps réel

- Gestion des utilisateurs et des droits d’accès

- Communication sécurisée via Wi-Fi et LoRaWAN

- Interface mobile et web pour les utilisateurs finaux

- Application de gestion pour les administrateurs

### 📌 Liens utiles

Repo Master (ce dépôt) : NSC1-MasterRepo

Repo Web uniquement : https://github.com/Leo-RD/NSC1_DOOR_2
