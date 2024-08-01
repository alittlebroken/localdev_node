# Node local dev container
A simple local development server utilising node

The docker images use the local folder the docker-compose command 
is used from to persist the app code you develop.

## Tech stack

### Prerequisite
- Windows 11
- Docker Desktop

### Production
- Node

### Development
- nodemon
- jest

## Installation

### NOTES
- Docker will give the parent name the same as the folder that the docker-compose comman was issued from
- The actual images will be named based on the service names you set in the docker compose yaml file

### Setup

- Clone the github repo
```cmd
git clone https://github.com/alittlebroken/localdev-node.git
```

- Update project folder name
```cmd
ren localdev-node <project_name>
cd <project_name>
```

- Update the remote git repo to your new repo location
```cmd
git remote set-url origin <new remote repo>
```

- Edit the docker-compose.yaml file and set the service names to your desired names
- Add any environment vars or other options like mounted volumes that you require

- Build and start the docker image
```cmd
docker-compose up --build -d
```

- Start containers after first build
```cmd
docker-compose up -d
```

- Attach to an running container
```cmd
docker-composeexec <service name> bash
```

- Launch vscode
```cmd
code .
```