---
titulo: "Anonimização dos CPFs"
pull_request: [espec001](https://github.com/transparencia-mg/especificacoes-portal-transparencia/pull/1)
---

# Visão geral da intervenção


# Motivação / contexto da intervenção

A exigência de a administração pública divulgar informações consta na Lei Complementar nº 101/2000 (Lei de Responsabilidade Fiscal- LRF) que foi  complementada pelo Decreto Federal n° 7.185/2010, que regulamentou os padrões mínimos de qualidade da informação e reforçou o entendimento da divulgação dos dados em sentido amplo:

> _“Art.7º Sem prejuízo dos direitos e garantias individuais constitucionalmente estabelecidos, o SISTEMA deverá gerar, para disponibilização em meio eletrônico que possibilite amplo acesso público, pelo menos, as seguintes informações relativas aos atos praticados pelas unidades gestoras no decorrer da execução orçamentária e financeira:_
>
> _I - quanto à despesa:_
>
>_[...]_
>
> _d) a pessoa física ou jurídica beneficiária do pagamento, inclusive nos desembolsos de operações independentes da execução orçamentária, exceto no caso de folha de pagamento de pessoal e de benefícios previdenciários.”_

Nesse sentido, atualmente, o Portal da Transparência divulga nas consultas de Despesa e Restos a pagar informações completas (nome e CPF) de todos os credores que recebem benefícios previdenciários do Estado, contrariando o Decreto em questão.

Entretanto, sua divulgação tem sido objeto de questionamentos pela sociedade. Assim, com a finalidade de atender plenamente o que determina a legislação a Diretoria Central de Transparência Ativa (DTA), unidade responsável pela gestão do Portal da Transparência, propõe a alteração da forma de exibição do dados nessas consultas.

Destaca-se ainda que as demais consultas, como por exemplo, convênios e remuneração não sofrerão alterações, uma vez que, o entendimento corrente é o de que a divulgação de informações completas e íntegras possibilita a qualquer cidadão conhecer, questionar e atuar como fiscal da aplicação dos recursos públicos, para o exercício do controle social – pois está possibilitado o cruzamento de dados dos beneficiários de políticas públicas.

# Especificação

## Consulta Despesa

1. Quando o usuário realizar o download dos dados, esses deverão ser exibidos anonimizados conforme o especificado. No entanto, a base deverá conter a informação completa.

2. A anonimização será aplicada apenas nos credores pessoas físicas que receberem valores na classificação dos elementos de despesa listados abaixo.

|Código|Descrição|
|-------|:--------|
|01| aposentadorias do rpps, reserva remunerada e reformas dos militares|
|03| pensões do RPPS e do militar|
|05| Outros benefícios previdenciários do servidor militares
|59| Pensões especiais
|31.2|premiacoes culturais, artisticas, cientificas, desportivas e outras / prêmios lotéricos|



### Consulta por Órgão

* 1º nível (Filtro Órgão) - Não haverá alteração

* 2º nível (Filtro Função) - Não haverá alteração
* 3º nível (Filtro Elemento de Despesa) - Não haverá alteração
* 4º nível (Filtro Favorecido):

Ao clicar no ___Elemento de despesa___ listados no item 5, o Portal exibirá um gráfico treemap e uma tabela. O cidadão poderá navegar pelos níveis de detalhamento tanto no gráfico quanto na tabela. Dados da tabela:

|Favorecido| CNPJ/CPF | Item de despesa | Valor Empenhado |Valor Liquidado| Valor Pago|
|---------|--------|---------------|-----------|----------|---------|

As regras para anonimização são:

 * __Campo Favorecido:__ Exibir apenas as iniciais do nome do favorecido.

 * __Campo CPF:__ Ocultar os 3 dos três primeiros e dos dois últimos dígitos verificadores.

  _Exemplo:_

  ___Favorecido:___ Cassio Gustavo de Castro - CPF: 028.659.616.48

  O Portal deverá exibir da seguinte forma:

|Favorecido| CNPJ/CPF | Item de despesa | Valor Empenhado |Valor Liquidado| Valor Pago|
|---------:|:--------:|:---------------:|:-----------:|:----------:|:---------|
|C.G.C     |** .659.616-**|Auxílio Reclusão| 10.000,00|10.000,00|10.000,00|


* 5º nível (Formulário de Detalhamento): Os campos do formulário de detalhamento deverão seguir as regras descritas acima.

___Empenho da despesa:___

_Campo Razão Social do Credor:_ Nesse campo deverá ser exibido o nome do favorecido e CPF descaracterizado conforme regra mencionada acima.

![Empenho da Despesa](static/empenho_despesa.png)

___Liquidação e Pagamento___

_Campo CNPJ/CPF e Descrição do Favorecido:_ Deverá ser exibido o nome do favorecido e CPF descaracterizado conforme regra mencionada acima.

![Liquidação e Pagamento](static/liquidacao_pagamento.png)

### Consulta por Função

* 1º nível (Filtro Função) - Não haverá alteração
* 2º nível (Filtro Subfunção) - Não haverá alteração
* 3º nível (Filtro Órgão) - Não haverá alteração
* 4º nível (Filtro Programa) - Não haverá alteração
* 5º nível (Filtro Ação) - Não haverá alteração
* 6º nível (Filtro Elemento de despesa): Não haverá alteração
* 7º nível (Filtro Favorecido): __Mesmas alterações aplicadas no 4º nível (Filtro Favorecido) da consulta por órgão.__
* 8º nível (Formulário de Detalhamento): __Mesmas alterações aplicadas no formulário de detalhamento da consulta por órgão.__.

### Consulta por Programa

