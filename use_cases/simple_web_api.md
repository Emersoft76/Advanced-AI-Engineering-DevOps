# 🔹 API REST Simples com Python + Flask

Este projeto demonstra a criação de uma API RESTful simples usando Flask. É ideal para entender os fundamentos de criação de endpoints, estruturação de aplicações e integração com Docker.

---

## 🛠️ Tecnologias

- [Python](https://www.python.org/)
- [Flask](https://flask.palletsprojects.com/)
- [Docker](https://www.docker.com/)

---

## 📁 Estrutura de Arquivos

```bash
simple_web_api/
├── app.py
├── requirements.txt
└── Dockerfile
```

---

## 📜 Código Fonte
app.py
```python
from flask import Flask, jsonify, request

app = Flask(__name__)

@app.route('/')
def index():
    return jsonify({"message": "API Flask Online!"})

@app.route('/hello/<name>', methods=['GET'])
def hello(name):
    return jsonify({"message": f"Hello, {name}!"})

if __name__ == '__main__':
    app.run(debug=True, host='0.0.0.0')
```

requirements.txt
```ini
flask==2.2.5
```

---

## 🐳 Docker
Dockerfile
```dockerfile
FROM python:3.10-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . .

CMD ["python", "app.py"]
```
Comandos
```bash
docker build -t flask-api .
docker run -p 5000:5000 flask-api
```

---

## 🧪 Teste

- Acesse: http://localhost:5000/
- Teste: http://localhost:5000/hello/Dev

---

## ✅ Conclusão

- Este exemplo fornece um ponto de partida para APIs com Python, ideal para integração posterior com CI/CD e microsserviços.

---

