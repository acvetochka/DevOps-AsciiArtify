# MVP

1. Демонстрацію по встановленню ArgoCD можна знайти [тут](./argocd.md)

2. Після входу в систему `https://127.0.0.1:8080/` створюємо новий додаток.
- Натискаємо `+ NEW APP`
- Вводимо назву додатку    `demo`
- Синхронізація - `Manual`
- В параметрах синхронізації обираємо `AUTO-CREATE NAMESPACE`

![argo-create-app](/assets/argo-create-app.png)
- URL - `https://github.com/den-vasyliev/go-demo-app`
- PATH - `helm`

![argo-create-app](/assets/argo-create-app2.png)
- Обираємо кластер та вводимо namespace

![argo-create-app](/assets/argo-create-app3.png)

3. Синхронізація додатку

![argo-sync](/assets/argo-sync.png)

4. Переадресація портів

```
k port-forward -n demo svc/ambassador 8081:80
```

5. Вивід версії додатку (в іншому вікні терміналу)
```
curl localhost:8081
```

6. Завантаження зображення

```
wget -O <img-name> <img-url>
curl -F 'image=@<img-name>' localhost:8081/img/
```


## Demonstration

[Demo-video](https://asciinema.org/a/CToQGGgWD1g0m1IpIoxHOcpvS)

![argocd-demo](/assets/argocd-demo.gif)

- Docker

```
wget -O /tmp/docker.png https://static-00.iconduck.com/assets.00/docker-icon-512x370-5593ilur.png

```
```
curl -F 'image=@/tmp/docker.png' localhost:8081/img/
```

![docker](/assets/docker.png)

- Kubernetes

```
wget -O /tmp/kub.png https://static-00.iconduck.com/assets.00/kubernetes-icon-512x499-3mjeet3c.png

```
```
curl -F 'image=@/tmp/kub.png' localhost:8081/img/
```

![kubernetes](/assets/kubernetes.png)

- AWS

```
wget -O /tmp/aws.png https://static-00.iconduck.com/assets.00/aws-icon-512x306-hz71jncq.png
```
```
curl -F 'image=@/tmp/aws.png' localhost:8081/img/
```

![aws](/assets/aws.png)