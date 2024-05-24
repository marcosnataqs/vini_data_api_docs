# **Documentação da API** :pushpin:
Essa etapa contém as visões da documentação da API, incluindo autenticação, endpoints disponíveis, e exemplos de requisições e respostas para a RESTful API. 

## **Visão geral da API**
A Vini Data API é uma API RESTful que foi desenvolvida para obter dados do site de vitivinicultura da Embrapa. É uma opção segura para extração dos dados do site para alimentação de modelos de Machine Learning. Por ter sido desenvolvida com o uso da biblioteca FastAPI, sua especificação e interface pode ser experimentada por meio do suíte *Swagger*.

<!-- #### Termos utilizados
… -->

## **RESTful API**

### **Endpoints**

Nossa API disponibiliza endpoints para algumas funcionalidades:

| ENDPOINTS | DESCRIÇÃO |
| --- | --- |
| **GET** /api/vitivinicultura/productions/{year}| Retorna a um conjunto de objetos (JSON) de Produção para um ano específico contendo produto, quantidade e tipo. O ano é um parâmetro obrigatório para a requisição ser bem sucedida.
| **GET** /api/vitivinicultura/processings/{year}| Retorna a um conjunto de objetos (JSON) de Processamento para um ano específico contendo produto, quantidade, tipo e classificação. O ano é um parâmetro obrigatório para a requisição ser bem sucedida.
| **GET** /api/vitivinicultura/commercializations/{year}| Retorna a um conjunto de objetos (JSON) de Comercialização para um ano específico contendo produto, quantidade e tipo. O ano é um parâmetro obrigatório para a requisição ser bem sucedida.
| **GET** /api/vitivinicultura/imports/{year}| Retorna a um conjunto de objetos (JSON) de Importação para um ano específico contendo país, quantidade, valor e classificação. O ano é um parâmetro obrigatório para a requisição ser bem sucedida.
| **GET** /api/vitivinicultura/exports/{year}| Retorna a um conjunto de objetos (JSON) de Exportação para um ano específico contendo país, quantidade, valor e classificação. O ano é um parâmetro obrigatório para a requisição ser bem sucedida.
| **POST** /api/auth/register| Cria um novo registro de usuário, senha
| **POST** /api/auth/jwt/login| Realiza o login e retorna o Bearer Token do usuario.
| **POST** /api/auth/logout| Realiza o logout

## RESTful API exemplos

Aqui estão alguns exemplos de interações possíveis de serem realizadas na interface da API:

#### Cria um novo registro de usuário 
##### Requisição (POST):
```curl
curl -X 'POST' \
  'https://vini-data-api.onrender.com/api/auth/register' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "email": "user@example.com",
  "password": "string",
  "is_active": true,
  "is_superuser": false,
  "is_verified": false
}'
```
##### Request URL

https://vini-data-api.onrender.com/api/auth/register

##### Response Body
```json
{
  "id": "xxxxx-xxxx-xxx-876d-729be7d4xxxx",
  "email": "user@example.com",
  "is_active": true,
  "is_superuser": false,
  "is_verified": false
}
```

#### Consulta os dados

Consulta os dados para o ano de 2020 na rota de Produção

##### Requisição (GET):

```curl
curl -X 'GET' \
  'https://vini-data-api.onrender.com/api/vitivinicultura/productions/2020' \
  -H 'accept: application/json' \
  -H 'Authorization: Bearer ***Token***'
```

##### Request URL

https://vini-data-api.onrender.com/api/vitivinicultura/productions/2020


##### Response Body

```json
{
  "productions": [
    {
      "product": "Tinto",
      "quantity": 146075996,
      "type": "VINHO DE MESA"
    },
    {
      "product": "Branco",
      "quantity": 26432799,
      "type": "VINHO DE MESA"
    },
    {
      "product": "Rosado",
      "quantity": 1391200,
      "type": "VINHO DE MESA"
    }
    ...] 
...
}

```

