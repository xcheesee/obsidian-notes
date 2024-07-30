
## Shared Responsability Model

![[sharedResp.jpg]]

A AWS opera em uma logica de "Responsabilidade Compartilhada", que determina a responsabilidade de seguranca atribuida a AWS: o hardware, data centers, edge locations, softwares de servicos serverless... e a responsabilidade de seguranca atribuida ao usuario:
Dados de usuario, controle de acesso a rede(EC2, VPC, RDS...) acesso aa conta de servico AWS, encriptacao de dados, autenticacao, configuracao... Ou seja, O usuario encarrega-se da seguranca **na** cloud e a AWS encarrega-se da seguranca **da** cloud.

DELIMITACAO DE RESPONSABILIDADE:

Usuario
- User Data
- Application
- Guest OS
-----------------------------------------
AWS
- Hypervisor
- Network
- Physical


## IAM(Identity and Access Management)

A criacao e configuracao de todos servicos AWS sao feitas por meio de calls de APIs. Quando um usuario ou um servico solicita acesso a outro servico, ocorre uma API request para o servico solicitado, mas antes da request atingir o servico ela eh autenticada pelo AWS IAM.

Servico que controla cadastro, edicao e permissao de usuarios. Um usuario criado, por padrao, nao possui nenhum acesso, acesso a qualquer ferramenta ou servico deve ser explicitamente autorizada, uma pratica chamada *least privilege principle*.

### Policy

O controle de permissoes eh feito por meio de um documento chamada ***IAM Policy*** , um documento JSON que descreve quais APIs um usuario pode ou nao acessar. Policies podem ser 
atribuidas a usuarios ou a grupos, que por sua vez seriam atribuidos a usuarios.

### Roles

Outra forma de definir permissoes eh por meio de ***Roles(cargos)*** , um cargo eh similar ao grupo, no sentido de que um cargo possui permissoes especificas de APIs, porem um cargo pode ser atribuido por um tempo limitado para um usuario e tambem eh a principal maneira de atribuir permissoes a servicos AWS, como EC2 ou Lambda.


### Access Analyzer
O servico Access Analyzer realiza uma varredura em seus recursos ativos na aws e cria um relatorio de todos perfis ou contas aws externas que possuem acesso a aquele recurso, alem da conta principal.

 ***Shared Responsability***: AWS cuida da seguranca ***da*** cloud, enquanto o usuario cuida da seguranca ***na*** cloud

## Artifact

Servico de compliance da AWS. Artifact disponibiliza documentos e acordos necessarios para verificacao de compliance, em todos servicos controlados pela AWS.

**A AWS responsabiliza-se pelo compliance da camada gerenciada por ela, ou seja, infraestrutura e dispositivos fisicos. O hosteamento de suas aplicacoes na AWS nao fazem delas compliant, o compliance das aplicacoes cabem ao usuario.**

## KMS

Servico de encriptacao de dados da AWS, que cria e gerencia chaves de encriptacao para entao serem utilizadas nos servicos aws, como EC2, S3, EBS..., por meio de integracoes de servico. Encripta tanto dados em repouso, quanto dados em transito

## CloudHSM

Servico de encriptacao que, ao contrario do KMS, apenas oferece o hardware para encriptacao, sendo assim, a encriptacao em si cabe ao usuario a realizar

## Inspector

