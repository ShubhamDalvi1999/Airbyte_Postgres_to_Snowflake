
<h2 align="center">
  Welcome to My Docker-Hosted Postgres to Snowflake Data Transfer Project!
  <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="28">
</h2>

<!-- Intro -->
<h3 align="center">
        <samp>&gt; Hey There!, I am
                <b><a target="_blank" href="https://yourwebsite.com">Shubham Dalvi</a></b>
        </samp>
</h3>

<p align="center"> 
  <samp>
    <br>
    「 I am a data engineer with a passion for big data, distributed computing, and data visualization 」
    <br>
    <br>
  </samp>
</p>

<div align="center">
<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&random=false&width=435&lines=Spark+%7C+DataBricks++%7C+Power+BI+;Snowflake+%7C+Azure++%7C+Airflow;3+yrs+of+IT+experience+as+Analyst+%40+;Accenture+;Passionate+Data+Engineer+" alt="Typing SVG" /></a>
</div>

<p align="center">
 <a href="https://linkedin.com/in/yourprofile" target="_blank">
  <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="yourprofile"/>
 </a>
</p>
<br />

<!-- About Section -->
# About Me
 
<p>
 <img align="right" width="350" src="/assets/programmer.gif" alt="Coding gif" />
  
 ✌️ &emsp; Enjoy solving data problems <br/><br/>
 ❤️ &emsp; Passionate about big data technologies, distributed systems, and data visualizations<br/><br/>
 📧 &emsp; Reach me : dshubhamp1999@gmail.com<br/><br/>

</p>

<br/>
<br/>
<br/>

## Skills and Technologies

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Airbyte](https://img.shields.io/badge/Airbyte-000000?style=for-the-badge&logo=airbyte&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=for-the-badge&logo=snowflake&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![VSCode](https://img.shields.io/badge/Visual_Studio-0078d7?style=for-the-badge&logo=visual%20studio&logoColor=white)

<br/>

## Project Overview

This project demonstrates how to set up a PostgreSQL database hosted on Docker, create tables, and transfer data from PostgreSQL to Snowflake using Airbyte. The project includes setting up the environment, creating the database schema, and automating the data transfer process.

## Table of Contents
- [Technologies Used](#technologies-used)
- [Skills Demonstrated](#skills-demonstrated)
- [Setup PostgreSQL on Docker](#setup-postgresql-on-docker)
- [Creating the Database and Tables](#creating-the-database-and-tables)
- [Configuring Airbyte](#configuring-airbyte)
- [Data Transfer to Snowflake](#data-transfer-to-snowflake)
- [Usage Instructions](#usage-instructions)

## Technologies Used
- **PostgreSQL**: For database management.
- **Docker**: To containerize and host the PostgreSQL instance.
- **Airbyte**: To extract and load data from PostgreSQL to Snowflake.
- **Snowflake**: For data warehousing.
- **Python**: For scripting and automation.

## Skills Demonstrated
- **Data Engineering**: Setting up and managing a PostgreSQL database in Docker.
- **Docker**: Containerizing services for ease of use and portability.
- **ETL Processes**: Automating data transfer from PostgreSQL to Snowflake.
- **Airbyte Configuration**: Setting up and managing data connectors.

## Setup PostgreSQL on Docker
### Initial Setup
Start by pulling the PostgreSQL Docker image and running a container.

```bash
docker pull postgres
docker run --name my_postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
```

### Accessing the PostgreSQL Database
Connect to the PostgreSQL instance running inside the Docker container.

```bash
docker exec -it my_postgres psql -U postgres
```

## Creating the Database and Tables

### Creating a Database
Create a new database for storing your data.

```sql
CREATE DATABASE my_database;
```

### Creating Tables
Define the schema and create tables within the database.

```sql
CREATE TABLE transactions (
    transaction_id SERIAL PRIMARY KEY,
    amount DECIMAL(10, 2),
    transaction_date DATE
);
```

## Configuring Airbyte

### Setting Up Airbyte
Install and run Airbyte to handle the data transfer.

```bash
docker-compose up -d
```

### Connecting PostgreSQL and Snowflake
Create a new connection in Airbyte, specifying PostgreSQL as the source and Snowflake as the destination. Map the tables and fields as needed.

## Data Transfer to Snowflake
### Running the Sync
Trigger the data sync from PostgreSQL to Snowflake using Airbyte's interface or API.

## Usage Instructions
1. Ensure Docker and Airbyte are installed and running.
2. Set up PostgreSQL on Docker using the provided commands.
3. Create the necessary tables in PostgreSQL.
4. Configure Airbyte with the appropriate source and destination settings.
5. Trigger the data sync and verify the results in Snowflake.
