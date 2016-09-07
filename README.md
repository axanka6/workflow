<a href="http://www.covalent.com.br/" target="_blank" title="Workflow">
    <img 
    	alt="Workflow of the Covalent.com.br"
    	src="http://covalent.com.br/images/logotipo/black.png" 
    	width="150px">
</a>

<br>

# Workflow

Em nosso workflow todo projeto é uma aplicação o que nos dá agilidade nos processos, 
somos guiados pelos testes, garantido qualidade de código com o minimo de burocracia 
possível.


### Ferramentas

- [Trello](https://trello.com/) 		`Controle de tarefas`
- [Slack](https://slack.com/) 			`Comunicação centralizada`
- [Vagrant](http://vagrantup.com/) 		`Ambiente e compartilhamento`
- [Bitbucket](https://bitbucket.com/) 	`Versionamento de código`
- [Codacy](https://codacy.com) 			`Review automatizado de código`
- [TDD](http://migre.me/umRFW) 			`Controle de qualidade do código`


<br>


# Trello

> Planejamento dos projetos.

Há 2 boards essenciais o board principal é o ´Pipeline´ onde cada card representa 
um projeto e pecorre as listas do Board. Desde o primeiro contato com o cliente 
em `Costumers`. Passa por `Proposal`, `Planning` até se tornar realmente um projeto 
na lista `project`.


## Pipeline

O card na lista `project` deve conter o titulo do projeto que deve ser apenas 
uma palavra e ter os membros responsáveis pelo projeto e a data do primeiro sprint 
além de um checklist que deve conter os passos desenvolvidos durante o `planning` e na 
sua descrição deve ter informações do cliente, telefone, email e a descrição
do projeto. 


## #project

O segundo board é onde as Tarefas definidas no `plannig` serão desenvolvidas pelo time. 
O board deve ter o titulo igual o do card em `project` precedido de uma *#* assim 
eles são agrupados no trello e tem uma correspondência direta com o canal no 
slack.


### Estrutura interna do board 

[Development Board Example](https://trello.com/b/JlUd28HU/development-board-example)

- Backlog 		`Tasks que serão entregues naquele sprint`
- Hold On		`Tasks que aguardam algum obstaculo para serem desenvolvidas`
- Developing	`Implementando as tasks`
- Review		`Code Review manual e automatizado`
- Production 	`Task já em produção`
- Master		`Tasks já incorporadas no branch master`


## Cards

O padrão de cards esta intrissicamente ligado a os
commits no repositório, temos uma filosofia "um card, 
um commit", porém no inicio do projeto há bastante 
atividades que não são ligadas a desenvolvimento. 
Esses cards devem seguir o mesmo padrão, toda atividade 
independente da area que pertence é uma task para o 
projeto, assim temos `Task`, `Refact`, `Issue`.


## Task

A maior partes das atividades são tasks, são criadas a partir 
do refinamento do backlog owner. O titulo deve ser a descrição 
da tarefa em uma linha precedida por `Task00: ` numeração não 
reflete necessariamente a priorização das Tasks. 


## Refact   

São Tasks que tem por objetivo uma mudança no material, 
sintaxe ou lógica mais que não altere os resultados da tarefa. 
O formato do titulo é o mesmo das `Tasks` mas precedido por 
`Refact00:`.


## Issue

Os issues são incidências de erros após a conclusão de uma Task, 
reportadas pelo cliente ou durante a revisão do código. O formato 
do titulo é o mesmo das anteriores só que precedidos por `Issue00:`, 
porém a numeração é atribuida de acordo com a Task que contêm os erros.


<br>


# Bitbucket

> Versionamento dos projetos.


## Repositórios

O titulo do projeto deve ter o mesmo nome do card em `project` 
de `pipeline` e possuir um README.md com as instruções para 
iniciar um projeto, ferramentas utilizadas, configurações de 
ambiente e links para documentação, downloads e etc. 


### Branchs

Cada funcionalidade, refact ou problema corrigido de ser entregue 
via pull request. Assim o branch deve ter o mesmo titulo do card 
no `Done`, porém sem a descrição. Todo projeto tem três branchs 
principais: Master, Production e Review. 



#### Review

Este é o branch submetido a o code review, garantindo que não haja código 
sem uso, repetido, complexo e fora de estilo. Apenas código com nota `A` 
irão para a produção. 


#### Master

Este branch é o branch responsável pelo código em produção da aplicação.



### Commits	

A mensagem deve seguir o seguinte formato sendo atribuido em cada parte as 
mesmas informações do card que deu origem aquele projeto.

<div>
	<h4>Tipo00: Titulo da task, issue ou refact</h4>

	<p>
		Uma descrição mais detalhada, se  necessaria. Quebra de linha<br>
		perto de 72 caracteres com uma linha vazia entre o titulo e a<br>
		descrição que devera descrever as alteração nos arquivos.
	</p>
	<p>
		Caso seja necessario separe cada paragrafo por uma linha vazia<br>
		para manter a organização das ideias.
	</p>
</div>

<br>
