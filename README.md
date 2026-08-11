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

<img width="1264" height="715" alt="image" src="https://github.com/user-attachments/assets/34ba00f1-f50b-4b4e-bb79-075b2ae57b16" />


<img width="1083" height="619" alt="image" src="https://github.com/user-attachments/assets/2af171f9-b40e-47ce-bf17-02249fc3a5fa" />


<img width="1919" height="943" alt="image" src="https://github.com/user-attachments/assets/ae13df55-b4c6-4db4-86f0-3261c4639f30" />



<img width="1918" height="943" alt="image" src="https://github.com/user-attachments/assets/e251ab26-6626-474d-af60-090c6534852b" />
