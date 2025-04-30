# Checkpoint 1 - API de Pedidos

Este projeto é um sistema de gerenciamento de pedidos desenvolvido em **Spring Boot** como parte do checkpoint da disciplina **Arquitetura SOA e Web Services**.

📌 **Feito por:** João Antonio Rihan (rm99656) e Rodrigo Fernandes Serafim (rm550816) 🚀


## 📌 Tecnologias Utilizadas
- Java 17
- Spring Boot 3.1
- Spring Data JPA
- H2 Database (banco de dados em memória)
- Lombok
- Maven

## 📁 Estrutura do Projeto

```
src/main/java/br/com/fiap/checkpoint1
├── controller  // Endpoints REST
├── model       // Entidade Pedido
├── repository  // Interface de acesso ao banco
├── service     // Regras de negócio
```

## 🚀 Como Executar o Projeto
### 1️⃣ Clonar o Repositório
```sh
git clone https://github.com/joaorihan/soapoint.git
cd fiap-checkpoint1
```

### 2️⃣ Compilar e Rodar a API
```sh
mvn spring-boot:run
```
A API estará disponível em **http://localhost:8080**.

## 🗄️ Configuração do Banco H2
O projeto utiliza o **H2 Database** em memória. Para acessar o console:

- URL: [http://localhost:8080/h2-console](http://localhost:8080/h2-console)
- JDBC URL: `jdbc:h2:mem:pedidosdb`
- Username: `sa`
- Password: (vazio)

## 📌 Endpoints Disponíveis

### 🔹 **Criar um Pedido**
📌 `POST /pedidos`

#### 📝 Exemplo de Request Body:
```json
{
  "clienteNome": "João Antônio",
  "valorTotal": 150.50
}
```
#### ✅ Exemplo de Response:
```json
{
  "id": 1,
  "clienteNome": "João Antônio",
  "dataPedido": "2024-03-25",
  "valorTotal": 150.50
}
```

---
### 🔹 **Listar todos os Pedidos**
📌 `GET /pedidos`

#### ✅ Exemplo de Response:
```json
[
  {
    "id": 1,
    "clienteNome": "João Antônio",
    "dataPedido": "2024-03-25",
    "valorTotal": 150.50
  }
]
```

---
### 🔹 **Buscar um Pedido pelo ID**
📌 `GET /pedidos/{id}`

#### ✅ Exemplo de Response:
```json
{
  "id": 1,
  "clienteNome": "João Antonio",
  "dataPedido": "2024-03-25",
  "valorTotal": 150.50
}
```

---
### 🔹 **Atualizar um Pedido**
📌 `PUT /pedidos/{id}`

#### 📝 Exemplo de Request Body:
```json
{
  "clienteNome": "Rodrigo Fernandes",
  "valorTotal": 200.00
}
```
#### ✅ Exemplo de Response:
```json
{
  "id": 1,
  "clienteNome": "Rodrigo Fernandes",
  "dataPedido": "2024-03-25",
  "valorTotal": 200.00
}
```

---
### 🔹 **Deletar um Pedido**
📌 `DELETE /pedidos/{id}`

#### ✅ Exemplo de Response:
```
204 No Content
```

## 📷 Prints dos Testes

Aqui estão as imagens dos testes realizados no **Postman**:

Criando um novo pedido
![Teste 1](./img/imagem1.PNG)
<br>
Buscando todos os pedidos
![Teste 2](./img/imagem2.PNG)
<br>
Buscar um pedido pelo ID
![Teste 3](./img/imagem3.PNG)
<br>
Atualizar um pedido
![Teste 4](./img/imagem4.PNG)
<br>
Deletar um pedido
![Teste 5](./img/imagem5.PNG)
<br>

---



