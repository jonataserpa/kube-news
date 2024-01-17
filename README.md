# Projeto kube-news Kubernetes

### Objetivo
O projeto Kube-news é uma aplicação escrita em NodeJS e tem como objetivo ser uma aplicação de exemplo pra trabalhar com o uso de containers.

### Configuração
Pra configurar a aplicação, é preciso ter um banco de dados Postgre e pra definir o acesso ao banco, configure as variáveis de ambiente abaixo:

DB_DATABASE => Nome do banco de dados que vai ser usado.
DB_USERNAME => Usuário do banco de dados.
DB_PASSWORD => Senha do usuário do banco de dados.
DB_HOST => Endereço do banco de dados.

### COMANDOS

- docker build -t kube-news -f Dockerfile .
- docker compose up -d --build

- k3d cluster create meucluster --servers 3 --agents 3 -p "9005:30000@loadbalancer"
- docker container ls
- kubectl apply -f k8s/deployment.yaml
- kubectl get all
- kubectl get po
- kubectl get deploy
- kubectl get replicaset
- kubectl logs number do pod
- kubectl get service
- kubectl delete pod name-do-pod
- kubectl get po
- kubectl port-forward service/kubenews 9005:80
- k3d cluster delete meucluster

- kubectl delete pod name-pod && watch 'kubectl get pod'
- docker build -t jonataserpa/kube-news:v2 --push .

### Services

Criação dos 2 services do Tipo ClientIP para expor o banco de dados na rede
e outro do tipo NodePort para expor a aplicação, 
no caso não usei o Loadbalancer pois é apenas em ambiente de CLoud

