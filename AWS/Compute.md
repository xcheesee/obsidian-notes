## EC2

Servico de maquinas virtuais escalaveis e elasticas, com configuracao de hardware e alta disponibilidade

* Maquina Virtual gerenciada pela aws
* Pay-as-you-use
* Servidores on demand
* Paga somente por servidores ligados
* Existem multiplas maquinas ec2 em um host qualquer(Multitenancy)
* Pode configurar S.O, hardware e software instalado 
* Possivel reconfigurar hardware da instancia on demand
* Possivel configurar network da instancia

### Tipos de Instancias

**Cada Instancia pertence a um grupo de instancia, chamado familia**

Familias de instancias:
* General purpose - Recursos balanceados, utilizados para workloads diversos, como web servers
* Compute optimized - Recursos com foco a computacao intensiva, utilizados para workloads que necessitam alta taxa de processamento, como modelagem cientificas
* Memory optimized - recursos com foco a velocidade e gerenciamento de memoria
* Accelerated computing - similar ao compute optimized, porem utiliza de hardware acceleration para executar tarefas compativeis de modos mais eficiente, como processamento de graficos
* Storage optimized - recursos com foco de memoria nao volatil, utilizados para workloads que necessitam guardar e acessar dados armazenados localmente.

### Biling


* **On Demand**: Cobra o usuario pelo tempo em que usou a instancia.
* **Savings**: Cobra um valor abaixo do on demand, porem necessita que o usuario pague de forma adiantada pelo acesso aa maquina, de 1 a 3 anos.
* **Reserved Instance**: Similar ao Savings, com opcoes de pagamento imediato, metade imediato e nada imediato
	* **Standard**: o pagamento varia de acordo com a instancia a ser reservada, e nao eh possivel alterar-la apos o pagamento
	* **Convertible**: permite a reconfiguracao do hardware da instancia
* **Spot Instances**: Oferece um valor de ate 90% de desconto, em troca da compra de utilizacao de maquinas que se encontram ociosas. E a aws pode reinvidicar tais instancias a qualquer momento
* **Dedicated Host**: Normalmente utilizado por motivo de compliance, esta instancia reserva um host de forma integral, desta forma eliminando multitenancy no host

## Elastic Load Balancing

Servico que roteia requests de rede feita aas instancias EC2 de forma que todas elas recebam o mesmo workload

**Escalabilidade vs Elasticidade vs Agilidade**:

- Escalabilidade: Abilidade de acomodar uma demanda maior, seja por fazer o hardware mais potente(Escalar Verticalmente) ou aumentando a quantidade de nodes(Escalar Horizontalmente)
- Elasticidade: No momento em que um sistema eh escalavel, elasticidade se da pela habilidade de adaptar os nodes baseados na demanda atual
- Agilidade: Relacionado aa disponibilidade de recursos de TI, no sentido em que recursos estao disponiveis "on-demand".

### Tipos de Load Balancer

- Application(Http/Https/gRPC) - Layer 7
	 - Http Routing
	 - Static DNS
- Network(TCP/UDP) - Layer 4
	- High Performance
	- Static IP
- Gateway - Layer 3
	- GENEVE Protocol
	- Route Traffic to Firewalls
	- Intrusion detection
	- Deep Packet Inspection
- Classic(Legado desde 2023) - Layer 4 & 7

## ASG(Auto Scaling Group)

O ASG aumenta ou diminui o numero de instancias disponiveis baseado na demanda dos usuarios
- Possui configuracao de numero maximo e minimo de instancias disponiveis

## MarketPlace

Catalogo digital que disponibiliza milhares de softwares por vendors independentes(3rd party)


