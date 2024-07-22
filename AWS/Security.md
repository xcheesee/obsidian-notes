
## IAM(Identity and Access Management)

Servico que controla cadastro, edicao e permissao de usuarios. Um usuario criado, por padrao, nao possui nenhum acesso, acesso a qualquer ferramenta ou servico deve ser explicitamente autorizada, uma pratica chamada *least privilege principle*.

### Policy

O controle de permissoes eh feito por meio de um documento chamada ***IAM Policy*** , um documento JSON que descreve quais APIs um usuario pode ou nao acessar. Policies podem ser 
atribuidas a usuarios ou a grupos, que por sua vez seriam atribuidos a usuarios.

### Roles

Outra forma de definir permissoes eh por meio de ***Roles(cargos)*** , um cargo eh similar ao grupo, no sentido de que um cargo possui permissoes especificas de APIs, porem um cargo pode ser atribuido por um tempo limitado para um usuario e tambem eh a principal maneira de atribuir permissoes a servicos AWS, como EC2 ou Lambda.


### Access Analyzer
O servico Access Analyzer realiza uma varredura em seus recursos ativos na aws e cria um relatorio de todos perfis ou contas aws que possuem acesso a aquele recurso, alem da conta principal.

 ***Shared Responsability***: AWS cuida da seguranca ***da*** cloud, enquanto o usuario cuida da seguranca ***na*** cloud

## Artifact

Servico de compliance da AWS. Artifact disponibiliza documentos e acordos necessarios para verificacao de compliance, em todos servicos controlados pela AWS

## KMS

Servico de encriptacao de dados da AWS, que encripta tanto dados em repouso, quanto dados em transito

## Inspector

Servico de analise de seguranca, que analisa toda sua infraestrutura aws e faz recomendacoes baseado nas ocorrencias achadas. Inspector pode tambem realizar acoes definidas pelo usuario baseado em uma ocorrencia achada.