# 🎮 API RESTFul de Gerenciamento de Jogos e Listas  

API RESTFul desenvolvida em **Java Spring Boot** para gerenciar jogos e listas de estilos de jogos.  

---

## 🚀 O que foi feito  

- **Listagem de jogos:** Endpoint que retorna todos os jogos cadastrados.  
- **Listagem de listas:** Endpoint que retorna todas as listas de estilos de jogos.  
- **Busca por ID:** Endpoint para buscar um jogo ou uma lista pelo ID.  
- **Listagem de jogos por lista:** Endpoint que retorna todos os jogos vinculados a uma lista específica.  
- **Reordenação de jogos:** Funcionalidade para alterar a posição de jogos dentro de uma lista.  
- **Tratamento de erros:** Respostas claras para casos como ID inexistente ou requisições inválidas.  

---

## 📌 Endpoints  (Todos os retornos em JSON)

### 1. **Listar Todos os Jogos**  
- **GET** `/games`  
- Retorna uma lista com todos os jogos cadastrados.  

### 2. **Listar Todas as Listas**  
- **GET** `/lists`  
- Retorna todas as listas de estilos de jogos.  

### 3. **Buscar Jogo por ID**  
- **GET** `/games/{id}`  
- Retorna os detalhes de um jogo específico.  

### 4. **Listar Jogos de uma Lista**  
- **GET** `/lists/{listId}/games`  
- Retorna todos os jogos vinculados a uma lista específica.  

### 5. **Reordenar Jogos em uma Lista**  
- **POST** `/lists/{listId}/replacement`  
- Altera a posição de um jogo dentro de uma lista.  
- **Corpo da Requisição (JSON):**  
  ```json
  {
    "sourceIndex": 2,
    "destinationIndex": 0
  }

---

## 🛠️ Tecnologias Utilizadas
### - Java 21
### - Spring Boot
### - PostgreSQL
### - Docker
### - Postman

---

## Estrutura de Contêineres No Docker

O projeto utiliza dois contêineres Docker:

- Um contêiner para o banco de dados PostgreSQL, onde os dados da aplicação são armazenados.
- Um contêiner para o Adminer (PostAdmin), utilizado para acessar e gerenciar o banco de dados de forma visual.
