# Cyber-Siege Project

This project uses **Docker** to manage a PostgreSQL database and a Redis cache. Below are instructions to set up the environment and run the project.

## Prerequisites

- **Docker** and **Docker Compose** installed on your machine.
- Create a `.env` file to store sensitive environment variables.

## Environment Variables

Before running the project, create a `.env` file in the root directory of the project with the following content:

```bash
# PostgreSQL credentials
POSTGRES_USER=user
POSTGRES_PASSWORD=12345678
POSTGRES_DB=cyber-siege

# Redis credentials
REDIS_PASSWORD=redispass123
```

## How to Run the Project
1. Clone the repository and navigate to the project directory
```bash
git clone <repository-url>
cd <repository-folder>
```
2. Create the .env file with the necessary environment variables (see above)
3. Start the services using Docker Compose
```bash
docker-compose up -d
```
4. Check the running containers
```bash
docker ps
```
# PostgreSQL
You can connect to the PostgreSQL database using the following command
```bash
docker exec -it postgres_db psql -U user -d cyber-siege
```
# Redis
To interact with Redis and test authentication:
1. Connect to the Redis CLI
```bash
docker exec -it redis_cache redis-cli
```
2. Try the PING command (without authentication, it should fail)
```bash
ping
```
You should receive an error: NOAUTH Authentication required.
3. Authenticate using the password from the .env file
```bash
auth <Redis_password>
```
4. After successful authentication, test with PING again:
```bash
ping
```
You should receive: PONG.