* 1º nível (Filtro Programa) - Não haverá alteração
* 2º nível (Filtro Órgão) - Não haverá alteração
* 3º nível (Filtro Ação) - Não haverá alteração
* 4º nível (Filtro Elemento de despesa)- Não haverá alteração
* 5º nível (Filtro Favorecido) - __Mesmas alterações aplicadas no 4º nível (Filtro Favorecido) da consulta por órgão.__
* 6º nível (Formulário de Detalhamento): __Mesmas alterações aplicadas no formulário de detalhamento da consulta por órgão.__.

### Consulta por Favorecido Nome

O portal exibirá a opção para escolher o período da consulta – formato aaaa.

O portal exibirá a opção de escolher tipo da consulta e, ao selecionar o tipo ___Favorecido por nome___, permitirá que o cidadão escreva o nome do favorecido e retornará todos os resultados que se encaixem no termo informado do filtro.

___OBSERVAÇÃO___: O Portal deverá exibir os favorecidos que apresentem a anonimização, contudo a sua exibição deverá seguir as regras estabelecidas.

O Portal da Transparência irá listar o resultado da consulta em um gráfico treemap e em tabela.  O cidadão poderá navegar pelos níveis de detalhamento tanto no gráfico quanto na tabela.

* 1º nível (Filtro Favorecido) - __Mesmas alterações aplicadas no 4º nível (Filtro Favorecido) da consulta por órgão.__

* 2º nível (Filtro Elemento de despesa) - Não haverá alteração
* 3º nível (Filtro Item de despesa) - Não haverá alteração
* 4º nível* (Filtro Órgão) - Não haverá alteração
* 5º nível (Formulário de Detalhamento): __Mesmas alterações aplicadas no formulário de detalhamento da consulta por órgão.__.

### Consulta por Favorecido CPF/CNPJ

O portal exibirá a opção para escolher o período da consulta – formato aaaa.
O portal exibirá a opção de escolher tipo da consulta e, ao selecionar o tipo ___Favorecido por CPF/CNPJ___, permitirá que o cidadão escreva o número do CPF ou CNPJ do favorecido e retornará todos os resultados que se encaixem no termo informado do filtro.

___OBSERVAÇÃO___: Os favorecidos que apresentarem o CPF anonimizado deverão ser exibidos no resultado da busca, contudo a sua exibição seguirá as regras estabelecidas.

O Portal da Transparência irá listar o resultado da consulta em um gráfico treemap e em tabela.  O cidadão poderá navegar pelos níveis de detalhamento tanto no gráfico quanto na tabela.

* 1º nível (Filtro Favorecido) - __Mesmas alterações aplicadas no 4º nível (Filtro Favorecido) da consulta por órgão.__

* 2º nível (Filtro Elemento de despesa) - Não haverá alteração
* 3º nível (Filtro Item de despesa) - Não haverá alteração
* 4º nível (Filtro Órgão) -Não haverá alteração
* 5º nível (Formulário de Detalhamento): __Mesmas alterações aplicadas no formulário de detalhamento da consulta por órgão.__.

### Pesquisa Avançada

Quando o cidadão selecionar o campo ___Exibir favorecidos___” o Portal deverá retornar a lista dos favorecidos que correspondem aos elementos da despesa especificados na alínea com o nome e CPF anonimizados conforme o estabelecido.

## Especificação da consulta Restos a pagar

Todas as páginas da consulta deverão exibir ícones com links para compartilhar consultas no facebook e twitter e a possibilidade de fazer download da planilha completa em csv, exportar para pdf e imprimir conforme padrão já adotado em outras consultas do Portal. Exibir cabeçalho e legenda da tabela e “migalhas” conforme padrão.

Todos os gráficos da consulta irão buscar a o valor pago no ano conforme o já adotado em outras consultas.

Todos dos gráficos deverão apresentar legenda conforme o já adotado em outras consultas.

### Consulta por Órgão

* 1º nível (Filtro Órgão) - Não haverá alteração
* 2º nível (Filtro Elemento de despesa) - Não haverá alteração
* 3º nível (Filtro Item de despesa) - Não haverá alteração
* 4º nível (Filtro Favorecido):

Ao clicar no ___Item de despesa___ listados no irem 5 o Portal exibirá uma tabela. Dados da tabela:

|Favorecido| CNPJ/CPF | Número do empenho | valor inscrito processado |valor inscrito não processado| valor pago no ano| valor a pagar|
|---------|--------|---------|-----------|----------|---------|--------|

Regras para anonimização:

* __Campo Favorecido:__ Exibir apenas as iniciais do nome do favorecido.

* __Campo CPF:__ Ocultar os 3 dos três primeiros e dos dois últimos dígitos verificadores.

_Exemplo:_

___Favorecido:___ Cassio Gustavo de Castro - CPF: 028.659.616.48

O Portal deverá exibir da seguinte forma:

|Favorecido| CNPJ/CPF | Número do empenho | valor inscrito processado |valor inscrito não processado| valor pago no ano| valor a pagar|
|---------|--------|---------|-----------|----------|---------|--------|
|C.G.C|** .659.616-**|316| 10.000,00|0,00|10.000,00|0,00|


* 5º nível (Formulário de Detalhamento): __Mesmas alterações aplicadas no formulário de detalhamento da consulta por órgão.__.

# Dúvidas / Pendências

Dúvidas???

Grupo 3 / Elemento: OUTROS SERVICOS DE TERCEIROS - PESSOA FISICA / Item de despesa: Estagiários????
Grupo 3 / Elemento 13: Obrigações Patronais / Item: INSS – Demais Despesas

----FIM----
