## CloudWatch

Servico que disponibiliza metricas para todos servicos AWS, que permite a criacao de dashboards para consolidar diversas metricas em um grupo

### CloudWatch Events

Utilizado para filtrar e rotear eventos para recursos alvos especificados para seu processamento.

### CloudWatch Alarms

Utilizado para disparar alarmes e executar acoes quando uma metrica ultrapassa um limite especificado pelo usuario

** Alarmes de billing estao disponiveis somente na regiao us-east-1

### CloudWatch Logs

Servico utilizado para receber e armazenar logs, seja em instancias EC2, seja em maquinas on-premises, utilizando o agent cloudwatch

## EventBridge

Servico utilizado para realizar acoes de forma programada, seja em algum horario especifico(Cron job), baseado em alguma acao de um servico AWS, ou ate mesmo a partir eventos de servicos de Terceiros, como SaaS parceiros(integrado) e aplicativos de terceiros(necessita configuracao)

## CloudTrail

Servico de governanca, compliance e auditoria de sua conta AWS, que mantem um historico de eventos feitos em sua conta AWS, em especifico, Calls de APIs

## X-Ray


Servico de analise que fornece GUI com informacoes de todos servicos conectados de uma aplicacao, de forma isolada, para fins de troubleshooting

## CodeGuru

Servico baseado em ML que fornece code review automatizado e recomendacoes de performance

## Health Dashboard

Disponibiliza status de funcionamento de todos servicos atualmente em deploy, de todas regioes. Oferece tambem status de saude de sua conta aws e acontecimentos que possam impactar seus servicos.
Dados podem ser agregados em uma organizacao