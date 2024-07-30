
## Elastic Block Store(EBS)

O armazenamento padrao de uma instancia EC2 esta atrelado fisicamente com essa instancia, assim quando eventualmente essa instancia eh finalizada, todas informacoes armazenadas nela tambem sao perdidas, para combater esse problema,utiliza-se da ferramenta EBS.

Servico de armazenamento de dados que permite a gravacao e permanencia de dados para instancias de EC2. Com a possibilidade de configuracao de tamanho e tipo, e realizacao de backups incrementais por meio de "snapshots"

## Simple Storage Service(S3)

Servico de armazenamento voltado para armazenar dados de diversos tipos e finalidades, com um tamanho virtualmente ilimitado, pode armazenar arquivos de ate 5tb de tamanho em unidades de armazenamento chamadas "buckets"

Tipos de Instancias S3:
* **Standard**: instancia voltada para armazenamento de uso geral, possui ***11 noves*** de durabilidade 
* **Static site hosting**: instancia voltada para utilizacao como um servidor de site statico, por meio do upload dos arquivos do site para a instancia
* **Infrequent Access**: Utilizada para arquivos que sao assessados infrequentemente, porem precisam ser recuperados a qualquer momento, de maneira rapida
* **Glacier Flexible Retrieval**: Utilizada para tipos de dados que necessitam ser armazenadas por um grande periodo de tempo e que nao necessitem de acesso rapido - Storage minimo: 90 dias
	* Expedited: 1 a 5 minutos para recuperacao dos dados
	* Standard: 3 a 5 horas para recuperacao dos dados
	* Bulk 5 a 12 horas para recuperacao dos dados(Gratis)
* **Glacier Instant Retieval**: Utilizada para tipos de dados que necessitam ser armazenadas por um grande periodo de tempo, mas necessitem de acesso rapido(Milisegundos) - Storage minimo: 90 dias
* **Glacier Deep Archive**: Para armazenamento de dados, normalmente de auditoria, que tem acesso ainda mais infrequente que outras instancias Glacier - Storage minimo: 180 dias
	* Standard: 12 horas
	* Bulk: 48 horas

S3 tambem possui politicas de transferencia, ou seja, eh possivel configurar a  migracao de um dado entre tipos de instancias s3 a partir de um periodo de tempo predefinido, por meio da plataforma ***S3 intelligent-tiering***, que incorre taxas de monitoramento e auto-tiering, porem nao possui taxa de recuperacao de dados no bucket.

- Possivel habilitar versionamento, onde arquivos alterados ou deletados ainda permanecem no bucket, porem com ids de versao diferentes

### Replication (CRR & SRR)

Servico de copias assincronas de buckets s3, tanto na mesma regiao(srr) ou em regioes diferentes(crr).

- Ambos buckets devem estar com versionamento habilitado
- Buckets podem estar em contas aws diferentes
- Copia ocorre assincronamente
- Devem estar com as devidas permissoes IAM

Casos de Uso:
- **CRR**: Compliance, acesso de baixa latencia, replicar dados entre contas
- **SRR**: Agregacao de logs, sincronizacao entre ambientes de producao e teste

### Access Logs

Servico S3 que mantem registro de requests, como tipo de request, qual recurso foi solicitado, data e hora, e etc.

## Elastic File System(EFS)

File system de Linux que pode ser acessada por multiplas instancias EC2 simultaneamente, que escala automaticamente

## Relational Database Service(RDS)

Serviço de banco de dados relacional administrado pela AWS, que suporta query com diversas linguagens.

Responsabilidade da AWS:
- provisionamento automatico
- patching de S.O.
- backups contínuos
- dashboard de monitoramento
- Criacao de replicas de leitura
***Nao ha possibilidade de conexao por via SSH em uma managed RDS***

**Tipos de deployment RDS**:
- Multi-region: Read-replicas em multiplas regioes
- Multi-AZ: Fail-over DB um uma AZ diferente que eh ativada casa haja problema no DB principal
- Read-replica: Replicas da DB para leitura, que proporcionam escalabilidade e melhor latencia de leitura
## Aurora

