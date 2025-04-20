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
- **Sistema de rotas completo**
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
PORT=3333
DATABASE_URL=postgresql://usuario:senha@host:porta/database
JWT_SECRET=sua_chave_secreta
CLOUDINARY_CLOUD_NAME=seu_cloud_name
CLOUDINARY_API_KEY=sua_api_key
CLOUDINARY_API_SECRET=sua_api_secret
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

