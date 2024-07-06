# Lucky Number Generator Job

## Descrição

Este projeto demonstra como criar um Job no Kubernetes que gera números aleatórios da sorte. O Job utiliza o contêiner `busybox` para executar um script simples que imprime dois números aleatórios no intervalo de 1 a 70.

## Tecnologias e Ferramentas

- **Kubernetes**: Plataforma para orquestração de contêineres, que facilita o gerenciamento, escalabilidade e implantação de aplicações em contêineres.
- **YAML**: Linguagem de serialização de dados usada para definir o Job no Kubernetes.
- **busybox**: Imagem de contêiner que fornece um ambiente de shell básico para executar scripts.

## Tópicos Abordados

- Criação e configuração de um Job no Kubernetes.
- Uso de comandos shell em contêineres.
- Como gerar números aleatórios usando o shell `sh`.
- Como gerenciar e monitorar Jobs no Kubernetes.

## Funcionalidade

Na vida real, este tipo de Job pode ser usado para tarefas simples que precisam ser executadas uma única vez, como geração de relatórios, processamento de dados em lote, ou outras operações que não precisam de execução contínua.

No mercado de trabalho, entender como criar e gerenciar Jobs no Kubernetes é útil para profissionais de DevOps, engenheiros de infraestrutura e desenvolvedores que trabalham com aplicações baseadas em contêineres. Esses conhecimentos são essenciais para a automação de tarefas e para o gerenciamento eficiente de processos em ambientes de produção.


## Descrição

O arquivo `job.yaml` define um Job no Kubernetes que executa um contêiner `busybox`. O contêiner executa um script que gera dois números aleatórios entre 1 e 70 e os imprime.

## Uso

Para usar este arquivo, aplique-o ao seu cluster Kubernetes com o comando:

```bash
kubectl apply -f job.yaml
```
## Verificar o Status do Job

Para verificar o status do Job e dos Pods criados, execute:
 ```bash
 kubectl get jobs
 kubectl get pods
```
## Obter os Números Aleatórios

Após a conclusão do Job, para visualizar a saída do Job, que inclui os números aleatórios gerados, use:

```bash
kubectl logs <nome-do-pod>
```
Substitua <nome-do-pod> pelo nome do Pod gerado pelo Job. O nome do Pod pode ser encontrado na lista de Pods com o comando `kubectl get pods`.

A saída deve ser semelhante a:

```bash
Starting script...
Lucky number 1 = <número>
Lucky number 2 = <número>
Script finished.
```


