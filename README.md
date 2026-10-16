# 🤖 Robot de Livraison Autonome & Application Flutter

**Projet académique — Université Française d’Égypte (UFE), Le Caire**  
**Année universitaire : 2023–2024**

---

# 🇫🇷 Version française

## 📌 Présentation

Ce projet académique porte sur la conception d'un système de livraison autonome destiné à une cafétéria. Il combine un robot mobile de service, développé autour d'une plateforme Arduino, et une application mobile Flutter permettant aux utilisateurs de passer et de gérer leurs commandes.

Le système vise à automatiser le processus de livraison, depuis la prise de commande jusqu'au déplacement du robot vers le point de livraison.

## ⚙️ Fonctionnalités principales

- 🛒 Gestion et traitement des commandes
- 📱 Application mobile Flutter pour passer des commandes
- 🤖 Commande des moteurs et déplacement du robot
- 🚧 Détection et évitement des obstacles
- 🛑 Arrêt du robot lorsqu'un obstacle est trop proche
- 🔔 Notifications et suivi du processus de commande
- ☕ Application à un scénario de livraison en cafétéria

## 🔄 Workflow

```text
Passage de commande
        ↓
Traitement de la commande
        ↓
Attente de la livraison
        ↓
Navigation du robot
        ↓
Livraison de la commande
```

## 🏗️ Architecture du système

Le système est organisé autour de quatre couches principales :

- **Interface utilisateur :** application Flutter permettant aux utilisateurs d'interagir avec le système.
- **Couche applicative :** gestion du processus de commande et des interactions entre les composants.
- **Couche données :** stockage et gestion des données de l'application.
- **Couche robotique :** commande des moteurs, lecture des capteurs, navigation et évitement des obstacles.

## 🤖 Robot mobile et circuit Arduino

Le prototype robotique utilise une carte Arduino pour traiter les informations des capteurs et commander les moteurs à courant continu.

### Matériel

- Carte Arduino Uno
- 2 moteurs à courant continu avec réducteur JGA25-370, 12 V – 133 RPM
- 4 roues de 10 cm de diamètre
- Circuit de commande des moteurs basé sur un pont en H L293D
- Capteur ultrasonique pour mesurer la distance aux obstacles
- Capteur PIR pour détecter les mouvements dans son champ de détection
- Buzzer pour les alertes sonores
- LED pour l'indication d'état

### Fonctionnement du circuit

- **Commande des moteurs :** l'Arduino pilote les deux moteurs à travers le circuit L293D.
- **Détection des obstacles :** le capteur ultrasonique mesure la distance entre le robot et les objets situés devant lui.
- **Évitement des obstacles :** le programme arrête le robot et commande une manœuvre de rotation lorsqu'un obstacle entre dans la zone de détection définie.
- **Arrêt d'urgence de proximité :** lorsque la distance mesurée atteint le seuil critique de 10 cm, le robot s'arrête et le buzzer émet une alerte sonore.
- **Détection de mouvement :** le capteur PIR fournit une information complémentaire sur les mouvements détectés. Il ne remplace pas la mesure de distance du capteur ultrasonique.

### Schéma du circuit Arduino

![Circuit Arduino du robot mobile autonome](Robot%20Circuit/Autonomous%20robot.png)

*Circuit de commande du robot comprenant l'Arduino, le pilote de moteurs, les capteurs et les éléments de signalisation.*

## 📱 Application mobile Flutter

L'application mobile constitue l'interface utilisateur du système. Elle est destinée à faciliter la prise de commande et la gestion du processus de livraison.

Les fonctionnalités prévues comprennent :

- Interface de commande pour les utilisateurs
- Gestion des commandes de cafétéria
- Intégration avec les données de l'application
- Communication avec le système de livraison

## 🎯 Objectif du projet

Développer un prototype de livraison autonome en environnement de cafétéria en associant robotique mobile, systèmes embarqués, détection d'obstacles et application mobile.

---

# 🇬🇧 English Version

# 🤖 Autonomous Delivery Robot & Flutter Application

**Academic Project — French University of Egypt (UFE), Cairo**  
**Academic Year: 2023–2024**

## 📌 Overview

This academic project focuses on designing an autonomous delivery system for a cafeteria. It combines an Arduino-based mobile service robot with a Flutter mobile application that allows users to place and manage orders.

The system aims to automate the delivery workflow, from order placement to the robot's movement toward the delivery location.

## ⚙️ Key Features

- 🛒 Order management and processing
- 📱 Flutter mobile application for placing orders
- 🤖 DC motor control and robot movement
- 🚧 Obstacle detection and avoidance
- 🛑 Proximity-triggered stopping
- 🔔 Notifications and order workflow management
- ☕ Cafeteria delivery use case

## 🔄 Workflow

```text
Place an Order
      ↓
Process the Order
      ↓
Wait for Delivery
      ↓
Robot Navigation
      ↓
Deliver the Order
```

## 🏗️ System Architecture

The system is organized into four main layers:

- **User Interface Layer:** Flutter application for user interaction.
- **Application Layer:** order processing and interactions between system components.
- **Data Layer:** application data storage and management.
- **Robotics Layer:** motor control, sensor readings, navigation, and obstacle avoidance.

## 🤖 Mobile Robot and Arduino Circuit

The robotic prototype uses an Arduino board to process sensor readings and control the DC motors.

### Hardware Components

- Arduino Uno
- 2 JGA25-370 geared DC motors, rated at 12 V and 133 RPM
- 4 wheels, each with a diameter of 10 cm
- L293D H-bridge motor driver
- Ultrasonic distance sensor for obstacle detection
- PIR motion sensor for detecting movement within its field of view
- Buzzer for audible alerts
- LEDs for status indication

### Circuit Operation

- **Motor control:** the Arduino controls both DC motors through the L293D motor driver.
- **Obstacle detection:** the ultrasonic sensor measures the distance between the robot and objects in front of it.
- **Obstacle avoidance:** the program stops the robot and commands a turning maneuver when an obstacle enters the defined detection range.
- **Proximity emergency stop:** when the measured distance reaches the critical threshold of 10 cm, the robot stops and activates the buzzer.
- **Motion detection:** the PIR sensor provides supplementary movement information. It does not replace the ultrasonic sensor's distance measurements.

### Arduino Circuit Diagram

![Arduino circuit of the autonomous mobile robot](Robot%20Circuit/Autonomous%20robot.png)

*Arduino-based control circuit featuring the motor driver, sensors, and audible and visual indicators.*

## 📱 Flutter Mobile Application

The mobile application provides the user interface for interacting with the delivery system. It is designed to support order placement and delivery workflow management.

Intended functionalities include:

- User interface for placing cafeteria orders
- Order management
- Integration with application data
- Interaction with the delivery system

## 🎯 Project Objective

To develop an autonomous cafeteria delivery prototype integrating mobile robotics, embedded systems, obstacle detection, and a Flutter mobile application.

---

## 📚 Project Information

- **Institution:** French University of Egypt (UFE), Cairo, Egypt
- **Academic Year:** 2023–2024
- **Project Type:** Academic / Engineering Project
- **Domains:** Mobile Robotics, Embedded Systems, Flutter, Autonomous Delivery

## 👥 Project Team

- Kaltam Ahmat Kossi
- Karim Magdy
- Kirolos Akram

**Supervisor:** Pr. Sherin Moussa