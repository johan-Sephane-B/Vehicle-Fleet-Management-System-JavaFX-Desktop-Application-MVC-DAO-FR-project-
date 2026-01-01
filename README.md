# 🚗 Système de Gestion de Parc Automobile

## 📌 Présentation

Ce projet est une **application desktop de gestion de parc automobile** développée en **Java avec JavaFX**. Il repose sur une architecture **MVC (Model–View–Controller)** et le **patron de conception DAO (Data Access Object)** afin d’assurer une séparation claire des responsabilités et une bonne maintenabilité du code.

L’application simule un système réel de gestion de flotte automobile, dans un contexte académique et professionnel.

---

## 🎯 Fonctionnalités principales

* Gestion des **véhicules** (ajout, modification, suppression, consultation)
* Gestion des **missions**
* Gestion des **affectations / participations**
* Gestion des **utilisateurs et rôles**
* Persistance des données via une base **MySQL**
* Interface graphique moderne avec **JavaFX (FXML)**

---

## 🧱 Architecture du projet

Le projet suit une architecture en couches bien définies :

* **Model** : entités métier (Vehicule, Mission, Participation, etc.)
* **DAO** : accès aux données (DAO générique + DAO spécifiques avec JDBC)
* **View** : interfaces graphiques JavaFX (`.fxml`)
* **Controller** : logique applicative et gestion des événements

Cette architecture permet :

* une séparation claire des responsabilités,
* une meilleure lisibilité du code,
* une évolutivité facilitée.

---

## 🛠️ Technologies utilisées

* **Java** (modulaire)
* **JavaFX**
* **JDBC**
* **MySQL**
* **Architecture MVC**
* **DAO Pattern**

---

## 📂 Structure du projet

```
📁 src/
 ├── 📁 model        # Entités métier
 ├── 📁 dao          # Accès aux données (DAO, DAOImpl)
 ├── 📁 view         # Interfaces JavaFX (FXML)
 ├── 📁 controller   # Contrôleurs JavaFX
 └── module-info.java
```

---

## ▶️ Prérequis et exécution

### Prérequis

* Java JDK 11 ou plus
* JavaFX configuré
* Serveur MySQL

### Exécution

1. Cloner le projet
2. Configurer la base de données MySQL
3. Mettre à jour les paramètres de connexion JDBC
4. Lancer la classe principale de l’application

---

## 🎓 Contexte

Projet académique réalisé dans le cadre d’une formation en **informatique / MIAGE**, visant à appliquer les bonnes pratiques de développement logiciel et de conception orientée objet.

---

## 🚀 Évolutions possibles

* Authentification et gestion avancée des rôles
* Interface web ou API REST
* Sécurité et chiffrement des données
* Statistiques et tableaux de bord

---

## 👤 Auteur

**Stéphane**

---

📌 *Ce projet est à but pédagogique et peut servir de base pour des projets professionnels plus avancés.*
