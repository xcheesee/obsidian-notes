
## Route 53

Servico de DNS gerenciado da AWS

### Policies

Route 53 disponibiliza politicas de distribuicao de trafego, que sao:
- Simple: Nao ha roteamento de trafego nem health checks
- Weighted: roteamento de trafego baseado em pesos de instancias previamente definidos
- Latency: roteamento de trafego baseado na localizacao no usuario, que redirecionara o usuario para a instancia mais proxima dele
- Failover: roteamento em caso de failover que redireciona o usuario para a instancia saudavel previamente configurada na queda da instancia principal

eh capaz de redirecionar o trafego do usuario com base em metricas como:
* Latencia
* GeoLocation
* Geopriximity
* Round Robin

## CloudFront

Servico de CDN da AWS, que utiliza o conteudo de cache da pagina e leva-o para as localizacoes edge da Amazon. CloudFront oferece protecao DDoS, integracao com Shield e AWS Web Application Firewall

## S3 Transfer Acceleration

Servico de transferencia de dados, que aumenta a velocidade de transferencia por meio das CDN, que recebem os dados as serem transferidor e redirecionam para a Bucket alvo

## AWS Global Accelerator

Servico voltado para o aumento da performance e disponibilidade das suas aplicacoes, por meio da utilizacao da rede interna da AWS no roteamento de requests para aplicacoes

## Outposts

Solucao on-premises que oferece "Server racks" com a mesma infraestrutura, servicos e ferramentas que as da cloud AWS. Quando o servico eh solicitado, a AWS montara tais racks on-premise

## WaveLength

Servico que permite que recursos edge sejam disponibilizados em datacenters 5G, o que permite que dispositivos utilizando 5G recebam esses recursos mais rapidamente

## Local Zones

Servico que permite a extensao de uma vpc para mais locais em uma regiao, para que os recursos de sua aplicacao estejam mais perto do usuario final