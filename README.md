Heather Design — Plataforma Completa

Plataforma web de portfólio para designers, desenvolvida em equipe, com landing page pública e painel administrativo com autenticação, permitindo gerenciamento completo de projetos, serviços e conteúdo.

Hospedado na nuvem Azure com acesso público via IP
Arquitetura fullstack: Frontend + Backend + Banco de Dados

Visão Geral

O Heather Design é um sistema completo que simula um produto real de mercado, permitindo que designers tenham autonomia para:

Exibir seus trabalhos de forma profissional
Gerenciar projetos e serviços
Controlar conteúdo sem depender de terceiros
❗ Problema

Designers frequentemente dependem de plataformas externas ou soluções limitadas para apresentar seus trabalhos, sem controle total sobre conteúdo, layout e dados.

💡 Solução

Foi desenvolvida uma plataforma própria com:

Landing page pública para exibição do portfólio
Painel administrativo protegido por login
Sistema completo de gerenciamento de conteúdo
Deploy na nuvem (Azure) com acesso público
Abordagem Técnica

O projeto segue uma arquitetura cliente-servidor (fullstack):

Frontend: interface moderna e interativa
Backend: API REST para regras de negócio
Banco de dados: armazenamento estruturado
Cloud (Azure): deploy e acesso público
Stack Tecnológica
Frontend
React
React Router DOM
Axios
Chart.js
Swiper
SCSS
Backend
Node.js
Express
JWT (autenticação)
Multer (upload de imagens)
dotenv
CORS
Banco de Dados
MySQL
Infraestrutura
Azure (deploy e hospedagem)

Funcionalidades Principais
Área Pública
Exibição de portfólio
Carrossel de projetos
Informações da designer
Formulário de contato
Área Administrativa
Login com autenticação JWT
CRUD de projetos (portfólio)
CRUD de serviços
Upload de imagens
Visualização de mensagens
Dashboard com faturamento mensal
Arquitetura do Sistema
[ Frontend (React) ]
↓
[ API REST (Node.js + Express) ]
↓
[ Banco de Dados (MySQL) ]
↓
[ Azure (Cloud Hosting) ]
Autenticação

O sistema utiliza JWT (JSON Web Token) para proteger rotas administrativas:

Login gera um token
Token é armazenado no cliente
Enviado em requisições protegidas via header:
x-access-token: <token>
Estrutura do Projeto

O repositório está dividido em duas partes principais:

/frontend → Interface do usuário (React)
/backend → API e regras de negócio (Node.js)
Como executar o projeto
Backend
cd backend
npm install
npm start
Frontend
cd frontend
npm install
npm start

Certifique-se de que o backend está rodando antes do frontend

Configuração
Variáveis de ambiente (Backend)

Crie um arquivo .env:

PORT=3010

MYSQL_HOST=
MYSQL_USER=
MYSQL_PWD=
MYSQL_DB=
Deploy

O projeto foi implantado na Azure, permitindo:

Acesso público via IP
Simulação de ambiente real de produção
Integração completa entre front, back e banco
Equipe

Projeto desenvolvido em equipe com foco em:

Simular ambiente real de desenvolvimento
Aplicar boas práticas de arquitetura
Construir um produto funcional completo
Diferenciais do Projeto
✔️ Fullstack completo (frontend + backend + banco)
✔️ Autenticação real com JWT
✔️ Upload de imagens
✔️ Dashboard com dados
✔️ Deploy em cloud (Azure)
✔️ Estrutura escalável e organizada
Possíveis Melhorias Futuras
Deploy com domínio personalizado
Sistema de permissões (multiusuário)
Integração com pagamentos
Otimização de performance
CI/CD pipeline
