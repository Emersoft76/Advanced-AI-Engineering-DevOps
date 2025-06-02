# 🪟 Setup do Ambiente de Desenvolvimento no Windows

Este guia fornece um passo a passo para configurar um ambiente moderno de desenvolvimento no Windows, com foco em arquitetura de software, DevOps, CI/CD e desenvolvimento backend/frontend.

---

## 📦 Requisitos

| Ferramenta          | Versão recomendada | Link para download                  |
|---------------------|--------------------|-------------------------------------|
| Python              | 3.10+              | [python.org](https://www.python.org/downloads/windows/) |
| Node.js + npm       | 18+                | [nodejs.org](https://nodejs.org/en/download/) |
| Docker Desktop      | Latest             | [docker.com](https://www.docker.com/products/docker-desktop/) |
| Visual Studio Code  | Latest             | [code.visualstudio.com](https://code.visualstudio.com/) |
| Git for Windows     | Latest             | [git-scm.com](https://git-scm.com/download/win) |
| WSL2 + Ubuntu       | Ubuntu 22.04 LTS   | [Microsoft Docs](https://learn.microsoft.com/windows/wsl/) |

---

## 🛠️ Etapas de Instalação

### 1. Instale o **Python**
- Acesse o link acima e baixe o instalador.
- Marque a opção `Add Python to PATH`.
- Verifique:
```bash
python --version
pip --version
```

### 2. Instale o **Node.js + npm**
- Use o instalador oficial.
- Verifique:
```bash
node -v
npm -v
```

### 3. Instale o **Node.js + npm**
- Exige WSL2 habilitado.
- Após instalar, ative a integração com Ubuntu.
- Verifique:
```bash
docker --version
```

### 4. Habilite o **WSL2**
- No PowerShell (admin):
```powershell
wsl --install
```
- Reinicie e instale o Ubuntu via Microsoft Store.
- Verifique:
```bash
wsl --list --verbose
```

### 5. Instale o **Git para Windows**
- Inclua as ferramentas no terminal.
- Verifique:
```bash
git --version
```

### 6. Instale o **Visual Studio Code**
- Instale a extensão Remote - WSL.
- Recomendações:
   - Docker Extension
   - Python
   - ESLint
   - Prettier
 
 ---

## 🌐 Testando o Ambiente

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
```

2. Rode um projeto simples:
```bash
cd use_cases/simple_web_api
python app.py
```

3. Teste o Docker:
```bash
docker build -t teste-api .
docker run -p 5000:5000 teste-api
```

---

