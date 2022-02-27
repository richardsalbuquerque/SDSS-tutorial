# SDSS-tutorial (English)

## Overview
There are over a milion of astronomical objects in the Sloan Digital Sky Survey (SDSS) database, 
by asking the right question you will be able to select the exatly the object you want, for example:
the brightest, less bright or the furthest, all in seconds.

You need to writte a query to get information in database, but be carefull! The wrong query can
return Gigabytes of information, you will need to learn about the SQL language to get information
from SDSS, this is a common language for working with data.

## Importants information

First, I want to talk about some parameters that we will use to code the algorithm that searches
for the filamentary structure. Definetively, the redshift is one of the most important parameters,
as it gives the imformation about how far away we are. The redshift of a spectrum is in the 'z'
column of the specObj table, we need to save it to write the query.

This job is looking for galaxy to make a density profile, so we need to specify the type of
object we want, then in the specObj we are going to filter the column objType for select the name 
'GALAXY' value '0' (URL documentation: http://skyserver.sdss.org/dr8/en/help/browser/browser.asp).

SkyServer's Query tool is limited to 90 seconds of search time and 100,000 results. If you want to write
queries that return more than 100,000 objects, you have to be clever: split your query into multiple pieces.

## More about SQL commands

An SQL query consists of three pieces, or blocks: the SELECT block, the FROM block and the WHERE block.

The first block, SELECT, tell us what column of data we want, example:

SELECT ra, dec, z

The second block, FROM, going to search the information specified in select part in a table, example:

FROM specObj

The third one, WHERE, will add restrictions to selection the exact object characteristics you want, example:

WHERE ra BETWEEN 130 AND 145 AND z < 0.05 AND objType='GALAXY'

With the above command lines, you will select right ascension and declination data from objects
which have spectroscopy data and are located on right ascension between 130° and 145° with redshift
less than 0.05 and they are galaxy.

# SDSS-tutorial (Português)

## Visão geral
Existem mais de um milhão de objetos astronômicos na base de dados do Sloan digital Sky Survey (SDSS),
fazendo a pergunta certa você poderá encontrar o exato objeto requerido, por exemplo: o mais brilhante,
menos brilhante ou até mesmo o mais distânte, tudo isso em questão de segundos.

Você precisará escrever uma "query" para obter informações do banco de dados, tome cuidado! A "query"
errada pode retornar um arquivo de Gigabytes de tamanho, você precisará aprender algumas técnicas da
linguagem SQL para trabalhar com esses dados, esta é uma ferramenta comun quando estamos estudando
grandes quantidades de dados.

## Informações importantes

Primeiramente, quero destacar alguns parâmetros essenciais para o algorítimo de busca das estruturas
filamentares do universo. Definitivamente, o redshift é um dos mais importante, pois nos da a informação
do quão longe estamos procurando.

Este trabalho objetiva pegar dados de galáxias para fazer um perfil de densidade de um filamento. Dessa forma,
na tabela specObj pegaremos a coluna objType e selecionaremos dados de GALAXY que recebem o valor '0'
(URL da documentação: http://skyserver.sdss.org/dr8/en/help/browser/browser.asp).

A ferramenta de consulta do SkyServer é limitada a 90 segundos de tempo de pesquisa e 100.000 resultados. 
Se você quiser escrever consultas que retornem mais de 100.000 objetos, você precisa ser esperto:
divida sua consulta em várias partes.

## Mais sobre comandos SQL

Uma consulta SQL consiste em três partes, ou blocos: o bloco select, from e where.

O primeiro bloco, SELECT, nos diz qual coluna de dados queremos, exemplo:

SELECT ra, dec, z

O segundo bloco, FROM, vai buscar as informações especificadas na parte selecionada em uma tabela, exemplo:

FROM specObj

O terceiro, WHERE, adicionará restrições à seleção das características exatas do objeto que você deseja, por exemplo:

WHERE ra BETWEEN 130 AND 145 AND z < 0,05 AND objType='GALAXY'

Com a linhas de comandos acima, você selecionarará dados de ascensão reta e declinação de objetos
que possuem dados de espectroscopia e estão localizados na ascensão reta entre 130° e 145° com redshift 
menor que 0,05 e são galáxias.


