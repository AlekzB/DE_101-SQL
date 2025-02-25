# Data Engineering 101 - SQL

This repository will be hosting the current directories of the databases containers.

## Docker
Docker provides virtual infrastructure to deploy any type of services.

The Docker part use two files:
1. .env.dev: This file is used to contain the environment variables (In this case for the development enviroment)
2. docker-compose.yml: This file contain the docker services description in order to build the containers.

### Docker commands
```bash
# Start (and create if it is neccesary) the services described in the yaml file
docker-compose up
# OPTIONS:
# --env-file Take an environment file to use the variables as an input for docker-compose.yml
# -d Detach mode: Start services in the foreground.

# Execute commands to run inside the container
docker exec
# OPTIONS:
# -i Interactive mode: Keep STDIN open even if not attached
# -t Allocate a pseudo-TTY: is essentially a text input output environment aka shell.
# container-name: Specify the container name or ID
# command-to-execute: The most common command is /bin/bash, maybe you must use /bin/sh instead (You can use psql or mysql commands here)

# Show the current running docker services
docker ps
# Recommendation:
# Run with | grep your_container_name in order to watch only your desired containers

# Stop a container
docker stop container_name

# Delete a container
docker rm container_name

# Delete an image
docker rmi image_name

# Stops all the services of the docker-compose file
docker-compose stop

```
