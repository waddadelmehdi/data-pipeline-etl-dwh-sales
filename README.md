# data-pipeline-etl-dwh-sales

# 🚀 End-to-End Sales Data Pipeline & Data Warehouse

Un pipeline de données complet de bout en bout (ETL) permettant l'extraction des ventes depuis une base ERP opérationnelle, leur transformation/orchestration, leur stockage dans un Data Warehouse PostgreSQL, et leur restitution sur un tableau de bord Power BI.

---

## 🏗️ Architecture du Projet

```text
+-------------------+      +-------------------+      +-------------------+      +------------------+
|  ERP Source DB    | ---> |   Mage.ai         | ---> |  Data Warehouse   | ---> |  Power BI        |
|  (PostgreSQL:5431)|      |  (Orchestrator)   |      |  (PostgreSQL:5433)|      |  (Reporting/BI)  |
+-------------------+      +-------------------+      +-------------------+      +------------------+

```
## 📸 Aperçu du Projet

### 1. Infrastructure Docker Desktop
Les 4 conteneurs (`postgres_source`, `postgres_dwh`, `mage_orchestrator`, `metabase_app`) s'exécutent de façon isolée et interconnectée.
<img width="1264" height="715" alt="image" src="https://github.com/user-attachments/assets/2a3134bf-8ae8-4749-a785-1d2e64982e00" />



### 2. Pipelines d'Orchestration Mage.ai
* **Pipeline d'ingestion :** Chargement des données brutes ERP vers la zone de Staging.
<img width="1083" height="619" alt="image" src="https://github.com/user-attachments/assets/f970a985-5ac0-4ab8-a150-a8395e1159de" />


* **Pipeline DWH :** Transformation, nettoyage et construction du modèle en étoile (`dim_clients` et `fact_ventes`).
<img width="891" height="751" alt="image" src="https://github.com/user-attachments/assets/dda479b7-1561-40b6-a62b-e627e50f599f" />


### 3. Reporting & Dashboard (Metabase)
Visualisation analytique des ventes (ex: répartition du chiffre d'affaires par ville).
<img width="1918" height="943" alt="image" src="https://github.com/user-attachments/assets/08fc4f02-5cf2-4f8a-b004-a8112bc456c3" />
