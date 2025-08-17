# 🚦 Trafic Management System

Un projet en **C** simulant la gestion du trafic routier à l’aide de files d’attente (queues) et de feux de circulation. Ce système illustre la priorité des véhicules et la régulation de leur passage en fonction de l’état du feu.

---

## 📖 Vue d’Ensemble

Le projet implémente :

* Une **file d’attente dynamique** pour gérer les véhicules.
* Un système de **priorité** : véhicules d’urgence, bus, voitures, vélos.
* La **simulation d’un feu de circulation** avec cycles (ROUGE, JAUNE, VERT).
* La **journalisation** des événements dans un fichier `traffic_log.txt`.

---

## 📂 Structure du Projet

```
Trafic_management/
├── libraries/
│   └── queue.h         # Définition des structures et fonctions de gestion de file
├── main.c              # Programme principal (simulation)
├── README.md           # Documentation du projet
└── traffic_log.txt     # Fichier de log généré lors de l'exécution
```

---

## ⚙️ Compilation et Exécution

1. Compiler le projet :

```bash
gcc main.c -o traffic
```

2. Lancer la simulation :

```bash
./traffic
```

---

## 🚗 Types de Véhicules

* **🚑 Emergency (urgence)** → priorité maximale
* **🚌 Bus** → priorité moyenne
* **🚗 Car (voiture)** → priorité basse
* **🚲 Bike (vélo)** → priorité la plus basse

---

## 🔦 Gestion des Feux de Circulation

Le système simule un cycle :

* 🔴 Rouge → arrêt total
* 🟡 Jaune → transition
* 🟢 Vert → autorisation de passage

Chaque changement d’état est affiché et journalisé.

---

## 📜 Fonctionnalités Principales

* **Création de véhicules** avec ID, type et temps d’arrivée.
* **Ajout dans la file** avec gestion des priorités.
* **Suppression (déqueue)** conditionnée par l’état du feu.
* **Simulation de cycles** de feux de circulation.
* **Affichage en console** de la file d’attente.
* **Log automatique** des événements dans `traffic_log.txt`.

---

## 📝 Exemple d’Exécution

```
État initial de la file d'attente:
[U] -> [B] -> [C] -> [V] -> NULL

Simulation du cycle des feux de circulation:
Le feu de circulation est devenu JAUNE.
Le feu de circulation est devenu VERT.
...

Retrait des véhicules:
Véhicule 3 retiré.
Véhicule 2 retiré.
...

État final de la file d'attente:
NULL
```

---

## 📦 Améliorations Futures

* Support multi-voies.
* Gestion avancée des priorités (temps d’attente).
* Interface graphique pour visualiser le trafic.
* Génération de statistiques (temps d’attente moyen, nombre de véhicules).

---
