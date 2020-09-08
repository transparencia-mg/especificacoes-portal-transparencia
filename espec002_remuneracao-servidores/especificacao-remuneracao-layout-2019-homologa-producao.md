
---
Título: "Conferência dos dados em produção - Consulta Remuneração"
Contrato Manutenção: 15210010062019 (INF. 3951)
Proposta comercial: 626584/19
Mantis: 0146470
output:
  html_document:
    theme: united
    toc: yes
  pdf_document:
    toc: yes
  word_document:
    toc: yes
---

## Homologação no ambiente de produção

## Leiaute - Tabelas navegação por filtros
<a href="#top">(inicio)</a>

Incluir os campos ___remuneração bruta e remuneração líquida___ nas tabelas de resultado dos filtros



<div class="alert alert-success">

<s>O conteúdo das colunas estão incorretos na navegação por faixa salarial</s>

__CORRIGIDO__

* Servidor
* Masp
* Órgão Exercício
* Remuneração Bruta
* Remuneração Líquida


![](static/producao-sequencia-colunas-corrigido.jpg)

</div>

## Leiaute - Formulários detalhamento situação funcional e histórico de recebimentos

Os dados da situação funcional devem refletir a situação do mês/ano selecionado no filtro da _[barra de pesquisa]_ da consulta.

___Exemplo:___ Caso o usuário selecione os filtros `Ano: 2015 Mês: Janeiro` na _[barra de pesquisa]_, a situação funcional apresentada na tabela _[situação funcional]_ será a correspondente ao período Jan/2015.

<div class="alert alert-success">


__CONFERE__

Dados foram conferidos tomando como exemplo a Servidora: MARCELA OLIVEIRA FERREIRA DIAS

JUNHO/2020

![](static/producao-situacao-funcional-marcela-jun-2020.png)

MAIO/2019
![](static/producao-situacao-funcional-marcela-mai-2019.png)

</div>


### Histórico recebimentos

<div class="alert alert-success">

Favor alterar o nome dos meses para a língua Portuguesa
--

![](static/producao-nome-meses-corrigido.jpg)

</div>


* Quando o número de linhas da tabela _[histórico recebimentos]_ for superior ao limite da página deve ser aplicada paginação conforme padrão das demais consultas; <div class="alert alert-warning"> **OBS** Não é possível verificar essa funcionalidade (paginação) em produção, pois a base de dados disponibilizada corresponde a apenas 18 meses. Dados serão verificados em produção.

</div>


* O cabeçalho da tabela histórico recebimentos deve ser congelado, ou seja, quando o usuário usar a barra de rolagem vertical o cabeçalho da tabela deve ficar sempre visível. ___Exemplo:___ [Cabeçalho fixo (_Fixed Header_)](https://uxdesign.cc/design-better-data-tables-4ecc99d23356#86cf);

<div class="alert alert-success">

__CONFERE__
![](static/producao-cabecalho.png)

</div>

__OBSERVAÇÃO:__ Essa funcionalidade não deve apresentar outra barra de rolagem dentro da tabela histórico recebimentos.

* Os dados apresentados na tabela _[histórico recebimentos]_ devem refletir o primeiro mês da série histórica disponível até o mês/ano selecionado no início da pesquisa.

<div class="alert alert-success">

__CONFERE__

MAIO/2019
![](static/producao-serie-historica.png)
![](static/producao-serie-historica2.png)

</div>

    ___Exemplo:___ O servidor Luiz possui dados disponíveis de Mai/2015 a Out/2019. Caso o usuário selecione no filtro da _[barra de pesquisa]_ os dados de Out/2017, o Portal exibirá dos dados de Mai/2015 a Out/2017.

##### Glossário Interativo: TOOL TIP

O glossário interativo do histórico recebimentos deve apresentar os seguintes textos:

<div class="alert alert-success">

<s>Não está sendo exibido no tooltip</s> - __CORRIGIDO__

1. __Outros valores:__ Valores pagos em condições excepcionais e transitórias, tais como: Indenizações, Decisões Judiciais, Ajuda de Custo, Alimentação e outros valores de natureza eventual.

![](static/producao-outros-valores.jpg)

</div>


#### Formulário de detalhamento

Exportação de arquivos

<div class="alert alert-success">

<s>Ao exportar os dados em csv a ordem dos meses está incorreta</s> __CORRIGIDO__


![](static/producao-ordem-mes-corrigido.jpg)

</div>

<div class="alert alert-success">

__CORRIGIDO__

A ordem da planilha a partir das empresa ainda encontra-se incorreto.

![](static/producao-ordem-empresas-corrigido.jpg)

![](static/espec-arquivo-csv.png)

</div>

<div class="alert alert-success">

As colunas não estão movíveis nesse nível
--

![](static/producao-mover-coluna-corigido.jpg)

</div>

<div class="alert alert-success">

Alinhar os valores do formulário de rendimentos
--

![](static/producao-alinhar-valores-corrigido.jpg)

</div>
