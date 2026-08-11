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

<img width="1264" height="715" alt="image" src="https://github.com/user-attachments/assets/2a3134bf-8ae8-4749-a785-1d2e64982e00" />
