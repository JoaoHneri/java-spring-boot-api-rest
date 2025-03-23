# 📌 API REST VollMed (Spring Boot + JWT)

👋 **Seja bem-vindo ao projeto VollMed!**

Este é um projeto de API REST segura desenvolvido com **Java**, **Spring Boot** e **Spring Security**, utilizando autenticação baseada em **JWT (JSON Web Token)**. O projeto tem como objetivo gerenciar cadastros e operações relacionadas a médicos e pacientes, aplicando boas práticas de segurança e organização.

---

## 🚀 Tecnologias utilizadas

- Java 17+
- Spring Boot
- Spring Security
- JWT (JSON Web Token)
- MySQL
- Spring Data JPA
- Bean Validation
- Lombok

---

## ⚙️ Configuração do projeto

### 📋 Banco de Dados (`application.properties`):

Utilize este modelo adaptando ao seu ambiente local:

```properties
spring.application.name=sua-api
spring.datasource.url=jdbc:mysql://localhost:<porta>/<nome_banco>
spring.datasource.username=<usuario_banco>
spring.datasource.password=<senha_banco>

server.error.include-stacktrace=never

api.security.token.secret=${JWT_SECRET:<sua_chave_jwt>}

````
## 🔑 Autenticação JWT

Para autenticar e obter o Token JWT utilize o endpoint abaixo:

**POST `/login`**

**Exemplo de requisição:**

```json
{
  "login": "usuario_exemplo",
  "senha": "senha_exemplo"
}
```

**Exemplo de resposta:**

```json
{
  "token": "token.jwt.exemplo"
}
```

**Utilize o token obtido no cabeçalho HTTP das requisições protegidas da seguinte forma:**

```properties
Authorization: Bearer token.jwt.exemplo
```
