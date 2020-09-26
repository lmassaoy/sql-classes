# Aula 1 - SQL - Que 'trem' é esse?

**Standard Query Language** ou para nosso idioma: Linguagem padrão para queries.

Essa é a linguagem utilizada nos bancos de dados para realizar diversos tipos de operações como:

- Criação (INSERT)
- Leitura (SELECT)
- Atualização (UPDATE)
- Exclusão (DELETE)

Operações estas conhecidas como "CRUD" (Create/Read/Update/Delete).

## Links para leitura para aprofundamento teórico/histórico:
- [Wikipedia](https://pt.wikipedia.org/wiki/SQL)
    - Explicação completinha; meio pesada no começo mas é ótima
- [Alura](https://www.alura.com.br/artigos/o-que-e-sql#:~:text=SQL%20significa%20Standard%20Query%20Language,SQL%20Server%2C%20entre%20muitos%20outros.)
    - Abordagem mais tranquila
- [W3Schools](https://www.w3schools.com/sql/default.asp)
    - Tutorial **COMPLETO**. Nem sei pra que eu to fazendo esse repo...
- [TutorialsPoint](https://www.tutorialspoint.com/sql/index.htm)
    - Outro guia pesado. Já me tirou diversas dúvidas

# SGBD escolhido para iniciação: MySQL

[![mysql.png](https://i.postimg.cc/v8pnN2Rs/mysql.png)](https://postimg.cc/Lh3hqT6C)

Até o dono da padaria do seu bairro já ouviu falar de MySQL, né? E você?

**NÃO!?**

Poxa, aí eu invoco o [Wikipedia](https://pt.wikipedia.org/wiki/MySQL) em modo de ataque para mudar isso já! :)

Em curta: o **MySQL** é um sistema de gerenciamento de banco de dados (SGBD), que utiliza a linguagem SQL (AVA, Yamada!). De acordo com o [DB-engines](https://db-engines.com/en/ranking) o **MySQL** está na **segunda posição do rank global** de uso de bancos de dados :V doideira, né?

Felizmente existe a versão *Community* para nós estudarmos, que inclusive é de graça ;) e será ela que utilizaremos nessa jornada.

## Instalação do MySQL

Peço que você siga as instruções oficiais para realizar a instalação do [MySQL Community Edition](https://www.mysql.com/products/community/) e do [MySQL Workbench](https://www.mysql.com/products/workbench/).

Utilizaremos o Workbench como nossa ferramenta principal para operar nossos bancos de dados.

As instalações constumam ser bem simples e os sites oficiais ensinam o passo-a-passo. Mostre-me que você é digno, levanta o Mjolnir do chão e **DYI**.

[![thor.png](https://i.postimg.cc/Cx9gV849/thor.png)](https://postimg.cc/pmQ7fp4B)

# Banco de dados

![DB](https://upload-icon.s3.us-east-2.amazonaws.com/uploads/icons/png/4962338431536834823-64.png)

De acordo com o Santo Graal (aka [Wikipedia](https://pt.wikipedia.org/wiki/Banco_de_dados#:~:text=Bancos%20de%20dados%20ou%20bases,uma%20pesquisa%20ou%20estudo%20cientifico.)):

"*São coleções organizadas de dados que se relacionam de forma a criar algum sentido (Informação) e dar mais eficiência durante uma pesquisa ou estudo cientifico.*"

Lindo, né?

Numa linguagem mais simples, eu diria que bancos de dados são repositórios para armazenarmos **tabelas** de dados (sim, *beeeem* parecidas com aquelas do Excel que você pensou) e seus **relacionamentos**, assim como outros recursos como **triggers*** (gatilhos) e **procedures** (procedimentos).

Mas vamos com calma. Nosso foco inicial são as **TABELAS** :)

# Tabelas

Acho que uma forma simples de explicar o que uma tabela é, é justamente lembra-lo de uma planilha do MS Excel. Se você já viu uma, então é exatamente assim que uma tabela é. Outra analogia seria uma **matriz**. Ou pensa numa folha quadriculada xD

![Table](https://cdn.sqlservertutorial.net/wp-content/uploads/sql-server-select-customers-table.png)
*from [sqlservertutorial.net](https://www.sqlservertutorial.net/sql-server-basics/sql-server-select/)*

Ela possuí:
- Colunas (Columns)
- Linhas (Rows)

## Colunas (Columns)

Uma coluna é um "atributo" ou característica que um registro terá. Uma tabela pode ter várias colunas, de diferentes tipos ([data types](https://dev.mysql.com/doc/refman/8.0/en/data-types.html)). Entre os mais comuns temos:
- Numérico (Numeric)
    - Inteiro (Int)
    - Decimal (Decimal)
- Data e Hora (Data and Time)
    - Data (Date)
    - Data e hora (Datetime)
    - Timestamp
- Texto (Varchar)

E alguns outros mais avançados que não vale a pena conhecermos **agora**.

## Linhas ou Registros (Rows)

Uma linha ou registro é como se fosse um cadastro de uma informação, informando todos os valores de suas caraceterísticas. Por exemplo:
- Imagine que você está olhando uma tabela de cadastro de pessoas. Nessa tabela você tem as colunas **ID** (número de identificação), **Nome** e **Idade**
- Dito isso você tem várias pessoas cadastradas, onde cada pessoa é representada em uma linha (registro). Como seria então isso visualmente:

|ID|Nome|Idade|
|-|-|-|
|1|Naruto|16|
|2|Goku|50|
|3|Ichigo|17|

Isso aí é uma tabela :P *"mais fácil que voar"* - [Jefferson do LinuxTips](https://twitter.com/badtux_)

# Objetivo da aula

Minha intenção nessa aula é preparar seu primeiro banco de dados e sua primeira tabela (é mega simples de fazer isso, os comandos estão disponíveis no arquivo [how_to_import_into_mysql.txt]()). Na sequência popularemos com a ajuda do Workbench importando o arquivo [titanic.csv] para dentro da tabela criada. Para por fim começarmos a baguncinha:
- Consultar os dados de uma tabela SQL

Que orgulho, hein! Dá até pra por no LinkedIn já ;D

**VEM COMIGO!**