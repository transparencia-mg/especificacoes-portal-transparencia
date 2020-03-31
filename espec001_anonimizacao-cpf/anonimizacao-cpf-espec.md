---
contrato_manutencao: nº 15210010062019 (INF. 3951)
proposta_comercial: nº 626584/19
mantis: nº 0143530
pull_request: '[espec001](https://github.com/transparencia-mg/especificacoes-portal-transparencia/pull/1)'
titulo: Anonimização dos CPFs
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da demanda
<a href="#top">(inicio)</a>

Essa demanda visa anonimizar os nomes e CPFs de credores pessoas físicas nas consultas de Despesa e Restos a Pagar (RP) em classificações orçamentárias específicas.

As classificações orçamentárias iniciais estão definidas nesta especificação, no entanto, a solução deve ser flexível para que outras classificações possam ser inseridas na regra de anonimização mediante provocação da CGE.

O método de anonimização deve ser aplicado nos resultados das consultas de Despesa e RP que apresentem informação de nome e CPF, bem como nas funcionalidades de exportação de dados.

No entanto as informações devem ser armazenadas de forma completa no banco de dados do Portal, permitindo inclusive a realização de buscas nos campos anonimizados.

# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

O Portal da Transparência retirou do rol de credores da consulta de despesa e restos a pagar os favorecidos do elemento item de despesa 3102 - PRÊMIOS LOTÉRICOS nos anos de 2002 a 2019, para atender a Portaria nº 26/2014 da Loteria Mineira do Estado de Minas. A referida portaria estabelece, em seu art. 2º, que a LEMG manterá, independente de classificação, sigilo sobre a informação pessoal, relativa à intimidade, à vida privada, à honra e à imagem dos apostadores sorteados da Loteria do Estado de Minas Gerais.

A medida adotada pela DTA para preservar informações sobre apostadores sorteados da LEMG foi a exclusão de todos os dados divulgados no Portal da Transparência referentes aos pagamentos realizados no elemento item 3102, até que fosse realizada manutenção evolutiva no Portal da Transparência para divulgar os dados sem a exposição dos ganhadores. Em consulta, a ASSJUR da CGE, o entendimento predominante foi o de anonimizar o nome e o CPF dos apostadores sorteados.

# Especificação
<a href="#top">(inicio)</a>

Inicialmente cabe destacar que os registros do elemento item de despesa 3102 deverão ser novamente carregados na base de dados do Portal da Transparência.

## Método de anonimização

A anonimização deve ser aplicada nas consultas de Despesa e Restos a Pagar para todos os registros do elemento item de despesa 3102 - PRÊMIOS LOTÉRICOS. O método de anonimização consiste em:

1. Substituir o nome do credor pelo valor "INFORMAÇÃO COM RESTRIÇÃO DE ACESSO"; e
2. Substituir o CPF do credor pelo valor "000.000.000-00".

As regras acima devem ser aplicadas inclusive no caso em que o nome e CPF sejam apresentados no mesmo campo, como nos formulários de detalhamento apresentados acima.

No banco de dados do Portal da Transparência as informações de nome e CPF devem ser armazenadas sem anonimização, permitindo filtros que utilizem essas informações.

## Consulta Despesa e Restos a Pagar

A anonimização deve ser aplicada:

* Gráficos e tabelas do nível favorecido (eg. [Despesa](http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-orgaos/2019/01-01-2019/31-12-2019/3873/1874/510/20/39); [RP](http://www.transparencia.mg.gov.br/despesa-estado/restos-a-pagar/restospagar-orgaos/2018/3718/510/39/20/2704/130/59))
* Formulários de detalhamento de documentos (eg. [Despesa](http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-orgaos/2019/01-01-2019/31-12-2019/3873/1874/510/20/39/897363/2704/empenhado/412/12420866/0/0); [RP](http://www.transparencia.mg.gov.br/despesa-estado/restos-a-pagar/restospagar-orgaos/2018/3718/510/39/20/2704/130/59/3774671));
* Pesquisa avançada;
* Imprimir página;
* Exportar para csv;
* Exportar para pdf.


### Exemplos

#### Gráficos e tabelas do nível favorecido

Ao acessar o nível favorecido das classificações orçamentárias que devem ser anonimizadas, o Portal deverá exibir

| Favorecido | CNPJ/CPF | Item de despesa | Valor Empenhado |Valor Liquidado| Valor Pago|
|---|---|---|---|---|---
INFORMAÇÃO COM RESTRIÇÃO DE ACESSO|000.000.000-00|Prêmios Lotéricos| 10.000,00|10.000,00|10.000,00|

#### Formulários de detalhamento de documentos

Ao acessar os formulários de detalhamento os seguintes campos devem ser anonimizados:

* Campo ___Razão Social do Credor___ do formulário de empenho da despesa:

![](static/empenho_despesa.png)

 * Campo ___CNPJ/CPF e Descrição do Favorecido___ do formulário de liquidação e pagamento:

![](static/liquidacao_pagamento.png)

#### Pesquisa Avançada

A anonimização deve ocorrer quando o usuário marcar o campo ___exibir favorecidos___.
