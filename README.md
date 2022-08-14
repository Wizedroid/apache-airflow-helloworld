# Getting Started with Apache Airflow



## Instalation and Overview

`curl -LfO 'https://airflow.apache.org/docs/apache-airflow/2.0.2/docker-compose.yaml`

This file contains several service definitions:

`airflow-scheduler`: The scheduler monitors all tasks and DAGs, then triggers the task instances once their dependencies are complete.
`airflow-webserver` - The webserver available at http://localhost:8080.
`airflow-worker` - The worker that executes the tasks given by the scheduler.
`airflow-init` - The initialization service.
`flower` - The flower app for monitoring the environment. It is available at http://localhost:8080.
`postgres` - The database.
`redis` - The redis - broker that forwards messages from scheduler to worker.



### Initialize the database and create user account

`docker-compose up airflow-init`

### Startup

`docker-compose up`

### Cleanup

`docker-compose down --volumes --rmi all`
