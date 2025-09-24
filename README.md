# 🚀 Mini-projet Azure Data Factory - Sakila

## 📌 Description
Ce projet illustre la mise en place d’une **solution ETL (Extract, Transform, Load)** sur **Azure** en utilisant :
- **Azure Data Factory (ADF)** pour l’orchestration et la transformation des données.
- **Azure SQL Database** pour stocker les données sources et cibles.
- **Azure Storage Account** pour le stockage des données intermédiaires.
- **Azure Resource Group** pour organiser les ressources.

Le projet s’appuie sur la base de données **Sakila** (base de démo classique) afin de construire un **mini Data Warehouse** avec des dimensions et des faits.

---

## ⚙️ Architecture
L’architecture du projet repose sur plusieurs composants Azure :

- **Resource Group** : `Sakila_demo`
- **Azure Data Factory** : `factorysakila`
- **Serveur SQL** : `serversakila`
- **Bases de données SQL** :
  - `sakiladb` : base source
  - `sakila_DW_simple` : entrepôt de données cible (Data Warehouse)
- **Stockage Blob** : `stockageblobsakila`

---

## 📊 Flux de données
### Pipelines créés dans Azure Data Factory :
1. **FluxDimCustomer** → transformation et chargement de la dimension *Customer*  
2. **FluxDimFilm** → transformation et chargement de la dimension *Film*  
3. **FluxDimStore** → transformation et chargement de la dimension *Store*  
4. **FluxFactRental** → transformation et chargement de la table de faits *Rental*  

➡️ Ces pipelines alimentent progressivement le **Data Warehouse**.

---

## 🛠 Étapes principales
1. **Création des ressources** dans Azure Portal (ADF, SQL Server, Blob Storage).
2. **Développement des pipelines** dans Azure Data Factory Studio.
3. **Chargement des données sources** depuis `sakiladb`.
4. **Transformation et nettoyage** via les flux de données (ADF Data Flows).
5. **Chargement dans le Data Warehouse** `sakila_DW_simple`.
6. **Validation avec SSMS** (SQL Server Management Studio) pour vérifier les données chargées.

---

## ✅ Résultats
- Données transformées et stockées dans les dimensions :
  - `DimCustomer`
  - `DimFilm`
  - `DimStore`
- Données factuelles consolidées dans :
  - `FactRental`
- Plus de **16 000 lignes insérées** avec succès dans la table de faits (voir capture d’écran des exécutions réussies).

---

## 📸 Captures d’écran
Quelques visuels du projet :
- Vue d’ensemble d’Azure Data Factory
- Pipelines exécutés avec succès
- Flux de données (Data Flow) détaillés
- Tables créées dans le Data Warehouse (`sakila_DW_simple`)
- Validation des résultats dans SSMS

*(Les captures sont disponibles dans le dossier `/screenshots` du projet)*

---

## 🧑‍💻 Technologies utilisées
- **Azure Data Factory (V2)**
- **Azure SQL Database**
- **Azure Blob Storage**
- **SQL Server Management Studio (SSMS)**
- **Azure Portal**

---

## 📂 Structure du dépôt
