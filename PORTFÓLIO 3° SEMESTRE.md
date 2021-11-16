# <center>Dashboard Score SPC</center>

## - Descrição do projeto
A equipe desenvolverá um trabalho em parceria com o Spc, onde será desenvolvida uma plataforma para que usuários possam consultar informações referentes ao seu cadastro positivo. Este trabalho será feito pelos alunos do 3° semestre do curso de Banco de Dados, da Fatec de São José dos Campos, cumprindo os objetivos propostos pela organização do projeto integrador.
### - Proposta comercial
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

## Índice

<!--ts-->
*  [Descrição do Projeto](#descricao-do-projeto)
*  [Tecnologias](#tecnologias)
*  [Contribuições Individuais](#contribuicoes-individuais)
*  [Aprendizados Efetivos](#aprendizados-efetivos)
<!--te-->

## - Tecnologias
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)![jQuery](https://img.shields.io/badge/jquery-%230769AD.svg?style=for-the-badge&logo=jquery&logoColor=white)![Bootstrap](https://img.shields.io/badge/bootstrap-%23563D7C.svg?style=for-the-badge&logo=bootstrap&logoColor=white)
As linguagens de Front End foram utilizadas para funcionar como a interface do sistema que foi desenvolvido. A mostra do diagrama e a aplicação do funcionamento de seus recursos foram apresentados em cima dessas ferramentas. O jQuery e o Bootstrap entraram nessa equação para permitir que eu pudesse explorar novos recursos do desenvolvimento front end, trazendo melhorias para a plataforma criada.
![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
A ferramenta de banco de dados em questão foi escolhida para armazenar as informações que o cliente enviou e fazer a integração desses dados recebidos com a mostra de dashboard do sistema.
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=java&logoColor=white)
Esta linguagem foi utilizada para criar funções dentro da plataforma, permitindo que a mesma apresente recursos como filtros e cálculo de performance financeira do usuário.
![GitLab](https://img.shields.io/badge/gitlab-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white)
Escolhi o Gitlab por conta de um recurso extra que a plataforma tem em relação ao Github. Ambas permitem a integração com terminal Gitbash e a criação de branchs para gerenciamento das alterações no código, considerando que estamos falando de um projeto realizado em equipe, com a contribuição de diferentes desenvolvedores. Porém, o Gitlab possue um recurso extra, que são as Milestones, através das issues criadas e do gráfico de KanBan fornecido, consegui fazer um gerenciamento muito superior de cada sprint em relação ao que seria possível fazer pelo Github.

## - Contribuições Individuais
- Parte do banco de dados criado para armazenar as informações enviadas pelo SPC.
```
CREATE TABLE `modalidade` (
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

- Banner rotativo
```
<ol class="carousel-indicators">
  <li data-target="#meuCarousel" data-slide-to="0" class="active"></li>
  <li data-target="#meuCarousel" data-slide-to="1"></li>
  <li data-target="#meuCarousel" data-slide-to="2"></li>
  <li data-target="#meuCarousel" data-slide-to="3"></li>
  <li data-target="#meuCarousel" data-slide-to="4"></li>
  <li data-target="#meuCarousel" data-slide-to="5"></li>
  <li data-target="#meuCarousel" data-slide-to="6"></li>
</ol>
```

- Configurações para conexão entre Back End e banco de dados 
```
version: '3'

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

## - Aprendizados Efetivos
### Priorização de requisitos
Já havíamos trabalhado com os conceitos de requisitos funcionais e não funcionais em um projeto anterior, porém ainda não tínhamos muita noção de como distribuir essas exigências entre as sprints. Porém, nesse projeto, com uma base teórica mais aprofundada nesses conceitos, conseguimos melhorar esse tipo de distribuição para organizar melhor a forma como os projetos são desenvolvidos.
### User stories
Utilizamos esse recurso para explicar melhor quais são os benefícios do nosso projeto, que tipo de público ele pode atingir e como esse atingimento é realizado, além de apresentar os motivos que atingem os objetivos de realização dos mesmos em todas as frentes analisadas.
### Desenvolvimento de readme
Neste projeto, nos foi cobrado com mais afinco o desenvolvimento de um readme de maior qualidade. Portanto, estudamos os recursos de layout e aprendemos mais sobre a linguagem markdown para desenvolvermos um documento de maior qualidade.