# Gantree-Backend-Docker #

This docker container is designed to simplify the setup and usage of the gantree backend

## Setup

### Install Docker

For information on setting up docker see [docs.docker.com/install](https://docs.docker.com/install)

### Accounts

- Firebase (not via Google Cloud Platform)
- Email server

See the env files below for the required configurations and where to put them

### Configure Env

Edit the file `./env/backend.sample` and rename to `./env/backend`

Edit the file `./env/frontend.sample` and rename to `./env/frontend`

This is used for file permissions on any mapped directories

### Build With Docker-Compose

```bash
docker-compose build
```

Note: If you change the env files you'll need to rerun this step

### Run With Docker-Compose

We provider the USER_ID here to setup permissions on any mapped folders

```bash
USER_ID=$(id -u) docker-compose up
```

### Access Gantree Frontend

The app is now available at http://localhost:5000

### Access Files

Application files will appear in `./files`
