# Orquestração de containers com Docker Swarm

## O que é orquestração?
Gerenciar e escalar containers.

Um serviço que rege sobre outros serviços, verificando o funcionamento, garantindo que a aplicação permaneça saudável e sempre disponível.

Serviços que resolvem esse problema:
- Docker Swarm
- Kubernetes
- Apache Mesos

***

## O que é Docker Swarm
É uma ferramenta para orquestrar containers. 

Funciona em forma de cluster e pode escalar projetos facilmente de forma horizontal.

A vantagem entre outros orquestradores é que seus comandos são muito semelhantes ao do próprio Docker.

***

## Conceitos do Docker Swarm
**Nodes:** máquina que está abaixo da gestão do Swarm.

**Manager node:** Node que gerencia os demais nodes.

**Worker node:** Nodes que trabalham para o manager.

**Service:** Conjunto de Tasks enviadas pelo Manager para que os Workers executem.

**Task:** Comandos executados nos Nodes.

***

## Recuperar token do manager
`docker swarm join-token manager`