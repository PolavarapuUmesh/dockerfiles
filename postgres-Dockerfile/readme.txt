//Run postgresql database on docker-compose.yaml file for connecting to database//
docker-compose up -d
docker run exec -it DB_postgres psql -U user_got_mad -d postgresdb
Now , you can use the following commands to create a table, insert data, and query the data in the PostgreSQL database.
Devops Engineer can do what type of action can perform by connecting to postgresql  database using docker-compose?
Ans: Devops Engineer can perform the following actions by connecting to postgresql database using docker-compose:
1. Create a table: The devops engineer can create a table in the postgresql database using
docker-compose exec -it DB_postgres psql -U user_got_mad -d postgres
2. Insert data: The devops engineer can insert data into the table using the following command:
How can we connect database to  the application using docker-compose?
Ans: We can connect the database to the application using docker-compose by following these steps:
1. Create a docker-compose file that defines the services for the application and the database.
2. Use the docker-compose up command to start the services.
3. Use the docker-compose exec command to connect to the database from the application.
4. Use the docker-compose run command to run the application and connect to the database.
5. Use the docker-compose logs command to view the logs of the application and the database.
6. Use the docker-compose down command to stop and remove the containers.
7. Use the docker-compose up -d command to start the services in detached mode.
8. Use the docker-compose exec -it command to connect to the database from the application in interactive
9. Use the docker-compose run -it command to run the application and connect to the database in
10. Use the docker-compose logs -f command to view the logs of the application and the database
in real-time.


What is the use of docker-compose exec command?
Ans: The docker-compose exec command is used to execute a command inside a running container. It allows
you to run a command on a container that is already running, without having to start a new container
or attach to the container.
The general syntax of the docker-compose exec command is:
docker-compose exec <service_name> <command>
Where <service_name> is the name of the service that you want to execute the command on,
and <command> is the command that you want to execute.
For example, if you have a service named "web" and you want to execute the command "
psql -U user_got_mad -d postgresdb" inside the container, you can
use the following command:
docker-compose exec web psql -U user_got_mad -d postgresdb
This will execute the command "psql -U user_got_mad -d postgresdb"
inside the container named "web".

What is the use of docker-compose run command?
