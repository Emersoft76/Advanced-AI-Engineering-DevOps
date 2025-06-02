# ⚙️ CI/CD com GitHub Actions

O GitHub Actions é uma poderosa ferramenta nativa do GitHub para CI/CD, que permite automatizar testes, builds, deploys e muito mais através de pipelines baseados em YAML.

---

## 🚀 Exemplo Básico de Workflow

### 📄 `.github/workflows/main.yml`

```yaml
name: Node.js CI

on:
  push:
    branches: [main]

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - name: Checkout do código
      uses: actions/checkout@v3

    - name: Setup Node.js
      uses: actions/setup-node@v3
      with:
        node-version: 18

    - name: Instalação de dependências
      run: npm install

    - name: Execução dos testes
      run: npm test
```

---

## 🧠 Boas práticas

- Use secrets para armazenar senhas/tokens.
- Divida workflows em múltiplos arquivos (CI separado de CD).
- Inclua lint e coverage no pipeline.

---

## 🧪 Exemplo de Teste com Python
```yaml
name: Python CI

on: [push]

jobs:
  test:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v3

    - name: Setup Python
      uses: actions/setup-python@v4
      with:
        python-version: 3.10

    - name: Instalar dependências
      run: |
        python -m pip install --upgrade pip
        pip install -r requirements.txt

    - name: Rodar testes
      run: |
        pytest
```

---

🔗 Links úteis

- GitHub Actions Docs
- GitHub Marketplace

---
