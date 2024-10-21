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
