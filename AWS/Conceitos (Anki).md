
## 7 "R"s da Estrategia de Migracao (Anki)


- Retire: Desligue servicos nao utilizados
- Retain: Manter servicos on-premises(Compliance, Performance, Dependencies)
- Relocate : Mover servicos on-premises para alternativas cloud
- Rehosting: Migracoes de host para a cloud(Databases, applications, data)
- Replatforming: Migracao de solucoes para alternativas cloud
	- Database to RDS
	- Application to Elastic BeanStalk
- Repurchasing: Mudar para um produto cloud durante a migracao, para, por exemplo, uma aplicacao SaaS
- Refactor: Rearquitetar a aplicacao para aproveitar os beneficios do cloud

## Well Architected Framework Guiding Principles (Anki)

- Nao advinhe sua capacidade necessaria, utilize auto-scaling
- Teste seus sistemas em escala de producao
- Automatize para facilitar experimentacao de arquitetura(Ex.: CloudFormation Templates)
- Desenhe arquitetura que permita mudancas de requerimentos
- Desenhe arquitetura baseado em dados

## Principios de Design AWS Cloud (Anki)

- Escalabilidade
- Recursos descartaveis(Servers devem ter configuração simples e serem descartáveis)
- Automacao
- Loose Coupling
- Servicos no lugar de Servers

## 6 Pilares do Well Architected Framework (Anki)

- Operational Excellence
	Executar e monitorar sistemas para entregar valor de mercado e realizar melhora continua dos processos e procedimentos
	- Operations as Code
	- Frequent, small, reversible changes
	- Refine operations procedures
	- Anticipate failure
	- Learn from failure
	- Use Managed Services
	- Implement observability
- Security
	Proteja dados e sistemas enquanto entrega valor de mercado atraves de levantamento de risco e estrategias de mitigacao
	- Implemente uma estrategia de identidade
	- enable traceability
	- Apply security at all layers
	- Automate security best practices
	- Protect data in transit and at rest
	- keep people away from data\
	- prepare for security events
- Reliability
	Habilidade de um sistema de recuperar-se de problemas de infraestrutura ou servicos, adquirir recursos automaticamente para cumprir com demanda e mitigar falhas como erros de configuracao ou networking
	- Test recovery procedures
	- Automatically recover from failure
	- Scale horizontally
	- Stop guessing capacity
	- Manage change in automation
- Performance Efficiency
	Habilidade de utilizar recursos de computacao eficientemente e manter essa eficiencia conforme a demanda aumenta e a tecnologia evolui
	- Democratizar tecnologias avancadas
	- Go global in minutes
	- Use serverless infrastructure
	- Experiment more often
	- Mechanical sympathy
- Cost Optimization
	A Habilidade de executar sistemas para entregar valor pelo menor preco possivel
	- Adopt a consumption mode
	- Measure overall efficiency
	- Stop spending money on data center operations
	- Analyze and attribute expenditure
	- Use managed and application level services to reduce cost of ownership
- Sustainability
	Minimizar o impacto ambiental de workloads em cloud
	- Understand your impact
	- Establish sustainability goals
	- Maximize utilization
	- Anticipate and adopt new, more efficient hardware and software offerings
	- Use managed services
	- Reduce your downstream impact of your cloud workloads