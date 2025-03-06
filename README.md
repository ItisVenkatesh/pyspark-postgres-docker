# pyspark-postgres-docker
This repository provides a complete setup for running PostgreSQL in a Docker container using docker-compose and accessing its tables using PySpark via JDBC. It includes a docker-compose.yml file to spin up a PostgreSQL database and a PySpark script to connect, read, and process data from the database.

## 📌 Features:
	•	PostgreSQL setup using Docker and docker-compose
	•	JDBC connection for PySpark
	•	Example table creation and data retrieval using PySpark
	•	Steps to install dependencies and configure the setup

## 🛠️ Tech Stack
- **ETL Tools**: PySpark
- **Database**: Postgres
- **Language**: Python
- **Container**: Docker

## Prerequisites
- **Docker & Docker Compose** installed on your machine
- **Jupyter Notebook** or any notebook supported IDE
- **Pyspark**

## 🚀 Running the Project
1. Clone the repository:
    ``` bash
    git clone https://github.com/ItisVenkatesh/pyspark-postgres-docker.git
    cd pyspark-postgres-docker

2. Make sure that the Docker is running in your system.

3. Run docker-compose to start the postgres db container:

    ``` bash
    docket-compose up -d

4. Explore the notebook:
    Open pyspark-postgres-docker.ipynb and try running the cells.

5. Run docker-compose to stop the containers:
   - Once done, to stop the containers,
   ``` bash
   docker-compose down 

## License

This project is licensed under the MIT License - see the LICENSE file for details.