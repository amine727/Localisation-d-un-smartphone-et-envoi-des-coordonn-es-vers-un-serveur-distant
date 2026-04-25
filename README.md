# Localisation d’un smartphone et envoi des coordonnées vers un serveur distant

## 🧠 Description

Ce projet permet de :

- 📱 Récupérer la position GPS (latitude / longitude) depuis une application Android
- 🌐 Envoyer ces données vers un serveur PHP
- 🗄️ Stocker les coordonnées dans une base de données MySQL
- 🔍 Vérifier les données via phpMyAdmin

---


## ⚙️ Technologies utilisées

- Android (Java)
- PHP (PDO)
- MySQL
- XAMPP
- Postman (tests API)

---

## 📁 Structure du projet
localisation/
│
├── connexion/
│ └── Connexion.php
│
├── createPosition.php


### Table :


### Structure :

- id (INT, AUTO_INCREMENT)
- latitude (DOUBLE)
- longitude (DOUBLE)
- date_position (DATETIME)
- imei (VARCHAR)

---

## 🔌 Connexion à la base de données

📸 **Connexion.php**

<img width="948" height="442" alt="1" src="https://github.com/user-attachments/assets/217d68f3-4a9d-4a16-9a53-7f22e095a0e2" />

---

## 🌐 API PHP (createPosition.php)

📸 **Script PHP**

<img width="936" height="569" alt="2" src="https://github.com/user-attachments/assets/3b4b59b3-5cef-455f-babc-abed34db24e8" />

---

## 🧪 Test avec Postman


### Requête :

- Method: POST
- URL: http://localhost/localisation/createPosition.php

  
### Body (x-www-form-urlencoded):

| Key       | Value  |
|----------|--------|
| latitude  | 31.6   |
| longitude | -7.9   |
| imei      | 123456 |

📸 **Test Postman**

<img width="1264" height="772" alt="3" src="https://github.com/user-attachments/assets/0a5dc9de-9455-4cdc-8df8-dfe65de4823d" />

---

## 🗄️ Résultat dans phpMyAdmin

📸 **Base de données**

<img width="935" height="529" alt="4" src="https://github.com/user-attachments/assets/adee1488-8a22-452a-90c6-6d0a36806246" />

---

## 📱 Application Android

### Fonctionnalités :

- 📍 Récupération GPS
- 🌐 Envoi des données via Volley
- 📡 Communication avec API PHP

---

## 📊 Logs Android (Logcat)

📸 **Logs**

<img width="1791" height="231" alt="5" src="https://github.com/user-attachments/assets/fdc458cd-70bb-48d1-80f7-280270bec0c5" />

### Résultat :
GPS: Lat: 31.6 Lon: -7.9
SERVER: {"status":"success"}
