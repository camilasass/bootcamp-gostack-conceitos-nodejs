# bootcamp-gostack-conceitos-nodejs
Desafio sobre conceitos do Node.js aplicado no Bootcamp Go Stack da RocketSeat

## Como executar
- Primeiro clone o repositório na sua máquina (o exemplo abaixo usa SSH)
```
git clone git@github.com:camilasass/bootcamp-gostack-conceitos-nodejs.git
```

- Para executar:
```
yarn install
```

## Rotas
- `[POST] /repositories`: cria um repositório
- `[GET] /repositories`: lista os repositórios
- `[PUT] /repositories/:id`: atualiza o repositório com id passado na url
- `[DELETE] /repositories/:id`: deleta o repositório com id passado na url
- `[POST] /repositories/:id/like`: adiciona um like no repositório com id passado na url

## Exemplos

### POST /repositories

Requisição
```javascript
// POST /repositories
{
  "title": "Conceitos Node.js",
  "url": "https://github.com/camilasass/bootcamp-gostack-conceitos-nodejs",
  "techs": ["Node.js"]
}
```

Resposta
```javascript
{
  "id": "b5ee62d6-c359-4d33-aa11-f8b6882f53d4",
  "title": "Conceitos Node.js",
  "url": "https://github.com/camilasass/bootcamp-gostack-conceitos-nodejs",
  "techs": [
    "Node.js"
  ],
  "likes": 0
}
```


### GET /repositories

Requisição
```javascript
GET /repositories
```

Resposta
```javascript
[
  {
    "id": "b5ee62d6-c359-4d33-aa11-f8b6882f53d4",
    "title": "Conceitos Node.js",
    "url": "https://github.com/camilasass/bootcamp-gostack-conceitos-nodejs",
    "techs": [
      "Node.js"
    ],
    "likes": 0
  }
]
```


### PUT /repositories/:id

Requisição
```javascript
// PUT /repositories/b5ee62d6-c359-4d33-aa11-f8b6882f53d4
{
  "title": "Conceitos Node.js",
  "url": "https://github.com/camilasass/bootcamp-gostack-conceitos-nodejs",
  "techs": ["Node.js", "JavaScript"]
}
```

Resposta
```javascript
{
  "id": "b5ee62d6-c359-4d33-aa11-f8b6882f53d4",
  "title": "Conceitos Node.js",
  "url": "https://github.com/camilasass/bootcamp-gostack-conceitos-nodejs",
  "techs": [
    "Node.js",
    "JavaScript"
  ],
  "likes": 0
}
```

### DELETE /repositories/:id

Requisição
```javascript
DELETE /repositories/b5ee62d6-c359-4d33-aa11-f8b6882f53d4
```

Resposta
```javascript
// status 204
// No content
```

### POST /repositories/:id/like

Requisição
```javascript
POST /repositories/b5ee62d6-c359-4d33-aa11-f8b6882f53d4/like
```

Resposta
```javascript
{
  "id": "b5ee62d6-c359-4d33-aa11-f8b6882f53d4",
  "title": "Conceitos Node.js",
  "url": "https://github.com/camilasass/bootcamp-gostack-conceitos-nodejs",
  "techs": [
    "Node.js"
  ],
  "likes": 1
}
```
