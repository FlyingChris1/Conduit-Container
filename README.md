# Conduit-Container

This repository contains a fully containerized deployment of the Conduit Application.The goal of this setup is to provide a reproducible, secure, and production‑ready environment according to modern DevOps and containerization standards.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Quickstart](#Quickstart)
- [Usage](#Usage)

## Prerequisites

- Docker engine
- Docker compose

## Quickstart

- Clone the repository

```bash
git clone https://github.com/FlyingChris1/Conduit-Container.git
cd Conduit-Container
```
- Create Docker Image

```bash
cd conduit-frontend
docker build -t frontend .
```

```bash
cd conduit-backend
docker build -t backend .
```

- Convert example.env into .env

```bash
cp example.env .env
```


- Start Docker compose 

```bash
docker compose up -d
```

- check if your application is up and running

```bash
<your_server_ip>:8282
```

## Usage

- restart Container

```bash
docker compose restart
```

- stop Container

```bash
docker compose down -v
```

- Enter Conduit-Backend Container

```bash
docker compose exec -it backend bash
```

- Get Docker Compose logs

```bash
docker compose logs
```