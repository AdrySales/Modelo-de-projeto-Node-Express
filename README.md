# 🧱 Node Starter Base Project

Este repositório contém um projeto inicial em **Node.js** com uma estrutura robusta pronta para ser reutilizada em novos projetos. Ele já vem com:

### ✅ O que está incluído?

- **Autenticação com JWT**
- **Criptografia de senhas com bcrypt**
- **Conexão com Cloudinary** para upload de arquivos no CRUD de usuários como imagem de perfil
- **Migrations de usuários** com `knex`
- **Controllers com estrutura middleware separados para:**
  - Autenticação (`authController`)
  - Usuários (`userController`)
- **Sistema de rotas completo feito com express**
- **Testes unitários com Jest** para autenticação e usuários
- **Dockerfile e docker-compose configurados**
- **Estrutura organizada em MVC**

---

## 🚀 Como iniciar um novo projeto com essa base

1. **Clone este repositório:**

```bash
git clone https://github.com/seu-usuario/seu-repo-node-starter.git novo-projeto
cd novo-projeto
```

2. **Instale as dependências:**

```bash
npm install
```

3. **Configure seu banco de dados e Cloudinary:**

Crie um `.env` com base no `.env.example`:

```env
ENV=develop

PORT=8000

DB_PORT=5432
DB_HOST=db
DB_USER=postgres
DB_PASS=postgres
DB_NAME=meu_banco

FRONTEND_URL=http://localhost:8000
SENDINBLUE_API_KEY=SUA_API_KEY_DO_SENDINBLUE

JWT_SECRET=minha_chave_super_secreta
JWT_EXPIRES_IN=1d

CLOUDINARY_CLOUD_NAME=minhaContaCloudinary
CLOUDINARY_API_KEY=123456789
CLOUDINARY_API_SECRET=secreta123

```

4. **Suba o ambiente com Docker:**

```bash
docker-compose up --build
```

5. **Execute as migrations:**

```bash
npm run migrate
```

6. **Rode os testes:**

```bash
npm test
```

---

## 📁 Estrutura de pastas

```
├── src
├── tests
│   ├── authController.test.js
│   └── userController.test.js
│   ├── constants
│   │   ├── string.js
│   ├── controllers
│   │   ├── authController.js
│   │   └── userController.js
│   ├── database
│   │   ├── create-users.cjs
│   ├── helpers
│   ├── models
│   │   └── auth.js
│   │   └── users.js
│   ├── routes
│   │   └── index.js
│   │   └── auth.js
│   │   └── user.js
│   ├── utils
│   └── ...
├── docker-compose.yml
├── Dockerfile
├── .env.example
└── ...
```

---

## 💡 Sugestão de uso

Esse projeto foi feito pra ser clonado e adaptado rapidamente. Basta conectar com seu banco e sua conta do Cloudinary para ter um backend funcional desde o início.

