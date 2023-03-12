# minikube for test
```bash
minikube start -p leaderelection --driver docker --container-runtime containerd 
```

```bash
docker build -t  templarfelix/leaderelection:latest -f ./scripts/docker/Dockerfile .
```

```bash
docker push templarfelix/leaderelection:latest
```

```bash
kubectl apply -f ./scripts/k8s/
```
