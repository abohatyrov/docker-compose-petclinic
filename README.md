# docker-compose-petclinic

1. Clone the repository of petclinic app
```
git clone https://github.com/spring-projects/spring-petclinic.git
cd spring-petclinic
```

2. Clone this `docker-compose.yaml` in the root directory. 
Docker Compose file defines two services, db and app. The db service uses the mysql:5.7 image and creates a named volume for the MySQL data at db_data. It sets environment variables for the root password, database name, username, and password. The app service builds an image from the current directory (.) and exposes port 8080. It mounts the current directory as a volume at /app in the container and depends on the db service. It sets environment variables for the database URL, username, and password.

3. Build the Docker images and start the containers:
```
docker-compose up -d --build
```

Now you can access the application at http://localhost:8080
