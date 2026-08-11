# data-pipeline-etl-dwh-sales

Le dépôt GitHub est propre et bien structuré.

Voici un modèle complet de **README.md** professionnel pour transformer votre projet en une vraie vitrine technique pour les recuteurs :

```markdown
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

1. **Source ERP (PostgreSQL) :** Stocke les données transactionnelles des clients et ventes (`erp_db`).
2. **Orchestration (Mage.ai) :** Pipeline ETL automatisé assurant l'extraction, la transformation des types/statuts et le chargement.
3. **Data Warehouse (PostgreSQL) :** Modélisation en étoile (`dim_clients`, `fact_ventes`) prête pour l'analyse (`dwh_db`).
4. **Business Intelligence (Power BI) :** Visualisation des KPI clés, tendances de ventes et suivi des statuts de commandes.

---

## 🛠️ Tech Stack

* **Conteneurisation :** Docker, Docker Compose
* **Base de données :** PostgreSQL (Source & DWH)
* **ETL / Orchestration :** Mage.ai (Python)
* **Business Intelligence :** Power BI Desktop

---

## 🚀 Lancement Rapide

### 1. Prérequis

* [Docker Desktop](https://www.docker.com/products/docker-desktop/) installé et démarré.
* [Git](https://git-scm.com/) pour cloner le projet.

### 2. Configuration & Démarrage

```bash
# 1. Cloner le dépôt
git clone [https://github.com/waddadelmehdi/data-pipeline-etl-dwh-sales.git](https://github.com/waddadelmehdi/data-pipeline-etl-dwh-sales.git)
cd data-pipeline-etl-dwh-sales

# 2. Configurer les variables d'environnement
cp .env.example .env

# 3. Lancer l'infrastructure avec Docker Compose
docker compose up -d

```

---

## 🌐 Ports & Services

| Service | Description | URL / Port Local |
| --- | --- | --- |
| **Mage.ai** | Interface d'orchestration | `http://localhost:6789` |
| **ERP Source** | PostgreSQL (Données brutes) | `localhost:5431` |
| **Data Warehouse** | PostgreSQL (Données modélisées) | `localhost:5433` |
| **Metabase** | Service BI alternatif | `http://localhost:3000` |

---

## 📊 Modèle de Données (Data Warehouse)

* **`dim_clients` :** Identifiants et informations démographiques des clients.
* **`fact_ventes` :** Transactions de ventes nettoyées (`montant`, `statut`, `date_vente`, clés étrangères).

```

### Pour mettre à jour votre README sur GitHub :

1. Dans VS Code, ouvrez votre fichier `README.md`.
2. Remplacez son contenu par le texte ci-dessus et enregistrez (`Ctrl + S`).
3. Exécutez les commandes suivantes dans votre terminal :

```bash
git add README.md
git commit -m "docs: enrich README with architecture, setup guide, and tech stack"
git push origin main

```
