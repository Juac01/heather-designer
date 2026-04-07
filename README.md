Heather Design — Plataforma Completa

Plataforma de portfólio para designers desenvolvida em equipe com sistema de login e gerenciamento de projetos. Composta por uma landing page pública e um painel administrativo, seguindo uma arquitetura fullstack com frontend, backend e banco de dados.

Projeto hospedado na nuvem Azure com acesso público via IP.

Projeto funcional localmente (desenvolvido e testado antes do deploy)

Contexto

A designer precisava de uma plataforma própria para exibir seus trabalhos e gerenciar conteúdo de forma independente. A solução foi um sistema completo com landing page pública e painel admin protegido por autenticação, utilizando arquitetura cliente-servidor com React no frontend, Node.js no backend e MySQL para persistência de dados.

Problema

Designers frequentemente dependem de plataformas externas ou soluções limitadas para apresentar seus trabalhos, sem controle total sobre conteúdo, layout e dados.

Solução

Desenvolvimento de uma plataforma própria que permite:

Exibição profissional de portfólio
Gerenciamento completo de projetos e serviços
Controle de conteúdo via painel administrativo
Autonomia total sobre dados e apresentação
Abordagem

O sistema foi estruturado seguindo uma arquitetura cliente-servidor:

Frontend responsável pela interface e experiência do usuário
Backend responsável pelas regras de negócio e API REST
Banco de dados para armazenamento estruturado
Deploy em nuvem utilizando Azure
Tecnologias
Frontend
React
React Router DOM
Axios
Chart.js
Swiper
SCSS
Backend
Node.js
 + Express
JWT (jsonwebtoken)
Multer
dotenv
CORS
Banco de Dados
MySQL
Infraestrutura
Deploy na Azure
Funcionalidades
Área Pública
Exibição de portfólio
Carrossel de projetos
Informações da designer
Formulário de contato
Área Administrativa
Autenticação com JWT
CRUD de projetos
CRUD de serviços
Upload de imagens
Gerenciamento de mensagens
Visualização de faturamento mensal
Arquitetura
[ Frontend (React) ]
        ↓
[ API REST (Node.js + Express) ]
        ↓
[ Banco de Dados (MySQL) ]
        ↓
[ Azure (Cloud Hosting) ]
Autenticação

O sistema utiliza JWT para proteger rotas administrativas.

x-access-token: <token>

O token é gerado no login e deve ser armazenado pelo cliente para acesso às rotas protegidas.

Estrutura do Projeto
/frontend  # Interface do usuário (React)
/backend   # API e regras de negócio (Node.js)
Como executar localmente
Backend
cd backend
npm install
npm start
Frontend
cd frontend
npm install
npm start

Certifique-se de que o backend está rodando antes de iniciar o frontend.

Deploy

O projeto foi implantado na Azure, permitindo acesso público via IP e simulação de ambiente real de produção.

O desenvolvimento seguiu um fluxo completo:

Desenvolvimento local → Testes → Deploy na Azure → Validação em produção
Equipe

Projeto desenvolvido em equipe como simulação de um ambiente real de desenvolvimento, com foco em aplicação de boas práticas e construção de um sistema completo.