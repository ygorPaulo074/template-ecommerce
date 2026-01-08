# Template Ecommerce

Projeto base para um ecommerce em TypeScript.

## Visão rápida

- **Backend:** Node.js + Express + TypeScript
- **Frontend:** React (Create React App) + TypeScript
- **Banco de dados:** PostgreSQL
- **ORM:** TypeORM

## Objetivo

Fornecer um template simples e claro para iniciar um ecommerce em TypeScript, com convenções mínimas de projeto, scripts e instruções de desenvolvimento local.

## Pré-requisitos

- Node.js (>= 18)
- npm (>= 9)
- Docker (opcional, para Postgres local)

## Quickstart

### 1. Subir o Postgres via Docker Compose (na raiz)

```bash
docker-compose up -d
```

### 2. Copiar variáveis de ambiente

```bash
cp .env.example .env
```

### 3. Backend (abrir o repositório `backend` separadamente)

```bash
cd backend
npm install
npm run dev
```

### 4. Frontend (abrir o repositório `frontend` separadamente)

```bash
cd frontend
npm install
npm start
```

## Arquitetura e organização

- **Repositórios separados (recomendado):** `backend` / `frontend` / `db-migrations` (opcional).
- **Backend:** Organizado por features (ex.: `features/products`, `features/cart`) com camadas mínimas: routes → services → repositories.
- **Frontend:** Organização por features e componentes reutilizáveis em `shared`.

## Variáveis de ambiente (principais)

Consulte `.env.example` para uma lista completa.

- `PORT` — porta do backend (ex: 3000)
- `POSTGRES_HOST`, `POSTGRES_PORT`, `POSTGRES_DB`, `POSTGRES_USER`, `POSTGRES_PASSWORD`
- `JWT_SECRET` — segredo para tokens

## Scripts recomendados

### Backend

- `dev` — rodar em modo desenvolvimento
- `debug` — rodar com debug ativo
- `build` — compilar TypeScript para produção
- `start` — iniciar versão compilada
- `migrate` — aplicar migrations do banco de dados
- `seed` — popular dados iniciais
- `lint` — verificar qualidade do código
- `test` — rodar testes

### Frontend

- `start` — dev server
- `build` — build para produção
- `test` — testes de componentes
- `lint` — verificar qualidade do código

## Banco de dados

- Usar **TypeORM** para migrations e gerenciamento do schema
- Migrations e seeds devem ficar em um repositório ou pasta dedicada e versionadas

## Contribuição

- Abra **issues** para bugs/feature requests
- Envie **PRs** seguindo a convenção de commits

## Licença

MIT — ver `LICENSE`.

## Contato

Mantenha o `author`/`contato` no `package.json` de cada repositório.
