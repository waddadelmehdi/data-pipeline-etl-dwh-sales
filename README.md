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
