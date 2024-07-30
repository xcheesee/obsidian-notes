## CloudFormation

Servico AWS de orquestracao de recursos cloud, onde eh possivel configurar, de forma declarativa, infraestrutura cloud para ser executada automaticamente.

Recursos configurados dentro de uma CloudFormation stack possuem tags que permitem visualizar quanto aquela stack custara. Tambem eh possivel configurar execucao e delete automatico dos recursos com eventos, como algum horario especifico

### Application Composer

Servico de diagramacao de uma stack CloudFormation, onde eh possivel visualizar servicos em deploy e seus relacionamentos com outros servicos

## Cloud Development Kit(CDK)

SDK utilizado para definir infraestrutura cloud a partir de codigo, como Js, Java, .NET, etc.
Utilizado como alternativa ao CloudFormation caso nao seja desejavel utilizar o GUI da CloudFormation.

## BeanStalk

Paas(Platform as a Service) da AWS que fornece a habilidade de realizar o deploy de um aplicativo e configurar seus servicos concentrado em uma plataforma, focado nos use cases de um desenvolvedor.

Configuracoes de Instancia, OS, estrategia de deploy, provisionamento e load balacing sao automaticamente configuradas por BeanStalk.

Beanstalk tambem possui servico de monitoramento de saude, que informa suas metricas para CloudWatch

## CodeDeploy

Servico de deploy automatico hibrido, onde eh possivel realizar upgrade de aplicacoes tanto em cloud, quanto on-premises.

Servidores e instancias devem ser provisionadas e configuradas com o CodeDeploy Agent para terem acesso aa ferramenta

## CodeCommit

Servico de versionamento de codigo da AWS, similar ao Github, que fornece storage para codigo utilizando o modelo git de versionamento e comparacao de diffs

## CodeBuild

Servico de "Criacao de pkg" de codigo AWS, que compila, testa e produz um pacote pronto para ser implementado(deploy) seja na CodeDeploy ou outras ferramentas.

Tanto o codigo quanto o suite de testes devem ser especificados pelo usuario para CodeBuild realizar os jobs

## CodePipeline

Servico de orquestracao de codigo, que de forma pratica agrega as diferentes etapas do deploy(pipeline) em uma mesma plataforma. CodePipeline eh a base do desenvolvimento CI/CD

## Code Artifact

Servico de gerenciamento de artifacts, que sao pacotes de software que sao dependencias de outros pacotes de software. Trabalha com servicos de pacotes como NPM para armazenar pacotes de forma privada na nuvem

## CodeStar(descontinuado)

Servico que agrega e gerencia as atividades de desenvolvimento de software da AWS, pode ser utilizado para gerenciar CodeCommit, CodeBuild, CodePipeline, CodeDeploy, Elastic Beanstalk, EC2, etc....

Pode ser utilizado diretamente na nuvem, por meio do servico Cloud9

## Cloud9

cloud IDE da AWS, utilizado para escrever, executar e debugar codigo diretamente do navegador. Possui capacidade de colaboracao em tempo real(Pair Programming)

## Systems Manager(SSM)

Servico que auxilia na gestao em escala de aplicativos. 

features:
- automacao de patching
- rodar comandos em todos servidores simultaneamente
- armazenamento de parametros de configuracao
- Coleta de dados de aplicacoes, como apps, files, network config, system properties...
- Agregacao de dados operacionais

SSM eh compativel com Linux, Windows, MacOs e Raspberry Pi OS.
Eh necessario instalar o SSM agent nas maquinas a serem controladas.

Systems manager tambem permite a centralizacao de informacoes referentes a dados operacionais de multiplos servicos AWS, onde eh possivel criar grupos logicos de recursos, ou ambientes de desenvolvimento vs producao. Com esse recurso eh possivel analisar atividade recente de API, mudancas nas configuracoes de recursos, status de notificacoes, alertas e compliance de patches.

### Session Manager

permite conexao secure shell em suas maquinas SSM, sem a configuracao de ssh, keys, bastion hosts e sem precisar utilizar a port 22 da maquina

## Parameter Store

Servico de armazenamento de configuracoes e segredos, que pode armazenar dados como:
- API keys
- senhas
- configuracoes

parametros sao configuraveis com IAM, ou seja, cada parametro pode ser configurado para que apenas usuarios especificos podem visualiza-los
