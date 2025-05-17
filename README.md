# Atividade Spring Boot - API de Usuários

API REST simples para gerenciar usuários, utilizando Spring Boot com armazenamento em memória.

---

## Pré-requisitos

- Java 17 ou superior
- Maven
- Postman (para testar os endpoints)

---

## Como Rodar o Projeto

```bash
# Clone o repositório
git clone https://github.com/LucasPBolzan/atividade-spring-boot

# Entre no diretório
cd atividade-spring-boot

# Rode o projeto
mvn spring-boot:run

```
## Endpoints da API

Use o Postman para testar os endpoints abaixo.

---

### POST /users

**Descrição:** Cria um novo usuário.  
**URL:** `http://localhost:8080/users`  
**Headers Recomendados:**  
`Content-Type: application/json`

####  Exemplo de Body (JSON)

```json
{
  "name": "João",
  "age": 25
}
```
####  Exemplo de Resposta

```json
[
  {
    "id": 1,
    "name": "João",
    "age": 25
  }
]

```

### GET /users

**Descrição:** Lista todos os usuários cadastrados.  
**URL:** `http://localhost:8080/users`

####  Exemplo de Resposta

```json
[
  {
    "id": 1,
    "name": "João",
    "age": 25
  }
]

```

### PUT /users/{id}

**Descrição:** Atualiza um usuário existente pelo ID.  
**URL:** `http://localhost:8080/users/1` 
**Headers Recomendados:**  
`Content-Type: application/json`

####  Exemplo de Body (JSON)

```json
{
  "name": "João Modificado",
  "age": 25
}
```
####  Exemplo de Resposta

```json
[
  {
    "id": 1,
    "name": "João Modificado",
    "age": 25
  }
]

```


### DELETE /users/{id}

**Descrição:** Remove um usuário pelo ID.
**URL:** `http://localhost:8080/users/1` 
**Headers Recomendados:**  
`Content-Type: application/json`

#### Resposta

- **Status:** `200 OK`
- **Body:** *(sem conteúdo)*


