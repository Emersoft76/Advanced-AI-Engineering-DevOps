# 📊 Dashboard com React

Este projeto demonstra um dashboard de frontend simples construído com React, ideal para consumir APIs, exibir dados e simular aplicações web reais.

---

## 🛠️ Tecnologias

- [React](https://react.dev/)
- [Vite](https://vitejs.dev/)
- [Axios](https://axios-http.com/)

---

## 📁 Estrutura

```bash
react_dashboard/
├── public/
├── src/
│   ├── App.jsx
│   ├── components/
│   │   └── Dashboard.jsx
│   └── main.jsx
├── index.html
├── package.json
└── vite.config.js
```

---

## ▶️ Instruções

1. Criação do projeto
```bash
npm create vite@latest react_dashboard --template react
cd react_dashboard
npm install
npm install axios
```

2. Código

src/components/Dashboard.jsx
```jsx
import React, { useEffect, useState } from 'react';
import axios from 'axios';

const Dashboard = () => {
  const [message, setMessage] = useState('');

  useEffect(() => {
    axios.get('http://localhost:5000/')
      .then(res => setMessage(res.data.message));
  }, []);

  return (
    <div>
      <h2>Status da API:</h2>
      <p>{message}</p>
    </div>
  );
};

export default Dashboard;
```

src/App.jsx
```jsx
import Dashboard from './components/Dashboard';

function App() {
  return (
    <div>
      <h1>React Dashboard</h1>
      <Dashboard />
    </div>
  );
}

export default App;
```

---

## 🚀 Execução
```bash
npm run dev
```
Acesse http://localhost:5173

---

## ✅ Conclusão
Este projeto React consome a API Flask criada anteriormente e serve como base para qualquer frontend que consome REST APIs.

---
