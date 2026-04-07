# Heather Design — Plataforma Completa

Plataforma de portfólio para designers com landing page pública
e painel administrativo protegido. Arquitetura fullstack com
React, Node.js e MySQL, hospedada na Azure.

---

## Contexto

A designer precisava de uma plataforma própria para exibir seus
trabalhos e gerenciar conteúdo de forma independente — com
controle total sobre layout, dados e apresentação.

### Problema

Designers frequentemente dependem de plataformas externas e
soluções limitadas, sem autonomia sobre conteúdo ou dados.

### Solução

Sistema completo com:

- Exibição profissional de portfólio
- Gerenciamento de projetos e serviços via painel admin
- Autenticação JWT para acesso protegido
- Autonomia total sobre dados e apresentação

---

## Tecnologias

| Camada        | Tecnologias                                      |
|---------------|--------------------------------------------------|
| Frontend      | React, React Router DOM, Axios, Chart.js, Swiper, SCSS |
| Backend       | Node.js, Express, JWT, Multer, dotenv, CORS      |
| Banco de dados| MySQL                                            |
| Infraestrutura| Azure (Cloud Hosting)                            |

---

## Funcionalidades

### Área Pública

- Exibição do portfólio com carrossel de projetos
- Informações da designer
- Formulário de contato

### Área Administrativa

- Autenticação com JWT
- CRUD de projetos e serviços
- Upload de imagens
- Gerenciamento de mensagens
- Visualização de faturamento mensal

---

## Arquitetura

```
[ Frontend — React ]
        ↓
[ API REST — Node.js + Express ]
        ↓
[ Banco de Dados — MySQL ]
        ↓
[ Azure — Cloud Hosting ]
```

### Autenticação

Rotas administrativas protegidas via JWT.
O token é gerado no login e enviado no header das requisições:

```
x-access-token: <token>
```

---

## Estrutura do Projeto

```
/
├── frontend/    # Interface do usuário (React)
└── backend/     # API e regras de negócio (Node.js)
```

---

## Como Executar Localmente

### Backend

```bash
cd backend
npm install
npm start
```

### Frontend

```bash
cd frontend
npm install
npm start
```

> Certifique-se de que o backend está rodando antes de
> iniciar o frontend.

---

## Deploy

Projeto implantado na Azure com acesso público via IP.

Fluxo de desenvolvimento:

```
Desenvolvimento local → Testes → Deploy na Azure → Validação
```

---

## Equipe

Desenvolvido em equipe como simulação de ambiente real,
com foco em boas práticas e entrega de um sistema completo.