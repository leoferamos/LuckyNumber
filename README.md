# Lucky Number Generator

Este projeto contém um arquivo YAML para criar um Job no Kubernetes que gera números da sorte.

## Descrição

O arquivo `job.yaml` define um Job no Kubernetes que executa um contêiner `busybox`. O contêiner executa um script que gera dois números aleatórios entre 1 e 70 e os imprime.

## Uso

Para usar este arquivo, aplique-o ao seu cluster Kubernetes com o comando:

```bash
kubectl apply -f job.yaml
