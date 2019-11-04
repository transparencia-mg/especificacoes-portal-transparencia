
---
titulo: "Remuenração de Servidores"

pull_request: [pull_request_002](https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/feat/especificacao-remuneracao-servidores/especificacao-remuneracao-servidores.md)

---


# Visão Geral da Intervenção

Essa demanda visa divulgar no Portal da Transparência as remunerações de todos os exercícios anteriores disponíveis. Atualmente somente é divulgado dados para o exercício corrente.

Também deve ser alterado o formato de divulgação do histórico da remuneração, com inversão de linhas e colunas, de tal forma que seja possível a visualização de maior quantidade de meses.

Por fim, deve ser incluído funcionalidade de exportação para `.pdf` e `.csv` conforme formato definido nesta especificação.

Além disso também deve ser realizada a adequação do layout (entre planilha, banco de dados e interface) da Consulta de Remuneração no Portal da Transparência.

# Motivação / Contexto da Intervenção

Para atender o disposto no inc. VIII, do art. 4º do Decreto Estadual nº45.969/2012, o Portal da Transparência, por meio da consulta de __Remuneração de Servidores__ disponibiliza dados sobre a situação funcional e o histórico da remuneração, contendo os dados financeiros do ano corrente.

No entanto, o formato atual de divulgação no Portal da Transparência apresenta apenas os dados financeiros referentes ao ano corrente, o que tem sido objeto de questionamentos e dúvidas por parte dos usuários, por meio do Fale Conosco e 155, sobre a localização dos dados referentes a anos anteriores. 

A prática adotada pelo Portal da Transparência, é a transferência dos dados ao final do ano corrente para a base de dados do Portal de Dados Abertos, e a consequente exclusão desse dados na consulta de Remuneração. 

Visando atender com mais completude o disposto no inc. VIII, do art. 4º do Decreto Estadual nº 45.969/2012, a Diretoria Central de Transparência Ativa - DTA/CGE, recomenda a alteração do _layout_ da consulta de __Remuneração de Servidores__, com a inclusão do histórico da remuneração de todos os meses disponíveis, provavelmente a partir de 2012, ano em que foi iniciada a extração dos dados no SISAP pela Fazenda, sem mais excluir a base de dados após o encerramento do ano.

# Especificação

## Consulta Remuneração de Servidores

### Página Inicial

O cidadão seleciona a opção Pessoal e depois Remuneração dos Servidores e o Portal exibirá

1. Ano da consulta (aaaa) O portal exibirá a opção para escolher o período da consulta – formato aaaa.
2. Mês: sem alteração
3. consulta: sem alteração
4. Nome: sem alteração
5. Pesquisa
6. Pesquisa Avançada

#### Regras para a página inicial

1. Período/Ano: habilitar a consulta por ano no primeiro nível da consulta, semelhante a regra que já é adotada para a consulta de Despesa.

![](static/filtro_ano.jpg)

2. Mês: incluir no filtro mês, todos os meses do anos. Atualmente, só consta os meses de Janeiro a Agosto, considerando que o portal apresenta apenas os dados financeiros do ano corrente.


### Formulário Situação Funcional e Dados de Remuneração

1. Na visualização dos dados do servidor referente ao Histórico da Remuneração, a linha referente ao --mês/ano-- deverá apresentar dados financeiros dos últimos 12 meses contados do filtro realizado na página inicial da consulta de Remuneração

|Mês/Ano|Ago/2019|Jul/2019|Jun/2019|Mai/2019|Abr/2019|Mar/2019|Fev/2019|Jan/2019|Dez/2018|Nov/2018|Out/2018|Set/2018|
|-------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|
|-----|


![](static/historico_remuneracao.jpg)

2. A cada nova carga no Portal referentes aos dados de remuneração dos servidores, deverá ser excluída a última coluna da barra, referente ao mês mais antigo.

3. E, posteriormente, deverá ser incluída na primeira coluna (após o mês/ano), o mês da carga atual dos dados de remuneração.



![](static/pdf_planilha.jpg)

## Demais funcionalidades

* Na divulgação do quantitativo de servidores por faixa salarial, deve-se manter o salário mínimo do exercício corrente.

* Incluir funcionalidade de exportação de salvar os dados funcionais e financeiros em PDF e visualizar por meio de `csv`. O modelo deve ser

| Nome      | Cargo | Mês      | Remuneracao | Deducoes |
|-----------|-------|----------|-------------|----------|
| Francisco | DAD6  | JAN/2012 | 2.438,39    | 487,68   |
| Francisco | DAD7  | FEV/2012 | 2.438,39    | 487,68   |

# Dependências/Integrações

Não se aplica.


# Exemplos

[Governo do Paraná](http://www.transparencia.pr.gov.br/pte/pages/pessoal/remuneracoes/exibir_remuneracao?windowId=729)


# Dúvidas

* Temos acesso aos dados de anos anteriores da remuneração sem decisões judiciais? Qual o impacto se planilhas de anos anteriores com descaracterização forem carregadas no Portal?

1. A situação funcional do servidor será histórica? Ou seja, será possível pesquisar a situação funcional de um servidor no mês de Maio de 2014 ou somente a situação funcional atual?????

3. Concentrar as informações de servidores que possem mais de um cargo em uma mesma tela.
Atualmente, o Portal da Transparência apresenta os dados de servidores com mais de um cargo em telas separadas:
![](static/telas_separadas.jpg)

Sugestão: Permitir a visualização dos cargos e remunerações em uma única tela. Diferenciando os cargos por números, a exemplo com o que ocorre no Governo do Paraná

![](static/unica_tela.jpg)
