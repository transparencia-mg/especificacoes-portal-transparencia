# Visão geral da demanda

Essa demanda visa acrescentar modos de pesquisa adicionais a [consulta de Restos a Pagar](http://www.transparencia.mg.gov.br/despesa-estado/restos-a-pagar), nos moldes da [consulta de Despesa](http://www.transparencia.mg.gov.br/despesa-estado/despesa). Devem ser acrescentados os modos de pesquisa:

1.  Filtro favorecido por nome;
2.  Filtro favorecido por CPF/CNPJ;
3.  Pesquisa Avançada.

Os filtros dos três modos de pesquisa devem possuir funcionalidade de autocompletar (eg. [consulta compras](http://www.transparencia.mg.gov.br/compras-e-patrimonio/compras-e-contratos)) com possibilidade de seleção múltipla. O escopo das sugestões deve se restringir aos valores existentes no ano corrente, indicando caso nenhuma correspondência for encontrada.

### _Observações gerais:_

*   **Filtro favorecido por CPF/CNPJ**: O filtro por CPF/CNPJ deve realizar autocomplete e buscar com CPFs/CNPJs formatados ou númericos.

*   **Pesquisa Avançada**: A pesquisa avançada deve possuir um botão de marcar/desmarcar todas as colunas. Além disso, o autocomplete da pesquisa avançada deve possuir código e descrição das classificações orçamentárias (eg. [consulta proposta orçamentária](http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/proposta-orcamentaria/proposta-pesquisa-avancada))

# Motivação / contexto da demanda

As consultas do Portal de Transparência possuem como padrão a possibilidade de pesquisa por meio de filtros (eg. [_Filtro Favorecido - Consulta Despesas_](http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-favorecidos/2019/01-01-2019/31-12-2019/0/LUCIANA%20CASSIA%20NOGUEIRA/0/3)) e pesquisa avançada (eg. [_Pesquisa Avançada - Consulta Despesa_](http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-pesquisa-avancada)). No entanto, na reestruturação do Portal de Transparência, ocorrida entre 2015 e 2017, a consulta de Restos a Pagar não foi contemplada com essa possibilidade, sendo disponibilizada apenas com o filtro de [pesquisa Órgão](http://www.transparencia.mg.gov.br/despesa-estado/restos-a-pagar).

Atualmente, a Diretoria Central de Transparência Ativa têm recebidos diversos questionamentos por do telefone do Portal quanto a não possibilidade de outras formas de pesquisa na consulta de Restos a Pagar. Nesse sentido, com o objetivo de ofertar mais opções aos usuários essa nova especificação visa acrescentar os filtros de favorecidos por nome e CPF/CNPJ e pesquisa avançada nos moldes da consulta de despesa.

A decisão de acrescentar apenas os filtros mencionados acima se deve ao levantamento realizado no google analytics considerando como parâmetro os filtros da consulta de despesa.

Conforme tabela abaixo os filtros por Programa e função são poucos utilizados.


|Filtros Consulta Despesa | Acessos |%
|------|------|------
|Órgãos |132.412|86,4%
|Programa|	429	|0,28%
|Função	|4.179	|2,73%
Favorecido	|16.235	|10,59%
**_Total de sessões_**	|**_153.255_**

**Fonte**: Google Analytics -período jan/2019 a 23/out/2019

# Especificação

## Página Inicial

Para contemplar a inclusão dos novos filtros a página inicial deverá sofrer alterações conforme abaixo:

O cidadão seleciona a opção Restos a pagar e o Portal exibirá:

*   **Ano da consulta (aaaa)**: Conforme padrão adotado atualmente.

*   **Consulta**: Órgão, Favorecido por nome, Favorecido por CPF/CNPJ.

*   **Filtro:** Exibir filtro para selecionar uma opção.

*   **Data Ínicio e Fim**: Conforme padrão adotado atualmente

*   **Pesquisar**: Conforme padrão adotado atualmente

*   **Pesquisa Avançada**:

Exemplo:
![](static/pagina-inicial.png)

|Ano | Consulta | Filtro| Início	| Fim	| Pesquisa |Pesquisa Avançada|
|------|------|------|----|-----|-----|----
||Órgão (Consulta Principal)|					
||Favorecido nome					
||Favorecido por CPF/CNPJ					

### Observações Gerais

*   O filtro favorecido por Nome deve ter a opção de autocomplete;

*   O filtro favorecido por Nome deve permitir que o cidadão digite qualquer parte do nome e o portal retornará todos os itens que encaixem na pesquisa;

*   O filtro favorecido por CPF/CNPJ deve realizar a busca com CPFs/CNPJs formatados ou númericos.

*   A Pesquisa Avançada deve possuir um botão de marcar/desmarcar todas as colunas. Além disso, o autocomplete da pesquisa avançada deve possuir código e descrição das classificações orçamentárias ([eg. consulta proposta orçamentária](http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/proposta-orcamentaria/proposta-pesquisa-avancada));

*   Todas as páginas da consulta devem exibir ícones com links para compartilhar consultas no facebook e twitter e a possibilidade de fazer download da planilha completa em csv, exportar para pdf e imprimir conforme padrão já adotado em outras consultas do Portal;

*   Todas as páginas devem exibir cabeçalho e legenda da tabela e “migalhas” conforme padrão;

*   Todos os gráficos da consulta irão buscar a o valor pago no ano e apresentar legenda conforme o já adotado em outras consultas.

*   Em todos os níveis o cidadão poderá avançar para os próximos níveis tanto clicando no gráfico quanto na tabela.

## Consulta Favorecido por nome

**_1º nível (Favorecido)_**

O portal deve exibir a opção de escolher tipo da consulta e ao selecionar o tipo _[Favorecido por nome]_, permiti que o cidadão escreva o nome completo ou parte do nome do favorecido. O Portal retorna todos os resultados que se encaixem no termo informado do filtro.

O Portal da Transparência irá listar o resultado da consulta em um gráfico treemap e em tabela.

<<Título do gráfico: Favorecidos>>

![](static/modelo-grafico-treemap.png)

|Favorecido	|CNPJ/CPF	|Valor inscrito processado|	Valor não inscrito processado|	Valor pago no ano	Valor a pagar
|----|----|-----|----|----|
_Link para o próximo nível_			

**2º nível (Elemento de Despesa)**

Ao clicar no nome do _[Favorecido]_ o Portal exibirá um gráfico treemap e uma tabela.

<<Título do gráfico: Nome do favorecido selecionado no nível anterior>>
![](static/modelo-grafico-treemap.png)

|Categoria Econômica	|Grupo de Despesa	|Elemento de Despesa	|Valor inscrito processado	|Valor não inscrito processado	|Valor pago no ano|	Valor a pagar
|----|-----|-----|-----|-----|-----|------
_Link para o próximo nível_

**3º nível (Item de despesa)**

Ao clicar no _[Elemento de despesa]_ o Portal exibirá um gráfico treemap e uma tabela.

<<Título do gráfico: Nome do elemento de despesa selecionado no nível anterior>> ![](static/modelo-grafico-treemap.png)

|Fonte de Recursos	|Modalidade de Aplicação	|Item de Despesa	|Valor inscrito processado|	Valor não inscrito processado	|Valor pago no ano	|Valor a pagar
|----|-----|-----|-----|-----|-----|------
_Link para o próximo nível_			

**4º nível (Órgão)**

Ao clicar em _[Item de despesa]_ o Portal exibirá um gráfico treemap e uma tabela.

<<Título do gráfico: Nome do item de despesa selecionado no nível anterior>> ![](static/modelo-grafico-treemap.png)

|Código| Órgão	|Valor inscrito processado|	Valor não inscrito processado	|Valor pago no ano	|Valor a pagar|
|----|-----|-----|-----|-----|---
_Link para o próximo nível_

**5º nível (Número de Empenho)**

Ao clicar em _[órgão]_ o Portal exibirá e uma tabela.

|Data| Número do Empenho	|Valor inscrito processado	|Valor não inscrito processado	Valor pago no ano|	Valor a pagar|
|----|-----|-----|-----|--
_Link para o próximo nível_				

**_OBS: A data deverá ser a data de registro inicial do empenho_**

**6º nível (Formulário de detalhamento)**

Ao clicar no _[número do empenho]_ o Portal exibirá o Formulário de detalhamento igual ao utilizado atualmente na consulta por órgão.

![Formulário de detalhamento](static/formulario-detalhamento.png)

## Consulta Favorecido por CPF/CNPJ

**_1º nível (Favorecido)_**

O portal deve exibir a opção de escolher tipo da consulta e ao selecionar o tipo _[Favorecido por CPF/CNPJ]_, permiti que o cidadão escreva o número do CPF/CNPJ formatados ou númericos. O Portal retorna todos os resultados que se encaixem no termo informado do filtro.

**2º nível (Elemento de Despesa)**

Mesma regra do nível favorecido por nome

**3º nível (Item de despesa)**

Mesma regra do nível favorecido por nome

**4º nível (Órgão)**

Mesma regra do nível favorecido por nome

**5º nível (Número de Empenho)**

Mesma regra do nível favorecido por nome

**6º nível (Formulário de detalhamento)**

Mesma regra do nível favorecido por nome

## Consulta Avançada

A consulta avançada terá 12 campos de filtro e parâmetro de ano:

1.  Órgão
2.  Função
3.  Subfunção
4.  Programas
5.  ação
6.  Categoria Econômica
7.  Grupo de Despesa
8.  Modalidade de Aplicação
9.  Elemento de despesa
10.  Item de Despesa
11.  Fonte de Recursos
12.  Identificador de Procedência e Uso (IPU)

O usuário poderá escolher em exibir ou não a lista dos favorecidos. Como padrão o portal não exibirá os favorecidos.

Favorecidos

 <input type="checkbox" disabled=""> Exibir favorecidos 
 <input type="checkbox" disabled="" checked=""> Não exibir Favorecidos

#### _Observações Gerais:_

*   A Pesquisa Avançada deve possuir um botão de marcar/desmarcar todas as colunas.

*   O autocomplete da pesquisa avançada deve possuir código e descrição das classificações orçamentárias ([eg. consulta proposta orçamentária](http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/proposta-orcamentaria/proposta-pesquisa-avancada));

*   Ao exibir o favorecido o Portal deverá retornar o nome e CNPJ/CPF do favorecido, conforme já ocorre na [Consulta de despesa](http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-resultado-pesquisa-avancada/2019/01-01-2019/31-12-2019/3853/0/3684/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/1/0).

*   O Portal dever ter a funcionalidade de autocompletar (desde a primeira letra), desconsiderando acentuação, letras maiúsculas/minúsculas e palavras intermediárias (ex.: Ao digitar "gestao pública", um dos resultados será "Gestão da Administração Pública").

*   O cidadão poderá informar mais de um valor para cada filtro. Ao informar um valor de filtro, listar todas as opções. Se o cidadão não informar um valor para cada filtro, o Portal considerará todos os valores possíveis para cada filtro não informado.

*   O cidadão poderá escolher os campos que ele quer que apareça no resultado (seguir modelo das demais consultas).

*   O cidadão deverá escolher o ano da pesquisa.

*   Ao exibir o resultado na tabela a consulta deverá retornar as colunas valor inscrito processado, valor inscrito não processado, valor pago no ano e valor a pagar.

# Dependências / Integrações

A integração será realizada com o armazém do SIAFI (BO) conforme ocorre atualmente.

# Exemplos

Seguir o modelo atual da [consulta de Despesa](http://www.transparencia.mg.gov.br/despesa-estado/despesa) do Portal de Transparência

# Dúvidas
