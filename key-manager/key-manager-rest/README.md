## Como executar

O serviço REST depende do servidor gRPC pra funcionar. Portanto, não esqueça de subir o [gRPC-server](https://github.com/Rayllanderson/kubernetes-manifestos/tree/main/key-manager/key-manager-grpc).

Ou execute todos de uma vez [aqui](https://github.com/Rayllanderson/kubernetes-manifestos/tree/main/key-manager/todos) (mais fácil)

### Executando
```shell
  kubectl apply -f . # executando todos os arquivos da pasta
```

### Verificando se tudo subiu certinho
```shell
  kubectl get pods # vai listar os pods em execução. Também mostrará se ele está READY(1) ou NÃO(0)
  
  # se quiser ficar escutando uma mudança nos acontecer
  kubectl get pods --watch
```

### Deletando 
```shell
  kubectl delete -f . # deleta todos os manifestos em execução da pasta
  
  kubectl delete -f nome-do-arquivo-yml # deleta um manofesto específico em execução

```

### Acessando

O nosso serviço é exposto externamente, através de um NodePort. Disponível na porta `30003`.

Portando, para acessar o serviço Rest, basta acessar com um client HTTP na porta `30003`.
