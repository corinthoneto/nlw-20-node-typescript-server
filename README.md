# NLW Agents

Projeto desenvolvido durante o evento **NLW (Next Level Week)** da Rocketseat, focado em criar uma aplicação de agentes inteligentes.

## 🚀 Tecnologias

- **Runtime**: Node.js com TypeScript
- **Framework**: Fastify
- **Database**: PostgreSQL com pgvector
- **ORM**: Drizzle ORM
- **Validação**: Zod
- **Linter**: Biome
- **Containerização**: Docker & Docker Compose

## 📋 Pré-requisitos

- Node.js 18+
- Docker e Docker Compose
- Git

## ⚙️ Configuração

### 1. Clone o repositório
```bash
git clone <repository-url>
cd server
```

### 2. Instale as dependências
```bash
npm install
```

### 3. Configure as variáveis de ambiente
Crie um arquivo `.env` na raiz do projeto:
```env
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
PORT=3333
```

### 4. Inicie o banco de dados
```bash
docker-compose up -d
```

### 5. Execute as migrações e seed
```bash
npm run db:seed
```

## 🏃‍♂️ Executando o projeto

### Desenvolvimento
```bash
npm run dev
```

### Produção
```bash
npm start
```

O servidor estará disponível em `http://localhost:3333`

## 📁 Estrutura do Projeto

```
src/
├── db/
│   ├── connection.ts
│   ├── migrations/
│   ├── schema/
│   └── seed.ts
├── http/
│   └── routes/
├── env.ts
└── server.ts
```

## 🔧 Scripts Disponíveis

- `npm run dev` - Executa o servidor em modo desenvolvimento com hot reload
- `npm start` - Executa o servidor em modo produção
- `npm run db:seed` - Executa o seed do banco de dados

## 📊 Banco de Dados

O projeto utiliza PostgreSQL com pgvector para suporte a operações vetoriais. A estrutura atual inclui:

- **Tabela `rooms`**: Armazena informações sobre salas/ambientes

## 🛠️ Padrões de Projeto

- **Clean Architecture**: Separação clara entre camadas
- **Type Safety**: TypeScript + Zod para validação
- **Database First**: Migrações gerenciadas pelo Drizzle
- **Environment Variables**: Validação de variáveis com Zod
- **CORS**: Configurado para desenvolvimento local 