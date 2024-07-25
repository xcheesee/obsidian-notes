
## Organizations

Organizations permitem que seja consolidado o gerenciamento de multiplas contas AWS, com agregacao de custos, discontos sobre uso em volume, compartilhamento de recursos EC2 e restringir privilegios de contas utilizando Service Control Policies(SCP). Possui uma API que automatiza a criacao de contas.

## Service Control Policies(SCP)

- Whitelist ou blacklist de acoes IAM.
- Aplicado ao nivel Organizacional ou de Conta.
- Nao aplicavel aa conta Mestre.
- Aplicavel aa todos outros tipos de conta, inclusive root.
- não afeta contas service-linked.
- Nao permite acoes por default(Allow deve ser definido)

## Control Tower

Servico de configuracao e gerenciamento de ambientes AWS multi-account, de forma segura e seguindo compliance. Control Tower cria e organiza AWS Organizations, configura SCPs e CloudTrail para todas contas relacionadas e reforca a seguranca da organizacao como um todo.
Control Tower disponibiliza uma dashboard para controlar e configurar todos os servicos relacionados aa seguranca da organizacao

## Resource Access Manager(RAM)

Servico de compartilhamento de recursos AWS entre contas, onde voce pode disponibilizar um servico que possui a outra conta ou organizacao AWS


## Service Catalog

Portal onde servicos , que sao pre-aprovados por um admin da organizacao, podem ser acessados pelos demais usuarios da organizacao, eliminando assim a possibilidade de um usuario acessar recursos que nao fazem parte da logica de servico da organizacao. Service Catalog ofecere "Products" aos usuarios, que sao templates CloudFormation pre configurados por um admin.

## Compute Optimizer

Servico de analise de compute e reducao de custos, que analisa seus recursos de compute e recomenda acoes de provisionamento ou desativacao de recursos, baseados na utilizacao 

## Pricing Calculator

Servico de estimativa de custos de recursos AWS

## Billing Dashboard

Servico que disponibiliza o custo acumulado durante a data de billing atual, assim como previsao de custo restante baseado na utilizacao dos recursos, separado por recurso

### Free Tier

Disponibiliza a utilizacao restante de recursos no nivel gratis da aws

## Cost and Usage Report

Servico que disponibiliza todos os detalhes de custos e usos, assim como metadados, dos recursos aws utilizados ate o momento. esse recurso pode ser integrado com Athena, Redshift ou QuickSight

## Cost Explorer

Visualizacao de custos de recursos aws em formato timelapse, permite previsao de utilizacao e custo de recurso de ate 12 meses 

## Billing Alarm

Dados de cobranca eh localizado em CloudWatch em us-east-1, que possui dados de cobranca de todos servicos, mundialmente. Em CloudWatch pode ser configurado um alarme quando um limite estipulado for ultrapassado.

## AWS Budgets

Servico de criacao de alarmes quando um servico, ou sua previsao de custo, passa de um limite pre-configurado.
Existem 4 tipos de budgets: Uso, Custo, Reserva e Savings Plans, com o limite de ate 5 notificacoes SNS por budget.

## Cost Anomaly Detection

Utilizando ML, identifica e notifica gastos anomalos, baseados no historico de gastos de sua conta

## Service Quota

Servico que te notifica quando voce se aproxima do limite de cota de um servico contratado, e permite a solicitacao de mais cota, ou a finalizacao do recurso em questao

## Trusted Advisor

Serviço que audita sua conta e notifica você baseado em 6 criterios:
- Otimização de custos
- Performance
- Segurança - Free
- Tolerância a Falhas
- Limites de Serviços - Free
- Excelência Operacional

Todas Checagens de Trusted Advisor sao incluidas apenas nos planos Business e Enterprise, que tambem inclui acesso programatico ao Trusted Advisor

## Planos

- Basic: Free
	- Customer Service & Communities - 24/7 access to customer service, documentation, whitepapers and support forums
	- AWS Trusted Advisor: Core checks em Seguranca e Limite de Servicos
	- AWS Personal Health Dashboard
- Developer: 
	- Business hours email access to Cloud Support - 1 contato, com respostas entre  <24 horas ou <12 horas, dependendo da severidade
- Business:
	- AWS Trusted Advisor: Todos Checks + Acesso a API
	- Suporte 24/7 por telefone, email e chat com Cloud Support, com contatos ilimitados, com resposta de <4 horas e <1 hora, em casos extremos
	- Acesso ao Infrastructure Event Management, com custos adicionais\
- Enterprise On-Ramp:
	- Acesso a uma gama de Technical Account Managers(TAM)
	- Concierge Support Team(para custos e melhores praticas de sua conta)
	- Infrastructure Event Management, Well-Architected & Operations Reviews
	- Tempo de resposta do suporte de ate <30 mins, em casos extremos
- Enterprise:
	- Technical Account Manager(TAM) designado
	- Tempo de resposta do suporte de ate <15mins, em casos extremos

Todo plano mais premium recebe os beneficios dos planos anteriores