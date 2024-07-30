
## Regions (Anki)

Uma Region eh um conjunto de 2 ou mais Availability Zones localizadas em um local especifico, onde cada AZ eh uma entidade separada, de forma que caso haja um desastre na localizacao dessa region, a probabilidade de todas as AZs dessa region eh minimizada, assim permitindo a continuacao do funcionamento dessa region

**Precos de recursos AWS variam de acordo com a region onde estao localizados, devido a custos de Impostos ou compliance especificos daquele local**

## Availability zones (Anki)

Conjuntos de 1 ou mais Data Centers com conexoes redundades e de baixa latencia, gerenciados e pertencentes aa AWS, onde sao localizados os recursos fisicos dos servicos disponibilizados pela plataforma

**Os data centers AWS estao em constante desenvolvimento, assim sendo, alguns recursos podem nao estar disponiveis para determinadas Regions**

## Edge Locations (Anki)

Servidores de Cache espalhados pelo globo, utilizados principalmente pelo CloudFront e Route 53 para entregar conteudo estatico para os usuarios da aplicacao com baixa latencia.