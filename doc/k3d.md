# Порядок розгортання Kubernetes кластера за допомогою k3d


## 1. Встановлення поточної версії k3d

- wget: 
```
wget -q -O - https://raw.githubusercontent.com/k3d-io/k3d/main/install.sh | bash
```

- curl:
```
curl -s https://raw.githubusercontent.com/k3d-io/k3d/main/install.sh | bash
```

## 2. Створення Kubernetes кластера з k3d

```
k3d cluster create <cluster-name>
```

## 3. Отримання інформації про кластер 

```
k3d cluster create <cluster-name>
```

Перевірка стану кластера

``` 
kubectl get nodes
```

## 4. Розгортання додатку

Варіант 1

```
kubectl create deployment <deployment-name> --image=<image-name>
```

Приклад
```
kubectl create deployment hello-world --image=gcr.io/google-samples/hello-app:1.0
```

Варіант 2 (за допомогою конфігураційного файлу)

```
touch deployment.yaml
```

```
nano deployment.yaml
```

``` yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: hello-world
spec:
  replicas: 1
  selector:
    matchLabels:
      app: hello-world
  template:
    metadata:
      labels:
        app: hello-world
    spec:
      containers:
      - name: hello-world
        image: gcr.io/google-samples/hello-app:1.0
        ports:
        - containerPort: 8080
```

```
kubectl apply -f deployment.yaml
```


## 5. Перевірка розгортання
```
kubectl get pods
```


