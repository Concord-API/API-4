## Guia de Instalação - *Trivio*



### 1. Pré-requisitos

Antes de iniciar, instale:

- Git ([Download](https://git-scm.com/downloads))

- Docker ([Download](https://www.docker.com/))

- Node.js 24.15+([Download](https://nodejs.org/en/download))

- Visual Studio Code ([Download](https://code.visualstudio.com/download))

---

### 2. Clonar o Repositório Principal

No Vscode clone o repositório:

```bash
git clone --recurse-submodules https://github.com/Concord-API/API-4.git
cd API-4
```

> **Observação:** Se já tiver clonado sem os submódulos, execute:

```
git submodule update --init --recursive
```

### 3. Configuração do Backend

**1° Renomeie o arquivo `.env.example` para `.env` e configure:**

```
# Oracle
ORACLE_PASSWORD=123
APP_USER=trivio
APP_USER_PASSWORD=123

# Spring
DB_HOST=oracle
DB_PORT=1521
DB_NAME=FREEPDB1
DB_USER=trivio
DB_PASSWORD=123

# JWT Auth
JWT_SECRET=smRwGB4ybnL3iSYp6W+56stG4KS9C49+sxEXAcnoGY4=
    
```
2º Instalar a extensão "Dev Containers"

Apertar a tecla 'F1' no Vscode e digitar: 'Reopen in Container'

Após isso, digitar no terminal:

```bash
cd api4-backend 
cd trivio
./mvnw spring-boot:run
```
Saída esperada: Tomcat started on port(s): 8080 (http)
                Started Application in X seconds

### 4. Configuração do Frontend

Abrir um novo terminal e colar:

```bash
cd API4-Frontend
cd trivio
npm install
```
Após, renomear `.env.example` para `.env` e inserir o caminho da api

```bash
VITE_API_URL=http://localhost:8080
```

Voltar ao terminal e colar:
```bash
npm run dev
```

Saída esperada:

Local: http://localhost:5173