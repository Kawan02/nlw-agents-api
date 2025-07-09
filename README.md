# NLW Agents API

API desenvolvida durante o evento **NLW Agents** da RocketSeat, utilizando tecnologias modernas para criar uma aplicação robusta e escalável.

## 🚀 Tecnologias

- **Node.js** - Runtime JavaScript
- **TypeScript** - Linguagem de programação tipada
- **Fastify** - Framework web rápido e eficiente
- **Drizzle ORM** - ORM moderno para TypeScript
- **PostgreSQL** - Banco de dados relacional
- **pgvector** - Extensão para vetores no PostgreSQL
- **Zod** - Validação de schemas
- **Biome** - Linter e formatter

## 📋 Pré-requisitos

- Node.js 18+
- Docker e Docker Compose
- PostgreSQL (via Docker)

## ⚙️ Configuração

1. **Clone o repositório**
```bash
git clone <repository-url>
cd nlw-agents/api
```

2. **Instale as dependências**
```bash
npm install
```

3. **Configure as variáveis de ambiente**
Crie um arquivo `.env` na raiz do projeto:
```env
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5433/agents
```

4. **Inicie o banco de dados**
```bash
docker-compose up -d
```

5. **Execute as migrações**
```bash
npx drizzle-kit migrate
```

6. **Popule o banco com dados iniciais**
```bash
npm run db:seed
```

## 🏃‍♂️ Executando o projeto

**Desenvolvimento:**
```bash
npm run dev
```

**Produção:**
```bash
npm start
```

A API estará disponível em `http://localhost:3333`

## 📁 Estrutura do Projeto

```
src/
├── db/           # Configurações do banco de dados
├── http/         # Rotas e controllers
├── env.ts        # Validação de variáveis de ambiente
└── server.ts     # Servidor principal
```

## 🛠️ Scripts Disponíveis

- `npm run dev` - Executa em modo desenvolvimento com hot reload
- `npm start` - Executa em modo produção
- `npm run db:seed` - Popula o banco com dados iniciais

## 📝 Padrões de Projeto

- **Clean Architecture** - Separação clara de responsabilidades
- **Type Safety** - Uso extensivo de TypeScript e Zod
- **Database First** - Migrações e schema definidos via Drizzle
- **API RESTful** - Endpoints seguindo padrões REST
- **Environment Validation** - Validação de variáveis de ambiente com Zod

---

Desenvolvido durante o **NLW Agents** da RocketSeat 🚀 