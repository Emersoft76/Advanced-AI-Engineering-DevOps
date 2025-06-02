# 🔁 Fundamentos de DevOps e CI/CD

DevOps é a junção de práticas, ferramentas e cultura que integram desenvolvimento (Dev) e operações (Ops), promovendo entregas contínuas, confiáveis e rápidas.

---

## 🧩 Conceitos Essenciais

### 🔄 Integração Contínua (CI)
- Automatiza testes, builds e validação do código a cada commit.
- Detecta falhas mais cedo no ciclo de desenvolvimento.

### 🚀 Entrega Contínua (CD)
- Automatiza deploy para ambientes de staging/homologação.
- Pode incluir deploy em produção com gatilhos manuais.

### ⚙️ Deployment Contínuo (CD++)
- Extensão da entrega contínua com deploy automático em produção.

---

## 🛠️ Pipeline de CI/CD: Etapas Típicas

| Etapa             | Ação                                    |
|-------------------|------------------------------------------|
| Checkout          | Clonar o repositório                    |
| Build             | Compilar, instalar dependências          |
| Test              | Executar testes automatizados            |
| Lint              | Validar estilo e qualidade de código     |
| Package           | Gerar imagens Docker, artefatos          |
| Deploy            | Deploy automatizado com infraestrutura   |
| Monitoramento     | Verificar estado pós-deploy              |

---

## ⚒️ Ferramentas Comuns

| Categoria     | Ferramenta         |
|---------------|--------------------|
| CI/CD         | GitHub Actions, GitLab CI, Jenkins |
| Containers    | Docker, Podman      |
| Orquestração  | Kubernetes, Helm    |
| Cloud         | Azure, AWS, GCP     |
| Observability | Prometheus, Grafana |

---

## 📘 Padrões DevOps

- **Infraestrutura como Código (IaC)** – Terraform, Ansible
- **Segurança no pipeline (DevSecOps)**
- **Microserviços + CI/CD por serviço**
- **Monitoramento e feedback contínuo**

---

## 🧪 Exemplos no Repositório

- [Workflow com GitHub Actions](../ci_cd/github_actions.md)
- [Dockerfile prático](../ci_cd/docker_build.md)
- [Deploy Kubernetes + Azure](../ci_cd/kubernetes_deploy.md)

---

## 🔗 Referências

- [DevOps na Microsoft](https://learn.microsoft.com/devops/)
- [CI/CD com GitHub Actions](https://docs.github.com/actions)
- [Kelsey Hightower - Kubernetes the Hard Way](https://github.com/kelseyhightower/kubernetes-the-hard-way)
