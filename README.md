AVengers API - LiveCode DIO (01/04/2021)
Descrição
API desenvolvida com SpringBoot e Kotlin para cadastro de Vingadores.

-Tecnologias Utilizadas
  IntelliJ IDEA
  SpringBoot 2.4.4
  Maven
  Kotlin
  SpringData JPA
  PostgreSQL
  Flyway
  Java 8
  Heroku
  Design Arquitetural
-Camada de Aplicação: Controllers, Configurações, Exception Handling, DTOs, Bean Validations.
-Camada de Domínio: Modelos, Interfaces de Repositório, Serviços.
-Camada de Infraestrutura: Repositório JPA, Entidades, Comunicação com o banco de dados via proxy.

-Recursos API
  GET - 200 OK
  GET {id}/detail - 200 OK ou 404 Not Found
  POST - 201 Created ou 400 Bad Request
  PUT {id} - 202 Accepted ou 404 Not Found
  DELETE {id} - 202 Accepted ou 404 Not Found

-Testes

-Flyway para gerenciamento de versões do banco de dados.

-Estrutura de tabelas:
  avenger: Tabela com colunas id, nick, person, description, history.
  Profiles

-Configurações de profiles para diferentes ambientes:

application.yaml
application-dev.yaml
application-heroku.yaml
Deploy com Docker
Arquivo backend-services.yaml configurado para usar PostgreSQL e pgAdmin.
Comandos:
Deploy: docker-compose -f backend-services.yaml up -d
Undeploy: docker-compose -f backend-services.yaml down
Heroku
Criação de app no Heroku, link com GitHub e configuração de variáveis de ambiente.
Arquivo Procfile para deploy no Heroku.
Comandos para rodar a API
Executar a API localmente:
bash
Copy code
./mvnw spring-boot:run -Dspring-boot.run.profiles=dev
