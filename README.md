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
git clone git@github.com:alittlebroken/localdev_node.git
```

- Update project folder name
```cmd
ren localdev_node <project_name>
cd <project_name>
```

- Update the remote git repo to your new repo location
```cmd
git remote set-url origin <new remote repo>
```

- Edit the docker-compose.yaml file and set the service names to your desired names
- Add any environment vars or other options like mounted volumes that you require

- Build and start the docker image(s)
#### Default
```cmd
docker-compose -f docker-compose.yaml up --build -d
```

#### API + DB
```cmd
docker-compose -f api-docker-compose.yaml up --build -d
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
