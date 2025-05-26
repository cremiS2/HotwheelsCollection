
# 🚗🔥 CollectionHotwheels – Aplicativo + API

O **CollectionHotwheels** é um sistema completo composto por uma API backend e um aplicativo mobile frontend.  
Ele permite o gerenciamento de uma coleção de carros HotWheels, com funcionalidades completas de cadastro, listagem, edição e exclusão de veículos.

---

## 🎯 Visão Geral

- **Backend:** API REST desenvolvida em **Java + MySQL**
- **Frontend:** Aplicativo mobile construído com **React Native**
- **Integração:** A comunicação entre app e API é feita via **Axios**

---

## 🧰 Tecnologias Utilizadas

### 🔧 Backend (API Java + MySQL)

- **Java** – Plataforma para lógica de negócio e APIs REST  
- **Spring Boot** – Framework Java para aplicações web  
- **MySQL** – Banco de dados relacional  
- **Swagger** – Interface de documentação e testes  
- **CORS** – Permite requisições entre diferentes origens  

### 📱 Frontend (React Native)

- **React Native** – Criação de apps mobile nativos
- **Axios** – Cliente HTTP para consumir a API
- **React Navigation** – Navegação entre telas
- **Expo Image Picker** – Seleção de imagens da galeria/câmera
- **Expo Linear Gradient** – Aplicação de gradientes
- **UUID** – Geração de identificadores únicos
- **Toastify Message** – Feedbacks visuais ao usuário

---

## 🚀 Funcionalidades

Tanto no app quanto na API, o sistema permite:

- ✅ Visualizar todos os carros cadastrados
- 🔍 Ver detalhes de um carro
- ➕ Cadastrar um novo carro com imagem
- ✏️ Editar dados de um carro
- ❌ Excluir um carro individualmente
- 🧹 Excluir todos os carros da base (via API)
- 📩 Mensagens de feedback e confirmação
- 📖 Documentação interativa com Swagger (API)

---

## 📄 Endpoints da API (Spring Boot)

> Base URL: `https://localhost:8080/hotwheels`

### 🔹 Criar um novo carro  
**POST** `/hotwheels`  
```json
{
  "nome": "Twin Mill",
  "modelo": "Modelo D",
  "ano": 2010,
  "imagem": "http://example.com/images/twinmill.jpg"
}
```

### 🔹 Listar todos os carros  
**GET** `/hotwheels`

### 🔹 Buscar um carro por ID  
**GET** `/hotwheels/{id}`

### 🔹 Atualizar dados de um carro  
**PUT** `/hotwheels/{id}`  
```json
{
  "nome": "BMW X6",
  "modelo": "2021",
  "ano": 2021,
  "imagem": "http://example.com/images/bmw-x6-2021.jpg"
}
```

### 🔹 Deletar um carro por ID  
**DELETE** `/hotwheels/{id}`

### 🔹 Deletar todos os carros  
**DELETE** `/hotwheels/delete-all`

### 🔹 Mensagem de boas-vindas  
**GET** `/hotwheels/welcome`

---

## 📱 Telas do Aplicativo

1. **Tela Inicial (Home)**  
   ![]()

2. **Tela de Cadastro de Carro**  
   ![]()

3. **Tela de Edição de Carro**  
   ![](./assets/tela_3.jpg)

4. **Tela de Detalhes do Carro**  
   ![](./assets/tela_4.jpg)

5. **Tela de Confirmação de Exclusão**  
   ![](./assets/tela_5.jpg)

6. **Tela de Sucesso/Feedback**  
   ![](./assets/tela_6.jpg)

---

## 🔗 Integração

O **app React Native** se conecta diretamente à **API Java Spring Boot** hospedada localmente ou em um servidor remoto, usando `Axios`.

Exemplo de URL no `carService.js`:
```js
const API_BASE = 'https://localhost:8080/hotwheels';
```

---

## ▶️ Como Rodar o Projeto

### 🔧 Backend

1. Configure o MySQL e crie o banco de dados
2. Atualize o arquivo `application.properties` com os dados de conexão
3. Compile e execute o projeto Spring Boot
4. Acesse `http://localhost:8080/swagger-ui.html` para testar a API

### 📱 Frontend

1. Instale as dependências com `npm install`
2. Execute o app com `npx expo start`
3. Teste no celular com o **Expo Go**

---
