# Run Langflow


## Docker compose
To run Langflow with Docker compose, you need to have Docker and Docker compose installed on your machine. You can install Docker and Docker compose by following the instructions on the [official Docker documentation](https://docs.docker.com/get-docker/).

The docker-compose file uses `latest` tag; it's recommended to pull the latest version of the images before running the docker-compose file.

To start the Langflow services using Dokploy, run the following command:

```bash
compose -p <entity id> -f ./docker-compose.override.yml -f ./docker-compose.yml up -d --build --remove-orphans
```

To start the Langflow services in raw mode only, run the following command:

```bash
docker compose -f ./docker-compose.override.yml -f ./docker-compose.yml up -d --build --remove-orphans
```

After running the command, you can access the Langflow services at the following url: http://localhost:80.

Edit the `.env` file to change the port or other configurations.