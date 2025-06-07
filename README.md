# 📊 Projet Big Data & Machine Learning — Groupe 03

Projet réalisé dans le cadre du module *Machine Learning et Big Data* — Master 2 Science des Données  
Encadré par : Dr Constantin  
Date de rendu : 7 juin 2025

---

## 🧩 Objectif du projet

Créer un pipeline de traitement de données **basé sur l'architecture Kappa** pour :
- Collecter des données financières en temps réel depuis [polygon.io](https://polygon.io)
- Les stocker dans **Elasticsearch**
- Entraîner un modèle de **Machine Learning** pour prédire le prix de clôture (`close`) à partir du **volume**
- Visualiser et interagir avec les résultats via une **application Streamlit**

---

## structuration du projet
BigDataML/
├── virtualEnv/                        ← environnement virtuel
├── visualisation.py                      ← application Streamlit (visualisation + prédiction)
├── collect_data.py     ← collecte des données depuis polygon.io vers Elasticsearch
├── predict.py ← prédiction "offline" en script

---

## ⚙️ Architecture technique

```mermaid
graph TD;
    A[polygon.io API] --> B[Script de streaming Python];
    B --> C[Elasticsearch];
    C --> D[Application Streamlit];
    C --> E[Script ML - Prédiction close];
