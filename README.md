# pyspark-postgres-docker
This repository provides a complete setup for running PostgreSQL in a Docker container using docker-compose and accessing its tables using PySpark via JDBC. It includes a docker-compose.yml file to spin up a PostgreSQL database with PGAdmin and a PySpark script to connect, read, and process data from the database.

## 📌 Features:
	•	PostgreSQL with PGAdmin setup using Docker and docker-compose
	•	JDBC connection for PySpark
	•	Example table creation and data retrieval using PySpark
	•	Steps to install and configure the setup

## 🛠️ Tech Stack
- **ETL Tools**: PySpark
- **Database**: Postgres with PGAdmin
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
    docker-compose up -d

4. Open PGAdmin:

    Open the link [http://localhost:8080/] (http://localhost:8080/) in any web browser.
    Login using the username and password mentioned in docker-compose.yml file.

5. Configure server:

    - Right click on servers and click "Register".
    - Choose "Server...".
    - Give name as "test_server".
    - Go to "Connection" tab.
        - Mention Host Name/address as db
        - Mention the user name and passwords as in docker-compose.yml
        - [Optional] Enable "Save password?"
    - Click "Save" at the bottom.

6. Configure data for notebook testing:
    - Expand test_user database.
    - Expand Schemas and then public.
    - Use the button Query Tool on top.
    - Execute below queries.

    ```sql
    CREATE TABLE employees (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    age INT
    );

    INSERT INTO employees (name, age) VALUES
    ('Name_A', 30),
    ('Name_B', 25),
    ('Name_C', 35);


7. Explore the notebook:
    ``` bash
    cd notebooks
    
    - Open pyspark-postgres-docker.ipynb with any IDE.
    - In the spark config for postgres jar, replace the value "path/to/notebooks/jars/postgresql-42.7.5.jar" according to your file location. The jar file is provided as part of this Repo.
    - Try changing and running the cells.

8. Run docker-compose to stop the containers:
   - Once done, to stop the containers.

   ``` bash
   docker-compose down 

## License

This project is licensed under the MIT License - see the LICENSE file for details.