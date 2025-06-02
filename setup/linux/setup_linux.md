# 🐧 Setup do Ambiente de Desenvolvimento no Linux

Este guia fornece as instruções para configurar um ambiente de desenvolvimento robusto e moderno no Linux, ideal para aplicações em Python, Node.js, DevOps, CI/CD e Cloud.

---

## 📦 Requisitos

| Ferramenta         | Comando de Instalação / Link                  |
|--------------------|-----------------------------------------------|
| Python 3.10+       | `sudo apt install python3 python3-pip`        |
| Node.js 18+        | Usar NodeSource ou nvm                        |
| Docker             | `sudo apt install docker.io` + `docker-compose` |
| Git                | `sudo apt install git`                        |
| Visual Studio Code | [VS Code .deb](https://code.visualstudio.com/) |
| Kubernetes (local) | `minikube` ou `kind`                          |

---

## 🛠️ Etapas de Instalação

### 1. Atualize o sistema
```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Python + pip
```bash
sudo apt install python3 python3-pip -y
python3 --version
pip3 --version
```

### 3. Node.js + npm
```bash
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs
node -v
npm -v
```

### 4. Docker + Docker Compose
```bash
sudo apt install docker.io docker-compose -y
sudo usermod -aG docker $USER
newgrp docker
docker --version
```

### 5. Git
```bash
sudo apt install git -y
git --version
```

### 6. Visual Studio Code
- Baixe o .deb no site oficial
- Instale com:
```bash
sudo dpkg -i code_*.deb
sudo apt install -f
```

---

## 🧰 Ferramentas adicionais recomendadas

- nvm – Gerenciador de versões Node.js
- pyenv – Gerenciador de versões Python
- virtualenv – Ambientes Python isolados
- Minikube ou Kind – Cluster Kubernetes local

---

## ✅ Teste do Ambiente

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
```
2. Rode um exemplo:
```bash
cd use_cases/simple_web_api
python3 app.py
```
3. Teste Docker:
```bash
docker build -t test-api .
docker run -p 5000:5000 test-api
```

---



