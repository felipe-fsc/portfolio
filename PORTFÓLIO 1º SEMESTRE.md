# <center>Web Bot - Portal da Transparência</center>

## - Descrição do projeto
Desenvolver um web bot que faça uma raspagem de dados em um site, coletando dados referentes as despesas gastas por políticos de cargo eletivo, coletando informações que serão arquivadas, onde as mesmas serão desmembradas em quanto cada tipo de despesa consumiu do valor pago em impostos pelo contribuinte.
### - Proposta comercial
O objetivo do projeto é que um grupo de alunos desenvolva uma aplicação em que seja utilizado um WebBot desenvolvido pelo grupo, usando o na solução de um problema proposto pelo grupo.

## Índice

<!--ts-->
*  [Descrição do Projeto](#descricao-do-projeto)
*  [Tecnologias](#tecnologias)
*  [Contribuições Individuais](#contribuicoes-individuais)
*  [Aprendizados Efetivos](#aprendizados-efetivos)
<!--te-->

## - Tecnologias
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
Utilizei essa linguagem pela sua simplicidade, como esse é um projeto de 1° semestre, meu nível técnico ainda era de um programador iniciante, com algumas noções de lógica e sem muitas aplicações práticas como desenvolvedor.
Fazer um projeto em Python funcionou muito bem, pois além da simplicidade, pude fazer bom uso das bibliotecas que integram com essa linguagem, o que me permitiu trazer bons recursos para o bot que foi desenvolvido.<br>
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
O Pandas foi um recurso fundamental para o que pude fazer depois da etapa de extração de dados. Como a informação captada foi retornada como um arquivo .csv, minha equipe decidiu criar uma interface no Excel para retornar esses dados de forma organizada e o Pandas foi uma biblioteca que serviu muito bem com os recursos fornecidos.<br>
![GitLab](https://img.shields.io/badge/gitlab-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white)
Fui instruído a utilizar uma ferramenta de versionamento de código.
Escolhi o Gitlab por conta de um recurso extra que a plataforma tem em relação ao Github. Ambas permitem a integração com terminal Gitbash e a criação de branchs para gerenciamento das alterações no código, considerando que estamos falando de um projeto realizado em equipe, com a contribuição de diferentes desenvolvedores. Porém, o Gitlab possue um recurso extra, que são as Milestones, através das issues criadas e do gráfico de KanBan fornecido, consegui fazer um gerenciamento muito superior de cada sprint em relação ao que seria possível fazer pelo Github.

## - Contribuições Individuais
- Criei uma função que retorna um ranking ordenando despesas dos deputados de acordo com a quantidade de deputados selecionados (no exemplo foram 10)
```
CONTROLE = 10

while CONTROLE != 0 :

    qtd_dp = str(input("\n \nINFORME A QUANTIDADE DE DEPUTADOS PARA ANALISE:  \n"))

    print("PARA TABELA COM OS " + qtd_dp + " DEPUTADOS MAIS GASTÕES   = 1 \nPARA TABELA COM OS " + qtd_dp + " DEPUTADOS MENOS GASTÕES  = 2 \n"
      "PARA GRAFICO COM OS " + qtd_dp + " DEPUTADOS MAIS GASTÕES  = 3 \nPARA GRAFICO COM OS " + qtd_dp + " DEPUTADOS MENOS GASTÕES = 4\n"
      "PARA SAIR = 0\n")

    CONTROLE = int(input("INFORME A ANALISE DESEJADA: "))

    qtd_dp = int(qtd_dp)
```

- Criei comandos que permitem ao usuário ordenar esse ranking em ordem crescente ou decrescente
```
# ORDENAR DADOS DA TABELA ATRAVÉS DA FUNÇÃO "sort_values"

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

- Criei um bot que acessou uma api e fez a captura dos dados inseridos na mesma, gerando um arquivo .csv com as informações captadas
```
import requests

URL = 'https://dadosabertos.camara.leg.br/api/v2/deputados'
RESP = requests.get(URL).json()

FILE_CSV = open('NOME_ID_TOTAL.csv', 'w')  # criando arquivo csv para escrever nome, ID, e total de gastos de cada deputado
```

## - Aprendizados Efetivos
### Git ![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white) ![GitLab](https://img.shields.io/badge/gitlab-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white)
Descobri o quanto essa ferramenta é fundamental para um profissional de TI, o Git é como se fosse um Linkedin do programador. Fui apresentado a ferramenta pela Fatec, criei acesso a plataforma, fiz o primeiro repositório para o desenvolvimento desse projeto e comecei a utilizar essa tão importante ferramenta de versionamento de código, aprendendo sobre os recursos disponíveis dessa linguagem e aplicando-os durante o período onde compartilhados os códigos desse projeto.
### Scrum
Aprendi a aplicar os conceitos da metodologia ágil, através do framework Scrum durante a prática de desenvolvimento do projeto.
Recebi o suporte de dois alunos do 6° semestre, que se integraram ao trabalho da minha equipe, cumprindo os papéis de Scrum Master e Product Owner, auxiliando nossa equipe durante todo o projeto.
### Kanban
Fomos instruídos a utilizar a metodologia Kan Ban para organizar as atividades do nosso projeto, categorizando as tarefas em: backlog, planejamento, desenvolvimento, entrega e aprovação.
### Gestão de issues (milestones)
Utilizamos as milestones, que são um recurso disponibilizado pelo GitLab para organizar as entregas de cada sprint, fazendo a atribuição das issues para cada integrante da equipe, fazendo essa gestão de forma semelhante ao que encontramos no Trello.
