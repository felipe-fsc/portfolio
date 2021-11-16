# <center>VEP - Visão Estratégica de Projetos</center>

## - Descrição do projeto
Desenvolver um software de visão estratégica de projetos, que permita ao gestor de uma equipe criar tarefas, definir prazos e metas, distribuir essas demandas para a equipe e analisar se as atividades estão sendo cumpridas dentro do prazo proposto.
### - Proposta comercial
O principal objetivo do projeto é desenvolver um sistema para a Visão Estratégica de Projetos, o sistema será desenvolvido para facilitar o planejamento de projetos de uma empresa.

## Índice

<!--ts-->
*  [Descrição do Projeto](#descricao-do-projeto)
*  [Tecnologias](#tecnologias)
*  [Contribuições Individuais](#contribuicoes-individuais)
*  [Aprendizados Efetivos](#aprendizados-efetivos)
<!--te-->

## - Tecnologias
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)<br>
As linguagens de Front End foram utilizadas para funcionar como a interface do sistema que foi desenvolvido. A mostra do diagrama e a aplicação do funcionamento de seus recursos foram apresentados em cima dessas ferramentas.<br>
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)<br>
Essa linguagem foi utilizada pois para fazer a conexão entre a interface e o banco de dados. Um dos requisitos do projeto era justamente permitir com que as informações preenchidas na interface do sistema fossem armazenadas em um BD.<br>
![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)<br>
A ferramenta de banco de dados em questão foi escolhida para armazenar as informações preenchidas nos formulários de CRUD do sistema criado.

## - Contribuições Individuais
- Banco de dados criado para armazenar as informações preenchidas nos CRUD's.
```
CREATE DATABASE gantt;
CREATE TABLE `gantt_links` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `source` int(11) NOT NULL,
  `target` int(11) NOT NULL,
  `type` varchar(1) NOT NULL,
  PRIMARY KEY (`id`)
);
CREATE TABLE `gantt_tasks` (
  `id` int NOT NULL AUTO_INCREMENT,
  `text` varchar(255) NOT NULL,
  `start_date` datetime NOT NULL,
  `duration` int NOT NULL,
  `progress` float NOT NULL,
  `parent` int NOT NULL,
  `sortorder` int NOT NULL,
  PRIMARY KEY (`id`)
);
```

- Função do NodeJS que retorna na interface do sistema todos os dados já cadastrados
```
app.get("/data", function (req, res) {
	Promise.all([
		db.query("SELECT * FROM gantt_tasks ORDER BY sortorder ASC"),
		db.query("SELECT * FROM gantt_links")
	]).then(function (results) {
		var tasks = results[0],
			links = results[1];

		for (var i = 0; i < tasks.length; i++) {
			tasks[i].start_date = tasks[i].start_date.format("YYYY-MM-DD hh:mm:ss");
			tasks[i].open = true;
		}

		res.send({
			data: tasks,
			collections: {links: links}
		});

	}).catch(function (error) {
		sendResponse(res, "error", null, error);
	});
});
```

- Função do Javascript criada para validar tentativa de login com um determinado preenchimento de usuário e senha 
```
<script type="text/javascript">
	function validar(){
		if ($("#usuario").val().toUpperCase()!= "ADMIN" || $("#senha").val()!= "megadev2020") {
			return alert("Usuário ou Senha invalido");
		}
		window.location.href="index.html";

	}
	$("#usuario, #senha").keypress(function(event){
		if (event.keyCode == 13) {
			validar()
		}
	})
</script>
```

## - Aprendizados Efetivos
### Padrões de projeto
Aprender sobre design patterns foi fundamental para não termos que enfrentar problemas recorrentes que ocorrem durante o desenvolvimento de um software. Com esse tipo de informação em mãos, sempre que esbarramos em um desses problemas, conseguimos resolver rápido por ter uma lista de soluções baseadas em boas práticas utilizadas comumente pela comunidade de desenvolvedores.
### Framework
As frameworks foram uma grande descoberta para nossa equipe durante esse projeto, pois tivemos uma base de saída para começar o desenvolvimento, ao invés de trabalhar todo o projeto do zero. Esse ponto de partida nos permitiu adiantar várias etapas e entregar um resultado final de maior qualidade, além de conseguir apresentar mais recursos graças ao tempo que foi ganho.
### Reunião de retrospectiva
Aprendemos e aplicamos mais este recurso da metodologia Scrum, para realizar um projeto com melhorias constantes durante sua execução, para melhor harmonia entre seus integrantes e para identificar acertos e erros das etapas anteriores.
### Avaliação de soft skills
Organizamos o grupo para nos avaliarmos referente a conduta geral dos integrantes durante o projeto e a colaboração de todos dentro do cenário de comunicação, organização e trabalho em equipe, afinal de contas, um projeto não sobrevive apenas da capacidade técnica de seus desenvolvedores.
