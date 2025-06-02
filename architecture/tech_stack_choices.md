# 🧠 Decisões de Stack Tecnológica

Este documento detalha as tecnologias adotadas neste repositório, com justificativas técnicas e alinhamento às boas práticas de arquitetura, DevOps e desenvolvimento moderno.

---

## 📌 Critérios de Escolha

| Critério                   | Justificativa                                              |
|----------------------------|------------------------------------------------------------|
| Maturidade                 | Preferência por tecnologias consolidadas e bem documentadas |
| Comunidade                 | Forte suporte e base de usuários                           |
| Integração DevOps          | Suporte nativo a CI/CD e containers                        |
| Custo de Manutenção        | Simplicidade, curva de aprendizado moderada                |
| Suporte multiplataforma    | Linux e Windows                                            |

---

## 🧰 Tecnologias Selecionadas

### 🔹 **Backend**

| Tecnologia  | Motivo                                                             |
|-------------|--------------------------------------------------------------------|
| Python + Flask | Leve, simples e excelente para APIs rápidas e protótipos        |
| Node.js + Express | Alta performance para I/O, excelente para microsserviços     |

### 🔹 **Frontend**

| Tecnologia | Motivo                                           |
|------------|--------------------------------------------------|
| React + Vite | Rápido, modular, ecossistema maduro             |

### 🔹 **CI/CD**

| Ferramenta      | Motivo                                        |
|-----------------|-----------------------------------------------|
| GitHub Actions  | Integração nativa, simples e poderosa         |

### 🔹 **Infraestrutura**

| Ferramenta    | Motivo                                        |
|---------------|-----------------------------------------------|
| Docker        | Padronização, portabilidade                   |
| Kubernetes    | Orquestração de serviços escaláveis           |
| Azure AKS     | Infraestrutura gerenciada, escalável          |

---

## ⚙️ Alternativas Consideradas

| Categoria    | Escolhida         | Alternativas           | Observações                            |
|--------------|-------------------|-------------------------|----------------------------------------|
| Backend      | Flask / Express   | FastAPI, NestJS         | Optou-se por simplicidade + popularidade |
| CI/CD        | GitHub Actions    | GitLab CI, Jenkins      | GitHub já incluído e com marketplace forte |
| Orquestração | Kubernetes (AKS)  | ECS, Nomad              | K8s é padrão da indústria                |

---

## 🧭 Conclusão

As escolhas de stack refletem um equilíbrio entre robustez, simplicidade e aplicabilidade prática, priorizando o aprendizado estruturado e alinhado com as demandas reais do mercado.

---
