# Spring Security JWT Authentication

Este projeto é uma implementação de autenticação baseada em JWT (JSON Web Token) utilizando o Spring Security e Spring Boot. O objetivo principal é estudar a integração de autenticação e autorização em APIs RESTful, com foco em segurança, utilizando a prática de boas práticas como a criação de tokens JWT e a proteção de endpoints.

## Tecnologias Utilizadas

- **Spring Boot**: Framework para construção de aplicações Java de forma rápida e fácil.
- **Spring Security**: Framework de segurança para autenticação e autorização.
- **JWT (JSON Web Token)**: Tecnologia para autenticação baseada em tokens, permitindo que o estado de autenticação seja mantido entre requisições.
- **JPA (Java Persistence API)**: Para interação com o banco de dados utilizando Hibernate.
- **H2 Database**: Banco de dados em memória para facilitar o desenvolvimento e testes.
- **Lombok**: Biblioteca para reduzir a verbosidade do código.
- **BCrypt**: Algoritmo para criptografia de senhas.

## Funcionalidades

- **Cadastro de Usuários**: Permite registrar novos usuários com e-mail, nome e senha criptografada.
- **Login de Usuários**: Validação de credenciais e geração de JWT.
- **Proteção de Endpoints**: Apenas usuários autenticados (com token válido) podem acessar endpoints protegidos.

## Endpoints

### 1. **POST /auth/register**
- Registra um novo usuário.
- **Exemplo de body**:
  ```json
  {
    "name": "Felipe Bertoni",
    "email": "felipe@example.com",
    "password": "senha123"
  }

### 2. **POST /auth/login**
- Faz o login com o usuário cadastrado
- **Exemplo de body**:
  ```json
  {
      "email": "guilherme1.andrade@gmail.com",
      "password": "123456"
  }

### 3. **GET /user**
- Acessa o UserController, onde só tem acesso quando estiver com Cadastro realizado
- **Exemplo de body**:
  ```json
  {
      "email": "guilherme1.andrade@gmail.com",
      "password": "123456"
  }
