# ☸️ Deploy com Kubernetes

Este guia mostra como fazer deploy de uma aplicação containerizada em um cluster Kubernetes local (Minikube) ou na nuvem (AKS – Azure Kubernetes Service).

---

## 📁 Estrutura

```bash
k8s/
├── deployment.yaml
├── service.yaml
```

---

## 📜 deployment.yaml
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: myapi-deployment
spec:
  replicas: 2
  selector:
    matchLabels:
      app: myapi
  template:
    metadata:
      labels:
        app: myapi
    spec:
      containers:
      - name: myapi
        image: acr-name.azurecr.io/myapi:latest
        ports:
        - containerPort: 5000
```

---

## 📜 service.yaml
```yaml
apiVersion: v1
kind: Service
metadata:
  name: myapi-service
spec:
  type: LoadBalancer
  selector:
    app: myapi
  ports:
    - protocol: TCP
      port: 80
      targetPort: 5000
```

---

## 🚀 Execução Local com Minikube
```yaml
minikube start
kubectl apply -f k8s/
kubectl get pods
minikube service myapi-service
```

---

## 🚀 Deploy no AKS (Azure Kubernetes Service)

1. Configure o contexto do cluster:
```bash
az aks get-credentials --resource-group <RG> --name <CLUSTER_NAME>
```

2. Aplique os manifests:
```bash
kubectl apply -f k8s/
```

---

## 🛠️ Verificação
```bash
kubectl get pods
kubectl get services
kubectl logs <pod-name>
```

---

🔗 Links úteis

- Documentação Kubernetes
- AKS – Azure Kubernetes Service
- kubectl Cheat Sheet

---

