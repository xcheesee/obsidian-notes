## Lambda

Servico que permite que voce envie seu codigo fonte para uma "Lambda Function", uma ferramenta que permite que voce configurre um "trigger" e rode o codigo toda vez que esse trigger eh acionado

## ECS(Elastic Container Service)

Servico de Containers da AWS que provisiona e gerencia containers em sua maquina(EC2), com integracao ao [[Compute (Anki)#Elastic Load Balancing|Load Balancer]], porem toda configuracao dos contaners na instancia EC2 deve ser feita pelo usuario

## ECR(Elastic Container Registry)

Servico AWS que gerencia imagens docker privadas criadas pelo usuario, podendo ser utilizadas pelo ECS,EKS e Fargate

## Fargate

Plataforma serverless que permite a utilizacao de servicos de container(ECS*) e orquestracao(EKS**) de container que abstrai a configuracao do S.O, Servidor e orquestracao de containers


\*  Elastic Container Service
**  Elastic Kubernetes Service

## API Gateway

Servico de provisionamento de proxy(REST/WebSocket API) para servicos serverless de forma que um Client possa se comunicar com tais servicos.

Possui suporte para autenticacao de usuario, API Throttling, API Keys, monitoramento e seguranca.

## Batch

Servico de processamento batch(processos pontuais, que possuem inicio e fim definidos). Batch inicializa dinamicamente instancias EC2 e spot para a realização do batch job.

Batch Jobs são definidos por uma imagem Docker executada no ECS

## Lightsail

Serviço que provisiona servidores virtuais, com storage, database e networking. Alternativa simples e consolidada de: EC2, RDS, ELB, EBS, Route 53...
Nao implementa o conceito de escalabilidade e possui integração limitada com outros serviços AWS.