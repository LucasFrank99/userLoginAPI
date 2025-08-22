## 📖 Descrição

Este projeto é uma **API REST** desenvolvida em **Java** com **Spring Boot**, destinada à gestão de cadastros de usuário, utilizando **PostgreSQL** como banco de dados e **Spring Security** para autenticação e autorização baseada em segurança.

---

## 🚀 Tecnologias

- Java (versão atual do projeto)  
- Spring Boot  
- Spring Security  
- Spring Data JPA  
- PostgreSQL  
- Maven (ferramenta de build)

---

## ⚙️ Requisitos

Antes de começar, certifique-se de que você tem:

- JDK instalado (versão 11 ou superior)  
- PostgreSQL configurado  
- Maven instalado (ou utilize o wrapper `./mvnw`)

---

## ▶️ Instalação e execução

1. Clone o repositório:
   ```bash
   git clone https://github.com/LucasFrank99/userLoginAPI.git
   cd userLoginAPI
   ```

2. Configure o banco de dados PostgreSQL (crie um banco adequado, ex: `userdb`).

3. Altere as configurações do banco no arquivo `application.properties` (veja detalhes abaixo).

4. Execute o projeto:
   ```bash
   ./mvnw spring-boot:run
   ```
   ou
   ```bash
   mvn spring-boot:run
   ```

---

## ⚙️ Configuração (`application.properties`)

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/seu_banco
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect

# Security
# (como exemplo, adapte conforme sua implementação)
spring.security.user.name=usuario
spring.security.user.password=senha
```

---

## 📌 Endpoints principais

| Método | Caminho               | Descrição                          |
|--------|------------------------|-------------------------------------|
| POST   | `/api/auth/register`  | Cadastra novo usuário               |
| POST   | `/api/auth/login`     | Autentica usuário e retorna token   |
| GET    | `/api/users/me`       | Retorna dados do usuário autenticado |

> *Observação:* Ajuste os endpoints acima conforme os definidos no seu código.

---

## 🧪 Testes

- Utilize o **Postman** ou similar para testar as requisições.  
- Certifique-se de adicionar o token JWT retornado no login ao header `Authorization: Bearer <token>` ao acessar endpoints protegidos.

---

## 🤝 Contribuição

Contribuições são bem-vindas! Para ajudar:

1. Faça um fork do projeto  
2. Crie uma branch nova (`git checkout -b feature/nome-da-feature`)  
3. Realize suas modificações e commit  
4. Envie para o seu fork (`git push origin feature/nome-da-feature`)  
5. Abra um Pull Request (PR) aqui no repositório principal


