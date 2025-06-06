# Projeto Devops - Igreja

Este é um fork de uma aplicação web feita por uma equipe durante o segundo período da disciplina de SPI. A proposta aqui é containerizar toda a aplicação usando Docker e adicionar testes automatizados com Cypress.

- **Backend**: Node.js com Express e Sequelize
- **Frontend**: HTML, CSS e JavaScript servidos por um servidor NGINX
- **Banco de Dados**: MariaDB

Cada parte do sistema roda em seu próprio container e tudo é orquestrado com Docker Compose.

---

## O que você vai precisar

Antes de começar, é necessário ter instalado:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

---

## Como rodar o projeto

### 1. Clone o repositório

Abra o terminal e rode:

```bash
git clone git@github.com:IAbrahanArley/igreja-anglicana-comunhao.git
cd igreja-anglicana-comunhao
```

### 2. Configure as variáveis de ambiente

Crie um arquivo `.env` na raiz do projeto com o seguinte conteúdo:

```env
DB_USER=user
DB_PASSWORD=123456
DB_NAME=doador
DB_PORT=3307
DB_HOST=db
```

Essas variáveis serão usadas para configurar a conexão do backend com o banco de dados.

### 3. Suba os containers

No terminal, execute:

```bash
docker-compose up --build
```

Após a construção e inicialização dos containers, a aplicação estará disponível nos seguintes endereços:

- Frontend: http://localhost:8080
- Backend (API): http://localhost:3001
- Banco de Dados (MariaDB): localhost:3307

---

## Estrutura do Projeto

```bash
/api        # Backend (Node.js + Express)
/front      # Frontend estático (HTML/CSS/JS)
docker-compose.yml
.env
README.md
DESENVOLVIMENTO.md
```

---

## Tecnologias Utilizadas

- Node.js + Express
- Sequelize (ORM)
- MariaDB
- NGINX
- Docker e Docker Compose
- Cypress (para testes end-to-end)
