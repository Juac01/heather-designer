# 🎨 Heather Design — Frontend

Plataforma de portfólio desenvolvida para a **Heather Designer**, criada em equipe com o objetivo de aprender e simular conceitos reais de desenvolvimento web. O projeto conta com uma **landing page pública** para exibição dos trabalhos e um **painel administrativo** protegido por autenticação.

> Projeto hospedado na nuvem **Azure** com acesso público via IP.
> Projeto funcional localmente

---

## 💡 Contexto

A designer precisava de uma plataforma própria para exibir seus trabalhos e gerenciar conteúdo de forma independente. A solução foi um sistema completo com landing page pública e painel admin protegido por login, com arquitetura cliente-servidor usando **React** no front, **Node.js** no back e **MySQL** para os dados.

---

## 🛠️ Tecnologias

- [React](https://react.dev/) + [React Router DOM](https://reactrouter.com/)
- [Axios](https://axios-http.com/) — consumo da API REST
- [Chart.js](https://www.chartjs.org/) / [react-chartjs-2](https://react-chartjs-2.js.org/) — gráfico de faturamento mensal
- [Swiper](https://swiperjs.com/) — carrossel de portfólio
- [React Hot Toast](https://react-hot-toast.com/) / [React Toastify](https://fkhadra.github.io/react-toastify/) — notificações
- SCSS — estilização
- Deploy na **Azure**

---

## 📁 Estrutura do Projeto

```
src/
├── api/
│   └── constantes.js              # URL base da API (local ou Azure)
├── components/
│   ├── cabecalho/                 # Header público e admin
│   ├── cardPortfolio/             # Card de projeto com ações de editar/excluir
│   ├── carrossel/                 # Carrossel com Swiper
│   └── rodape/                    # Rodapé
├── pages/
│   ├── Home/                      # Landing page pública
│   ├── Login/                     # Tela de autenticação
│   ├── naoEncontrado/             # Página 404
│   └── AdministrarTelas/
│       ├── HomeAdmin/             # Painel: portfólio, agenda e mensagens
│       ├── AdicionarServico/      # Criar ou editar serviço
│       ├── adicionarPortfolio/    # Criar ou editar projeto do portfólio
│       └── FaturamentoMensal/     # Gráfico de faturamento mensal
```

---

## 📌 Rotas da Aplicação

| Rota                   | Acesso  | Descrição                                |
| ---------------------- | ------- | ---------------------------------------- |
| `/` ou `/home`         | Público | Landing page da designer                 |
| `/login`               | Público | Login da administradora                  |
| `/admin`               | Admin   | Painel com portfólio, agenda e mensagens |
| `/criar-servico`       | Admin   | Adicionar novo serviço                   |
| `/criar-servico/:id`   | Admin   | Editar serviço existente                 |
| `/criar-portfolio`     | Admin   | Adicionar novo projeto                   |
| `/criar-portfolio/:id` | Admin   | Editar projeto existente                 |
| `/faturamento`         | Admin   | Gráfico de faturamento mensal            |

---

## 🔐 Autenticação

O login é feito via **JWT**. O token retornado pela API é armazenado no `localStorage` e enviado no header `x-access-token` em todas as requisições protegidas. Rotas do painel administrativo redirecionam automaticamente para `/login` caso o token esteja ausente.

---

## ⚙️ Configuração da API

O arquivo `src/api/constantes.js` define a URL base da API. Basta comentar/descomentar a linha conforme o ambiente:

```js
// Ambiente local
export const API_URL = "http://localhost:3010";

// Ambiente Azure (descomentar para deploy)
// export const API_URL = 'http://52.233.83.184:3010'
```

---

## 🚀 Como executar localmente

```bash
# Instalar dependências
npm install

# Iniciar o projeto
npm start
```

> Certifique-se de que o backend está rodando na porta `3010` antes de iniciar o frontend.

---

## 👥 Equipe

Projeto desenvolvido em equipe como simulação de um ambiente real de desenvolvimento.

> **Backend:** [heather-design-backend](../heather-design-backend)
