# Trello Workflow

> Fluxo de planejamento dos projetos.

Para cada projeto temos 2 boards importantes. O board principal é ´Pipeline´
onde cada cliente pecorre as listas deste boad passando por desenvolvimento 
de um projeto desde o `costumers`, `meeting`, `planning` até `project`.


## Pipelines

O card na lista `project` deve conter o titulo do projeto que deve ser apenas 
uma palavra e ter os membros responsáveis pelo projeto e a data de entrega além 
de um checklist que deve conter os passos desenvolvidos durante o `planning` e na 
sua descrição deve ter informações do cliente, telefone, numero, email e a descrição
do projeto. 


## @project

O segundo board é onde as Tasks definidas em `plannig` serão desenvolvidas. O
board deve ter o titulo igual o do card em `project` precedido de uma *@* assim 
eles são agrupados no trello e tem uma correspondência direta com o canal no 
slack.


### Estrutura interna do board 

- Backlog 		`Tasks que serão entregues naquele sprint`
- Icebox		`Tasks que aguardam algum obstaculo para serem desenvolvidas`
- Test Of		`Criando os testes para estas tasks`
- Developing	`Implementando as tasks`
- Review		`Code Review manual e automatizado [Codacy]`
- Done			`Taks finalizadas`


## Cards

A estrutura de cards esta intrissicamento ligado a os commits no repositório, temos uma filosofia "um card, um commit", porém no inicio do projeto há bastante atividades que não são ligadas a desenvolvimento. Esses cards devem seguir o mesmo padrão, toda atividade independente da area que pertence é uma task para o projeto, assim temos `Tasks`, `Refact`, `Issue`.


### Tasks

A maior partes das atividades são tasks criadas durante o `planning`. O titulo deve ser a descrição da tarefa em uma linha precedida por `Task00 - ` onde há a numeração da tarefa. 


### Refact   

São Tasks que tem por objetivo uma mudança no material, sintaxe ou logica mais que não altere os resultados da tarefa.


### Issue

Os issues são incidências de erros após a conclusão de uma Task, reportadas pelo cliente ou durante a revisão do código.

