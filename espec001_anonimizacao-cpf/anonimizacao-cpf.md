---
| contrato_manutencao | proposta_comercial | pull_request | titulo | output |
|---|---|---|---|---
nº 15210010062019 (INF. 3951) | n | [espec001](https://github.com/transparencia-mg/especificacoes-portal-transparencia/pull/1) | "Anonimização dos CPFs" | | html_document |
theme | toc |
united | true |||
---

# Visão geral da demanda

Essa demanda visa anonimizar/descaracterizar os nomes e CPFs de credores pessoas físicas nas consultas de Despesa e Restos a Pagar (RP) em classificações orçamentárias específicas. As classificações orçamentárias iniciais (eg. Elemento item 31-02 - Prêmios lotéricos) estão definidas nesta especificação, mas a solução deve ser flexível para que demais classificações possam ser incluídas nesta regra de anonimização/descaracterização mediante provocação da CGE.

O método de anonimização/descaracterização deve ser aplicado nos resultados das consultas de Despesa e RP que apresentem informação de nome e CPF, notadamente:

* Nível favorecido (eg. [Despesa](http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-orgaos/2019/01-01-2019/31-12-2019/3873/1874/510/20/39); [RP](http://www.transparencia.mg.gov.br/despesa-estado/restos-a-pagar/restospagar-orgaos/2018/3718/510/39/20/2704/130/59))
* Formulários de detalhamento de documentos (eg. [Despesa](http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-orgaos/2019/01-01-2019/31-12-2019/3873/1874/510/20/39/897363/2704/empenhado/412/12420866/0/0); [RP](http://www.transparencia.mg.gov.br/despesa-estado/restos-a-pagar/restospagar-orgaos/2018/3718/510/39/20/2704/130/59/3774671));
* Pesquisa avançada.

As consultas passíveis de aplicação dessa regra, com seus respectivos filtros, são:
 * Consulta Despesa, na pesquisa básica (por órgão, por função, por programa, por favorecido nome ou por favorecido CPF) e na pesquisa avançada;
 * Consulta Restos a pagar, na pesquisa básica (por órgão) _e nos [demais filtros a serem implantados (favorecido por nome, favorecido por CPF/CNPJ e pesquisa avançada)](https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/feat/especificacao-consulta-restos-pagar/espec003_consulta-restos-a-pagar/inclusao-novos-filtros-consulta-restos-a-pagar.md)_

O método de anonimização/descaracterização consiste em:

1. Substituir o nome do credor pelo valor "INFORMAÇÃO COM RESTRIÇÃO DE ACESSO"; e
2. Substituir o CPF do credor pelo valor "000.000.000-00".

As regras acima devem ser aplicadas inclusive no caso em que os dois campos estejam sendo apresentados de maneira conjunta, como nos dois formulários linkados acima.

__Nota: No banco de dados do Portal da Transparência as informações de nome e CPF devem ser armazenadas sem anonimização/descaracterização, permitindo filtros que utilizem essas informações.__

# Motivação / contexto da demanda

A exigência de a administração pública divulgar informações consta na Lei Complementar nº 101/2000 (Lei de Responsabilidade Fiscal- LRF) que foi complementada pelo Decreto Federal n° 7.185/2010, que regulamentou os padrões mínimos de qualidade da informação e reforçou o entendimento da divulgação dos dados em sentido amplo, conforme art. 7º abaixo:

> _“Art.7º Sem prejuízo dos direitos e garantias individuais constitucionalmente estabelecidos, o SISTEMA deverá gerar, para disponibilização em meio eletrônico que possibilite amplo acesso público, pelo menos, as seguintes informações relativas aos atos praticados pelas unidades gestoras no decorrer da execução orçamentária e financeira:_
>
> _I - quanto à despesa:_
>
>_[...]_
>
> _d) a pessoa física ou jurídica beneficiária do pagamento, inclusive nos desembolsos de operações independentes da execução orçamentária, exceto no caso de folha de pagamento de pessoal e de benefícios previdenciários.”_

Nesse sentido, atualmente, o Portal da Transparência divulga nas consultas de Despesa e Restos a Pagar informações completas (nome e CPF) de __todos os credores__ que recebem benefícios previdenciários do Estado, contrariando o Decreto Federal em questão.

Além disso, sua divulgação tem sido objeto de questionamentos pela sociedade.

Outro item que também será alterado é a divulgação dos nomes e CPF de ganhadores de prêmio lotéricos. Atualmente, o Portal da Transparência retirou do rol de credores da consulta de despesa e restos a pagar os favorecidos do elemento item de despesa 3102 nos anos de 2002 a 2019, para atender a Portaria nº 26/2014 da Loteria Mineira do Estado de Minas. A referida portaria estabelece, em seu art. 2º, que a LEMG manterá, independente de classificação, sigilo sobre a informação pessoal, relativa à intimidade, à vida privda, à honra e à imagem dos apostadores sorteados da Loteria do Estado de Minas Gerais.

A medida adotada pela DTA para preservar informações sobre apostadores sorteados da LEMG foi a exclusão de todos os dados divulgados no Portal da Transparência referentes aos pagamentos realizados no elemento item 3102, até que fosse realizada manutenção corretiva no Portal da Transparência para divulgar os dados sem a exposição dos ganhadores. Em consulta, a ASSJUR da CGE, o entendimento predominante foi o de anonimizar o nome e o CPF dos apostadores sorteados.

Assim, com a finalidade de atender plenamente o que determina a legislação, a Diretoria Central de Transparência Ativa (DTA), unidade responsável pela gestão do Portal da Transparência, propõe a alteração na forma de exibição dos dados nas consultas de Despesas e Restos a Pagar, referentes aos credores de benefícios previdenciários e prêmios lotéricos.

Destaca-se ainda que as demais consultas, como por exemplo, convênios e remuneração não sofrerão alterações, uma vez que, o entendimento corrente é o de que a divulgação de informações completas e íntegras possibilita a qualquer cidadão conhecer, questionar e atuar como fiscal da aplicação dos recursos públicos, para o exercício do controle social – pois está possibilitado o cruzamento de dados dos beneficiários de políticas públicas.

# Especificação

Abaixo seguem as regras que deverão ser aplicadas nas consultas de despesa e restos a pagar.

1. Quando o usuário realizar o download dos dados, esses deverão ser exibidos anonimizados/descaraterizados. No entanto, a base deverá conter a informação completa.

2. Essa regra será aplicada apenas nos credores pessoas físicas que receberam valores na classificação orçamentária dos elementos de despesa listados abaixo.

__Tabela 01: Elementos de Despesa passíveis de Anonimização__

|Código|Descrição|
|-------|:--------|
|01| aposentadorias do RPPS, reserva remunerada e reformas dos militares|
|03| pensões do RPPS e do militar|
|05| Outros benefícios previdenciários do servidor ou do militar
|59| Pensões especiais
|31.2|premiacoes culturais, artisticas, cientificas, desportivas e outras / prêmios lotéricos|


## Consulta Despesa

A alteração será aplicada no nível no qual o nome dos favorecidos são exibidos, no formulário de detalhamento e no resultado da consulta avançada.

### Consulta por Órgão

* 1º nível (Órgão) - Não haverá alteração
* 2º nível (Função) - Não haverá alteração
* 3º nível (Elemento de Despesa) - Não haverá alteração
* 4º nível (Favorecido):

Ao clicar em qualquer um dos ___Elementos de despesa___ do 3º nível, que esteja listado na Tabela 01, o Portal exibirá um gráfico treemap e uma tabela. O cidadão poderá navegar pelos níveis de detalhamento tanto no gráfico quanto na tabela.  O Portal deverá exibir da seguinte forma:

__Tabela 02: Exemplo de aplicação da regra de anonimização/descaracterização__:

| Favorecido | CNPJ/CPF | Item de despesa | Valor Empenhado |Valor Liquidado| Valor Pago|
|---|---|---|---|---|---
"INFORMAÇÃO COM RESTRIÇÃO DE ACESSO"|*******.659.616**|Auxílio Reclusão| 10.000,00|10.000,00|10.000,00|

As regras para anonimização são:

 * __Campo Favorecido:__ Substituir o nome do credor pelo valor "INFORMAÇÃO COM RESTRIÇÃO DE ACESSO"

 * __Campo CPF:__ Ocultar os três primeiros dígitos e dos dois últimos dígitos verificadores.

* 5º nível (Formulário de Detalhamento): Os campos do formulário de detalhamento deverão seguir as regras descritas acima.

___Empenho da despesa:___

_Campo Razão Social do Credor:_ Nesse campo deverá ser exibido o nome do favorecido e CPF descaracterizados conforme regras da Tabela 02 acima.

![Empenho da Despesa](static/empenho_despesa.png)

___Liquidação e Pagamento___

_Campo CNPJ/CPF e Descrição do Favorecido:_ Deverá ser exibido o nome do favorecido e CPF descaracterizados conforme regras da Tabela 02.

![Liquidação e Pagamento](static/liquidacao_pagamento.png)

### Consulta por Função

* 1º nível (Função) - Não haverá alteração
* 2º nível (Subfunção) - Não haverá alteração
* 3º nível (Órgão) - Não haverá alteração
* 4º nível (Programa) - Não haverá alteração
* 5º nível (Ação) - Não haverá alteração
* 6º nível (Elemento de despesa): Não haverá alteração
* 7º nível (Favorecido): __Mesmas alterações aplicadas na Tabela 02.__
* 8º nível (Formulário de Detalhamento): __Mesmas alterações aplicadas na Tabela 02.__.

### Consulta por Programa

* 1º nível (Programa) - Não haverá alteração
* 2º nível (Órgão) - Não haverá alteração
* 3º nível (Ação) - Não haverá alteração
* 4º nível (Elemento de despesa)- Não haverá alteração
* 5º nível (Favorecido) - __Mesmas alterações aplicadas na Tabela 02.__
* 6º nível (Formulário de Detalhamento): __Mesmas alterações aplicadas na Tabela 02.__.

### Consulta por Favorecido Nome e Consulta por Favorecido CPF/CNPJ

O portal exibirá a opção de escolher tipo da consulta. Ao selecionar o tipo ___Favorecido por nome___, ou ___Favorecido por CPF/CNPJ___, permitirá que o cidadão escreva o nome do favorecido, ou seu CPF, respectivamente, e retornará todos os resultados que se encaixem no termo informado do filtro, __aplicadas as regras da Tabela 02__(visualização anonimizada/descaracterizada).

O Portal irá listar o resultado da consulta em um gráfico treemap e em tabela.  O cidadão poderá navegar pelos níveis de detalhamento tanto no gráfico quanto na tabela.

* 1º nível (Favorecido) - __Mesmas alterações aplicadas na Tabela 02.__
* 2º nível (Elemento de despesa) - Não haverá alteração
* 3º nível (Item de despesa) - Não haverá alteração
* 4º nível (Órgão) - Não haverá alteração
* 5º nível (Formulário de Detalhamento): __Mesmas alterações aplicadas na Tabela 02.__.

### Pesquisa Avançada

Quando o cidadão selecionar o campo ___Exibir favorecidos___ o Portal deverá retornar a lista dos favorecidos que correspondam aos elementos da despesa constantes da __Tabela 01__, aplicadas as regras da __Tabela 02__.


## Especificação da consulta Restos a pagar

As regras serão aplicadas no 4º nível (favorecido) e no formulário de detalhamento.

### Consulta por Órgão

* 1º nível (Órgão) - Não haverá alteração
* 2º nível (Elemento de despesa) - Não haverá alteração
* 3º nível (Item de despesa) - Não haverá alteração
* 4º nível (Favorecido):

  Ao clicar em algum ___Item de despesa___ listado no 3º nível, o Portal exibirá uma tabela e deverá seguir a regra da __Tabela 02__, conforme demonstrado abaixo:


|Favorecido| CNPJ/CPF | Número do empenho | valor inscrito processado |valor inscrito não processado| valor pago no ano| valor a pagar|
|"INFORMAÇÃO COM RESTRIÇÃO DE ACESSO"|***.659.616-**|316| 10.000,00|0,00|10.000,00|0,00|

* 5º nível (Formulário de Detalhamento): __Mesmas alterações aplicadas acima__.

# Dependências / Integrações

[Especificação que visa acrescentar modos de pesquisa adicionais a consulta de Restos a Pagar](https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/feat/especificacao-consulta-restos-pagar/espec003_consulta-restos-a-pagar/inclusao-novos-filtros-consulta-restos-a-pagar.md), nos moldes da consulta de Despesa


# Exemplos

Foi realizado pesquisa no Portal do Governo Federal, Espirito Santo e São Paulo e no que diz respeito a benefícios previdenciários e não foi localizado nenhum credor pessoa física.

# Dúvidas / Pendências

## Técnicas

* O método de anonimização/descaracterização escolhido influencia na estimativa de horas?

* As classificações orçamentárias para as quais o método de anonimização/descaracterização será aplicado influencia na estimativa de horas?

* Acrescentar novas consultas (eg. [Concursos](http://www.transparencia.mg.gov.br/estado-pessoal/concursos-realizados/concursos-orgaos-demandantes/2017/01-01-2017/31-12-2017/1/2/2/64)) que deverão ser anonimizadas/descaracterizadas influencia na estimativa de horas?

## Negócio

* O método de anonimização/descaracterização proposta está suficiente para garantir a privacidade dos credores?

* Ponderar e decidir sobre a inclusão do rol de dados de beneficiários dos itens abaixo na mesma especificação da Tabela 02:

Grupo 3 / Elemento: OUTROS SERVICOS DE TERCEIROS - PESSOA FISICA / Item de despesa: Estagiários????
Grupo 3 / Elemento 13: Obrigações Patronais / Item: INSS – Demais Despesas
OUTROS BENEFICIOS ASSISTENCIAIS DO SERVIDOR E DO MILITAR / Itens: auxílios funeral e natalidade.

1. Em seu art. 7º, o Decreto 7.185/2010 regulamenta que a exceção de disponiblização de dados de pessoa física estende-se a folha de pagamento de pessoa e a benefícios previdenciários.
No entanto, com base no julgamento do Recurso Extraordinário com Agravo (ARE) 652777 do Supremo Tribunal Federal é legítima a publicação, inclusive em sítio eletrônico, dos nome de servidores e dos valores dos correspondentes vencimentos e vantagens pecuniárias.
Ressalta-se que em relação aos dados de endereço, CPF e identidade o ARE 652777 permaneceu com a proibição.

..."E quanto à segurança física ou corporal dos servidores, seja pessoal, seja familiarmente, claro que ela resultará um tanto ou quanto fragilizada com a divulgação nominalizada dos dados em debate, mas é um tipo de risco pessoal e familiar que se atenua com a proibição de se revelar o endereço residencial, o CPF e a CI de cada servidor."

2. Em relação a divulgação de dados de pessoas físicas credores de benefícios previdenciários: a Lei Complementar nº 64/2002 dispõe que são benefícios assegurados pelo Regima Próprio de Previdência Social:

>I - ao segurado:
>aposentadoria;
>licença para tratamento de saúde;
>licença-maternidade;
>abono-família;
>
>II - ao dependente:
>pensão por morte;
>auxílio-reclusão.

No entanto, o Diário Oficial do Estado divulga as pessoas físicas autorizadas a receber os benefícios previstos na Lei Complementar 64/2002, assim, questiono se não é válida divulgação nominal dos beneficiários, deixando apenas anonimizado o CPF do previdenciário, seguindo a regra já estabelecida na ARE 652777.
O único benefício previdenciário que não consta no IOF é o auxílio reclusão, que para evitar questionamentos, pode ser anonimizado o CPF e o nome do beneficiário.

A título de exemplo, abaixo apresenta-se a divulgação no IOF de benefícios previdenciários.

2.a. aposentadoria
![](static/aposentadoria.jpg)

2.b. licença para tratamento de saúde
![](static/licenca_saude.jpg)

2.c. licença maternidade
![](static/licenca_maternidade.jpg)

2.d abono família
![](static/abono_familia.jpg)

2.e. pensão por morte
![](static/pensao_por_morte.jpg)




----FIM----
