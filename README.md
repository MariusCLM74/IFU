# Projet IFU : Optimisation des tournées de livraison – GoodCoffee Inc.

**Auteurs :** BAUDOIN Anaëlle, CHALUMEAU Marius, JESTIN Léna 
**Département :** Génie Industriel – INSA Lyon  
**Année universitaire :** 2025-2026  
**Cours :** Industrie du Futur – Optimisation de la chaîne logistique (L. MONCLA & F. TOUZOUT)

---

## Présentation du projet
Ce projet consiste à concevoir un système intelligent de planification de tournées pour la société **GoodCoffee Inc.**, basée à Brooklyn. L'objectif est de livrer quotidiennement des magasins Starbucks à travers New York en respectant les montées en charge progressives du contrat (de 20 à plus de 225 points de vente).

Le projet repose sur deux piliers technologiques :
1.  **Data Science** : inférence des coûts de transport (temps de trajet) via l'analyse d'un dataset de 1,5 million de courses de taxis (Yellow Taxi Trips)
2.  **Recherche Opérationnelle** : optimisation des tournées de véhicules (VRP) sous contrainte de capacité (300 kg par van)

---

## Structure du projet
* `Projet_IFU_Main.ipynb` : Notebook principal contenant le pipeline complet (Nettoyage, ML, Clustering, TSP)
* `gbr.pkl` : Modèle de **Gradient Boosting** pré-entraîné, chargé via `pickle` pour garantir une exécution rapide du TSP
* Fichiers .csv récupérés sur Moodle

---

## Instructions d'exécution (Google Colab)

Le code a été conçu pour être exécuté sur Google Colab.

1.  **Ouverture** : Importer le notebook dans l'environnement Colab.
2.  **Installation des dépendances** : La cellule initiale installe automatiquement les outils nécessaires :
    ```python
    !pip install pulp
    ```
3.  **Récupération des données** : le notebook inclut une cellule de récupération automatique des fichiers (via un dépôt GitHub) pour le modèle `.pkl` et les datasets
4.  **Lancement** : exécuter toutes les cellules
    * *Note : Les étapes de prédiction pour le Stage 4 peuvent prendre 2 à 3 minutes en raison du volume de calcul de la matrice de coûts.*