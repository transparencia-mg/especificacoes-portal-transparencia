# Anonimização  dos CPF

## Contextualização

A exigência de a administração pública divulgar informações consta na Lei Complementar nº 101/2000 (Lei de Responsabilidade Fiscal- LRF) que foi  complementada pelo Decreto Federal n° 7.185/2010, que regulamentou os padrões mínimos de qualidade da informação e reforçou o entendimento da divulgação dos dados em sentido amplo:
````
“Art.7º Sem prejuízo dos direitos e garantias individuais constitucionalmente estabelecidos, o SISTEMA deverá gerar, para disponibilização em meio eletrônico que possibilite amplo acesso público, pelo menos, as seguintes informações relativas aos atos praticados pelas unidades gestoras no decorrer da execução orçamentária e financeira:
I - quanto à despesa:
...
d) a pessoa física ou jurídica beneficiária do pagamento, inclusive nos desembolsos de operações independentes da execução orçamentária, exceto no caso de folha de pagamento de pessoal e de benefícios previdenciários.”
````

Nesse sentido, atualmente, o Portal da Transparência divulga nas consultas de Despesa e Restos a pagar informações completas (Nome e CPF) de todos os credores que recebem benefícios previdenciários do Estado, contrariando o Decreto em questão.

Entretanto, sua divulgação tem sido objeto de questionamentos pela sociedade. Assim, com a finalidade de atender plenamente o que determina a legislação a Diretoria Central de Transparência Ativa (DTA), unidade responsável pela gestão do Portal da Transparência, propõe a alteração da forma de exibição do dados nessas consultas.

Destaca-se ainda que as demais consultas, como por exemplo, convênios e remuneração não sofrerão alterações, uma vez que, o entendimento corrente é o de que a divulgação de informações completas e íntegras possibilita a qualquer cidadão conhecer, questionar e atuar como fiscal da aplicação dos recursos públicos, para o exercício do controle social – pois está possibilitado o cruzamento de dados dos beneficiários de políticas públicas.

## Especificação da Consulta Despesa

1 - Todas as páginas da consulta deverão exibir ícones com links para compartilhar consultas no facebook e twitter.

2-  Todas as páginas deverá apresentar a possibilidade de fazer download da planilha completa em csv, exportar para pdf e imprimir conforme padrão já adotado em outras consultas do Portal. Exibir cabeçalho e legenda da tabela e “migalhas” conforme padrão.

3- Quando o usuário realizar o download dos dados, esses deverão ser exibidos anonimizados conforme o especificado. No entanto, a base deverá conter a informação completa.

4- Todos dos gráficos deverão apresentar legenda conforme o já adotado em outras consultas.

5- A anonimização será aplicada apenas nos credores pessoas físicas que receberem valores na classificação dos elementos de despesa listados abaixo.

*Elementos de despesa:*

|Código | Descrição|
|-------:|:--------|
|01| aposentadorias do rpps, reserva remunerada e reformas dos militares|
|03| pensões do RPPS e do militar|
|05| Outros benefícios previdenciários do servidor militares
|59| Pensões especiais
|31.2|premiacoes culturais, artisticas, cientificas, desportivas e outras / prêmios lotéricos|

````
Dúvidas???

Grupo 3 / Elemento: OUTROS SERVICOS DE TERCEIROS - PESSOA FISICA / Item de despesa: Estagiários????
Grupo 3 / Elemento 13: Obrigações Patronais / Item: INSS – Demais Despesas
````


**Consulta por "Órgão"**

•	**1º nível** (Órgão) >>  **2º nível** (função) >> **3º nível** (Elemento de Despesa)   

``Sem alterações
``

•	**4º nível** (Favorecido)

Ao clicar no [Elemento de despesa] listados no item 5, o Portal exibirá um gráfico treemap e uma tabela. O cidadão poderá navegar pelos níveis de detalhamento tanto no gráfico quanto na tabela.

Dados da tabela: Favorecido, CNPJ/CPF, Item de Despesa, Valor Empenhado, Valor Liquidado, Valor Pago

````
Observações
- Campo Favorecido: Deverá ser exibido apenas as iniciais do nome do favorecido.

      Exemplo:
      Nome do Favorecido: Cassio Gustavo de Castro
            ==>> O Portal deverá exibir: C.G.C

- Campo CPF: Deverá ocultar os 3 dos três primeiros e dos dois últimos dígitos verificadores.

      Exemplo:
      CPF do Favorecido:028.659.616.48
            ==>> O Portal deverá exibir: ***.659.616.**


obs: Os dados só serão ocultados quando se tratar de favorecido pessoal física.

````

|Favorecido| CNPJ/CPF | Item de despesa | Valor Empenhado |Valor Liquidado| Valor Pago|
|---------:|:--------:|:---------------:|:-----------:|:----------:|:---------|
|C.G.C|** .659.616-**|Auxílio Reclusão| 10.000,00|10.000,00|10.000,00|


Link no valor empenhado, valor liquidado e valor pago. Os demais níveis deverão seguir o padrão já adotado.

**Formulário de detalhamento**

*- Empenho da despesa*

Campo Razão Social do Credor: Nesse campo deverá ser exibido o nome do favorecido e CPF descaracterizado conforme regra mencionada acima.

![Empenho da Despesa](empenho_despesa.png)

*- Liquidação e Pagamento*

Campo CNPJ/CPF e Descrição do Favorecido: Deverá ser exibido o nome do favorecido e CPF descaracterizado conforme regra mencionada acima.

![Liquidação e Pagamento](liquidacao_pagamento.png)



**Consulta por “Função”**

•**1º nível** (Função) >> **2º nível** (Subfunção) >> **3º nível** (Órgão) >> **4º nível** (Programa) >> **5º nível** (Ação) >> **6º nível** (Elemento de despesa)

