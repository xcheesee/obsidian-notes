
## Security Token Service(STS)

Servico que permite a criacao de credenciais de privilegios limitados, temporariamente(tempo determinado pelo usuario), para acessar seus recursos AWS.
STS eh utilizado para provisionar e validar IAM roles, tanto para contas, quanto para recursos(Ex.: EC2)

## Cognito

Servico que gerencia a identidade dos usuarios de sua aplicacao, que permite a criacao de contas e realizacao de logins com validacao pela AWS.

## Directory Services

Servico similar ao Microsoft Active Directory, que permite a utilizacao das credenciais de um usuario em qualquer maquina da rede para logar-se naquela maquina. Existem 3 tipos de Directory Services:
- Managed Microsoft AD: Criacao de AD na AWS, que cria uma ponte com a AD da Microsoft, assim permitindo o gerenciamento de usuarios tanto on-premises, quanto na nuvem
- AD Connector: Cria uma conexao(proxy) para a AD on-premises. Gerenciamento somente on-premises
- Simple AD: Managed Directory da AWS, que nao possui integracao com AD on-premises

## IAM Identity Center

Servico que habilita single sign-on para servicos como:
- Conta e Organizacao AWS
- Business cloud applications(Salesforce, Box, Microsoft 365...)
- Aplicacoes com integracao SAML2.0
- Instancias EC2 windows

Provisionamento de identidade pode ser gerenciada tanto pela AWS, quanto por servicos de terceiros, como: Active Directory, OneLogin, Okta...