Servico de analise de **seguranca** de servicos de compute(EC2, ECR, Lambda), que analisa toda sua infraestrutura aws e faz recomendacoes baseado nas ocorrencias achadas. Inspector pode tambem realizar acoes definidas pelo usuario baseado em uma ocorrencia achada, por meio do envio de ocorrencias para [[Monitoring#EventBridge|EventBridge]].

## Shield

Servico de protecao contra DDoS, que possui dois tiers

- **Standard**: Protecao para suas aplicacoes sem custo adicional
- **Advanced**: Protecao premium 24/7, com Assistencia prioritaria

## WAF

Filtra request na camada 7(HTTP), baseado em regras que protegem contra os ataques mais comuns de um recurso web, como SQL injection, HTTP Flood, DDoS

## Network Firewall

Servido de protecao da VPC que vai da camada 3 aa camada 7 e permite a analise de trafego da VPC em qualquer direcao

## Firewall Manager

Gerencia todas regras de seguranca em todas as contas de uma organizacao, como security groups, WAF, Network Firewall

## ACM(AWS Certificate Manager)

Servico de provisionamento de certificacao SSL/TLS para websites HTTPS em servicos AWS. Suporta tanto certificados privados(pago), quanto publicos(gratis) e fornece renovacao automatica de certificados.
Possue integracao com ELB, CloudFront e API Gateway

## Secrets Manager

Servico utilizado para guardar segredos, que permite definir rotacao de segredos apos uma certa quantidade de dias

## Guard Duty

Servico de descoberta e protecao contra ameacas. Utiliza de ML, deteccao de anomalias em servicos e dados de terceiros para descobrir ameacas.

Servicos analisados:
- CloudTrail
- VPC Flow Logs
- DNS Logs

Com Guard Duty voce pode tambem definir acoes a serem executadas em EventBridge, como desativacao do recurso, envio de notificacao e etc....

## Config

Auxilia na auditoria e compliance de seus recursos AWS, através do armazenamento de **configuracoes** e suas mudancas no tempo, que entao podem ser armazenados em uma S3. Config pode tambem, atraves da SNS, emitir alertas quando sua configuracao de infra for alterada

## Macie

Servico gerenciado de seguranca de dados e privacidade que utiliza de ML e Pattern Matching para descobrir e proteger dados sensiveis, atraves do envio de um evento para EventBridge quando alguma informacao de identificacao pessoal(PII) eh achada em, por exemplo, um bucket S3

## Security Hub

Ferramenta central de seguranca, utilizada para gerenciar a seguranca de multiplas contas AWS e automatizar checagem de seguranca, possui um dashboard integrado que mostra o status atual de seguranca e compliance de suas aplicacoes e permite a tomada de acoes diretamente desse dashboard

## Detective

Servico de seguranca que identifica, atraves da analise e investigacao automatica de uma falha, a causa raiz de um problema de seguranca ou atividade suspeita

## Abuse

Portal utilizado para reportar recursos AWS que estao sendo utilizados para praticar atos abusivos ou ilegais

## Root User

Acoes que somente o root user pode realizar na aws:
- **Alterar dados de conta**
- **Fechar conta**
- Restaurar permissoes IAM de um usuario
- visualizar cobrancas de taxas
- **Alterar ou cancelar o plano de suporte da AWS**
- **Registrar-se como vendedor no Reserved Instance Marketplace**
- Configurar MFA em uma bucket S3
- Cadastrar-se em GovCloud
- Editar ou Deleter bucket policy que inclue um VPC id invalido


## MFA

Autenticacao de usuario multifator IAM pode ser implementada de diversas maneiras na AWS.

### Security Keys

baseados no standard FIDO de seguranca, sao criadas a partir de um provedor certificado e permitem o acesso aas contar a partir de dispositivos hardware, fingerprint ou face, o que proporciona uma segurança ao mesmo tempo melhor e mais pratica que senhas.

## Virtual MFA Device

Aplicativos de celular previamente adicionados e configurados em sua conta AWS que disponibilizam, de forma segura, uma serie de numeros, aleatorios e rotacionais, que servem como uma camada a mais de seguranca alem de usuario e senha.

**Um aplicativo MFA permite a adicao de tokens de diversos servicos alem da AWS**

## Hardware MFA Device

Similiar ao Virtual MFA Device, disponibiliza uma serie de numeros aleatorios, porem os numeros sao disponibilizados atraves de um dispositivo fisico, configurado especificamente para mostrar OTPs(One Time Passwords) vinculados em sua conta AWS

**Dispositivos MFA devem ser adquiridos a partir da plataforma AWS, pois a AWS utiliza de "Token seeds" especificos para o funcionamento de seus OTPs**

**A AWS tambem disponibiliza Hardware MFA especificos para contas AWS GovCloud, devido a necessidades especificas de compliance, que sao disponibilizados atravez da companhia Hypersecu**