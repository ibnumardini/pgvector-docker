# pgvector Project

This project sets up a PostgreSQL database with the pgvector extension using Docker.

## Prerequisites

- Docker
- Docker Compose

## Getting Started

1. Clone the repository:

    ```sh
    git clone https://github.com/ibnumardini/pgvector-docker.git pgvector-docker
    cd pgvector-docker
    ```

2. Create a `.env` file in the project root directory and add the necessary environment variables:

    ```sh
    POSTGRES_USER=your_username
    POSTGRES_PASSWORD=your_password
    ```

3. Start the services using Docker Compose:

    ```sh
    docker-compose up -d
    ```

4. Access the PostgreSQL database:
    - Host: `localhost`
    - Port: `5432`
    - Username: `your_username`
    - Password: `your_password`

## Network Configuration

The Docker Compose configuration sets up a custom network with the following details:

- Subnet: `172.17.0.0/24`
- pgvector container IP: `172.17.0.3`

## Volumes

The PostgreSQL data is stored in a Docker volume mapped to `./pgdata` on the host machine.

## Stopping the Services

To stop the services, run:

```sh
docker-compose down
```

## Additional Information

For more information on pgvector, visit the [pgvector GitHub repository](https://github.com/pgvector/pgvector).
