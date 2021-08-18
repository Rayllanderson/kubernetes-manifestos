## Todos os Manifestos necessários pra rodar as aplicações do [Desafio Pix](https://github.com/zup-academy/orange-stack-documentacao/tree/master/desafio-01/01-key-manager#desafio-pix)

Uma alternativa (mais simples) para executar os serviços necessários do Desafio Pix de uma vez só!

### Executando

```bash

kubectl apply -f . # executando todos os manifestos dentro da pasta
  
```

### Verificando se tudo subiu certinho

```shell
  # leva um tempo até o deployment acontecer.
  # então é bom ficar de olho pra ver quando o deployment vai tá pronto
  kubectl get pods --watch # vai ficando ouvindo uma mudança nos pods acontecer

```

### Deletando 
```shell
  kubectl delete -f . # deleta todos os manifestos em execução da pasta
  
  kubectl delete -f nome-do-arquivo-yml # deleta um manifesto específico em execução
```

### Acessando

Aqui apenas o serviço REST é exposto externamente. O Serviço gRPC fica exposto apenas internamente, ou seja, não é possível acessar externamente com um client RPC.
O serviço REST fica dispoível externamente através de um NodePort. Disponível na porta `30003`.

Portando, para acessar o serviço Rest, basta acessar com um client HTTP na porta `30003`.
