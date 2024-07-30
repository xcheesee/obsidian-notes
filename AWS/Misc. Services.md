
## WorkSpaces


Serviço de DaaS(Desktop as a Service) que provisiona desktops Windows e Linux virtuais, escalavel e com pay-as-you-go prices

## AppStream 2.0

Servico de Stream de desktop, que permite que qualquer computador tenha acesso a um aplicativo de um desktop diretamente do navegador, assim evitando a compra e o provisionamento de infraestrutura

## IoT Core

Servico que permite a conexao de dispositivos IoT para a cloud, agindo como um pub/sub que permite a comunicacao entre dispositivos IoT, e entre dispositivos e servicos AWS

## Elastic Transcoder

Servico que realiza transcode de midias armazenadas em buckets S3 para o formato suportado pelo usuario requisitante

## AppSync

Servico de sincronizacao de dados entre aplicativos mobile e web em tempo real, utilizando GraphQL. AppSync possui integracoes com DynamoDB e Lambda

## Amplify

Stack de servicos e ferramentas que auxiliam no deploy de aplicativos full stack web e mobile. Possui servicos de:
- Autenticacao
- Storage
- API
- CI/CD
- PubSub
- Analytics
- AI/ML predictions
- Monitoring
- Github e mais

## Application Composer

GUI que facilita no design e criacao de servicos serverless na AWS, que gera output IaC utilizando CloudFormation. Application Composer tambem permite importar templates CloudFormation para seu design ser visualizado a partir da GUI

## Device Farm

Servico que testa seus Apps em dispositivos reais Web, Mobile e ate mesmo tablets, de forma concorrente e permitindo a configuracao de tais ambientes para fins de teste

## Backup

Servico de gerenciamento e automacao de backups de servicos AWS, de forma centralizada.
Permite configuracao de PITR, Retention Periods, Lifecycle Management, Backup Policies.
Possivel realizar Backups Cross-Region ou Cross-Account

## Elastic Disaster Recovery(DRS)

Servico que permite a recuperacao de seus servidores fisicos, virtuais e em cloud de forma rapida e facil, através da replicacao em block-level continua de seus servers

## DataSync 

Permite mover grandes volumes de dados on-premises para a AWS, sendo sincronizado por:
- S3
- EFS
- FSx for Windows

## Application Discovery Service

Servico de planejamento de migracao de plataformas on-premises para a cloud, que realiza scans de utilizacao de servidores e mapeamento de dependencias para criar um relatorio detalhado de migracao, que estara disponivel dentro da AWS Migration Hub

## Application Migration Service

Servico de migracao de solucoes on-premises para a cloud AWS, que utiliza Lift-and-Shift para simplificar migracoes de aplicacoes

## Migration Evaluator

Servico que auxilia na criacao de uma data-driven business case para a migracao AWS, que analisa o estado atual e o estado alvo para a criacao de um plano de migracao

## Migration Hub

Localizacao central de informacoes do levantamento, planejamento e acompanhamento de migracoes AWS

### Migration Hub Orchestrator

Disponibiliza templates pre-arranjados para a migracao de apps on-premises


## Fault Injection Simulator

Servico que simula stress da aplicacao, como por exemplo aumento repentino da CPU, para fins de teste, descobrimento de bugs e bottlenecks

## Step Functions

Permite a montagem de um workflow visual para a criacao de funcoes lambda

## Ground Station

Servico de gerenciamento de satelites, que permite controlar comunicacao entre satelites, processar dados e escalar operacoes de satelites. Provisiona uma rede global de "Ground Stations" que permitem o rapido download de dados de satelites para suas instancias EC2 ou S3

## Pinpoint

Servico de gerenciamento de comunicacao de marketing(SMS, E-Mail, Push, voice, in-app messaging) que permite a customizacao de mensagens, baseado no consumidor que recebera tal mensagem

## Well-Architected Tool

Servico que revisa sua arquitetura cloud em relacao aos [[Conceitos (Anki)#6 Pilares do Well Architected Framework| 6 pilares]] do Well-Architected Framework e implementa best practices arquiteturais.
Como o servico funciona?:
- Selecione o workload
- responda questoes sobre os 6 pilares
- receba dicas(videos e documentacao) e revise os resultados na dashboard

## Carbon Footprint Tool

Servico que analisa, quantifica, revisa e preve a emissao de carbono dos servicos AWS utilizados por voce

## Cloud Adoption Framework(CAF)

Whitepaper que auxilia na montagem e executao de um plano para sua transformacao digital atraves do uso inovativo da AWS. Criado por profissionais AWS baseado em best practices e licoes apreendidas de milhares de consumidores.

AWS CAF identifica capacidades organizacionais especificas que sustentam uma transformacao cloud de sucesso. Essas capacidades sao separadas 2 grupos de 3 perspectivas:
Grupo Business
- Business
	Ajuda a confirmar que seus investimentos em cloud acelerem sua ambicao de transformacao digital e resultados da empresa
- People
	Serve como uma ponte entre tecnologia e empresa, acelerando a jornada cloud para ajudar organizacoes mais rapidamente evoluirem para uma cultura de melhoria constante
- Governance
	Ajuda na orquestracao de suas iniciativas cloud enquanto maximiza os beneficios organizacionais e minimiza os riscos da transformacao cloud
Grupo Tecnico
- Platform
	Ajuda na criacao de uma plataforma cloud hibrida escalavel e de nivel empresarial, na modernizacao de workloads existentes e na implementacao de solucoes cloud-native
- Security
	Ajuda a alcancar a confidencialidade, integridade e disponibilidade de seus dados e workloads cloud
- Operations
	Ajuda a certificar que seus servicos cloud estao sendo entregues em um nivel que supri as necessidades de sua organizacao

### Dominios de Transformacao

Existem 4 dominios de transformacao relacionados ao CAF, sao eles:
- Tecnologia:
	Utilizar a cloud para migrar e modernizar infraestrutura legado, aplicacoes, dados e plataformas de analise
- Process:
	Digitalizar dados e analises para criar actionable insights, utilizar ML para melhorar experiencia de SAC 
- Organizacao:
	Reorganizar seus times de acordo com produtos e value streams, utilizar conceitos agile para iterar e evoluir rapidamente
- Produto
	Reimaginar seu modelo de negocio por meio da criacao de novas propostas de valor e modelos de renda

### Fases de Transformacao

CAF possui 4 fases de transformacao, sao elas:
- **Envision**: Demonstre como a cloud ira acelerar os resultados de seu negocio por meio da identificacao oportunidades de transformacao e crie uma fundacao para sua transformacao digital
- **Align**: Analise das 6 perspectivas CAF para achar lacunas que serao tratadas pelo plano de acao
- **Launch**: Criacao e entrega de iniciativas em producao e demonstre o crescimento do valor de negocio
- **Scale**: Expansao das iniciativas para a escala desejada enquanto descobre os beneficios desejados no negocio


## IQ

Servico que ajuda a achar um profissional certificados para ajudar-lo em seus projetos AWS.
IQ provisiona Video-conferencing, Contract management, secure collaboration, integrated billing

## Re:Post

Forum de Q&A gerenciado pela AWS que oferece crowd-sourced, expert-reviwed answers para suas perguntas tecnicas sobre a AWS

## Knowledge Center

Central de FAQ do forum re:Post

## Managed Services(AMS)

Servico que prove suporte de infraestrutura e aplicacao na AWS, atraves de um time especializado, que lida com atividades comuns, como change requests, monitoring, patch management, sescurity, and backup services