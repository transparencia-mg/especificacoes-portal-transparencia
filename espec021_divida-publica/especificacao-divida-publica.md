---
contrato_manutencao: nº  (INF. )
proposta_comercial:
mantis:
pull_request: '[]()'
titulo: Dívida Pública
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da demanda
<a href="#top">(inicio)</a>

Essa demanda visa alterar o mapa de carga da consulta execução da Dívida Pública para alinhar dados do PDT com os dados disponibilizados no Portal da Dívida Pública Estadual.

# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

Foi questionado pela equipe da SEF - Diretoria Central de Gestão da Dívida Pública que os dados publicados no portal da Transparência, ano 2021, referentes aos valores da Dívida Pública do Estado MG encontram divergentes dos valores publicados no [Portal da Dívida Pública](http://www.fazenda.mg.gov.br/tesouro-estadual/divida-publica/portal-da-divida-publica-estadual/).

# Especificação
<a href="#top">(inicio)</a>

Esse documento tem como base a alteração do mapa de carga da consulta 'Execução da Dívida Pública' com o objetivo de alinhá-la aos dados publicados no site da SEF.


## Página Inicial - Pesquisa Básica
<a href="#top">(inicio)</a>

### Texto explicativo
<a href="#top">(inicio)</a>

Inclusão de um campo que irá trazer uma breve explicação do conteúdo da consulta.

#### Atributos do campo<br><br> Exemplo: [Página Inicial - Consulta Acordo Judicial de Reparação da Vale](https://www.transparencia.mg.gov.br/eventos-extraordinarios/acordo-judicial-reparacao-vale?task=estado_recursosvale.listarExecucoes&amp;ano=&amp;dataInicio=01/01/2021&amp;dataFim=31/12/2022&amp;consulta=2&amp;filtro=)


1. O usuário poderá exibir mais detalhes do texto ao clicar em ***Mais*** ou ocultar ao clicar ***Menos***;
2. A funcionalidade deverá permitir a visualização de *tooltip* ao posicionar o mouse sobre uma palavra ou termo;
3. Ao clicar sobre a palavra ou termo o PdT deverá abrir um um *pop-up* em forma de glossário. [eg. pop-up](https://www.usaspending.gov/)
4. O PdT deverá permitir que por meio da área administrativa do Portal a equipe DTA inclua ou altere os dados desse campo incluindo os *tooltips*.


##### Texto Introdutório

>A [`Dívida Pública`]((a "Compromissos financeiros assumidos pelo governo, podem ser dívida pública interna (entidade pública dentro do país) e dívida pública externa (entidade pública no exterior).") pode ser conceituada como o conjunto de obrigações financeiras do Estado decorrente da necessidade de captação de recursos para execução de políticas públicas.
>
> A gestão da dívida pública estadual está fundamentada em um arcabouço jurídico-orçamentária que confere legitimidade ao processo de atendimento das necessidades de financiamento do governo e corrobora o compromisso da Subsecretaria do Tesouro Estadual – STE, inserida na estrutura organizacional da Secretaria de Estado de Fazenda de Minas Gerais de Minas Gerais - SEF/MG, de minimizar o custo da dívida em uma perspectiva de médio e longo prazos, visando assegurar a sustentabilidade do endividamento
>
>No âmbito da Secretaria de Estado da Fazenda, o [Decreto Estadual nº 47.794/19](https://www.almg.gov.br/consulte/legislacao/completa/completa-nova-min.html?tipo=DEC&num=47794&comp=&ano=2019&texto=consolidado#texto) estabeleceu a gestão do endividamento estatal como competência da Subsecretaria do Tesouro Estadual – STE, por meio da Superintendência Central de Governança de Ativos e da Dívida Pública – SCGOV.

##### Tooltip dos termos destacados dentro do texto inicial

- Compromissos financeiros assumidos pelo governo, podem ser dívida pública interna (entidade pública dentro do país) e dívida pública externa (entidade pública no exterior).

**Observação:**<br> Ao clicar em qualquer termo destacado o usuário será direcionado para o termo especifico dentro do glossário do Portal.


## Leiaute - Barra de navegação
<a href="#top">(inicio)</a>

A barra de navegação superior será composta pelos seguintes campos:

* Início (dd/mm/aaaa)
* Fim (dd/mm/aaaa)
* Botão *'Pesquisar'*

#### Atributos do campo<br><br>Exemplo: [Portal de Transparêcia ES](https://transparencia.es.gov.br/Despesa)

* No campo da data o usuário poderá selecionar ou digitar a data na caixa.
* O campo período será no formato **dd/mm/aaaa** composto por início e fim (eg. 01/04/2021 a 30/12/2021);<br><br>

![](static/formato-data.gif)

## Leiaute - Tabelas navegação
<a href="#top">(inicio)</a>

* A pesquisa básica irá apresentar como padrão a tabela de resultados com os dados do exercício vigente.

* A data de atualização dos dados (*Dados atualizados em*), o período, o ícone *Exibir Gráfico* ou *Fechar Gráfico*, Download, Compartilhar serão exibidos acima do gráfico/tabela de resultados, assim como ocorre na consulta do Acordo Judicial de Reparação da Vale:

![image](https://user-images.githubusercontent.com/52920939/196715269-7a603f03-4233-4eb3-9b64-4f5e724cff82.png)

* Como padrão os dados serão exibidos no formato de tabela e caso o usuário queira visualizar os dados em forma de gráfico deve clicar em '*Exibir Gráfico*' e os dados da tabela serão deslocados para baixo. Para retornar a exibição apenas no formato tabela o usuário deve clicar em '*Fechar Gráfico*'

* A opção de 'Exibir linhas' (quantidade de linhas) será exibida na parte superior da tabela.

* Os valores TOTAL GERAL e o SUBTOTAL serão exibidos na tabela de resultados de acordo com o comportamento do usuário:

  * **TOTAL GERAL:** quando o usuário não aplicar nenhum filtro na tabela ou quanto todos os dados forem exibidos em uma única página, ou seja, sem paginação;
  * **SUBTOTAL:** quando o usuário aplicar qualquer filtro na tabela através da barra de pesquisa ou quando houver paginação na tabela de resultado, ou seja, houver mais de uma página de resultado.

### Estrutura de design das tabelas de resultados da Pesquisa básica
<a href="#top">(inicio)</a>

 * Cabeçalho fixo - Fixer Header ([eg. Consulta de Remuneração do PdT](https://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-faixa/202112/3/1094/4022/C/3569184/995/26150365));
 * Rolagem horizontal - Horizontal Scroll. Quando o número de colunas ultrapassar o limite da página o PdT deve possibilizar a rolagem horizontal;
 * Colunas movíveis e classificáveis conforme ocorre atualmente;
 * Paginação e seleção da quantidade de linhas a serem exibidas, conforme ocorre atualmente;
 * O texto deve ser ajustável nas colunas, ou seja, caso seja necessário pode haver quebra de linha;
 * A tabela apresentará campos clicáveis (com link) que irá direcionar o usuário para o próximo nível da consulta.
 * Os campos clicáveis serão destacados conforme o layout já adotado pelo PdT - [Consulta Acordo Judicial de Reparação da Vale](https://www.transparencia.mg.gov.br/eventos-extraordinarios/acordo-judicial-reparacao-vale?task=estado_recursosvale.listarExecucoes&amp;ano=&amp;dataInicio=01/01/2021&amp;dataFim=31/12/2022&amp;consulta=2&amp;filtro=).

### Leiaute - Gráficos
<a href="#top">(inicio)</a>

* O Gráfico apresentado como padrão será o tipo Treemap (Gráfico área) com os dados do exercício vigente.
* O usuário terá a opção de verificar série histórica da dívida pública ao clicar no gráfico de barra.
* Os gráficos apresentaram os dados da coluna 'Total Realizado'


### Download dos dados:
<a href="#top">(inicio)</a>

* **Download PDF:** O documento gerado em PDF deverá exibir:
  * logo do Portal de Transparência no início da página e
  * *URL*, paginação e a data no fim da página.
  * O arquivo gerado irá exibir os mesmos dados apresentados na tela considerando todos os filtros aplicados e inclusive o TOTAL GERAL ou SUBTOTAL conforme o comportamento do usuário.
  * ao selecionar essa opção o arquivo PDF deverá ser aberto em outra aba do navegador


* **Download Planilha (CSV):**
  * Será exibido a tabela completa de todas as páginas no formato CSV, independente do filtro aplicado.
  * Exibir código e descrição em campos distintos, independente de o usuário selecionar a opção '*Exibir código e descrição*'


* **Download base completa:**
  * O usuário será direcionado para o conjunto de dados da respectiva consulta no Portal de Dados Abertos.
  *O PdT deverá permitir que a equipe DTA inclua/altere a *url* desse campo através da área administrativa do Portal.                  
  * O PdT deverá permitir que por meio da área administrativa do Portal a equipe DTA decida se o campo Download Base Completa será exibido ou não no botão 'Download'

### Barra de pesquisa

* A barra de pesquisa da tabela de resultado deverá retornar os dados a medida que o usuário for digitando. O atributo *placeholder* deve ser aplicado na barra de pesquisa.
* A barra de pesquisa deve aceitar várias formas de preenchimento dos dados:
  * Desconsiderar acentuação, letras maiúsculas/minúsculas;
  * Desconsiderar palavras intermediárias (ex.: Ao digitar “gestao pública”, um dos resultados será “Gestão da Administração Pública”);
  * O usuário poderá pesquisar por qualquer coluna na tabela de resultados.

### Compartilhar dados:
<a href="#top">(inicio)</a>

O usuário poderá Compartilhar os link dos dados nos seguintes canais, no mínimo:

- Twitter
- Facebook
- WhatsApp
- Copiar link

## Pesquisa básica - Navegação por filtros
<a href="#top">(inicio)</a>

* 1º NÍVEL
  - [Tipo]() -> ao clicar o usuário será direcionado para o 2º nível
  - Juros e Encargos da Dívida
  - Amortização da Dívida
  - Valor Total Liquidado<br>

![image](https://user-images.githubusercontent.com/53793354/196471656-c57a815e-b03f-43b2-88a6-af4d6ce26d07.png)

* 2º NÍVEL
  - [Credor]() -> ao clicar o usuário será direcionado para o 3º nível
  - CNPJ
  - Juros e Encargos da Dívida
  - Amortização da Dívida
  - Valor Total Liquidado<br>

![image](https://user-images.githubusercontent.com/53793354/196471951-e972e04f-f18d-41bc-a135-0f6bf44874e5.png)

* 3º NÍVEL
  - Número do contrato
  - Número SIAFI
  - Juros e Encargos da Dívida
  - Amortização da Dívida
  - Valor Total Liquidado<br>

![image](https://user-images.githubusercontent.com/53793354/196472097-b515f944-ffea-4ca2-ae36-5d3e2cc2dd18.png)


## Campos Pesquisa básica - Navegação por filtros
<a href="#top">(inicio)</a>

Os dados dessa consulta serão extraídos do Universo BO SIAFI:
  * Armazém BO / Pastas públicas - SIAFI > SUPORTE- SIAFI > CGE > Nova-espec-divida-publica

#### Filtros da Consulta

* **1º NÍVEL**

Essa consulta será anual, ou seja, o usuário irá visualizar a execução da Dívida Pública conforme o período selecionado.

=>> Consulta BO: 1º nível - Tipo

| Armazém BO- SIAFI |Dimensão SIAFI| Filtro  |
|----|----------|------------|
| Ano de exercício |Período Contábil| Usar o período desejado |   
| Tipo ContratoConvênio Entrada - Cod |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Dados do Empenho - Despesa| - 01- Divida Pública<br>- 00- Sem informação |  
| Grupo Despesa - Descrição  |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Natureza da Despesa Realizada| - 2- Juros e Encargos da Dívida<br>- 6- Amortização da Dívida
| Elemento Despesa |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Natureza da Despesa Realizada |- 21- Juros sobre a Divida por Contrato<br> - 22- outros encargos sobre a dívida por contrato<br> - 71- Principal da dívida contratual resgatado


#### Campos da Tabela

| Armazém BO- SIAFI |Dimensão SIAFI| Campo PDT| Tooltip - PDT|
|----|----------|------------|----------|
| Projeto_Atividade - Descrição |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Programa de Trabalho - Despesa| Tipo |   
| Grupo Despesa - Descrição  |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > GMIFP - Despesa |  Amortização da Dívida| Amortização efetiva do principal da dívida pública contratual, interna eexterna e outros compromissos assumidos
| Grupo Despesa - Descrição  |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > GMIFP - Despesa |Juros e Encargos da Dívida| Taxas, Comissões, prêmios, e outros encargos com operações de crédito internas e externas e outros compromissos assumidos
| Valor Despesa Liquidada |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Valor Total Liquidado | Valor despesa liquidada referente ao somatório dos juros e encargos da dívida mais a amortização da dívida

* **2º NÍVEL**

=>> Consulta BO: 2º nível - Dívida Interna ou Dívida Externa

**Observação:**      
A navegabilidade para o segundo nível irá ocorre apenas nos projetos atividades:<br> - Gestão da Dívida Fundada Contratual Externa e<br>  - Gestão da Dívida Fundada Contratual Interna

| Armazém BO- SIAFI |Dimensão SIAFI| Campo PDT| Tooltip - PDT|
|----|----------|------------|----------|
| Razão Social do Credor |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Credor - Despesa| Credor |Entidades, governos e pessoas nacionais e estrangeiras com as quais o governo estadual contrai dívidas   
| CNPJ_CPF Credor Numérico |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Credor - Despesa| CNPJ |Número de identificação do credor - Cadastro nacional de pessoa jurídica (CNPJ).
| Grupo Despesa - Descrição  |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > GMIFP - Despesa | Amortização da Dívida|Amortização efetiva do principal da dívida pública contratual, interna e externa e outros compromissos assumidos
| Grupo Despesa - Descrição  |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > GMIFP - Despesa |Juros e Encargos da Dívida|Taxas, Comissões, prêmios, e outros encargos com operações de crédito internas e externas e outros compromissos assumidos
|Valor Despesa Liquidada |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Valor Total Liquidado| Valor despesa liquidada referente ao somatório dos juros e encargos da dívida mais a amortização da dívida

* **3º NÍVEL**

=>> Consulta BO: 3º nível -Contratos

| Armazém BO- SIAFI |Dimensão SIAFI| Campo PDT| Tooltip - PDT|
|----|----------|------------|----------|
| Num Ref Contrato Convênio Entrada |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Dados do Empenho - Despesa| Número do Contrato |  Número que identifica o instrumento de contratação 
| Contrato Convênio Entrada |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Dados do Empenho - Despesa| Número SIAFI|Número de identificação no SIAFI (Sistema Integrado de Administração Financeira)
| Grupo Despesa - Descrição  |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > GMIFP - Despesa | Amortização da Dívida|Amortização efetiva do principal da dívida pública contratual, interna e externa e outros compromissos assumidos
| Grupo Despesa - Descrição  |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > GMIFP - Despesa |   Juros e Encargos da Dívida|Taxas, Comissões, prêmios, e outros encargos com operações de crédito internas e externas e outros compromissos assumidos
| Valor Despesa Liquidada |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Valor Total Liquidado| Valor despesa liquidada referente ao somatório dos juros e encargos da dívida mais a amortização da dívida
