
## Route 53

Servico de DNS gerenciado da AWS

### Policies

Route 53 disponibiliza politicas de distribuicao de trafego, que sao:
- Simple: Nao ha roteamento de trafego nem health checks
- Weighted: roteamento de trafego baseado em pesos de instancias previamente definidos
- Latency: roteamento de trafego baseado na localizacao no usuario, que redirecionara o usuario para a instancia mais proxima dele
- Failover: roteamento em caso de failover que redireciona o usuario para a instancia saudavel previamente configurada na queda da instancia principal

## CloudFront

Servico de CDN da AWS, que utiliza o conteudo de cache da pagina e leva-o para as localizacoes edge da Amazon. CloudFront oferece protecao DDoS, integracao com Shield e AWS Web Application Firewall