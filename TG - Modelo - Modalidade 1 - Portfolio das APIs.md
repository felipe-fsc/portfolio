# Felipe Santos Carvalho

## Olá, meu nome é Felipe

Sou desenvolvedor fullstack e estudante do curso tecnólogo em Banco de Dados. Estas são as minhas experiências na Fatec de São José dos Campos.

## Meus Projetos

### Em 2019-2 trabalhei no desenvolvimento do projeto Operação Lava Bot, desenvolvido para a Fatec de São José dos Campos
##### Descrição do projeto
Desenvolver um web bot que faça uma raspagem de dados em um site, coletando dados referentes as despesas gastas por políticos de cargo eletivo, coletando informações que serão arquivadas, onde as mesmas serão desmembradas em quanto cada tipo de despesa consumiu do valor pago em impostos pelo contribuinte.
##### Proposta comercial
O objetivo do projeto é que um grupo de alunos desenvolva uma aplicação em que seja utilizado um WebBot desenvolvido pelo grupo, usando o na solução de um problema proposto pelo grupo.

[GIT](https://gitlab.com/operacao-lava-bot/operacao-lava-bot)

#### Tecnologias Utilizadas
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
Utilizei essa linguagem pela sua simplicidade, como esse é um projeto de 1° semestre, meu nível técnico ainda era de um programador iniciante, com algumas noções de lógica e sem muitas aplicações práticas como desenvolvedor.
Fazer um projeto em Python funcionou muito bem, pois além da simplicidade, pude fazer bom uso das bibliotecas que integram com essa linguagem, o que me permitiu trazer bons recursos para o bot que foi desenvolvido.

![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
O Pandas foi um recurso fundamental para o que pude fazer depois da etapa de extração de dados. Como a informação captada foi retornada como um arquivo .csv, minha equipe decidiu criar uma interface no Excel para retornar esses dados de forma organizada e o Pandas foi uma biblioteca que serviu muito bem com os recursos fornecidos.

![GitLab](https://img.shields.io/badge/gitlab-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white)
Fui instruído a utilizar uma ferramenta de versionamento de código.
Escolhi o Gitlab por conta de um recurso extra que a plataforma tem em relação ao Github. Ambas permitem a integração com terminal Gitbash e a criação de branchs para gerenciamento das alterações no código, considerando que estamos falando de um projeto realizado em equipe, com a contribuição de diferentes desenvolvedores. Porém, o Gitlab possue um recurso extra, que são as Milestones, através das issues criadas e do gráfico de KanBan fornecido, consegui fazer um gerenciamento muito superior de cada sprint em relação ao que seria possível fazer pelo Github.

#### Contribuições 
<details>
  <summary>Criei uma função que retorna um ranking ordenando despesas dos deputados de acordo com a quantidade de deputados selecionados (no exemplo foram 10)</summary>
  
  ```CONTROLE = 10

while CONTROLE != 0 :

    qtd_dp = str(input("\n \nINFORME A QUANTIDADE DE DEPUTADOS PARA ANALISE:  \n"))

    print("PARA TABELA COM OS " + qtd_dp + " DEPUTADOS MAIS GASTÕES   = 1 \nPARA TABELA COM OS " + qtd_dp + " DEPUTADOS MENOS GASTÕES  = 2 \n"
      "PARA GRAFICO COM OS " + qtd_dp + " DEPUTADOS MAIS GASTÕES  = 3 \nPARA GRAFICO COM OS " + qtd_dp + " DEPUTADOS MENOS GASTÕES = 4\n"
      "PARA SAIR = 0\n")

    CONTROLE = int(input("INFORME A ANALISE DESEJADA: "))

    qtd_dp = int(qtd_dp)
  ```
</details>

<details>
  <summary>Criei comandos que permitem ao usuário ordenar esse ranking em ordem crescente ou decrescente</summary>
  
  ```# ORDENAR DADOS DA TABELA ATRAVÉS DA FUNÇÃO "sort_values"

# ORDENANDO DECRESCENTE
    tabela_maior = PLANILHA.sort_values(['GASTO','ID'], ascending=False)
    tabela_maior[['GASTO','ID']]

# ORDENANDO CRESCENTE
    tabela_menor = PLANILHA.sort_values(['GASTO','ID'])
    tabela_menor[['GASTO','ID']]

    if CONTROLE == 1:

        print(tabela_maior.head(qtd_dp))

    elif CONTROLE == 2:

        print(tabela_menor.head(qtd_dp))

    elif CONTROLE == 3:
  ```
</details>

<details>
  <summary>Criei um bot que acessou uma api e fez a captura dos dados inseridos na mesma, gerando um arquivo .csv com as informações captadas</summary>
  
  ```import requests

URL = 'https://dadosabertos.camara.leg.br/api/v2/deputados'
RESP = requests.get(URL).json()

FILE_CSV = open('NOME_ID_TOTAL.csv', 'w')  # criando arquivo csv para escrever nome, ID, e total de gastos de cada deputado
  ```
</details>

#### Hard Skills
##### Git ![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
Descobri o quanto essa ferramenta é fundamental para um profissional de TI, o Git é como se fosse um Linkedin do programador. Fui apresentado a ferramenta pela Fatec, criei acesso a plataforma, fiz o primeiro repositório para o desenvolvimento desse projeto e comecei a utilizar essa tão importante ferramenta de versionamento de código, aprendendo sobre os recursos disponíveis dessa linguagem e aplicando-os durante o período onde compartilhados os códigos desse projeto.
##### Scrum
Aprendi a aplicar os conceitos da metodologia ágil, através do framework Scrum durante a prática de desenvolvimento do projeto.
Recebi o suporte de dois alunos do 6° semestre, que se integraram ao trabalho da minha equipe, cumprindo os papéis de Scrum Master e Product Owner, auxiliando nossa equipe durante todo o projeto.

#### Soft Skills
##### Kanban
Fomos instruídos a utilizar a metodologia Kan Ban para organizar as atividades do nosso projeto, categorizando as tarefas em: backlog, planejamento, desenvolvimento, entrega e aprovação.
##### Gestão de issues (milestones)
Utilizamos as milestones, que são um recurso disponibilizado pelo GitLab para organizar as entregas de cada sprint, fazendo a atribuição das issues para cada integrante da equipe, fazendo essa gestão de forma semelhante ao que encontramos no Trello.

### Em 2020-1 trabalhei no desenvolvimento de um projeto de uma plataforma para VEP (Visão Estratégica de Projetos), desenvolvido para a empresa Necto System
##### Descrição do projeto
Desenvolver um software de visão estratégica de projetos, que permita ao gestor de uma equipe criar tarefas, definir prazos e metas, distribuir essas demandas para a equipe e analisar se as atividades estão sendo cumpridas dentro do prazo proposto.
##### Proposta comercial
O principal objetivo do projeto é desenvolver um sistema para a Visão Estratégica de Projetos, o sistema será desenvolvido para facilitar o planejamento de projetos de uma empresa.

[GIT](https://gitlab.com/projeto-II/OEP)

#### Tecnologias Utilizadas
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
As linguagens de Front End foram utilizadas para funcionar como a interface do sistema que foi desenvolvido. A mostra do diagrama e a aplicação do funcionamento de seus recursos foram apresentados em cima dessas ferramentas.
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
Essa linguagem foi utilizada pois para fazer a conexão entre a interface e o banco de dados. Um dos requisitos do projeto era justamente permitir com que as informações preenchidas na interface do sistema fossem armazenadas em um BD.

![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
A ferramenta de banco de dados em questão foi escolhida para armazenar as informações preenchidas nos formulários de CRUD do sistema criado.

#### Contribuições 
<details>
  <summary>Banco de dados criado para armazenar as informações preenchidas nos CRUD's.</summary>
  
  ```CREATE DATABASE gantt;
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
</details>

<details>
  <summary>Função do NodeJS que retorna na interface do sistema todos os dados já cadastrados</summary>
  
  ```app.get("/data", function (req, res) {
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
</details>

<details>
  <summary>Função do Javascript criada para validar tentativa de login com um determinado preenchimento de usuário e senha</summary>
  
  ```<script type="text/javascript">
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
</details>

#### Hard Skills
##### Padrões de projeto
Aprender sobre design patterns foi fundamental para não termos que enfrentar problemas recorrentes que ocorrem durante o desenvolvimento de um software. Com esse tipo de informação em mãos, sempre que esbarramos em um desses problemas, conseguimos resolver rápido por ter uma lista de soluções baseadas em boas práticas utilizadas comumente pela comunidade de desenvolvedores.
##### Framework
As frameworks foram uma grande descoberta para nossa equipe durante esse projeto, pois tivemos uma base de saída para começar o desenvolvimento, ao invés de trabalhar todo o projeto do zero. Esse ponto de partida nos permitiu adiantar várias etapas e entregar um resultado final de maior qualidade, além de conseguir apresentar mais recursos graças ao tempo que foi ganho.

#### Soft Skills
##### Reunião de retrospectiva
Aprendemos e aplicamos mais este recurso da metodologia Scrum, para realizar um projeto com melhorias constantes durante sua execução, para melhor harmonia entre seus integrantes e para identificar acertos e erros das etapas anteriores.
##### Avaliação de soft skills
Organizamos o grupo para nos avaliarmos referente a conduta geral dos integrantes durante o projeto e a colaboração de todos dentro do cenário de comunicação, organização e trabalho em equipe, afinal de contas, um projeto não sobrevive apenas da capacidade técnica de seus desenvolvedores.

### Em 2020-2 trabalhei no desenvolvimento de uma plataforma para consulta de informações de proteção ao crédito, para a empresa SPC
##### - Descrição do projeto
A equipe desenvolverá um trabalho em parceria com o Spc, onde será desenvolvida uma plataforma para que usuários possam consultar informações referentes ao seu cadastro positivo. Este trabalho será feito pelos alunos do 3° semestre do curso de Banco de Dados, da Fatec de São José dos Campos, cumprindo os objetivos propostos pela organização do projeto integrador.
##### - Proposta comercial
A nossa proposta é desenvolver um dashboard que funcionará como uma linha do tempo. O objetivo é que o usuário da plataforma possa analisar sua vida financeira baseada em dados que englobam o passado, presente e futuro de sua vida financeira. Os recursos principais do dashboard serão os seguintes:
- Valor do score atual
- Banner com artigos informativos para os usuários
- Gráfico com valores em porcentagem, informando se as contas do cliente foram pagas dentro ou fora do prazo, se ainda estão em aberto ou se estão atrasadas, a partir da escolha de um determinado mês e ano.
- Gráfico com o histórico do score
- Tabela informando o quanto do orçamento do usuário foi designado para cada tipo de despesa em um determinado mês, que será escolhido pelo mesmo.
Com essas informações, a sequência de linha do tempo proposta funcionará da seguinte forma:
Passado: será designado pelo gráfico de histórico, onde o usuário poderá saber em qual momento de sua vida a sua análise de crédito esteve melhor ou pior.
Presente: o score atual trará essa informação, onde o cliente poderá saber como agir dependendo do valor que o mesmo receberá como retorno ao fazer sua consulta.
Futuro: a interface contará com um banner, que irá permitir acesso a artigos que podem ajudar no planejamento financeiro do usuário. Caso o mesmo tenha score baixo, ele terá acesso a dicas de gestão financeira e de como sair das dívidas. Caso o seu score for alto, existem também artigos com informações de dicas de investimento e de como funcionam as taxas bancárias, com o intuito de evitar despesas desnecessárias.

[GIT](https://github.com/felipe-fsc/Dashboard-SPC)

#### Tecnologias Utilizadas
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)![jQuery](https://img.shields.io/badge/jquery-%230769AD.svg?style=for-the-badge&logo=jquery&logoColor=white)![Bootstrap](https://img.shields.io/badge/bootstrap-%23563D7C.svg?style=for-the-badge&logo=bootstrap&logoColor=white)
As linguagens de Front End foram utilizadas para funcionar como a interface do sistema que foi desenvolvido. A mostra do diagrama e a aplicação do funcionamento de seus recursos foram apresentados em cima dessas ferramentas. O jQuery e o Bootstrap entraram nessa equação para permitir que eu pudesse explorar novos recursos do desenvolvimento front end, trazendo melhorias para a plataforma criada.

![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
A ferramenta de banco de dados em questão foi escolhida para armazenar as informações que o cliente enviou e fazer a integração desses dados recebidos com a mostra de dashboard do sistema.

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=java&logoColor=white)
Esta linguagem foi utilizada para criar funções dentro da plataforma, permitindo que a mesma apresente recursos como filtros e cálculo de performance financeira do usuário.

![GitLab](https://img.shields.io/badge/gitlab-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white)
Escolhi o Gitlab por conta de um recurso extra que a plataforma tem em relação ao Github. Ambas permitem a integração com terminal Gitbash e a criação de branchs para gerenciamento das alterações no código, considerando que estamos falando de um projeto realizado em equipe, com a contribuição de diferentes desenvolvedores. Porém, o Gitlab possue um recurso extra, que são as Milestones, através das issues criadas e do gráfico de KanBan fornecido, consegui fazer um gerenciamento muito superior de cada sprint em relação ao que seria possível fazer pelo Github.

#### Contribuições 
<details>
  <summary>Parte do banco de dados criado para armazenar as informações enviadas pelo SPC.</summary>
  
  ```CREATE TABLE `modalidade` (
  `cod_modalidade` varchar(3) NOT NULL,
  `des_modalidade` varchar(100) DEFAULT NULL,
  PRIMARY KEY (`cod_modalidade`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `modalidade`
--

LOCK TABLES `modalidade` WRITE;
/*!40000 ALTER TABLE `modalidade` DISABLE KEYS */;
INSERT INTO `modalidade` VALUES ('A01','EMPRESTIMO - CONSIGNADO'),('A02','EMPRESTIMO - CAPITAL DE GIRO'),('A04','EMPRESTIMO - CREDITO PESSOAL'),('A05','EMPRESTIMO - MICROCREDITO'),('A99','OUTROS EMPRESTIMOS'),('B01','FINANCIAMENTO - RURAL E AGROINDUSTRIAL'),('B02','FINANCIAMENTO - IMPORTACAO  E EXPORTACAO'),('B03','FINANCIAMENTO - IMOBILIARIOS SFH'),('B04','FINANCIAMENTO - MICROCREDITO'),('B05','FINANCIAMENTO - AQUISICAO DE BENS (VEICULOS)'),('B06','FINANCIAMENTO - IMOBILIARIO (OUTROS)'),('B07','FINANCIAMENTO - ARREENDAMENTO'),('B99','OUTROS FINANCIAMENTOS'),('C01','CONSORCIO'),('D01','CARTAO DE CREDITO'),('E01','CHEQUE ESPECIAL E CONTA GARANTIDA'),('E02','ADIANTAMENTO DEPOSITANTE'),('F01','AVAIS E FIANCASA HONRADOS'),('G01','TITULOS DESCONTADOS');
  ```
</details>

<details>
  <summary>Banner rotativo</summary>
  
  ```<ol class="carousel-indicators">
  <li data-target="#meuCarousel" data-slide-to="0" class="active"></li>
  <li data-target="#meuCarousel" data-slide-to="1"></li>
  <li data-target="#meuCarousel" data-slide-to="2"></li>
  <li data-target="#meuCarousel" data-slide-to="3"></li>
  <li data-target="#meuCarousel" data-slide-to="4"></li>
  <li data-target="#meuCarousel" data-slide-to="5"></li>
  <li data-target="#meuCarousel" data-slide-to="6"></li>
</ol>
  ```
</details>

<details>
  <summary>Configurações para conexão entre Back End e banco de dados</summary>
  
  ```version: '3'

services:
  mysqlsrv:
    image: mysql:5.7
    environment:
      MYSQL_ROOT_PASSWORD: "root"
      MYSQL_DATABASE: "spc_pi"
    ports:
      - "3307:3306"
    volumes:
      - spc-pi:/var/lib/mysql
    networks:
      - mysql-compose-network

volumes:
  spc-pi:
networks: 
  mysql-compose-network:
    driver: bridge
  ```
</details>
 
#### Hard Skills
##### Markdown
Neste projeto, nos foi cobrado com mais afinco o desenvolvimento de um readme de maior qualidade. Portanto, estudamos os recursos de layout e aprendemos mais sobre a linguagem markdown para desenvolvermos um documento de maior qualidade.

#### Soft Skills
##### Priorização de requisitos
Já havíamos trabalhado com os conceitos de requisitos funcionais e não funcionais em um projeto anterior, porém ainda não tínhamos muita noção de como distribuir essas exigências entre as sprints. Porém, nesse projeto, com uma base teórica mais aprofundada nesses conceitos, conseguimos melhorar esse tipo de distribuição para organizar melhor a forma como os projetos são desenvolvidos.
##### User stories
Utilizamos esse recurso para explicar melhor quais são os benefícios do nosso projeto, que tipo de público ele pode atingir e como esse atingimento é realizado, além de apresentar os motivos que atingem os objetivos de realização dos mesmos em todas as frentes analisadas.

### Em 2021-1 trabalhei no desenvolvimento de um sistema de divulgação de vagas de emprego, para a empresa Jet Soft
##### Descrição do projeto
Baseado no modelo de Aprendizado Por Projeto, nossa equipe trabalha para entregar uma solução operante para uma empresa parceira - Jet Soft - com o apoio do Docente desta instituição de ensino superior.
##### Proposta comercial
Desenvolver uma API que possibilita a busca de candidatos a partir de uma vaga, buscando uma contração veloz e assertiva. Dentre os critérios, deverão ser destaques a segurança e o desempenho da aplicação.

[GIT](https://gitlab.com/gabsmomilli/tecnocode)

#### Tecnologias Utilizadas
![Oracle](https://img.shields.io/badge/oracle-%23F00000.svg?style=for-the-badge&logo=oracle&logoColor=white)
A ferramenta de banco de dados em questão foi escolhida para armazenar as informações de candidatos a vagas de emprego, para que possam ser consultadas posteriormente pelos empregadores.
O Oracle também permite criar usuários com limitações de acesso específicas, o que é um diferencial em um sistema que será acessado tanto por usuários, quanto por administradores.

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=java&logoColor=white)
Esta linguagem foi utilizada para criar funções dentro da plataforma, como o cálculo de custo de transporte público via integração com o Google Maps.

![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
Como esse sistema se trata de uma plataforma Full Stack, utilizamos o React pela facilidade que o mesmo apresenta ao se conectar com banco de dados e com códigos Back End.
As linguagens de Front End foram utilizadas para funcionar como a interface do sistema que foi desenvolvido. Os formulários preenchidos pelos candidatos e as páginas de listagem de vagas e de candidatos foram apresentadas em cima dessas ferramentas.

![GitLab](https://img.shields.io/badge/gitlab-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white)
Escolhi o Gitlab por conta de um recurso extra que a plataforma tem em relação ao Github. Ambas permitem a integração com terminal Gitbash e a criação de branchs para gerenciamento das alterações no código, considerando que estamos falando de um projeto realizado em equipe, com a contribuição de diferentes desenvolvedores. Porém, o Gitlab possue um recurso extra, que são as Milestones, através das issues criadas e do gráfico de KanBan fornecido, consegui fazer um gerenciamento muito superior de cada sprint em relação ao que seria possível fazer pelo Github.

#### Contribuições 
<details>
  <summary>Configurações do banco de dados Oracle com as requeridas permissões de administrador do sistema.</summary>
  
  ```CREATE TABLESPACE  tecnocode
DATAFILE  'C:\BD\tecnocode.dbf' SIZE 1M
AUTOEXTEND ON;
------------------
-- CRIA USUARIO --
------------------
CREATE USER tecnocode
IDENTIFIED BY tecnocode
DEFAULT TABLESPACE tecnocode
TEMPORARY TABLESPACE TEMP
QUOTA UNLIMITED ON tecnocode;
-----------------
-- PRIVILEGIOS --
-----------------
GRANT DBA TO tecnocode WITH ADMIN OPTION;
  ```
</details>

<details>
  <summary>Cadastro de candidato no sistema</summary>
  
  ```const mock = {
    id_candidato: "",
    id_endereco: "",
    nome_candidato: "",
    descricao_candidato: "",
    estado_civil_candidato: "",
    sexo_candidato: "",
    idade_candidato: "",
    nascimento_candidato: "",
    competencia_candidato: [
        {id_competencia: "", descricao_competencia: "" },
        {id_competencia: "", descricao_competencia: "" },
    ],
    idiomas_candidato: [
        {id_idioma: "", descricao_idioma: "", nivel_idioma: ""},
        {id_idioma: "", descricao_idioma: "", nivel_idioma: ""},
    ],
    graduacao_candidato: [
        {id_graduacao: "", descricao_graduacao: "", inicio_graduacao: "", fim_graduacao: ""},
    ],
    experiencia_candidato: [
        {id_experiencia: "", descricao_experiencia: "", inicio_experiencia: "", fim_experiencia: ""},
    ]

}
  ```
</details>

<details>
  <summary>Desenvolvi uma função no Oracle Sql para converter o endereço cadastrado pelo candidato em valores de latitude e longitude.
O objetivo dessa função é medir a distância entre o endereço que a empresa que está oferecendo a vaga cadastra e o endereço cadastrado pelo candidato, caso o empregador queira filtrar as pessoas que se cadastraram pela distância que as mesmas terão que percorrer até o local de trabalho, o que foi um dos requisitos a serem cumpridos durante esse projeto.</summary>
  
  ```create or replace function get_address_by_lat_long (vacancy_lat float, vacancy_long float, range_distance number)
    return output_address PIPELINED is
    begin
        for RECORD_OUTPUT IN (
        select *
        from
        (
          SELECT
            adr_id,
            adr_lat,
            adr_long,
            adr_cep_pczc,
            adr_detail,
            adr_num,
            adr_hood,
            adr_city,
            adr_state,
            TRUNC((
               6371 *  -- em quilometros
               acos(cos((vacancy_lat * 3.14)/ 180) * --latitude da vaga -23.1622
               cos((adr_lat * 3.14)/ 180) * 
               cos((adr_long * 3.14)/ 180 - 
               (vacancy_long * 3.14)/ 180) + --longitude da vaga -23.1622
               sin((vacancy_lat * 3.14)/ 180) * 
               sin((adr_lat * 3.14)/ 180))
            ), 1) AS distance 
          FROM address
        ) x
        where distance <= range_distance AND distance > 0)-- quilometros
  ```
</details>

#### Hard Skills
##### Funções de Product Owner
Assumi o posto de Product Owner nesse projeto, tendo um contato mais próximo com o cliente e podendo ser colaborativo com a equipe ao atuar em funções estratégicas durante todo o calendário de desenvolvimento.
##### Oracle Sql
Utilizamos um serviço de database diferente nesse projeto, saindo do padrão do MySql utilizado nos projetos anteriores, o que nos ajudou muito na integração com as matérias de banco de dados do semestre de aplicação desse projeto.

#### Soft Skills
##### Avaliação Pacer
Seguimos criteriosamente essa avaliação, fazendo as revisões internamente entre os integrantes da equipe, o que nos permitiu evoluir profissionalmente a medida em que as sprints avançavam.
##### Diagrama de caso de uso
Utilizamos esse recurso para apresentar de forma clara a todas as pessoas que irão acessar a documentação, como o projeto se aplica no ponto de vista do usuário e o que o sistema executa por trás da interface.


### Em 2021-2 trabalhei no desenvolvimento do Educalytics, uma plataforma de ensino a distância, para a empresa Ionic Health

##### Descrição do Projeto
Nossa equipe aplicou a metodologia de aprendizado por projeto, com o objetivo de desenvolver uma aplicação para uma empresa parceira chamada Ionic Health, todo o projeto foi desenvolvido com o suporte dos professores da Fatec de São José dos Campos.
Os detalhes serão listados nas próximas etapas.
##### Proposta Comercial
Desenvolver uma aplicação que seja capaz de buscar dados de uma fonte externa, que no caso é uma aplicação legado chamada Skillshare, com o objetivo de prover aos usuários informações suficientes para a administração de uma instituição de ensino.
Os dados são gerados pelos alunos que acessam de forma constante uma plataforma educacional.
Por conta disso, dados como o histórico de uso, incluindo a interação dos usuários através de chats e registro de logs, tarefas, performance dos estudantes e avaliações da plataforma serão extraídos, compilados e apresentados para o cliente.
Eventualmente, o sistema deverá ser apto a transmitir o comportamento dos usuários das aplicações legado e fornecer os dados a instituição de ensino de forma eficaz, o que ajudará no processo de tomada de decisão da entidade.
Seguindo os princípios listados acima, o sistema irá apresentar uma interface gráfica de usuário na forma de um dashboard, com os dados considerados mais importantes do ponto de vista da instituição.

[GIT](https://gitlab.com/rafaelEstevam/back-educalytics)
For DASHBOARD (FRONTEND), please acess: https://gitlab.com/rafaelEstevam/front-educalytics

#### Tecnologias Utilizadas
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=java&logoColor=white)
O Java foi a principal linguagem de back end da plataforma.

![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
O Javascript foi a linguagem base para posteriormente utilizarmos Node e React como frameworks que auxiliaram no desenvolvimento do código.

![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)

![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
Utilizamos o MySql para armazenar as informações referentes ao banco de dados relacional da plataforma.

![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
O React foi o framework de Javascript utilizado como a principal ferramenta de desenvolvimento da interface do sistema.

![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
Utilizamos o Postman como ferramenta auxiliar para testar os métodos da API.

![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
Utilizamos o Git para fazer o versionamento do código.

![GitLab](https://img.shields.io/badge/gitlab-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white)
O Gitlab foi o site utilizado para fazermos a administração das features do projeto entre os programadores, utilizando recursos como KanBan, issues, milestones e gráfico de burndown.

![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
Utilizamos o MongoDb como banco de dados não relacional para trabalhar com os registros de mensagens enviadas e para armazenar as informações de movimentação no sistema por parte dos usuários em arquivos de log. 
#### Git Flow
Seguimos esse padrão para melhorar o controle de versionamento através das branchs utilizadas no projeto.

#### Contribuições
<details>
  <summary>Criei o dashboard da interface principal da plataforma</summary>
  
  ```function  Dashboard()  {

  

const  {enqueueSnackbar}  =  useSnackbar();

const  [data, setData]  =  useState({});

const  [mongoData, setMongoData]  =  useState({});

  

const  handleGetData  =  async()  =>  {

try{

const result =  await API.get('/tss/avgData');

setData(result.data);

}catch{

enqueueSnackbar('Não foi possível buscar os dados',  {variant:  'error'});

}

}

  

const  handleGetMongoData  =  async()  =>  {

try{

const result =  await axios.get('https://api-chat-educalytics.herokuapp.com/connections/data/all');

setMongoData(result.data);

}catch{

enqueueSnackbar('Não foi possível buscar os dados',  {variant:  'error'});

}

}

  

useEffect(()  =>  {

handleGetData();

handleGetMongoData();

}, []);

  

return (

<>

<Grid  container  spacing={5}>

<Grid  item  xs={9}>

<Grid  container  spacing={3}>

<Grid  item  xs={12}>

<Title  title="Dashboard"  />

</Grid>

<Grid  item  xs={7}>

<Grid  container  spacing={3}>

<Grid  item  xs={4}>

<AverageCard

helper="Em minutos"

title="Tempo Total"

subtitle="Uso da plataforma"

type="hour"

label="Alunos"

value={mongoData?.totalTimeOnlineInMinutes}

/>

</Grid>

<Grid  item  xs={4}>

<AverageCard

title="Total de conexões"

subtitle="Logins na plataforma"

label="Alunos"

type="value"

value={mongoData?.totalConnections}

/>

</Grid>

<Grid  item  xs={4}>

<AverageCard

helper="Total de minutos online dos usuários / Total de minutos ao longo do ano"

title="Engajamento médio"

subtitle="Uso da plataforma"

label="Alunos"

value={(mongoData?.averageEngagementForConnection *  100).toFixed(2)}

/>

</Grid>

</Grid>

<br/>

<NumberOfAccess  />

</Grid>

<Grid  item  xs={5}>

<ListCard  title="Média / Engajamento"  subtitle=""  label="Alunos"  />

</Grid>

</Grid>

</Grid>

<Grid  item  xs={3}>

<PerformanceCard  title="Avaliação de desempenho"  />

</Grid>

</Grid>

</>

);

}
  ```
</details>

<details>
  <summary>Criei a conexão da plataforma com os métodos da API</summary>
  
  ```const  handleGetAll  =  ()  =>  {

API.get('/login/all').then((response)  =>  {

setData(response.data);

}).catch((e)  =>  {

enqueueSnackbar('Não foi possível fazer a consulta',  {variant:  "error"});

})

}

const  handleOnSubmit  =  (e)  =>  {

e.preventDefault();

  

if(!values.id){

API.post('/login/new',  values).then((response)  =>  {

enqueueSnackbar('Salvo com sucesso',  {variant:  "success"});

handleGetAll()

}).catch((e)  =>  {

enqueueSnackbar('Não foi possível salvar a categoria',  {variant:  "error"});

});

}else{

API.put(`/login/edit/${values.id}`,  values).then((response)  =>  {

enqueueSnackbar('Salvo com sucesso',  {variant:  "success"});

handleGetAll();

}).catch((e)  =>  {

enqueueSnackbar('Não foi possível salvar a categoria',  {variant:  "error"});

});

}

}

const  handleDelete  =  ()  =>  {

API.delete(`/login/delete/${values.id}`).then(()  =>  {

enqueueSnackbar('Categoria apagada com sucesso',  {variant:  "success"});

setValues({email:  "",  password:  ""});

handleGetAll();

}).catch(()  =>  {

enqueueSnackbar('Não foi possível apagar a categoria. Ela pode estar vinculada à uma tarefa.',  {variant:  "error"});

});

};
  ```
</details>

<details>
  <summary>Criei a estrutura DDL do banco de dados do sistema</summary>
  
  ```-- MySQL Script generated by MySQL Workbench

-- Wed Nov 3 00:57:31 2021

-- Model: New Model Version: 1.0

-- MySQL Workbench Forward Engineering

  

SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0;

SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0;

SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='ONLY_FULL_GROUP_BY,STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION';

  

-- -----------------------------------------------------

-- Schema dm_participation

-- -----------------------------------------------------

  

-- -----------------------------------------------------

-- Schema dm_participation

-- -----------------------------------------------------

CREATE  SCHEMA  IF  NOT  EXISTS  `dm_participation`  DEFAULT  CHARACTER  SET utf8 ;

USE  `dm_participation` ;

  

-- -----------------------------------------------------

-- Table `dm_participation`.`dim_assigments`

-- -----------------------------------------------------

CREATE  TABLE  IF  NOT  EXISTS  `dm_participation`.`dim_assigments` (

`asg_id`  BIGINT(8) NOT  NULL AUTO_INCREMENT,

`asg_type`  VARCHAR(250) NULL,

`asg_number`  INT  NULL,

PRIMARY  KEY (`asg_id`))

ENGINE = InnoDB;

  
  

-- -----------------------------------------------------

-- Table `dm_participation`.`dim_time`

-- -----------------------------------------------------

CREATE  TABLE  IF  NOT  EXISTS  `dm_participation`.`dim_time` (

`tim_id`  BIGINT(8) NOT  NULL AUTO_INCREMENT,

`chatCreatedAt`  DATETIME  NULL,

`chatDisconnect`  VARCHAR(50) CHARACTER  SET  'utf8'  NULL,

`chatHashConnection`  VARCHAR(50) CHARACTER  SET  'utf8'  NULL,

`chatFrom`  VARCHAR(50) CHARACTER  SET  'utf8'  NULL,

`chatId`  VARCHAR(50) CHARACTER  SET  'utf8'  NULL,

`chatUserId`  INT  NULL,

`chatUpdatedAt`  DATETIME  NULL,

PRIMARY  KEY (`tim_id`))

ENGINE = InnoDB;

  
  

-- -----------------------------------------------------

-- Table `dm_participation`.`dim_student`

-- -----------------------------------------------------

CREATE  TABLE  IF  NOT  EXISTS  `dm_participation`.`dim_student` (

`std_id`  BIGINT(8) NOT  NULL AUTO_INCREMENT,

`std_name`  VARCHAR(250) NULL,

`std_status`  BINARY(1) NULL,

PRIMARY  KEY (`std_id`))

ENGINE = InnoDB;

  
  

-- -----------------------------------------------------

-- Table `dm_participation`.`dim_class_of`

-- -----------------------------------------------------

CREATE  TABLE  IF  NOT  EXISTS  `dm_participation`.`dim_class_of` (

`idclass_of`  BIGINT(8) NOT  NULL AUTO_INCREMENT,

`range`  VARCHAR(250) NULL COMMENT 'range = periodo do semestre letivo.',

`available`  INT  NULL COMMENT 'available = tempo possível na plataforma',

PRIMARY  KEY (`idclass_of`))

ENGINE = InnoDB;

  
  

-- -----------------------------------------------------

-- Table `dm_participation`.`fact_participation`

-- -----------------------------------------------------

CREATE  TABLE  IF  NOT  EXISTS  `dm_participation`.`fact_participation` (

`acc_elap`  INT  NULL COMMENT 'tempo total logado',

`prf_qtd_dlr`  INT  NULL,

`prf_qtd_asg`  INT  NULL,

`dim_time_tim_id`  BIGINT(8) NOT  NULL,

`dim_assigments_asg_id`  BIGINT(8) NOT  NULL,

`dim_student_std_id`  BIGINT(8) NOT  NULL,

`dim_class_of_idclass_of`  BIGINT(8) NOT  NULL,

INDEX  `fk_fact_participation_dim_time_idx` (`dim_time_tim_id`  ASC) VISIBLE,

INDEX  `fk_fact_participation_dim_assigments1_idx` (`dim_assigments_asg_id`  ASC) VISIBLE,

INDEX  `fk_fact_participation_dim_student1_idx` (`dim_student_std_id`  ASC) VISIBLE,

INDEX  `fk_fact_participation_dim_class_of1_idx` (`dim_class_of_idclass_of`  ASC) VISIBLE,

PRIMARY  KEY (`dim_time_tim_id`, `dim_assigments_asg_id`, `dim_student_std_id`, `dim_class_of_idclass_of`),

CONSTRAINT  `fk_fact_participation_dim_time`

FOREIGN KEY (`dim_time_tim_id`)

REFERENCES  `dm_participation`.`dim_time` (`tim_id`)

ON DELETE  NO  ACTION

ON  UPDATE  NO  ACTION,

CONSTRAINT  `fk_fact_participation_dim_assigments1`

FOREIGN KEY (`dim_assigments_asg_id`)

REFERENCES  `dm_participation`.`dim_assigments` (`asg_id`)

ON DELETE  NO  ACTION

ON  UPDATE  NO  ACTION,

CONSTRAINT  `fk_fact_participation_dim_student1`

FOREIGN KEY (`dim_student_std_id`)

REFERENCES  `dm_participation`.`dim_student` (`std_id`)

ON DELETE  NO  ACTION

ON  UPDATE  NO  ACTION,

CONSTRAINT  `fk_fact_participation_dim_class_of1`

FOREIGN KEY (`dim_class_of_idclass_of`)

REFERENCES  `dm_participation`.`dim_class_of` (`idclass_of`)

ON DELETE  NO  ACTION

ON  UPDATE  NO  ACTION)

ENGINE = InnoDB;

  
  

SET SQL_MODE=@OLD_SQL_MODE;

SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS;

SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS;
  ```
</details>

#### Hard Skills

##### MongoDb 
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
Utilizamos o MongoDb como banco de dados não relacional para trabalhar com os registros de mensagens enviadas e para armazenar as informações de movimentação no sistema por parte dos usuários em arquivos de log. 
##### Versionamento de banco de dados
Realizei o processo de versionamento do banco de dados utilizando o Flyway, com o objetivo de manter um registro das alterações aplicadas no banco de dados.

#### Soft Skills
##### Clean code
Como esse foi um projeto de programação com muitas features desenvolvidas em conjunto, precisamos nos atentar para que o código ficasse legível para todos os programadores envolvidos, por isso definimos um padrão baseado nas boas práticas de Clean Code para trabalhar esse desenvolvimento em conjunto de forma organizada.
##### Quality assurance
Utilizamos o processo de garantia de qualidade com o objetivo de otimizar a eficácia das nossas entregas e conseguir desenvolver um projeto que equilibrasse o atendimento dos requisitos, com o melhor aproveitamento educacional possível dos conceitos que foram apresentados e com um tempo de aplicação que fosse coerente com a realidade dos estudantes.

### Em 2022-1 desenvolvi um projeto para a matéria de Laboratório de Desenvolvimento em Banco de Dados 6, onde foi criada uma rede neural baseada nos conceitos de KNN (K Nearest Neighbors)
##### Descrição do Projeto
Foi desenvolvido um sistema que combina os conceitos de rede neural e KNN (K Nearest Neighbors) em inteligência artificial. O objetivo da rede neural é aprender a jogar o jogo Flappy Bird, onde a tomada de decisão da rede neural deve ser se o pássaro pula ou não, essa tomada de decisão será baseada em 3 critérios:
1 - Distância do pássaro em relação ao chão
2 - Distância do pássaro para a parte superior do obstáculo
3 - Distância do pássaro para a parte inferior do obstáculo
##### Proposta Comercial
O projeto foi solicitado pelo Professor Fabrício Galende, que ministra a matéria Laboratório de Desenvolvimento em Banco de Dados 6, o objetivo é utilizar o KNN para criar uma inteligência artificial que seja capaz de identificar os padrões de uma imagem, no caso do jogo, a IA precisa identificar a posição dos canos para definir as distâncias do pássaro, tanto em relação ao cano superior, quanto em relação ao inferior.
O aprendizado de definição de padrões de imagem tem valia no sentido de ser um sistema que pode ser aplicado em várias outras frentes, como sistema de identificação de formas geométricas e sistemas de predição de doenças, baseado em imagens de exames, como raio-x e ultrassom por exemplo.

[GIT](https://gitlab.com/felipefsc/flappy-bird-knn)

#### Tecnologias Utilizadas

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

Utilizei essa linguagem por solicitação do professor, o Python é bastante recomendado para o desenvolvimento de códigos de inteligência artificial e se mostrou bem eficiente durante a execução desse projeto.

#### Contribuições
<details>
  <summary>Utilizei a biblioteca pygame para importar o código do jogo Flappy Bird para o Python</summary>
  
  ```import pygame

TELA_LARGURA  =  500

TELA_ALTURA  =  800

IMAGEM_CANO  = pygame.transform.scale2x(pygame.image.load(os.path.join('imgs',  'pipe.png')))

IMAGEM_CHAO  = pygame.transform.scale2x(pygame.image.load(os.path.join('imgs',  'base.png')))

IMAGEM_BACKGROUND  = pygame.transform.scale2x(pygame.image.load(os.path.join('imgs',  'bg.png')))

IMAGENS_PASSARO  =  [

pygame.transform.scale2x(pygame.image.load(os.path.join('imgs',  'bird1.png'))),

pygame.transform.scale2x(pygame.image.load(os.path.join('imgs',  'bird2.png'))),

pygame.transform.scale2x(pygame.image.load(os.path.join('imgs',  'bird3.png'))),

]

  

pygame.font.init()

FONTE_PONTOS  = pygame.font.SysFont('arial',  50)
  ```
</details>

<details>
  <summary>Criei a função que posiciona os obstáculos do jogo de forma randômica na interface</summary>
  
  ```class  Cano:

DISTANCIA  =  200

VELOCIDADE  =  5

  

def  __init__(self,  x):

self.x  =  x

self.altura  =  0

self.pos_topo  =  0

self.pos_base  =  0

self.CANO_TOPO  = pygame.transform.flip(IMAGEM_CANO,  False,  True)

self.CANO_BASE  =  IMAGEM_CANO

self.passou  =  False

self.definir_altura()

  

def  definir_altura(self):

self.altura  = random.randrange(50,  450)

self.pos_topo  =  self.altura  -  self.CANO_TOPO.get_height()

self.pos_base  =  self.altura  +  self.DISTANCIA
  ```
</details>

<details>
  <summary>Desenvolvi a função da inteligência artificial que toma a decisão de se o pássaro vai subir ou descer, levando em conta os seguintes critérios:

1 - Distância do pássaro em relação ao chão
2 - Distância do pássaro para a parte superior do obstáculo
3 - Distância do pássaro para a parte inferior do obstáculo</summary>
  
  ```for  i,  passaro  in  enumerate(passaros):

passaro.mover()

#aumentar a fitness do pássaro

lista_genomas[i].fitness +=  0.1

output  =  redes[i].activate((passaro.y,  abs(passaro.y  -  canos[indice_cano].altura),  abs(passaro.y  -  canos[indice_cano].pos_base)))

if  output[0]  >  0.5:

passaro.pular()
  ```
</details>

#### Hard Skills
##### Machine Learning
Aprender a desenvolver programas com funções de aprendizado de máquina foi muito importante para a minha carreira, devido a vasta gama de recursos onde essas funções podem ser aplicadas, posso citar exemplos como sistemas de recomendação e predição de fraturas e doenças.
##### KNN (K Nearest Neighbors)
Dentre os conceitos que aprendi de inteligência artificial, posso destacar o KNN, que foi utilizado para desenvolver esse projeto.

#### Soft Skills
##### Inteligência artificial
Aprender conceitos de inteligência artificial foi algo que colaborou bastante para ampliar meus conhecimentos em programação, esses conceitos podem ser aplicados de várias formas e isso me permite avançar bastante no crescimento da minha carreira.
##### Rede neural
Foi bastante interessante programar e ir entendendo na prática como funciona uma rede neural, critérios bem estabelecidos nesse tipo de projeto permitem que esses neurônios simulados criem por si só padrões bem complexos.

## Meus Principais Conhecimentos

Com os conhecimentos adquiridos no ambiente acadêmico, nas minhas experiências profissionais e em projetos que decidi desenvolver para praticar programação, optei por atuar como desenvolvedor full stack.
Tomei o cuidado de me especializar em uma stack que possuísse uma linguagem de programação de cada tipo, conseguindo assim atuar como desenvolvedor front ou back end e tendo também uma base sólida de conhecimento em linguagens de banco de dados.

### Front End
Durante um período da faculdade, comecei a estudar as frameworks de Javascript, que era uma linguagem que eu já tinha um bom nível de conhecimento técnico. Fazendo as análises, identifiquei o React como uma linguagem de front end para me especializar, levando em consideração não só a fatia de mercado disponível para quem conhece essa linguagem, mas também a facilidade que os recursos apresentados trazem para o trabalho do programador, além de que esse framework apresenta um template de design bem mais organizado.

### Back End
Utilizei o C# como principal linguagem de back end da minha stack. Como é uma linguagem orientada a objetos, a curva de aprendizado é menor caso eu precise trabalhar com projetos em linguagens similares, como Java e Python por exemplo. Além disso, o C# tem uma estrutura muito boa para o desenvolvimento de testes automatizados e automações de funções, quando o mesmo é integrado com o Selenium.

### Banco de dados
#### Relacional
Utilizei o MySql como especialidade, é a principal linguagem de banco de dados disponível no mercado, tem bons softwares de auxílio, bastante material para consulta e permite consultas bem integradas com o modelo de DER (Diagrama Entidade Relacionamento), utilizado para fazer a arquitetura de banco de dados.
#### Não relacional
O MongoDB foi a linguagem utilizada para aprofundar meus conhecimentos em banco de dados não relacional, é um sistema muito bom para conversão de arquivos .csv em banco de dados e também funciona muito bem para registro de logs de aplicações.

## Contatos

*  [GIT](https://www.gitlab.com/felipefsc)

*  [LinkedIn](https://www.linkedin.com/in/felipe-santos-454060187/)
