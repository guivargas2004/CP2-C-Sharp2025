

Tema: Catálogo simples de Autores e Livros
Resumo: Esta API REST permite gerenciar autores e seus livros com CRUD completo usando C# (.NET 8) e Entity Framework Core (SQLite). A documentação interativa fica disponível via Swagger.

Integrantes do grupo (Challenge)

- Guilherme Dal Pasolo — RM 98694

- Guilherme Faustino Vargas — RM 98278

- João Lucas Hedi Handa — RM 98458

- Ryan Perez Pacheco — RM 98782


Tecnologias

- .NET 8 (ASP.NET Core Web API)

- Entity Framework Core + SQLite

- Swagger

Como rodar o projeto
Pré-requisitos:

- .NET SDK 8 instalado

# 1) Vá até a pasta do projeto Web API
- cd EfCrudSample/EfCrudSample.Api

# 2) Restaurar e compilar
- dotnet restore
- dotnet build

# 3) Criar e aplicar a migration inicial (apenas na primeira vez)
- dotnet ef migrations add InitialCreate
- dotnet ef database update

# 4) Executar a API
- dotnet run

A API sobe (por padrão) em:

https://localhost:7123

http://localhost:5068

Abra o Swagger em:

https://localhost:7123/swagger
ou
http://localhost:5068/swagger


 O que a aplicação faz (funcionalidades)

- CRUD de Autores

- Criar, listar, buscar por id, atualizar e excluir autores

- Exclusão em cascade remove também os livros do autor

- CRUD de Livros

- Criar, listar, buscar por id, atualizar e excluir livros

- Validação: só cria livro se o AuthorId existir

- Relacionamento 1→N (Author tem muitos Books)

- Leituras performáticas com AsNoTracking

- Swagger para explorar/testar endpoints


