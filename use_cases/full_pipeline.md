# 🔁 Pipeline CI/CD Completo com Docker, GitHub Actions, Kubernetes e Azure

Este projeto mostra um pipeline completo que inclui build Docker, testes automatizados, push para container registry e deploy em Kubernetes no Azure (AKS).

---

## 🛠️ Tecnologias

- GitHub Actions
- Docker
- Kubernetes (AKS)
- Azure Container Registry (ACR)
- Helm (opcional)

---

## 🧩 Fases do Pipeline

| Etapa       | Ação                                                  |
|-------------|--------------------------------------------------------|
| CI          | Build e Teste com Docker                               |
| CD          | Push para Azure Container Registry                     |
| Deploy      | Deploy com `kubectl` para AKS                          |
| Observação  | Monitoramento com `kubectl get pods` + `logs`         |

---

## 🔄 GitHub Actions: `.github/workflows/deploy.yml`

```yaml
name: CI/CD Pipeline

on:
  push:
    branches: [main]

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout
      uses: actions/checkout@v3

    - name: Login no Azure
      uses: azure/login@v1
      with:
        creds: ${{ secrets.AZURE_CREDENTIALS }}

    - name: Build Docker image
      run: |
        docker build -t myapi .
        docker tag myapi acr-name.azurecr.io/myapi:latest

    - name: Push para ACR
      run: |
        docker push acr-name.azurecr.io/myapi:latest

    - name: Deploy para AKS
      uses: azure/aks-set-context@v1
      with:
        creds: ${{ secrets.AZURE_CREDENTIALS }}
        cluster-name: my-aks-cluster
        resource-group: my-resource-group

    - name: Apply Manifest
      run: |
        kubectl apply -f k8s/deployment.yaml
```

---

## ✅ Conclusão

Este pipeline representa um ciclo completo de DevOps moderno, com CI/CD, containers, cloud e automação de infraestrutura.
