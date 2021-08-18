# Manifestos necessários para rodar o Desafio Pix no Kubernates

## [Subindo o serviço gRPC](https://github.com/Rayllanderson/kubernetes-manifestos/tree/main/key-manager/key-manager-grpc)
  Instruções necessárias para executar o serviço gRPC, sendo exposto externamente com um NodePort.

## [Subindo o serviço REST](https://github.com/Rayllanderson/kubernetes-manifestos/tree/main/key-manager/key-manager-rest)
  Instruções necessárias para executar o serviço Rest sendo exposto externamente com um NodePort.

## [Subindo todos de uma vez só](https://github.com/Rayllanderson/kubernetes-manifestos/tree/main/key-manager/todos)
  Instruções pra subir todos os serviços necessários pra executar o Desafio Pix. 
  
  Aqui, apenas o serviço REST é exposto externamente. 
  O gRPC-server fica exposto somente para o Cluster (internamente)
