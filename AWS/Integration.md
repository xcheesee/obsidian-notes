## SQS(Simple Queue Service)
Envia, Armazena e recebe mensagens entre componentes de software. Uma mensagem enviada ao SQS fica armazenada ate ser processada

## SNS(Simple Notification Service)
Servico pub/sub, que, Assim como SQS, envia mensagens entre componentes, mas tambem consegue enviar notificacoes para os usuarios finais da aplicacao

## Kineses

Servico  que coleta, processa e analisa dados real-time em escala.

- Kineses data stream: disponibiliza streaming low-latency para receber dados que milhares de fontes
- Kineses data firehose: carrega dados para S3, Redshift, Elasticsearch, etc....
- Kineses data analytics: realiza analise em tempo read em streams utilizando SQL
- Kineses video Streams: Monitora video streams em tempo real para analise ou ML

## MQ

Servico gerenciado de messaging que, ao contrario de SQS e SNS, que sao proprietarios, utiliza "open protocols"(MQTT,AMQP,STOMP) para realizar envio/recebimento de mensagens com rabbitMQ ou activeMQ