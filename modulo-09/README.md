# Kubernetes

## O que é?
É uma ferramenta, criada pela Google, para orquestração de containers.

## Conceitos
- **Control Plane:** gestão do controles dos Nodes
- **Nodes:** máquinas sob a gestão de um Control Plane
- **Deployment:** execução de um projeto em um Pod
- **Pod:** containers que estão em um Node
- **Services:** serviços que expoem os Pods para acesso externo
- **kubectl:** cli do Kubernetes

***

## Minikube
Iniciar o minikube
```
minikube start --driver=DRIVER
```

Parar o minikube
```
minikube stop
```

Acessas dashboard do minikube
```
minikube dashboard
```

***

## Deployment
É a criação do serviço que rodará os Pods. 

A partir de uma imagem, diversos containers podem ser executados e replicados entre servidores. **O deployment não funciona a partir de uma imagem local.**

Criar deployment
```
kubectl create deployment NAME --image=IMAGE
```

Listar Deployments
```
kubectl get deployments
```

Listar detalhadamente Deployments
```
kubectl describe deployments
```

Listar Pods
```
kubectl get pods
```

Listar detalhadamente os Pods
```
kubectl describe pods
```

Verificar como o Kubernetes está confurado
```
kubectl config view
```

## Services
Criar um service
```
kubectl expose deployment NAME --type=TYPE --port=PORT
```

Detalhes de um service
```
minikube service NAME
```

Listar services
```
kubectl get services
```

Listar detalhes de um service
```
kubectl describe services/NAME
```

Escalar aplicação
```
kubectl scale deployment/NAME --replicas=REPLICAS
```

Verificar numero de replicas
```
kubectl get rs
```

Alterar imagem do deployment
```
kubectl set image deployment/<nome-deployment> <nome-container>=<nome-imagem>
```

Verificar o status de uma alteração
```
kubectl rollout status deployment/<nome-deployment>
```

Desfazer uma alteração
```
kubectl rollout undo deployment/<nome-deployment>
```

Deletar um service
```
kubectl delete service <service-name>
```

Deletar um deployment
```
kubectl delete deployment <deployment-name>
```

Disponibilizar service
```
minikube tunnel
```

***

## Modo declarativo
Toda a configuração é executada a partir de um arquivo que contém os comandos que devem ser executados.

### Chaves mais utilizadas
- **apiVersion:** versão da ferramenta
- **kind:** tipo do arquivo
- **metadata:** descrever algum objeto
- **replicas:** número de réplicas
- **containers:** especificações de containers

Criar deployment ou service a partir de arquivo
```
kubectl apply -f <path-yml-file>
```

Parar deployment ou service a partir de arquivo
```
kubectl delete -f <path-yml-file>
```


