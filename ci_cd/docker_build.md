# 🐳 Construindo Imagens Docker com Boas Práticas

O Docker permite empacotar uma aplicação com todas as suas dependências em containers reutilizáveis e portáveis.

---

## 📦 Estrutura de Imagem

### 🧱 Exemplo básico – Python App

```Dockerfile
FROM python:3.10-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . .

CMD ["python", "app.py"]
```

---

## ✅ Boas Práticas

| Prática            | Descrição                                           |
| ------------------ | --------------------------------------------------- |
| Imagens pequenas   | Use Alpine ou slim para reduzir o tamanho da imagem |
| Multi-stage builds | Separe build e runtime em stages diferentes         |
| Caching eficiente  | Coloque `COPY requirements.txt` antes do `COPY .`   |
| Healthchecks       | Use `HEALTHCHECK` para containers críticos          |
| Usuário não-root   | Utilize `USER appuser` em produção                  |
| Tags controladas   | Evite `:latest` em produção                         |

---

## 🔄 Multi-Stage Example
```Dockerfile
FROM node:18 AS builder
WORKDIR /app
COPY . .
RUN npm ci && npm run build

FROM nginx:alpine
COPY --from=builder /app/dist /usr/share/nginx/html
```

---

📜 Comandos Docker
```bash
docker build -t myapp .
docker run -d -p 8080:80 myapp
docker push <usuario>/myapp:tag
```

---

## 🔗 Recursos

- Dockerfile Best Practices
- Dive – Analyzer de imagens Docker

---
