[![Docker Pulls](https://badgen.net/docker/pulls/cauachagas/kube-news?icon=docker&label=pulls)](https://hub.docker.com/r/cauachagas/kube-news/)
[![Docker Image Size](https://badgen.net/docker/size/cauachagas/kube-news?icon=docker&label=image%20size)](https://hub.docker.com/r/cauachagas/kube-news/)

# kube-news

### Rodando com Kubernetes

Primeiro é preciso criar um cluster Kubernetes

```k3d cluster create meucluster -p "81:30000@loadbalancer"```

onde `meucluster` é o nome do cluster, onde a porta 81 da nossa máquina escuta a porta 30000 do cluster.

Depois é preciso navegar para src. Com o comando

`kubectl apply -f k8s/`

é criado a menor unidade Kubernetes, chamado de pod.

![](https://drive.google.com/uc?export=view&id=1Y2X2mwJ4a16YGpkYmAZ7_cl95x5Jorjy)

Para checar o Post no banco de dados pode ser feito `port-forward` do serviço `postgre` para acessar pela nossa porta 5432 a porta 5432 do pod

`kubectl port-forward service/postgre 5432:5432`

Configurando a conexão com o banco é possível acessar os dados

![](https://drive.google.com/uc?export=view&id=1ntLnvqq9RyMMw-HvRtfttGam8YvNt6-2)
