# SDSS-tutorial (English)

## Overview
There are over a million of astronomical objects in the Sloan Digital Sky Survey (SDSS) database, 
by asking the right question you will be able to select the exactly the object you want, for example:
the brightest, less bright or the furthest, all in seconds.

You need to write a query to get information in the database, but be carefull! The wrong query can
return Gigabytes of information, you will need to learn about the SQL language to get information from SDSS, this is a common language for working with data.

## Importants information

First, I want to talk about some parameters that we will use to code the algorithm that searches
for the filamentary structure. Definitely, the redshift is one of the most important parameters,
as it gives the information about how far away we are. The redshift of a spectrum is in the 'z'
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
which have spectroscopy data and are located on right ascension between 130?? and 145?? with redshift
less than 0.05 and they are galaxy.

# SDSS-tutorial (Portugu??s)

## Vis??o geral
Existem mais de um milh??o de objetos astron??micos na base de dados do Sloan digital Sky Survey (SDSS),
fazendo a pergunta certa voc?? poder?? encontrar o exato objeto requerido, por exemplo: o mais brilhante,
menos brilhante ou at?? mesmo o mais distante, tudo isso em quest??o de segundos.

Voc?? precisar?? escrever uma "query" para obter informa????es do banco de dados, tome cuidado! A "query"
errada pode retornar um arquivo de Gigabytes de tamanho, voc?? precisar?? aprender algumas t??cnicas da
linguagem SQL para trabalhar com esses dados, esta ?? uma ferramenta comum quando estamos estudando
grandes quantidades de dados.

## Informa????es importantes

Primeiramente, quero destacar alguns par??metros essenciais para o algoritmo de busca das estruturas
filamentares do universo. Definitivamente, o redshift ?? um dos mais importante, pois nos d?? a informa????o do qu??o longe estamos procurando.

Este trabalho objetiva pegar dados de gal??xias para fazer um perfil de densidade de um filamento. Dessa forma,
na tabela specObj pegamos a coluna objType e selecionaremos dados de GALAXY que recebem o valor '0'
(URL da documenta????o: http://skyserver.sdss.org/dr8/en/help/browser/browser.asp).

A ferramenta de consulta do SkyServer ?? limitada a 90 segundos de tempo de pesquisa e 100.000 resultados. 
Se voc?? quiser escrever consultas que retornem mais de 100.000 objetos, voc?? precisa ser esperto:
divide sua consulta em v??rias partes.

## Mais sobre comandos SQL

Uma consulta SQL consiste em tr??s partes, ou blocos: o bloco select, from e where.

O primeiro bloco, SELECT, nos diz qual coluna de dados queremos, exemplo:

SELECT ra, dec, z

O segundo bloco, FROM, vai buscar as informa????es especificadas na parte selecionada em uma tabela, exemplo:

FROM specObj

O terceiro, WHERE, adiciona restri????es ?? sele????o das caracter??sticas exatas do objeto que voc?? deseja, por exemplo:

WHERE ra BETWEEN 130 AND 145 AND z < 0,05 AND objType='GALAXY'

Com a linhas de comandos acima, voc?? selecionar?? dados de ascens??o reta e declina????o de objetos
que possuem dados de espectroscopia e est??o localizados na ascens??o reta entre 130?? e 145?? com redshift 
menor que 0,05 e s??o gal??xias.


