** Estrutura padrão para desenvolvimento Back-end DDD **

Conteúdo estrutural:
- Typescript: Sintaxe padrão
- Babel: transpile e build
- Express: gerenciamento de rota, middlewares
- Celebrate JOI: validação de parâmetros de rota
- JWT: autenticação
- Redis: cache de consultas
- tsyringe: injeção de dependência
- Typeorm: ORM de banco de dados
- jest: testes automatizados

Padronização para design de código
- eslint
- prettier
- editorconfig

Gerenciador de pacotes:
- yarn (opcional)

** Instrução para execução **
1. Acesse a pasta do projeto e execute a atualização de dependência:
   (yarn ou npm install)

2. Instale o redis ou crie um container do mesmo
   (docker run --name redis_container -p 6379:6379 -d -t redis:alpine)

3. Instale o mondodb ou crie um container para o mesmo
   (docker run —name mongodb_container -p 27017:27017 -d -t mongo)

4. Instale o postgres(BD de exemplo) ou crie um container para o mesmo
   (docker run --name postgres_container -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres )

5. Configure os arquivos 'ormconfig.json' e '.env' para o endereço e porta do host onde se encontram os dbs


6. Rode as migrations para criar os schemas nos dbs ( yarn typeorm migrations:run )


7. Execute a aplicação ( yarn dev:server )

