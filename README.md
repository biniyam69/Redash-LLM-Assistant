# LLM Assistant Plugin for Redash - Visualize Data with Natural Language

---

## Set up Prerequisites

### Install Required Packages

```bash
$ sudo apt -y install docker.io docker-buildx docker-compose-v2 build-essential curl pwgen python3-venv xvfb
```

### Add User to Docker Group

```bash
$ sudo usermod -aG docker $USER
```

### Install Node Version Manager (NVM)

```bash
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```

Log out and log back in for changes to take effect.

### Install NodeJS version 16 using NVM

```bash
$ nvm install --lts 16
$ nvm alias default 16
$ nvm use 16
```

Confirm NodeJS version:

```bash
$ nvm list
```

### Install Yarn 1.x

```bash
$ npm install --global yarn@1.22.19
```

## Clone Redash Source Code and Install Dependencies

```bash
$ git clone https://github.com/birehan/Redash-NLP-Chatbot-Analytics
$ cd redash
$ yarn
```

## Generate Environment Variables

Generate the `.env` file containing required environment variables:

```bash
$ make env
```

Add your OpenAI API key to the `.env` file:

```
OPENAI_API_KEY=*****************************************
```

## Compile and Build

### Build Redash Frontend

```bash
$ make build
```

### Build Local Redash Docker Image

```bash
$ make compose_build
```

## Start Redash Locally

### Create Database

```bash
$ make create_database
```

### Start Docker Containers

```bash
$ make up
```

Access Redash web interface at http://localhost:5001.

### Screenshots

Creating a query
---
![create_query](https://github.com/biniyam69/AI-Contract-Lawyer/assets/91191700/c1b55f56-dee1-4453-87d5-85903e418e4e)
---

Visualizing
---
![creating_visualization](https://github.com/biniyam69/AI-Contract-Lawyer/assets/91191700/29662f7a-934f-48b1-b410-2509d3ddccae)
---
## Shut Down Containers

```bash
$ make down
```

---

Open for collaborations
