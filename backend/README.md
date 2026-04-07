# Heather Design — Backend

API REST desenvolvida para a plataforma de portfólio da **Heather Designer**, criada em equipe com o objetivo de aprender e simular conceitos reais de desenvolvimento web. Responsável por autenticação, gerenciamento de projetos, serviços, mensagens de contato e upload de imagens.

> Projeto hospedado na nuvem **Azure** com acesso público via IP.

> Projeto funcional localmente

---

## Contexto

A designer precisava de uma plataforma própria para exibir seus trabalhos e gerenciar conteúdo de forma independente. A solução foi um sistema completo com landing page pública e painel admin protegido por login, com arquitetura cliente-servidor usando **React** no front, **Node.js** no back e **MySQL** para os dados.

---

## Tecnologias

- [Node.js](https://nodejs.org/) + [Express](https://expressjs.com/)
- [MySQL](https://www.mysql.com/) com [mysql2](https://github.com/sidorares/node-mysql2)
- [JWT (jsonwebtoken)](https://github.com/auth0/node-jsonwebtoken) — autenticação
- [Multer](https://github.com/expressjs/multer) — upload de imagens
- [dotenv](https://github.com/motdotla/dotenv) — variáveis de ambiente
- [CORS](https://github.com/expressjs/cors)
- Deploy na **Azure**

---

## Estrutura do Projeto

```
src/
├── controller/
│   ├── loginController.js         # Rota de autenticação
│   ├── portfolioController.js     # CRUD de projetos + upload de imagem
│   ├── servicoController.js       # CRUD de serviços + faturamento
│   └── mensagemController.js      # CRUD de mensagens de contato
├── service/
│   ├── login/                     # Lógica de autenticação
│   ├── portfolio/                 # Regras de negócio do portfólio
│   ├── servico/                   # Regras de negócio dos serviços
│   └── mensagem/                  # Regras de negócio das mensagens
├── repository/
│   ├── connection.js              # Conexão com o MySQL
│   ├── loginRepository.js
│   ├── portfolioRepository.js
│   ├── servicoRepository.js
│   └── mensagemRepository.js
├── middlewares/
│   └── uploadImages.js            # Configuração do Multer
├── utils/
│   └── jwt.js                     # Geração e validação de token JWT
├── storage/
│   └── capaPorfolio/              # Imagens salvas no servidor
└── rotas.js                       # Registro de todas as rotas
```

---

## Autenticação

As rotas protegidas exigem o token JWT no header da requisição:

```
x-access-token: <seu_token>
```

O token é gerado no endpoint `/login` e deve ser armazenado pelo cliente.

---

## Variáveis de Ambiente

Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:

```env
PORT=3010

MYSQL_HOST=
MYSQL_USER=
MYSQL_PWD=
MYSQL_DB=
```

---

## Como executar localmente

```bash
# Instalar dependências
npm install

# Iniciar o servidor
npm start
```

> A API estará disponível em `http://localhost:3010`

---

## Equipe

Projeto desenvolvido em equipe como simulação de um ambiente real de desenvolvimento.

