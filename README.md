# Deploy conversao-temperatura em kubernete
# Para acompanhar o build da imagem siga o link 
https://github.com/mauricionh01/conversao-temperatura.git
# Requisitos
* Kubctl
* K3d
* Docker
# Inicio do projeto
* Download conversao-temperatura
* https://github.com/mauricionh01/conversao-temperatura.git
* Criar a imagem conforme link 
# Iniciar o cluster
* Em meu projeto subi o cluster com 2 agents e 2 servers, mas dependendo do seu hardware pode ser criado com mais, tambem ja foi feito o bind da porta para acesso de qualquer maquina da rede
* k3d cluster create --agents 2 --servers 2 -p "80:30000@loadbalancer"
# Efetuar o deployment
kubectl apply -f deployment.yaml
