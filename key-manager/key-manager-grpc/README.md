## Como executar

O server gRPC depende disretamente dos microservices do Itaú e Banco central e o banco de dados. Por isso, deve-se executar eles primeiro para o funcionamento correto.

### Executando o Microservice do Banco Central
```shell
  cd .\bcb\ #entrando na pasta do Banco central. Se já estiver dentro dela, ignora.
  
  kubectl apply -f . # executando todos os arquivos 
```

### Executando o Microservice do Itaú
```shell
  cd .\erp-itau\ #entrando na pasta do erp itau. Se já estiver dentro dela, ignora.
  
  kubectl apply -f . # executando todos os arquivos de dentro da pasta
```

### Subindo o Postgres
```shell
  cd .\postgres\ #entrando na pasta do postgres. Se já estiver dentro dela, ignora.
  
  kubectl apply -f . # executando todos os arquivos de dentro da pasta
```

### Por fim, finalmente podemos subir o serviço gRPC
```shell
  cd .\grpc-server\ #entrando na pasta do grpc-server. Se já estiver dentro dela, ignora.
  
  kubectl apply -f . # executando todos os arquivos de dentro da pasta
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