``Sem alterações
``

•	**7º nível** (Favorecido)

``Mesmas alterações aplicadas no nível favorecido da consulta por órgão.
``



**Consulta por “Programa”**

•	**1º nível** (programa) >> **2º nível** (órgão) >> **3º nível** (ação) >> **4º nível**(Elemento de despesa)

``Sem alterações
``

•	**5º nível** (Favorecido)

``Mesmas alterações aplicadas no nível favorecido da consulta por órgão.
``

**Consulta por “Favorecido Nome”**

O portal exibirá a opção para escolher o período da consulta – formato aaaa.

O portal exibirá a opção de escolher tipo da consulta e, ao selecionar o tipo “Favorecido por nome”, permitirá que o cidadão escreva o nome do favorecido e retornará todos os resultados que se encaixem no termo informado do filtro.

*Obs*: O Portal deverá exibir os favorecidos que apresentem a anonimização deverão ser exibidos na consulta, contudo a sua exibição deverá seguir as regras estabelecidas.

O Portal da Transparência irá listar o resultado da consulta em um gráfico treemap e em tabela.  O cidadão poderá navegar pelos níveis de detalhamento tanto no gráfico quanto na tabela.

Link no nome do favorecido que irá para o próximo nível.


•	**1 º nível** (Favorecido)

``Mesmas alterações aplicadas no nível favorecido da consulta por órgão.
``

•	**2º nível** (Elemento de despesa) >> **3º nível** (Item de despesa) >> **4º nível** (Órgão)

``Sem alterações
``

•	**Formulário de Detalhamento**

``Mesmas alterações aplicadas no formulário de detalhamento da consulta por órgão.
``

**Consulta por “Favorecido CPF/CNPJ”**

O portal exibirá a opção para escolher o período da consulta – formato aaaa.
O portal exibirá a opção de escolher tipo da consulta e, ao selecionar o tipo “Favorecido por CPF/CNPJ”, permitirá que o cidadão escreva o número do CPF ou CNPJ do favorecido e retornará todos os resultados que se encaixem no termo informado do filtro.

*Obs*: Os favorecidos que apresentarem o CPF anonimizado deverão ser exibidos no resultado da busca, contudo a sua exibição seguirá as regras estabelecidas.

O Portal da Transparência irá listar o resultado da consulta em um gráfico treemap e em tabela.  O cidadão poderá navegar pelos níveis de detalhamento tanto no gráfico quanto na tabela.


Link no nome do favorecido que irá para o próximo nível.

**1 º nível** (Favorecido)

``Mesmas alterações aplicadas no nível favorecido da consulta por órgão.
``

•	**2º nível** (Elemento de despesa) >> **3º nível** (Item de despesa) >> **4º nível** (Órgão)

``Sem alterações
``

•	**Formulário de Detalhamento**

``Mesmas alterações aplicadas no formulário de detalhamento da consulta por órgão.
``

**Pesquisa Avançada**

Quando o cidadão selecionar o campo “ Exibir favorecidos” o Portal deverá retornar a lista dos favorecidos que correspondem aos elementos da despesa especificação na alínea com o nome e CPF anonimizados conforme o estabelecido.

## Especificação da consulta Restos a pagar

Todas as páginas da consulta deverão exibir ícones com links para compartilhar consultas no facebook e twitter e a possibilidade de fazer download da planilha completa em csv, exportar para pdf e imprimir conforme padrão já adotado em outras consultas do Portal. Exibir cabeçalho e legenda da tabela e “migalhas” conforme padrão.

Todos os gráficos da consulta irão buscar a o valor pago no ano conforme o já adotado em outras consultas.

Todos dos gráficos deverão apresentar legenda conforme o já adotado em outras consultas.

**Consulta por “Órgão”**

•	**1º nível** (Órgão) >> **2º nível** (Elemento de Despesa) >> **3º nível** (Item de Despesa)

``Sem alterações
``

•	**4º nível** (Favorecido)

Ao clicar no [Item de despesa] listados no número 4 o Portal exibirá uma tabela.

Dados da tabela: Favorecido, CNPJ/CPF, Número do empenho, valor inscrito processado, valor inscrito não processado, valor pago no ano, valor a pagar.

````
Observações
- Campo Favorecido: Deverá ser exibido apenas as iniciais do nome do favorecido.

      Exemplo:
      Nome do Favorecido: Cassio Gustavo de Castro
            ==>> O Portal deverá exibir: C.G.C

- Campo CPF: Deverá ocultar os 3 dos três primeiros e dos dois últimos dígitos verificadores.

      Exemplo:
      CPF do Favorecido:028.659.616.48
            ==>> O Portal deverá exibir: ***.659.616.**


obs: Os dados só serão ocultados quando se tratar de favorecido pessoal física.

``````

|Favorecido| CNPJ/CPF | Número do empenho | Valor Inscrito Processado |Valor Inscrito Não Processado| Valor pago no ano| Valor a Pagar|
|---------:|:--------:|:---------------:|:-----------:|:----------:|:--------:|:-------|
|C.G.C|** .659.616-**|316| 10.000,00|0,00|10.000,00|0,00|


Link no número do empenhado.

•	**Formulário de detalhamento**

*Empenho da Despesa*:

Campo Razão Social do Credor: Deverá ser exibido o nome do favorecido e CPF descaracterizado conforme regra mencionada acima.

![Empenho da Despesa](empenho_despesa.png)

*Liquidação e Pagamento*:

Campo CNPJ/CPF e Descrição do Favorecido: Deverá ser exibido o nome do favorecido e CPF descaracterizado conforme regra mencionada acima.

![Liquidação e Pagamento](liquidacao_pagamento.png)
