# Retail Data Pipeline ETL (Airflow & Docker)


## 🏗️ Project Architecture
Here is the high-level architecture of the pipeline, from data extraction to the final Star Schema in PostgreSQL.

![Project Architecture](./airflow_project_architecture.png.png)

## 📌 Project Overview
This project demonstrates an end-to-end Data Engineering...
## 📌 Project Overview
This project demonstrates an end-to-end **Data Engineering Pipeline** that extracts retail sales data from an API and a CSV source, transforms it using Python, and loads it into a **PostgreSQL Data Warehouse** utilizing a Star Schema design. The entire environment is containerized using **Docker** and orchestrated by **Apache Airflow**.

## 🏗️ Architecture
- **Orchestration:** Apache Airflow (Astro CLI).
- **Extraction:** Python scripts for API and local CSV parsing.
- **Transformation:** Data cleaning and schema mapping.
- **Storage:** PostgreSQL (Running in Docker).
- **Environment:** Docker & Docker-Compose.

## 📁 Project Structure
- `dags/`: Contains the main Airflow DAG (`retail_etl_dag.py`).
- `include/`: Includes core logic for Extract, Transform, Load (ETL).
  - `data/`: Raw data source (`retail_sales.csv`).
  - `extract.py`, `transform.py`, `load_postgres.py`: Modular ETL scripts.
- `Dockerfile` & `docker-compose.yaml`: Containerization settings.


## 📸 Project Showcase

### 1️⃣ Airflow Orchestration
This is the main dashboard showing our DAGs and the successful execution of the ETL pipeline.
![Airflow UI](./airflow_ui.png)
![DAG Run Status](./run_dag.png)

### 2️⃣ Pipeline Logic & Code
A glimpse into the Python logic behind the data extraction and transformation.
![DAG Code](./dag_code.png)
![Pipeline Structure](./sales_pipeline.png)

### 3️⃣ Infrastructure (Docker)
The entire system is containerized, ensuring a consistent environment for the database and Airflow workers.
![Docker Containers](./docker_containers.png)

### 4️⃣ Data Warehouse (PostgreSQL)
After the ETL process, data is structured into a Star Schema. Here are the Dimension and Fact tables.
![Dimension Products](./dim_products.png)
![Fact Sales](./fact_sales.png)

### 5️⃣ Project Organization
A clean and modular folder structure for easy maintenance.
![Folder Structure](./folder_project.png)



## 🚀 How to Run
1. **Clone the repository:**
   ```bash
   git clone <my-repo-link>

2.  Start the environment:

Make sure Docker is running, then use:

astro dev start

Or if using standard Docker Compose:
docker-compose up -d


3. Access Airflow:
Open http://localhost:8080 and trigger the retail_etl_postgre DAG.

📊 Database Schema (Star Schema)
The data is loaded into a PostgreSQL database named retail_etl_postgre.

Fact Tables: Detailed sales transactions.

Dimension Tables: Product and Store information for optimized analytical querying.


## 📸 Screenshots

airflow_ui.png

dag.png

dag_code.png

dag_review.png

dim_products.png

docker_containers.png

fact_sales.png

folder_project.png

run_dag.png

sales_pipeline.png

trigger.png


Developed by: Mohamed Shahat