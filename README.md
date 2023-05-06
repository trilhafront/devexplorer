# Série Dev Explorer - Projeto Full-stack

## 1. Projeto

O projeto é uma Aplicação Web chamada "Lista de Tarefas", onde será possível cadastrar, excluir, listar e editar tarefas por meio de uma página Web.

Projeto: https://github.com/trilhafront/devexplorer

<img style="max-width:500px" src="previa.png">

## 2. Banco de dados (PostgreSQL - Para armazenas as tarefas)

- [] Fazer o Fork do projeto: https://github.com/trilhafront/devexplorer

- [] Criar o ambiente (Github Codespaces) do Projeto

- [] Instalar o banco Postgres:

    docker network create network
    docker create --network network --name postgres -p 5432:5432 -e POSTGRES_PASSWORD=postgres postgres

- [] Gerenciar o banco Postgres:

    docker start postgres (para iniciar o banco)
    docker run -it --rm --network network postgres psql -h postgres -U postgres (para conectar no banco)
    docker ps (para verificar se o banco está no ar)
    docker stop postgres (para parar o banco)

- [] Criar uma tabela e fazer operações:

    create table tarefas (id serial primary key, titulo varchar(100), concluida boolean);
    insert into tarefas (titulo, concluida) values ('Estudar PostgreSQL', false);
    insert into tarefas (titulo, concluida) values ('Estudar Node.js', false);
    insert into tarefas (titulo, concluida) values ('Estudar Express.js', false);
    insert into tarefas (titulo, concluida) values ('Estudar JavaScript', false);
    insert into tarefas (titulo, concluida) values ('Estudar HTML', true);
    insert into tarefas (titulo, concluida) values ('Estudar CSS', false);
    
    select id, titulo, concluida from tarefas;

    truncate table tarefas; (para remover todas as linhas da tabela)
    drop table tarefas; (para remover a tabela)
## 3. API (Express - Para construir a API)
npm install express
    npm install cors (para evitar problemas de segurança)
npm install pg-promise
## 4. HTML (Para o conteúdo do Front-end da aplicação)
## 5. JavaScript (Para a interatividade do Front-end da aplicação)
## 6. CSS (Para a estilização do Front-end da aplicação)
