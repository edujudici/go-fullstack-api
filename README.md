# API Golang

API para gerenciamento de usuários e postagens, usando as tecnologias:

    - Go
    - GORM (A Golang ORM)
    - JWT
    - Mysql or Postgres
    - Gorilla Mux (For HTTP routing and URL matcher)
    - Docker
    - Docker Compose
    - Kubernetes

## Executando api

### Pré requisitos

- Docker
- kubectl
- Kind

### Deploy usando kind para executar arquivos do kubernetes:

- Criação de um novo cluster através do Kind
    ```
    kind create cluster
    ```

- Realizando o deploy conforme configuração do YAML
    ```
    kubectl apply -f k8s -R
    ```

- Compartilhando o serviço para ser possível acessar via postman
    ```
    kubectl port-forward svc/fullstack-app-mysql 8080:8080
    ```

### Deploy usando docker e docker compose

- Build e start dos containeres
    ```
    docker compose up -d --build
    ```