
# AlunoAPI

AlunoAPI é uma API para cadastro e gerenciamento de informações de alunos.


## Funcionalidades

- [x]   Cadastro de Aluno
- [x]   Consulta de Aluno Por ID e Nome
- [x]   Atualizar Aluno Pelo ID
- [x]   Deleta Todos os Aluno ou Deleta Por ID


## Documentação da API

#### Rota Padrão do Swagger
```
  GET /swagger/index.html
```

#### Retorna todos os Alunos
```
  GET /api/v1/aluno/
```

#### Retorna um Aluno pelo id
```
  GET /api/v1/aluno/{id}/id
```

#### Retorna um Aluno pelo Nome
```
  GET /api/v1/aluno/{nome}/nome
```
#### Criar Um Aluno
```
  POST /api/v1/aluno/
```
#### Atualizar Aluno Pelo id
```
  PUT /api/v1/aluno/{id}/id
```

#### Deleta Aluno Pelo id
```
  DELETE /api/v1/aluno/{id}/id
```

#### Deleta Todos os Alunos
```
  DELETE /api/v1/aluno/all
```


## Rodando localmente

#### Clone o projeto

```bash
  git clone https://github.com/GabrielLimaG3/AlunoAPI.git
```

#### Entre no diretório do projeto

```bash
  cd AlunoAPI
```

#### Instale as dependências

```bash
  dotnet restore
```

#### Configurar o Container do Postgres
```bash
  docker compose up -d
  sudo chmod 777 ./data
  sudo chown 999:999 ./data
```

#### Configura Migration e o Banco de Dados 

__obs__ : Crie uma migration (substitua <Nome_Migration> por um nome significativo, como InitialMigration):
```
  dotnet ef migrations add <Name_Migration>
  dotnet ef database update
```

#### Inicia a Aplicação

```bash
  dotnet watch run
```


## Stack utilizada

- Asp.Net Core
- Docker
- Postgres
- Entity Framework Core
- Swagger

