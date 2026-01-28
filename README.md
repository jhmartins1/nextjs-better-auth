# NextJS Better Auth

Um projeto Next.js com autenticação robusta utilizando Better Auth, integrado com provedores OAuth (GitHub e Google).

## 🚀 Tecnologias Utilizadas

- **[Next.js](https://nextjs.org/)** - Framework React com renderização no servidor
- **[TypeScript](https://www.typescriptlang.org/)** - Linguagem tipada para JavaScript
- **[Better Auth](https://better-auth.com/)** - Solução de autenticação moderna e segura
- **[Prisma](https://www.prisma.io/)** - ORM para gerenciamento de banco de dados
- **[OAuth 2.0](https://oauth.net/2/)** - Integração com GitHub e Google
- **[Tailwind CSS](https://tailwindcss.com/)** - Framework CSS utilitário
- **[ESLint](https://eslint.org/)** - Linter para qualidade de código
- **[PostCSS](https://postcss.org/)** - Ferramenta para transformar CSS

## 📋 Pré-requisitos

- Node.js 18+ instalado
- npm ou yarn
- Conta GitHub (para criar OAuth App)
- Conta Google (para criar OAuth App)
- Banco de dados (PostgreSQL, MySQL, SQLite, etc.)

## 🔧 Instalação

### 1. Clonar o repositório

```bash
git clone <seu-repositorio>
cd nextjs-better-auth
```

### 2. Instalar dependências

```bash
npm install
# ou
bun install
```

### 3. Configurar variáveis de ambiente

Crie um arquivo `.env` na raiz do projeto com o seguinte conteúdo:

```env
# Better Auth
BETTER_AUTH_SECRET=sua_chave_secreta_gerada
BETTER_AUTH_URL=http://localhost:3000

# GitHub OAuth
GITHUB_CLIENT_ID=seu_github_client_id
GITHUB_CLIENT_SECRET=seu_github_client_secret

# Google OAuth
GOOGLE_CLIENT_ID=seu_google_client_id
GOOGLE_CLIENT_SECRET=seu_google_client_secret

# Database
DATABASE_URL=sua_url_do_banco_de_dados
```

### 4. Executar o projeto

```bash
npm run dev
# ou
bun dev
```

Acesse `http://localhost:3000` no seu navegador.

## 🔑 Configuração do Banco de Dados

1. Crie um banco de dados vazio no seu provedor de banco de dados favorito.
2. Atualize a variável `DATABASE_URL` no arquivo `.env` com a URL de conexão do seu banco de dados.
3. Execute as migrações do Prisma:

```bash
# Executar migrações Prisma
npx prisma migrate dev
# ou
npx prisma db push
npx prisma generate
```

## 🛠️ Scripts Disponíveis

- `dev`: Inicia o servidor em modo de desenvolvimento
- `build`: Cria uma versão otimizada para produção
- `start`: Inicia o servidor em modo de produção

## 📚 Documentação

- [Documentação do Next.js](https://nextjs.org/docs)
- [Documentação do TypeScript](https://www.typescriptlang.org/docs/)
- [Documentação do Better Auth](https://better-auth.com/docs)
- [Documentação do Prisma](https://www.prisma.io/docs/)
- [Documentação do Tailwind CSS](https://tailwindcss.com/docs)
- [Documentação do PostCSS](https://postcss.org/docs)

Estrutura do Projeto:

```
├── app/                    # Rotas e páginas Next.js
│   ├── api/               # Rotas de API
│   ├── auth/              # Páginas de autenticação
│   ├── components/        # Componentes reutilizáveis
│   ├── dashboard/         # Páginas do dashboard
│   ├── layout.tsx         # Layout principal
│   ├── page.tsx           # Página inicial
│   └── globals.css        # Estilos globais
├── lib/                   # Utilitários e helpers
│   ├── actions/           # Server actions
│   ├── auth.ts            # Configuração de autenticação
│   └── generated/         # Código gerado (Prisma)
├── prisma/                # Configuração do banco de dados
├── public/                # Arquivos estáticos
├── .env.local             # Variáveis de ambiente (não commitar)
├── next.config.ts         # Configuração Next.js
├── tsconfig.json          # Configuração TypeScript
└── package.json           # Dependências do projeto
```