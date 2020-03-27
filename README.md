# Gantree-Backend-Docker #

This docker container is designed to simplify the setup and usage of the gantree backend

## Setup

### Install Docker

For information on setting up docker see [docs.docker.com/install](https://docs.docker.com/install)

### Configure Env

Edit the file `./env/backend.sample` and rename to `./env/backend`

Edit the file `./env/frontend.sample` and rename to `./env/frontend`

### Set USER_ID environment variable

```bash
export USER_ID=$(id -u)
```

### Build With Docker-Compose

```bash
docker-compose build
```

### Run With Docker-Compose

```bash
docker-compose up
```

### Access Gantree Frontend

The app is now available at http://localhost:5000

### Access Files

Application files will appear in `./files`

