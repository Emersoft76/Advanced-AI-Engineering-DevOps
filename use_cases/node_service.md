# ⚙️ Serviço com Node.js + Express

Este projeto mostra como construir um microserviço básico com Node.js e Express, ideal para APIs REST, middleware, validações e comunicação com bancos de dados.

---

## 🛠️ Tecnologias

- [Node.js](https://nodejs.org/)
- [Express.js](https://expressjs.com/)

---

## 📁 Estrutura

```bash
node_service/
├── index.js
├── package.json
└── Dockerfile
```

## 📜 Código
```js
index.js
const express = require('express');
const app = express();
const port = 3000;

app.get('/', (req, res) => {
  res.json({ message: 'Node Service Online!' });
});

app.get('/user/:name', (req, res) => {
  res.json({ user: req.params.name });
});

app.listen(port, () => {
  console.log(`Server running on http://localhost:${port}`);
});
```

package.json
```json
{
  "name": "node_service",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "start": "node index.js"
  },
  "dependencies": {
    "express": "^4.18.2"
  }
}
```

Dockerfile
```dockerfile
FROM node:18

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm install

COPY . .

CMD [ "npm", "start" ]
```

---

## 🚀 Execução
```bash
docker build -t node-service .
docker run -p 3000:3000 node-service
```

---

## ✅ Conclusão

Este microserviço é um exemplo básico de API com Node.js e pode ser integrado facilmente a sistemas maiores com pipelines e Kubernetes.

