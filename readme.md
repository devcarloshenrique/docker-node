## Como Usar Docker com Node.js

### Sem Utilizar Docker Compose e Nodemon

#### 1. Gerando a Imagem
`docker build -t devcarlos/docker-node .`

#### 2. Executando o Contêiner

**Simplesmente Executar:**
`docker run -p 3000:3000 -d devcarlos/docker-node`

**Executar com Nome Específico:**
`docker run --name node-app -p 3000:3000 -d devcarlos/docker-node`

### Utilizando Docker Compose e Nodemon

#### 1. Subir os Serviços com Docker Compose
`docker-compose up`

### Utilizando Docker Compose e TypeScript

#### 1. Adicionar Script no `package.json`

```
    "scripts": {
    "start": "ts-node-dev --respawn --poll server.ts"
    }
```

### Iniciar o Contêiner Parado e Anexar para Ver os Logs
`docker start -a <nome_ou_id_do_container>`