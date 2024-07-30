
## Enderecos IP na AWS

- **EC2**: Sao fornecidos enderecos IPv4 ***publicos*** novos cada vez que uma instancia eh inicializada, a nao ser que seja especificado um elastic IP nessa instancia. Enquanto isso, um endereco IPv4 ***privado*** eh criado junto com a instancia e nao muda, mesmo que essa instancia seja reinicializada

***Enderecos IPv6 sao gratis na AWS***
## VPC(Virtual Private Cloud)

rede privada, separadas por regiao, que contem seus servicos em estado de deploy. Permite configurar subnets, a nivel de AZ, publicas ou privadas, ou seja, acessavel, ou nao, aa internet.

Configuracoes de acesso a internet e a outras subnets devem ser feitas atravez das **Route Tables**

* Permissao de acesso irrestrito aa rede pela internet eh feita por meio do "IGW(Internet Gateway)"
* Permissao de acesso restrito aa rede pela internet eh feita por meio do "NGW(NAT Gateway)", encriptando os dados com uma VPN

### Network ACL
**Subnet Level**
Lista utilizada para checar se o packet que sai ou entra em uma subnet tem permissao para realizar tal acao (Stateless)

### Security Groups
**Instance Level**
Validacao de permissoes a nivel de instancia, que configura o que pode ser enviado e recebido e em que porta realizar tal acao, para cada instancia na rede (Stateful)

### Flow Logs

Captura informacoes sobre trafego ip navegando suas interfaces, fazendo com que se comportem como se fossem uma so rede

### VPC Peering

Conecta duas VPCs utilizando a rede AWS, de forma privada

### Endpoints

Permite a conexao com servicos AWS utilizando a rede privada AWS

## PrivateLink

Permite a conexao com endpoints VPC de terceiros a partir de sua propria VPC, de forma segura e escalavel, sem necessitar de VPC peering, internet gateway, NAT ou route tables
## Direct Connect

Permite a criacao de uma conexao *Física* direta e privada de sua rede com uma VPC da AWS

## Site to Site VPN

Permite a conexao privada e emcriptada ***pela internet*** de sua rede privada e uma VPC da AWS

## Transit Gateway

Servico utilizado para criar conexoes peering transitivas entre milhares de VPCs e redes on-premises

## Networking Ports

- **22**: SSH & SFTP - Linux Shell & Secure Upload File
- **21**: FTP - Upload File
- **80**: HTTP - Unsecured website
- **443**: HTTPS - Secured website
- **3389**: RDP - Windows Shell

