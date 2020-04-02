# Gantree-Backend-Docker (+ Web Application) #

This docker container is designed to simplify the setup and usage of the Gantree Web Application

## Setup

### Install Docker

For information on setting up docker see [docs.docker.com/install](https://docs.docker.com/install)

### Required Accounts

- Firebase (via [Firebase Console](https://console.firebase.google.com/), not via Google Cloud Platform)
- Email server ([ethereal.email](https://ethereal.email/) is good for testing)

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

We provide the `USER_ID` here to setup permissions on any mapped folders

```bash
USER_ID=$(id -u) docker-compose up
```

### Access Gantree Frontend

The app is now available at http://localhost:5000

### Access Files

Application files will appear in `./files`
