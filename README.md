# data-pipeline-etl-dwh-sales

Presque parfait ! Le rendu est très propre dans l'ensemble, mais il y a deux petits bugs de formatage à corriger dans votre `README.md` :

1. **Au niveau du Titre / Description (en haut) :** Le titre `# 🚀 End-to-End...` et `## 🏗️ Architecture du Projet` apparaissent en texte brut avec leurs hashtags `##`. Cela veut dire qu'il manque un saut de ligne ou qu'un bloc de code n'a pas été bien fermé juste au-dessus.
2. **Dans la section Git clone (en bas) :** La ligne `git clone [https://...](https://...)` contient un format de lien Markdown à l'intérieur d'un bloc de code shell. Dans du code, il faut simplement mettre l'URL brute.

---

### Le fichier `README.md` corrigé à copier-coller

Remplacez tout le contenu de votre fichier `README.md` local par ce texte exact :

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

---

### Pour appliquer la mise à jour :

Dans votre terminal VS Code :

```bash
git add README.md
git commit -m "fix: syntax formatting in README markdown"
git push origin main

```

Une fois poussé, actualisez votre page GitHub : le titre s'affichera correctement en grand et les blocs de code seront parfaitement lisibles !
