# airflow_etl_1

## 📌 Descrição | Description

### 🇧🇷 Português
Este projeto demonstra a utilização do **Apache Airflow** para orquestrar uma **pipeline de dados ETL (Extract, Transform, Load)**.  
A pipeline realiza a extração de dados a partir de um arquivo **CSV**, transforma os dados de forma simples e carrega as informações em um banco de dados **SQLite**.

O objetivo principal do projeto é **demonstrar conceitos fundamentais do Airflow**, como:
- Criação de DAGs
- Dependência entre tarefas
- Uso de **XCom** para comunicação entre tasks
- Orquestração de pipelines utilizando **Docker**

> ⚠️ O uso do SQLite é **apenas didático**. A mesma pipeline pode ser facilmente adaptada para outros bancos de dados (PostgreSQL, MySQL, etc).

---

### 🇺🇸 English
This project demonstrates the use of **Apache Airflow** to orchestrate an **ETL (Extract, Transform, Load) data pipeline**.  
The pipeline extracts data from a **CSV file**, applies simple transformations, and loads the data into a **SQLite database**.

The main goal of this project is to demonstrate **core Airflow concepts**, such as:
- DAG creation
- Task dependencies
- **XCom** usage for task communication
- Pipeline orchestration using **Docker**

> ⚠️ SQLite is used **for educational purposes only**. This pipeline can be easily adapted to other databases such as PostgreSQL or MySQL.

---

## 🎥 Demonstração | Demo

[![Demonstração do projeto](https://img.youtube.com/vi/nUfdyS666hc/0.jpg)](https://www.youtube.com/watch?v=nUfdyS666hc)

▶ Clique na imagem para assistir à execução completa do pipeline no Airflow.  
▶ Click the image to watch the full pipeline execution.

---

## 🏗️ Arquitetura da Pipeline | Pipeline Architecture

### ETL Flow
Start
  ↓
Setup Database
  ↓
Extract (CSV)
  ↓
Transform (Python)
  ↓
Load (SQLite)
  ↓
End

## Estrutura da DAG | DAG Structure
A DAG users_etl_pipeline é composta pelas seguintes tasks:

# start
Task inicial (EmptyOperator)
# setup_database
Cria a tabela users no banco SQLite (caso não exista) e limpa os dados antes da carga
# extract
Lê os dados do arquivo users.csv
# transform
Aplica transformações simples (neste projeto, apenas repassa os dados)
# load
Insere os registros no banco de dados SQLite
# end
Task final (EmptyOperator)

## 🧰 Tecnologias Utilizadas | Technologies Used

- Apache Airflow
- Python
- Docker & Docker Compose
- SQLite
- Pandas

## 🎯 Objetivo do Projeto | Project Goal

- Demonstrar o uso do Apache Airflow para orquestração de pipelines
- Aplicar conceitos de ETL na prática
- Criar um projeto simples, didático e replicável
- Servir como projeto de portfólio para estudos em engenharia de dados
