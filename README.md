# ✈️ Machine Learning : Prédiction du Prix des Billets d'Avion

## 📝 Présentation du Projet
Ce projet consiste à concevoir et déployer un modèle de **Machine Learning de régression** capable de prédire le prix des billets d'avion à partir de données réelles (plus de 300 000 réservations de vols). L'objectif est d'accompagner une plateforme de réservation en identifiant les facteurs clés qui influencent les tarifs (compagnie, escales, classe, durée, etc.) et en fournissant des prédictions hautement fiables.

## 🎯 Objectifs du Projet
* **Exploration & Rigueur Statistique** : Réaliser une Analyse Exploratoire des Données (EDA) approfondie et appliquer des tests statistiques pour valider l'impact des variables sur les prix.
* **Pipeline de Preprocessing Synchrone** : Mettre en place un pipeline de préparation de données robuste avec Scikit-learn afin d'éviter toute fuite de données (*Data Leakage*).
* **Modélisation Comparative** : Entraîner, évaluer et comparer plusieurs algorithmes de régression (Régression Linéaire, Random Forest, Réseaux de Neurones, etc.).
* **Optimisation des Performances** : Atteindre l'objectif métier d'une erreur absolue moyenne (**MAE < 15€**).
* **Industrialisation** : Exporter le modèle final entraîné pour permettre son intégration future.

## 🛠️ Stack Technique
* **Langage** : Python.
* **Manipulation & Analyse** : Pandas, NumPy.
* **Visualisation** : Matplotlib, Seaborn.
* **Machine Learning & Pipeline** : Scikit-learn (LinearRegression, RandomForestRegressor, MLPRegressor, etc.).
* **Sérialisation (Export)** : Joblib.
* **Gestion de Projet** : Jira & GitHub.

---

## 🏗️ Architecture du Pipeline de Machine Learning

Le projet suit une démarche structurée et itérative propre aux projets de Data Science :
1. **EDA & Tests Statistiques** : Compréhension des distributions et validation des hypothèses métier.
2. **Preprocessing (Pipeline)** : Nettoyage, encodage des variables catégorielles, mise à l'échelle (*scaling*) et séparation Train/Test.
3. **Modeling & Tuning** : Entraînement de différents estimateurs et optimisation des hyperparamètres.
4. **Évaluation** : Comparaison des performances basées sur les métriques **MAE**, **RMSE** et **R²**.

---

## 🚀 Étapes de Réalisation

### 1. Analyse Exploratoire des Données (EDA) & Statistiques 🔍
* Analyse de la distribution de la variable cible (*Price*) et détection des valeurs aberrantes.
* Visualisation des relations (impact de la classe, du nombre d'escales ou de la compagnie aérienne sur le prix).
* Application de tests statistiques (ANOVA, T-Test ou tests de corrélation) pour valider mathématiquement la pertinence des features avant la modélisation.

### 2. Pipeline de Preprocessing (Scikit-learn) ⚙️
* Traitement et nettoyage des données manquantes ou incohérentes.
* Encodage adapté des variables qualitatives (One-Hot Encoding pour les variables nominales, Ordinal Encoding pour les hiérarchies comme la classe).
* Normalisation / Standardisation des variables numériques (*StandardScaler* ou *MinMaxScaler*).
* Encapsulation complète dans un `Pipeline` ou `ColumnTransformer` pour garantir la reproductibilité sur le jeu de test.

### 3. Entraînement et Comparaison des Modèles 🧪
* Séparation stricte du dataset en données d'entraînement (Train) et données de test (Test).
* Entraînement d'un modèle de base (Baseline) puis de modèles plus complexes (Ensemble Learning, Deep Learning).
* Suivi et comparaison des résultats pour identifier le modèle qui généralise le mieux sans surapprentissage (*overfitting*).

### 4. Évaluation & Exportation 🏆
* Calcul et interprétation des erreurs : vérification de la conformité avec l'objectif de performance métier (**MAE < 15€**).
* Analyse des résidus du modèle sélectionné pour comprendre les zones d'incertitude.
* Sauvegarde du modèle final optimisé sous format `.joblib` pour mise en production.

---