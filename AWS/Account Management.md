
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

Visualizacao de custos de recursos aws em formato timelapse