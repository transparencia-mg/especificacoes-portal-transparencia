---
titulo: "Nova especificação da Consulta Restos a pagar"
pull_request:https://github.com/transparencia-mg/especificacoes-portal-transparencia/pull/3


# Visão geral da demanda

Essa demanda visa acrescentar modos de pesquisa adicionais a [consulta de Restos a Pagar](http://www.transparencia.mg.gov.br/despesa-estado/restos-a-pagar), nos moldes da [consulta de Despesa](http://www.transparencia.mg.gov.br/despesa-estado/despesa). Devem ser acrescentados os modos de pesquisa:

1. Filtro favorecido por nome;
2. Filtro favorecido por CPF/CNPJ;
3. Pesquisa Avançada.

Os filtros dos três modos de pesquisa devem possuir funcionalidade de autocompletar (eg. [consulta compras](http://www.transparencia.mg.gov.br/compras-e-patrimonio/compras-e-contratos)) com possibilidade de seleção múltipla. O escopo das sugestões deve se restringir aos valores existentes no ano corrente, indicando caso nenhuma correspondência for encontrada.

### _Observações gerais:_

* __Filtro favorecido por CPF/CNPJ__: O filtro por CPF/CNPJ deve realizar autocomplete e buscar com CPFs/CNPJs formatados ou númericos.

* __Pesquisa Avançada__: A pesquisa avançada deve possuir um botão de marcar/desmarcar todas as colunas. Além disso, o autocomplete da pesquisa avançada deve possuir código e descrição das classificações orçamentárias (eg. [consulta proposta orçamentária](http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/proposta-orcamentaria/proposta-pesquisa-avancada))

# Motivação / contexto da demanda

As consultas do Portal de Transparência possuem como padrão a possibilidade de pesquisa por meio de filtros (eg. [_Filtro Favorecido - Consulta Despesas_](http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-favorecidos/2019/01-01-2019/31-12-2019/0/LUCIANA%20CASSIA%20NOGUEIRA/0/3)) e pesquisa avançada (eg. [_Pesquisa Avançada - Consulta Despesa_](http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-pesquisa-avancada)). No entanto, na reestruturação do Portal de Transparência, ocorrida entre 2015 e 2017, a consulta de Restos a Pagar não foi contemplada com essa possibilidade, sendo disponibilizada apenas com o filtro de [pesquisa Órgão](http://www.transparencia.mg.gov.br/despesa-estado/restos-a-pagar).

Atualmente, a Diretoria Central de Transparência Ativa têm recebidos diversos questionamentos por do telefone do Portal quanto a não possibilidade de outras formas de pesquisa na consulta de Restos a Pagar. Nesse sentido, com o objetivo de ofertar mais opções aos usuários essa nova especificação visa acrescentar os filtros de favorecidos por nome e CPF/CNPJ e pesquisa avançada nos moldes da consulta de despesa.

A decisão de acrescentar apenas os filtros mencionados acima se deve ao levantamento realizado no google analytics considerando como parâmetro os filtros da consulta de despesa.

Conforme tabela abaixo os filtros por Programa e função são poucos utilizados.

| Filtros Consulta Despesa  | Acessos   | %       |
|---------------------------|----------:|--------:|
| Órgãos                    |   132.412 |  86,40% |
| Programa                  |       429 |   0,28% |
| Função                    |     4.179 |   2,73% |
| Favorecido                |    16.235 |  10,59% |
| ___Total de sessões___    |___153.255___

  __Fonte__: Google Analytics -período jan/2019 a 23/out/2019


# Especificação

## Página Inicial

Para contemplar a inclusão dos novos filtros a página inicial deverá sofrer alterações conforme abaixo:

 O cidadão seleciona a opção Restos a pagar e o Portal exibirá:

* __Ano da consulta (aaaa)__: Conforme padrão adotado atualmente.

* __Consulta__: Órgão, Favorecido por nome, Favorecido por CPF/CNPJ.

* __Filtro:__ Exibir filtro para selecionar uma opção.

* __Data Ínicio e Fim__: Conforme padrão adotado atualmente
*__Pesquisar__: Conforme padrão adotado atualmente
* __Pesquisa Avançada__:

Exemplo:
![Pagina Inicial](static/pagina-inicial.png)

|Ano| Consulta| Filtro|Início|Fim|Pesquisa|Pesquisa Avançada|
|---|:---------|-------|------|---|--------|-----------------|
|   |Órgão (Consulta Principal)
|   |Favorecido nome
|   |Favorecido por CPF/CNPJ

### Observações Gerais

* O filtro favorecido por Nome deve ter a opção de autocomplete;

* O filtro favorecido por Nome deve permitir que o cidadão digite qualquer parte do nome e o portal retornará todos os itens que encaixem na pesquisa;

* O filtro favorecido por CPF/CNPJ deve realizar a busca com CPFs/CNPJs formatados ou númericos.

* A Pesquisa Avançada deve possuir um botão de marcar/desmarcar todas as colunas. Além disso, o autocomplete da pesquisa avançada deve possuir código e descrição das classificações orçamentárias (eg. consulta proposta orçamentária);

* Todas as páginas da consulta devem exibir ícones com links para compartilhar consultas no facebook e twitter e a possibilidade de fazer download da planilha completa em csv, exportar para pdf e imprimir conforme padrão já adotado em outras consultas do Portal;

* Todas as páginas devem exibir cabeçalho e legenda da tabela e “migalhas” conforme padrão;

* Todos os gráficos da consulta irão buscar a o valor pago no ano e apresentar legenda conforme o já adotado em outras consultas.

* Em todos os níveis o cidadão poderá avançar para os próximos níveis tanto clicando no gráfico quanto na tabela.

## Consulta Favorecido por nome

__1º nível (Favorecido)__

O portal exibirá a opção de escolher tipo da consulta e, ao selecionar o tipo _[Favorecido por nome]_, permitirá que o cidadão escreva o nome completo ou parte do nome do favorecido. O Portal retornará todos os resultados que se encaixem no termo informado do filtro.

O Portal da Transparência irá listar o resultado da consulta em um gráfico treemap e em tabela.

<<Título do gráfico: Favorecidos>>

![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Favorecido| CNPJ/CPF|Valor inscrito processado| Valor não inscrito processado| Valor pago no ano| Valor a pagar|
|-----|-----|-----|-----|-----|---
|_Link para o próximo nível_


__2º nível (Elemento de Despesa)__

Ao clicar no nome do _[Favorecido]_ o Portal exibirá um gráfico treemap e uma tabela.

<<Título do gráfico: Nome do favorecido selecionado no nível anterior>>
![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Categoria Econômica|Grupo de Despesa| Elemento de Despesa| Valor inscrito processado| Valor não inscrito processado|Valor pago no ano | Valor a pagar
|-----|-----|-----|-----|-----|---|----
|||_Link para o próximo nível_

__3º nível (Item de despesa)__

Ao clicar no _[Elemento de despesa]_ o Portal exibirá um gráfico treemap e uma tabela.

<<Título do gráfico: Nome do elemento de despesa selecionado no nível anterior>>
![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Fonte de Recursos| Modalidade de Aplicação| Item de Despesa| Valor inscrito processado| Valor não inscrito processado|Valor pago no ano|Valor a pagar
|-----|-----|-----|-----|-----|---|----|
|||_Link para o próximo nível_

__4º nível (Órgão)__

Ao clicar em _[Item de despesa]_ o Portal exibirá um gráfico treemap e uma tabela.

<<Título do gráfico: Nome do item de despesa selecionado no nível anterior>>
![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Código| Órgão| Valor inscrito processado| Valor não inscrito processado| Valor pago no ano | Valor a pagar|
|-----|-----|-----|-----|-----|---|
||_Link para o próximo nível_

__5º nível (Número de Empenho)__

Ao clicar em _[órgão]_ o Portal exibirá e uma tabela.

|Data|Número do Empenho| Valor inscrito processado| Valor não inscrito processado| Valor pago no ano | Valor a pagar
|-----|-----|-----|-----|-----|---|
||_Link para o próximo nível_

___OBS: A data deverá ser a data de registro inicial do empenho___


__6º nível (Formulário de detalhamento)__

Ao clicar no _[número do empenho]_ o Portal exibirá o Formulário de detalhamento igual ao utilizado atualmente na consulta por órgão.

![Formulário de detalhamento](static/formulario-detalhamento.png)


## Consulta Favorecido por CPF/CNPJ

Os níveis desse filtro serão os mesmos da consulta _[Favorecido por nome]_

## Consulta Função

__1º nível (Função)__

O portal exibirá a opção de escolher tipo da consulta e, ao selecionar o tipo _[Função]_, permitirá que o cidadão escreva o nome da função ou selecione uma função na lista. O Portal retornará todos os resultados que se encaixem no termo informado do filtro.

O Portal da Transparência irá listar o resultado da consulta em um gráfico treemap e em tabela.

<<Título do gráfico: Funções>>

![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Função|Valor inscrito processado| Valor não inscrito processado| Valor pago no ano| Valor a pagar|
|-----|-----|-----|-----|----
|_Link para o próximo nível_

__2º nível (Subfunção)__

Ao clicar no nome da _[Função]_ o Portal exibirá um gráfico treemap e uma tabela. O cidadão poderá navegar pelos níveis de detalhamento tanto no gráfico quanto na tabela.

<< Título do gráfico: Nome da função selecionada no nível anterior>>
![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Código|Subfunção|Valor inscrito processado| Valor não inscrito processado|Valor pago no ano | Valor a pagar
|-----|-----|-----|-----|-----|---|
||_Link para o próximo nível_

__3º nível (órgão)__

Ao clicar na _[Subfunção]_ o Portal exibirá um gráfico treemap e uma tabela.

<< Título do gráfico: Nome da Subfunção selecionado no nível anterior>>
![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Código|Órgão| Valor inscrito processado| Valor não inscrito processado|Valor pago no ano|Valor a pagar
|-----|-----|-----|-----|-----|--
||_Link para o próximo nível_

__4º nível (Programa)__

Ao clicar em _[Órgão]_ o Portal exibirá um gráfico treemap e uma tabela.

<< Título do gráfico: Nome do órgão selecionado no nível anterior>>

![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Código do Programa|Programa| Valor inscrito processado| Valor não inscrito processado| Valor pago no ano | Valor a pagar|
|-----|-----|-----|-----|-----|---|
||_Link para o próximo nível_


__5º nível (Ação)__

Ao clicar no nome do _[Programa]_  Portal exibirá um gráfico treemap e uma tabela

<< Título do gráfico: Nome do programa selecionado no nível anterior>>

![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Código da Ação|Ação| Valor inscrito processado| Valor não inscrito processado| Valor pago no ano | Valor a pagar|
|-----|-----|-----|-----|-----|---|
||_Link para o próximo nível_

__6º nível (Elemento de Despesa)__

Ao clicar no nome da _[ação]_ o Portal exibirá um gráfico treemap e uma tabela.

<<Título do gráfico: Nome da Ação selecionada no nível anterior>>
![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Categoria Econômica|Grupo de Despesa| Elemento de Despesa| Valor inscrito processado| Valor não inscrito processado|Valor pago no ano | Valor a pagar
|-----|-----|-----|-----|-----|---|----
|||_Link para o próximo nível_

__7º nível (Favorecido)__

Ao clicar no nome do _[Elemento de despesa]_ o Portal exibirá um gráfico treemap e uma tabela.

<<Título do gráfico: Nome do Elemento de despesa selecionado no nível anterior>>

![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Favorecido| CNPJ/CPF|Valor inscrito processado| Valor não inscrito processado| Valor pago no ano| Valor a pagar|
|-----|-----|-----|-----|-----|---
|_Link para o próximo nível_

__8º nível (Lista dos empenhos)__

Ao clicar no nome do _[Favorecido]_ o Portal exibirá uma tabela.

|Data|Número do Empenho| Valor inscrito processado| Valor não inscrito processado| Valor pago no ano | Valor a pagar
|-----|-----|-----|-----|-----|---|
||_Link para o próximo nível_

___OBS: A data deverá ser a data de registro inicial do empenho___

__8º nível (Formulário de detalhamento)__

Ao clicar no número do empenho o Portal exibirá o Formulário de detalhamento igual ao utilizado atualmente na consulta por órgão.

![Formulário de detalhamento](static/formulario-detalhamento.png)

## Consulta Programa

__1º nível (Programa)__

O portal exibirá a opção de escolher tipo da consulta e, ao selecionar o tipo _[Programa]_, permitirá que o cidadão escreva o nome da função ou selecione um programa na lista. O Portal retornará todos os resultados que se encaixem no termo informado do filtro.

O Portal da Transparência irá listar o resultado da consulta em um gráfico treemap e em tabela.

<<Título do gráfico: Programas>>

![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Código do Programa|Programa| Valor inscrito processado| Valor não inscrito processado| Valor pago no ano | Valor a pagar|
|-----|-----|-----|-----|-----|---|
||_Link para o próximo nível_

__2º nível (Órgão)__

Ao clicar no _[Programa]_ o Portal exibirá um gráfico treemap e uma tabela.

<< Título do gráfico: Nome do Programa selecionado no nível anterior>>
![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Código|Órgão| Valor inscrito processado| Valor não inscrito processado|Valor pago no ano|Valor a pagar
|-----|-----|-----|-----|-----|--
||_Link para o próximo nível_

__3º nível (Ação)__

Ao clicar no _[Órgão]_ o Portal exibirá um gráfico treemap e uma tabela.

<< Título do gráfico: Nome do Órgão selecionado no nível anterior>>
![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Código da Ação|Ação| Valor inscrito processado| Valor não inscrito processado|Valor pago no ano|Valor a pagar
|-----|-----|-----|-----|-----|--
||_Link para o próximo nível_

__4º nível (Elemento de Despesa)__

Ao clicar no nome da _[ação]_ o Portal exibirá um gráfico treemap e uma tabela.

<<Título do gráfico: Nome da Ação selecionada no nível anterior>>
![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Categoria Econômica|Grupo de Despesa| Elemento de Despesa| Valor inscrito processado| Valor não inscrito processado|Valor pago no ano | Valor a pagar
|-----|-----|-----|-----|-----|---|----
|||_Link para o próximo nível_

__5º nível (Favorecido)__

Ao clicar no nome do _[Elemento de despesa]_ o Portal exibirá um gráfico treemap e uma tabela.

<<Título do gráfico: Nome do Elemento de despesa selecionado no nível anterior>>

![modelo-grafico-treemap](static/modelo-grafico-treemap.png)

|Favorecido| CNPJ/CPF|Valor inscrito processado| Valor não inscrito processado| Valor pago no ano| Valor a pagar|
|-----|-----|-----|-----|-----|---
|_Link para o próximo nível_

__6º nível (Lista dos empenhos)__

Ao clicar no nome do _[Favorecido]_ o Portal exibirá uma tabela.

|Data|Número do Empenho| Valor inscrito processado| Valor não inscrito processado| Valor pago no ano | Valor a pagar
|-----|-----|-----|-----|-----|---|
||_Link para o próximo nível_

___OBS: A data deverá ser a data de registro inicial do empenho___

__7º nível (Formulário de detalhamento)__

Ao clicar no número do empenho o Portal exibirá o Formulário de detalhamento igual ao utilizado atualmente na consulta por órgão.

![Formulário de detalhamento](static/formulario-detalhamento.png)

## Consulta Avançada

A consulta avançada terá 12 campos de filtro simples e parâmetro de ano:
1. Órgão
2. Função
3. Subfunção
4. Programas
5. ação
6. Categoria Econômica
7. Grupo de Despesa
8. Modalidade de Aplicação
9. Elemento de despesa
10. Item de Despesa
11. Fonte de Recursos
12. Identificador de Procedência e Uso (IPU)

O usuário poderá escolher em exibir ou não a lista dos favorecidos. Como padrão o portal não exibirá os favorecidos.

Favorecidos
- [ ] Exibir favorecidos
- [x] Não exibir Favorecidos

__OBS: Ao exibir o favorecido o Portal deverá retornar o nome e CNPJ/CPF do favorecido, conforme já ocorre na consulta de despesa.__

O cidadão poderá informar mais de um valor para cada filtro. Ao informar um valor de filtro, listar todas as opções e disponibilizar ao cidadão a funcionalidade de autocompletar (desde a primeira letra), desconsiderando acentuação, letras maiúsculas/minúsculas e palavras intermediárias (ex.: Ao digitar "gestao pública", um dos resultados será "Gestão da Administração Pública").

Se o cidadão não informar um valor para cada filtro, o Portal da Transparência considerará todos os valores possíveis para cada filtro não informado.

O cidadão poderá escolher os campos que ele quer que apareça no resultado (seguir modelo das demais consultas).

O cidadão deverá escolher o ano da pesquisa.

Ao exibir o resultado na tabela a consulta deverá retornar as colunas valor inscrito processado, valor inscrito não processado, valor pago no ano e valor a pagar.

# Dependências / Integrações

A integração será realizada com o armazém do SIAFI (BO) conforme ocorre atualmente.

# Exemplos

Seguir o modelo atual da [consulta de Despesa](http://www.transparencia.mg.gov.br/despesa-estado/despesa) do Portal de Transparência

# Dúvidas

## Técnicas

* O número de campos na pesquisa avançada impacta a estimativa de horas? Incluir favorecido como campo de filtro na consulta avançada impacta na estimativa de horas?

* Avaliar junto a Prodemge a possibilidade do cidadão não ter que digitar 3 digitos par exibir a lista dos favorecidos na consulta Favorecido por nome. Nesse sentido o filtro favorecido por nome deverá permitir que o cidadão digite qualquer parte do nome e o portal retornará todos os itens que encaixem na pesquisa.

## Negócio

  2. Avaliar a real necessidade de acrescentar todos os filtros, uma vez que conforme levantamento realizado no google analytics, considerando a consulta de despesa, os filtros mais utilizados são:

  * __Período analisado__: jan/2019 a 23/out/2019
  * __Total de acessos na consulta de despesa__: 153.255 sessões

      | Filtros    | Acessos   | %       |
      |------------|----------:|--------:|
      | Órgãos     |   132.412 |  86,40% |
      | Programa   |       429 |   0,28% |
      | Função     |     4.179 |   2,73% |
      | Favorecido |    16.235 |  10,59% |
      | __Total__  |__153.255__|         |

3. Avaliar se a navegação por nível deverá espelhar a da Consulta de Despesa.
