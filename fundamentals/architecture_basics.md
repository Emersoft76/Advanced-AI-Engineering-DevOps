# 🧱 Fundamentos de Arquitetura de Software

A arquitetura de software define a estrutura, os componentes e a comunicação entre partes de um sistema. Projetar uma boa arquitetura é essencial para garantir escalabilidade, manutenibilidade, segurança e performance.

---

## 🧠 Conceitos-Chave

### 🔹 1. Arquitetura Monolítica
- Toda a lógica em um único processo/aplicação.
- Simples de iniciar, difícil de escalar isoladamente.

### 🔹 2. Arquitetura em Camadas (Layered)
- Separação de responsabilidades:
  - Apresentação
  - Lógica de negócios
  - Persistência
  - Infraestrutura

### 🔹 3. Arquitetura baseada em Serviços
- **SOA**: Componentes independentes e reutilizáveis, mas ainda acoplados por contratos formais.
- **Microserviços**: Cada funcionalidade é um serviço independente, leve, com deploy separado.

### 🔹 4. Event-Driven Architecture (EDA)
- Comunicação por eventos.
- Escalável, assíncrona, altamente desacoplada.

### 🔹 5. Serverless
- Execução por demanda em cloud.
- Sem necessidade de gerenciar servidores.

---

## 🏗️ Componentes Arquiteturais

| Componente         | Função                                                  |
|--------------------|----------------------------------------------------------|
| API Gateway        | Entrada de chamadas, autenticação, roteamento            |
| Services           | Regras de negócio, funcionalidades do sistema            |
| Database Layer     | Persistência de dados, consultas                         |
| Message Broker     | Comunicação assíncrona entre serviços                    |
| Frontend           | Interface de usuário (React, Vue, etc.)                 |
| CI/CD Pipeline     | Automatiza build, testes, deploy                         |

---

## 🎯 Boas Práticas

- **Separação de responsabilidades** (SoC)
- **Alta coesão, baixo acoplamento**
- **Documentação arquitetural clara**
- **Segurança e escalabilidade desde o início**
- **Infraestrutura como código (IaC)**

---

## 📌 Exemplos no Repositório

| Exemplo                          | Abordagem Arquitetural           |
|----------------------------------|----------------------------------|
| [API Flask Simples](../use_cases/simple_web_api.md)         | Arquitetura Monolítica           |
| [Serviço Node.js + Docker](../use_cases/node_service.md)     | Microsserviço com Container      |
| [Pipeline CI/CD + K8s](../use_cases/full_pipeline.md)        | Arquitetura baseada em serviços  |

---

## 📘 Referências

- [The Twelve-Factor App](https://12factor.net/)
- [Microsoft Cloud Design Patterns](https://docs.microsoft.com/en-us/azure/architecture/patterns/)
- [Clean Architecture - Uncle Bob](https://8thlight.com/blog/uncle-bob/2012/08/13/the-clean-architecture.html)
