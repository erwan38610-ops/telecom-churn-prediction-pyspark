# 📡 Prédiction de l'attrition (Churn) Telecom avec PySpark

Ce projet vise à identifier les facteurs clés du désabonnement des clients chez un opérateur de télécommunications en utilisant l'écosystème **Apache Spark**.

## 📊 Problématique Métier
Le coût d'acquisition d'un nouveau client étant supérieur au coût de rétention, l'objectif est de prédire la probabilité de départ d'un client (Churn) à partir de données démographiques, de services souscrits et de facturation (Dataset IBM Telco).

## 🛠 Stack Technique & Méthodologie
L'intégralité du traitement a été réalisée avec l'API native de **PySpark** :
* **Spark SQL :** Ingestion et nettoyage des données (gestion des types, valeurs manquantes sur `TotalCharges`).
* **Feature Engineering (Pipelines) :** Utilisation de `StringIndexer`, `OneHotEncoder` et `VectorAssembler` pour préparer les données de manière scalable.
* **Machine Learning (MLlib) :** Comparaison de modèles (Régression Logistique vs Random Forest).

## 📈 Résultats Clés
* **Performance :** Précision (Accuracy) de **81%** et AUC de **0.84**.
* **Insights Business :** Le type de contrat (Month-to-month) et l'absence de support technique sont les prédicteurs les plus forts du désabonnement.
* **Scalabilité :** Utilisation de l'architecture distribuée de Spark pour garantir la montée en charge sur de gros volumes de données.

## 📂 Contenu du dépôt
* `Spark_IBM.ipynb` : Notebook complet des analyses et modèles.
* `Spark_IBM.pdf` : Support de présentation synthétisant la démarche et les résultats.