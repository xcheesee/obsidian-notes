### Metodologia != Framework
**Metodologia**: Fornece tudo que eh necessário para condução de um projeto. Mais completa que um framework, já que diz o que fazer, como fazer e possui etapas obrigatórias.
**Framework**: Um conjunto de regras. Eh um esqueleto que funciona como uma estrutura básica.
Apenas indica qual a trajetória, mas não indica exatamente como fazer, existindo a possibilidade de ser empregado juntamente com outros processos e técnicas.

### SCRUM
- Framework que ajuda pessoas, times e organizações a gerar valor através de soluções adaptativas.
- Reúne vários processos, técnicas e métodos.
- Baseado no empirismo, onde o conhecimento vem da experiencia e tomada de decisões com base no que eh observado.
- Baseado em LEAN, que reduz o desperdício e se concentra no que eh essencial

**Pilares do SCRUM**
1. **Transparência**: Informações devem ser claras e precisas para que todos tenham o mesmo entendimento
2. **Inspeção**: Time deve inspecionar constantemente os artefatos do SCRUM para detectar variações indesejadas
3. **Adaptação**: Se um inspetor determina que um ou mais aspectos de um processo desviou para fora dos limites aceitáveis, e que o resultado do produto será inaceitável, o processo ou o material sendo produzido deve ser ajustado

**Valores do SCRUM**
- Coragem
	- Fazer as coisa certas
	- Falar e ouvir opiniões diferentes
	- Compartilhar toda informação possível, a qual possa ajudar o time
- Comprometimento
	- Dedicação
	- Se aplica ao esforço, não ao resultado final
	- Priorizar qualidade, ao contrario de fazer todos os itens puxados na sprint
- Abertura
	- Aceitação, acessibilidade, receptividade, tolerância
	- Aprendizado, progresso, transparência e colaboração
- Foco
	- Focar no que eh importante
	- Time-box
	- Abordagem iterativa incremental
	- Simplicidade e objetividade
- Respeito
	- Aceitação dos pontos de vista
	- Correção de erros o mais rápido possível
	- Respeito pelas pessoas e suas experiencias profissionais e pessoais

### SCRUM Team
- Product Owner
	- Desenvolver e comunicar a meta do produto
	- Não eh chefe
	- Dono do backlog(cria, atualiza e prioriza os itens)
	- Estabelece a definicao de done
	- Representa a TI para o Sponsor
	- Representa o Sponsor para a TI
	- Escreve Historias de Usuário
- SCRUM Master
	- Guardiao das boas praticas scrum
	- Protege o time de interferencias externas
	- Promove o pensamento agil
	- Remove interferencias
	- Nao eh chefe
	- Remove impedimentos
	- Verifica metricas
	- Facilita a colaboracao dos stakeholders
- Time de Desenvolvimento
	- Diz como sera feito
	- Responsavel pela Execucao
	- Informam impedimentos
	- Estimas as historias de acordo com a complexidade
	- Devs, Tech Lead, QAs, UX, Designer

# Artefatos e Ritos

## DoR e DoD

- DoR(Definition of Ready)
	Definicao minima dos criterios necessarios para garantir que um item do backlog foi refinado e esta preparado para a sprint planning
	- Definido pelo time
	- Evita que os itens cheguem na planning com granularidade ruim, pouco ou nenhum detalhamento
	- Quando implementado, aumenta exponencialmente a probabilidade da historia ser concluida na sprint
- DoD(Definition of Done)
	o que a historia precisa ter para ser considerada finalizada
	Definida pelo Product Owner apos alinhamento com o time
	- Antes da conclusao de uma historia na sprint, o time faz um check conforme os criterios definidos para garantir que a historia esta no nivel que precisa para ser dada como concluida
	- Todo o time sabe exatamente o que significa um icremento do produto pronto
	- Transparencia e previsibilidade dos incrementos
	- Garante a qualidade na saida da sprint

DoR -> Sprint -> DoD

# Product Backlog
- Lista dinamica
- Funcionalidades, necessidades e desejos para o produto
- Ordenada por valor
- Apresentado por meio de User Stories

# User Stories
- Possui todas as caracteristicas, requisitos funcionais e prototipos de uma implementacao
- Exprime negocio e nao solucao

### Estrutura de uma User Storie
	Como <Tipo de Usuario>
	quero <Executar alguma tarefa>
	para que eu possa <Alcancar algum objetivo> 

# Refinamento
O time se reune para revisar as historias ja criadas que estao no backlog e tira qualquer duvida com o P.O

- 5 a 10% da sprint
- Detalhamento das historias
- Estimativas
- Valores e prioridades
- Colaboracao entre time e P.O
- Identificacao de pendencias e impedimentos
- Alinhamento com areas relacionadas



# Planning
O time se reune para revisar as historias que o P.O priorizou, definir estimativas das historias
- Planejamento de tudo que sera entregue durante a sprint
- ate 4h para sprints de 2 semanas
- Revisao das pendencias
- Colaboracao e negociacao entre o time
- Definicao das metas

### Ferramentas de estimativas

**Story Points**
- Utiliza a sequencia de  fibonacci para definir a complexidade de cada historia(1,2,3,5,8...)
- classificacao relativa, sem nenhuma relacao com espacos de tempo
- normalmenterealizadas atravez do planning poker

**T-Shirt Size**
- Utiliza os tamanhos mais comuns de camisetas(pp/p/m/g/gg)

### Sprint Backlog
	Lista de atividades do Product Backlog que serao entregues durante o sprint.

# Daily

O time se reune para alinha a evolucao da sprint e identificar possiveis impedimentos
- Movimentacao das tarefas no quadro
- Transparencia no andamento do sprint
- *Discussoes tecnicas no pos-daily*

# Review

O time se reune para avaliar se a meta da sprint foi atingida, apresentar o que foi feito durante a sprint e obter feedback do que foi entregue.

- Apresentacao das historias desenvolvidas em ambiente de testes
- O P.O discute/implementa o backlog do produto de acordo com o resultado da review

# Retrospectiva

O time fala sobre os pontos positivos e a melhorar sobre processo, ferramentas, pessoas e relacionamentos

- Inspeção dos pontos que ocorreram durante o sprint
- Inspeção de planos de ação combinados em sprints anteriores
- Planejamento de novos planos de ação