Serviço RDS proprietario da Amazon, que possui ferramentas de administracao que permitem a automatizacao de workloads do banco de dados.

Aurora possui uma performance de ate 5x maior que uma RDS convencional, pois eh optimizada para a nuvem

*Aurora tambem possui um servico serverless*

## Elasticache

Similar ao RDS, porem para DBs de cache(ex.:Redis), que sao DBs in-memory voltadas para servicos de leitura extensiva

## DynamoDB

Banco de Dados noSQL serverless. Por meio da criação de "tables" e armazenamento de itens nessas tables, eh possível armazenar uma quantidade virtualmente infinita de dados. O banco realiza por si só o dimensionamento e configuração das tables

### DynamoDB Accelerator(DAX)

Cache in-memory para DynamoDB, similar ao Elesticache, que oferece ate 10x de melhoria de performance comparado ao DynamoDB

### Global tables

Recurso do DynamoDB que proporciona replicacao multi-AZ de tabelas, com capacidade Active-Active(Read-Write) de dados nas DBs
## Redshift

Servico de data warehousing, utilizado para manter dados para fins analiticos, de tamanho ilimitado. Operam analises de dados historicos em ate 10x mais rapidamente que solucoes generalistas de armazenamento de dados, como RDS ou DynamoDB. Integrado com ferramentas de BI.

Reads em Redshift ocorrem de hora em hora, ao contrario de um DB convencional, que ocorrem por segundos

## Elastic MapReduce(EMR)

Servico que auxilia na criacao de clusters Hadoop para a analise e processamento de vastas quantidades de dados(Big Data), Esses cluster podem ser compostos de centenas de instancias EC2, atuando no provisionamento e configuracao desses clusters

## Athena

Servico serverless que realiza analise de objetos S3, utilizando linguagem SQL para realizar query dos arquivos. Athena eh integrado com ferramentas de report e dashboard AWS, como **Amazon [[Business Inteligence#Amazon QuickSight|QuickSight]]**

## DocumentDB

Assim como Existe implementacoes AWS de MySQL/PostgreSQL com RDS e Aurora, DocumentDB eh a alternativa em cloud de MongoDB

## Neptune

Servico de DB em grafo da AWS, recomendada para implementacao de redes sociais, grafos de conhecimento(Wikipedia), deteccao de fraude, engines de recomendacao e etc

## Timestream

Servico de DB para *Timeseries*(dataset que evolui conforme o tempo), com ferramentas de analise de timeseries integradas.

## QLDB(Quantum Ledger Database)

Servico AWS utilizado para revisar o historico de todas mudancas feitas nos dados de sua aplicacao  com o tempo, e assim, eh imutavel e protegido criptograficamente para a certificacao de tal imutabilidade

## Managed Blockchain

Servico AWS que permite que voce junte-se a uma blockchain publica, ou ate mesmo crie sua propria blockchain privada

## Glue

Servico ETL(Extract, Transform, Load) gerenciado da AWS, utilizado para preparar e transformar dados para analise e BI

## Database Migration Service(DMS)

Servico de Migracao de DB AWS, que permite migracao de DBs sem bloquear o acesso de tais 
## Snow
Recursos de hardware para coletar e processar dados em edge locations* ou migrar dados para dentro ou fora da AWS

*Snowball Edge*: Dispositivo(Hardware de armazenamento) utilizado para mover TBs ou PBs para dentro e fora da AWS
*Snowcone*: Dispositivo(Hardware de armazenamento) utilizado para mover ate 14TB de dados de forma rapida e segura
*Snowmobile*: **CAMINHAO** utilizado para mover milhares de PBs entre localizacoes, alternativa recomendada para transferencia de dados de mais de 10PBs

**Migracao de dados**:
- *Snowcone*
- *Snowball edge*
- *Snowmobile*
**Computacao Edge**:
- *Snowcone*
- *Snowball edge*

 \* Edge location se refere a uma localizacao que produz dados, mas pode nao ter, ou tem acesso limitado, aa internet e poder de computacao