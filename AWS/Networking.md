## VPC(Virtual Private Cloud)

Provedor de rede privada, que permite configurar subnets publicas ou privadas, ou seja, com ou sem internet.

* Permissao de acesso irrestrito aa rede pela internet eh feita por meio do "IGW(Internet Gateway)"
* Permissao de acesso restrito aa rede pela internet eh feita por meio do "PGW(Virtual Private Gateway)", encriptando os dados com uma VPN

### Network ACL

Lista utilizada para checar se o packet que sai ou entra em uma subnet tem permissao para realizar tal acao

### Security Groups

Validacao de permissoes a nivel de instancia, que configura o que pode ser enviado e recebido e em que porta realizar tal acao, para cada instancia na rede

## Direct Connect

Permite a criacao de uma conexao direta e privada com os componentes de uma VPC

## Route 53

Servico de DNS da AWS, que eh capaz de redirecionar o trafego do usuario com base em metricas como:
* Latencia
* GeoLocation
* Geopriximity
* Round Robin

Com Route 53 o admin eh capaz de comprar e administrar Domain names


## Cloudfront

Servico de CDN da AWS, que utilizando de dados enviados pelo servidor aas suas edge location, eh capaz de apresentar recursos requisitados pelo usuario mais expeditamente


## Networking Ports

- **22**: SSH & SFTP - Linux Shell & Secure Upload File
- **21**: FTP - Upload File
- **80**: HTTP - Unsecured website
- **443**: HTTPS - Secured website
- **3389**: RDP - Windows Shell