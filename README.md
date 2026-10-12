# Trabalho Desenvolvimento WEB Back-End com Java

## Tecnologias utilizadas
- Java 17
- SpringBoot 4.1
- Spring Data JPA
- MySQL 8.0
- Docker

## Descrição
CRUD para controle de clientes, produtos e pedidos.

## Inicialização
### Criar arquivo .env, copiando os dados do .env-example
```bash
cp .env-example .env
```

### Subir container MySQL
```bash
docker compose up -d
```

## End-points

### Clientes

| Método | Endpoint        | Descrição                        | Body JSON                              |
| ------ | --------------- | -------------------------------- |----------------------------------------|
|    <img src="https://img.shields.io/badge/GET-blue?style=flat-square" alt="GET" />    | `/clients`      | Lista todos os clientes          | --                                     |
|    <img src="https://img.shields.io/badge/GET-blue?style=flat-square" alt="GET" />    | `/clients/{id}` | Busca um cliente pelo ID         | --                                     |
|    <img src="https://img.shields.io/badge/POST-green?style=flat-square" alt="POST" />    | `/clients`      | Cadastra um novo cliente         | (all) name: string, clientSince: date  |
|    <img src="https://img.shields.io/badge/PATCH-orange?style=flat-square" alt="PATCH" />    | `/clients/{id}` | Atualiza parcialmente um cliente | (some) name: string, clientSince: date |
|    <img src="https://img.shields.io/badge/DELETE-red?style=flat-square" alt="DELETE" />    | `/clients/{id}` | Exclui um cliente                | --                                     |

---

## Produtos

### Endpoints disponíveis

| Método | Endpoint         | Descrição                        | Body JSON                                           |
| ------ | ---------------- | -------------------------------- |-----------------------------------------------------|
|  <img src="https://img.shields.io/badge/GET-blue?style=flat-square" alt="GET" />      | `/products`      | Lista todos os produtos          | --                                                  |
|  <img src="https://img.shields.io/badge/GET-blue?style=flat-square" alt="GET" />      | `/products/{id}` | Busca um produto pelo ID         | --                                                  |
|  <img src="https://img.shields.io/badge/POST-green?style=flat-square" alt="POST" />      | `/products`      | Cadastra um novo produto         | (all) name: string, price: decimal, stock: boolean  |
|  <img src="https://img.shields.io/badge/PATCH-orange?style=flat-square" alt="PATCH" />      | `/products/{id}` | Atualiza parcialmente um produto | (some) name: string, price: decimal, stock: boolean |
|  <img src="https://img.shields.io/badge/DELETE-red?style=flat-square" alt="DELETE" />      | `/products/{id}` | Exclui um produto                | --                                                  |


---

## Pedidos

### Endpoints disponíveis

| Método | Endpoint         | Descrição                     | Body JSON                                                       |
| ------ |------------------|-------------------------------|-----------------------------------------------------------------|
|  <img src="https://img.shields.io/badge/GET-blue?style=flat-square" alt="GET" />      | `/orders`        | Lista todos os pedidos        | --                                                              |
|  <img src="https://img.shields.io/badge/GET-blue?style=flat-square" alt="GET" />      | `/orders/{id}` | Busca um pedido pelo ID       | --                                                              |
|  <img src="https://img.shields.io/badge/POST-green?style=flat-square" alt="POST" />      | `/orders`      | Cadastra um novo pedido       | (all) clientId: integer, productId: integer, quantity: integer  |
|  <img src="https://img.shields.io/badge/PATCH-orange?style=flat-square" alt="PATCH" />      | `/orders/{id}` | Atualiza parcialmente um pedido | (some) clientId: integer, productId: integer, quantity: integer |
|  <img src="https://img.shields.io/badge/DELETE-red?style=flat-square" alt="DELETE" />      | `/orders/{id}` | Exclui um pedido              | --                                                              |

## Diagrama UML
<img src="diagram.png" alt="Diagrama">