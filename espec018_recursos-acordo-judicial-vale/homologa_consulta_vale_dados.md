---
contrato_manutencao: nº 15210010062019 (INF. 3951)
Link HTML: http://htmlpreview.github.io/?https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/master/espec018_recursos-acordo-judicial-vale/recursos-vale-homologa-dados.html
mantis:
pull_request: '[]()'
titulo: Transparência dos recursos da Vale - Acordo Judicial 04/02/2021
output:
  html_document:
    theme: united
    toc: yes
---

# **HOMOLOGAÇÃO CONSULTA VALE - DADOS**

### CONSULTA POR PROJETO

#### 1.1 ERRO – RESTOS A PAGAR - CORRIGIDO

Foram identificadas inconsistências ao comparar os dados do portal com os dados do armazém BO.

Ao filtrar os dados de 01/01/2022 a 31/12/2022 ou utilizar o filtro 01/01/2021 a 31/12/2022 identificamos erros nas colunas relacionadas a Restos a Pagar.

Foram identificados erros nos seguintes projetos:

##### Erro 1 - 9288133 – 2022 (todas as colunas de Restos a Pagar) - CORRIGIDO
	- vários empenhos (erro no cálculo da Despesa Liquidada)
  
![image](https://user-images.githubusercontent.com/52920939/171876085-c6f06620-35a3-4a46-8b44-22aed92e749f.png)

 
##### Erro 2 - 9288152 – 2022 (erro na coluna Valor Despesa Liquidada – Restos a Pagar) - CORRIGIDO
	- empenho 625  (erro no cálculo da Despesa Liquidada) 
  
![image](https://user-images.githubusercontent.com/52920939/171876127-c53f36c8-47c9-4051-b4e3-059772842110.png)

![image](https://user-images.githubusercontent.com/52920939/171876182-9b0bc953-a75b-4c99-b856-b1dbf70010ed.png)

##### Erro 3 - 9288191 – 2022 (erro na coluna Valor Despesa Liquidada – Restos a Pagar) - CORRIGIDO
	- empenho 14 (erro no cálculo da Despesa Liquidada)
 
![image](https://user-images.githubusercontent.com/52920939/171876229-cd428ca5-6825-4cbd-8eb7-30bc025fde85.png)

![image](https://user-images.githubusercontent.com/52920939/171876255-aeead151-43cf-4d8d-a7a1-0392e22678ba.png)


#### 1.2 ERRO – LISTA DOS EMPENHOS NO NÍVEL 2

Ao clicar em um projeto, o nível 2 da consulta apresenta a lista de empenhos. No entanto, o portal está considerando apenas os empenhos que tiveram execução no ano de 2022.

##### Correção 1: uma linha para cada ano do empenho
Para essa consulta, o portal deve listar todos os empenhos referentes ao projeto selecionado, independente de qual ano ele se refere, separando uma linha para cada ano.
E em cada linha deve ser informada apenas os dados a que se refere o ano da linha.
- Projeto 9288134
 
![image](https://user-images.githubusercontent.com/52920939/171876296-b43ef78c-e0be-43e5-aae3-7c7089918a39.png)


Utilize o mesmo comportamento adotado na consulta avançada.
 
![image](https://user-images.githubusercontent.com/52920939/171876322-587e1266-4772-4526-a504-e224274cac69.png)


 
##### Correção 2: acrescentar coluna PERÍODO
Além de listar todos os empenhos, o Portal deverá incluir uma coluna PERÍODO entre a coluna Empenho e a coluna Data de Registro do Empenho.

![image](https://user-images.githubusercontent.com/52920939/171876354-91911fb8-a5f8-4617-b5ec-5d0f8c8f61f9.png)
 

##### Correção 3: ocultar empenhos sem execução
Deverão ser listados apenas os empenhos que possuem execução nas colunas existentes do Portal. Caso algum empenho apareça zerado, essa linha do Portal não deverá ser exibida.

Exemplo: Empenho 237 da Controladoria Geral do Estado (projeto 9288155). Como não há execução nas colunas do Portal, essa linha não deverá ser exibida para esse projeto.
 
![image](https://user-images.githubusercontent.com/52920939/171876384-aa050669-9cac-4ddf-ba9b-c6603ba9241b.png)

 
### CONSULTA POR EXECUÇÃO

#### 2.1 ERRO – RESTOS A PAGAR

Verificar o item relatado na consulta por projeto – 1.1 – ERRO – RESTOS A PAGAR

#### 2.2 LISTA DA EXECUÇÃO DOS PROJETOS – NÍVEL 1- 

##### Situação: FILTRO COM MAIS DE 1 ANO
Ao selecionar no filtro de período, a opção com mais de 1 ano, o portal deverá apresentar o somatório dos dados de execução do filtro selecionado, e não a linha duplicada. 

![image](https://user-images.githubusercontent.com/52920939/171876420-d07bc0df-12bc-4f41-93f8-8e5c163236bd.png)

![image](https://user-images.githubusercontent.com/52920939/171876459-c3ff90aa-46cc-42b4-8641-291c95c2fa15.png)


#### 2.3 ERRO – LISTA DE EMPENHOS – consulta nível 2

Na consulta por execução, a lista de empenhos deve ter comportamentos distintos conforme o período da consulta selecionada.

##### Situação 1 – Filtro dentro de um mesmo ano.

Ao selecionar o filtro de período, por exemplo 01/01/2021 a 31/12/2021, devem ser listados todos os empenhos referentes ao ano selecionado com a execução somente daquele ano.

Exemplo 9288138 – empenhos 01/01/2021 a 31/12/2021 – dados apresentados apenas de 2022

![image](https://user-images.githubusercontent.com/52920939/171876512-ea57ef76-9387-44ad-94bf-4a904fe4f94c.png)
 
##### Situação 2 – Filtro com mais de um ano.

Ao selecionar o filtro de período, por exemplo 01/01/2021 a 31/12/2022, devem ser listados todos os empenhos referentes ao ano selecionado, adotando o comportamento de exibição de linhas para cada ano da execução do empenho e não o comportamento de somatório desses empenhos.

![image](https://user-images.githubusercontent.com/52920939/171876550-3f671656-bef3-48b1-9e05-0c129b754017.png)

 
Exemplo 9288134 – empenho 147 – exibição de uma linha para cada ano, informando em cada linha apenas a execução referente aquele ano. Além disso, deve ser acrescentada uma coluna PERÍODO entre a coluna Empenho e a coluna Data de Registro do Empenho.

![image](https://user-images.githubusercontent.com/52920939/171876586-b69c372c-44c7-498e-8e4b-7b2d275ba53c.png)
 
Utilize o mesmo comportamento adotado na consulta avançada.
 
![image](https://user-images.githubusercontent.com/52920939/171876619-b21811ae-d6f0-4464-a14d-57684cd66bc5.png)


#### 2.4 OCULTAR EMPENHOS SEM EXECUÇÃO
Verificar o item - Correção 3: ocultar empenhos sem execução


### 3. CONSULTA AVANÇADA

#### 3.1 ERRO NA EXIBIÇÃO DO DETALHAMENTO DO EMPENHO

Ao clicar para exibir os empenhos de um projeto, o link do portal não apresentando os dados;
 
![image](https://user-images.githubusercontent.com/52920939/171876661-b16c6221-18a1-4a96-8632-6b80320d9cf0.png)

#### 3.2 EXIBIR/OCULTAR CÓDIGO 

Ao selecionar o botão exibir/ocultar código o portal não está apresentando diferença. O comportamento está sendo o de exibir o código selecionando ou não o botão.
 
![image](https://user-images.githubusercontent.com/52920939/171876695-1372337a-0e0f-4ca8-b5c5-b504c56efc3a.png)

 
#### 3.3 ADICIONAR/REMOVER COLUNAS
O botão adicionar ou remover colunas não está habilitado
 
![image](https://user-images.githubusercontent.com/52920939/171876729-90240ec4-dfea-49aa-9fa1-a37088c1f143.png)


#### 3.4 OCULTAR EMPENHOS SEM EXECUÇÃO
Verificar o item - Correção 3: ocultar empenhos sem execução
Ao filtro o dado órgão 1521 – Controladoria Geral do Estado – ano de 2022, a consulta traz informações do empenho 237 que ainda não teve execução.

![image](https://user-images.githubusercontent.com/52920939/171876776-fd717e45-5c83-4067-90f8-d16f8c40999b.png)

#### 3.5 BOTÃO SAIR
Quando clicamos em sair após a aplicação de um filtro, a página retorna para um erro. O correto é voltar para a página inicial da consulta da Vale.
 
![image](https://user-images.githubusercontent.com/52920939/171876803-62e05d2b-49b2-45a8-83da-6f2f42da970d.png)

#### 3.6 BOTÃO LIMPAR TUDO
Quando clicamos no botão LIMPAR TUDO, o botão limpa os dados da exibição, mas não tem limpado os dados dos filtros selecionados.
Exemplo: cliquei em limpar tudo, e ao voltar no código projeto, o último projeto permaneceu selecionado.
 
![image](https://user-images.githubusercontent.com/52920939/171876836-bdacacea-a93a-4459-8e18-762baa606310.png)
 
### 4. CONSULTA POR MUNICIPIO

Foram identificados empenhos na consulta por munícipio que não possuem informações de execução.
Nesse caso, os empenhos não deverão ser aparecer na consulta.
Exemplo: 4395 – projeto 9288130

![image](https://user-images.githubusercontent.com/52920939/171876861-b7c2457e-6ffb-4708-b89b-1e1845f3b44e.png)

Exemplo 4400 – projeto 9288130

![image](https://user-images.githubusercontent.com/52920939/171876901-2ca623df-b883-4583-b111-b2cb0a0228a0.png)
