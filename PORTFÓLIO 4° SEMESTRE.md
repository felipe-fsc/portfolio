# <center>Job Nation</center>

## - Descrição do projeto
Baseado no modelo de Aprendizado Por Projeto, nossa equipe trabalha para entregar uma solução operante para uma empresa parceira - Jet Soft - com o apoio do Docente desta instituição de ensino superior.
### - Proposta comercial
Desenvolver uma API que possibilita a busca de candidatos a partir de uma vaga, buscando uma contração veloz e assertiva. Dentre os critérios, deverão ser destaques a segurança e o desempenho da aplicação.

## Índice

<!--ts-->
*  [Descrição do Projeto](#descricao-do-projeto)
*  [Tecnologias](#tecnologias)
*  [Contribuições Individuais](#contribuicoes-individuais)
*  [Aprendizados Efetivos](#aprendizados-efetivos)
<!--te-->

## - Tecnologias
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

## - Contribuições Individuais
- Configurações do banco de dados Oracle com as requeridas permissões de administrador do sistema.
```
CREATE TABLESPACE  tecnocode
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

- Cadastro de candidato no sistema
```
const mock = {
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

- Desenvolvi uma função no Oracle Sql para converter o endereço cadastrado pelo candidato em valores de latitude e longitude.
O objetivo dessa função é medir a distância entre o endereço que a empresa que está oferecendo a vaga cadastra e o endereço cadastrado pelo candidato, caso o empregador queira filtrar as pessoas que se cadastraram pela distância que as mesmas terão que percorrer até o local de trabalho, o que foi um dos requisitos a serem cumpridos durante esse projeto.
```
create or replace function get_address_by_lat_long (vacancy_lat float, vacancy_long float, range_distance number)
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

## - Aprendizados Efetivos
### Funções de Product Owner
Assumi o posto de Product Owner nesse projeto, tendo um contato mais próximo com o cliente e podendo ser colaborativo com a equipe ao atuar em funções estratégicas durante todo o calendário de desenvolvimento.
### Oracle Sql
Utilizamos um serviço de database diferente nesse projeto, saindo do padrão do MySql utilizado nos projetos anteriores, o que nos ajudou muito na integração com as matérias de banco de dados do semestre de aplicação desse projeto.
### Avaliação Pacer
Seguimos criteriosamente essa avaliação, fazendo as revisões internamente entre os integrantes da equipe, o que nos permitiu evoluir profissionalmente a medida em que as sprints avançavam.
### Diagrama de caso de uso
Utilizamos esse recurso para apresentar de forma clara a todas as pessoas que irão acessar a documentação, como o projeto se aplica no ponto de vista do usuário e o que o sistema executa por trás da interface.