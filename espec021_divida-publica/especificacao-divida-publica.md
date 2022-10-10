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

Foi questionado pela equipe da SEF - Diretoria Central de Gestão da Dívida Pública que os dados publicados no portal da Transparência, ano 2021, referentes aos valores da Dívida Pública do Estado MG encontram divergentes dos valores publicados no portal da dívida.

# Especificação
<a href="#top">(inicio)</a>

Esse documento tem como base a alteração do mapa de carga da consulta 'Execução da Dívida Pública' com o objetivo de alinhá-la aos dados publicados no site da SEF.


## Página Inicial - Pesquisa Básica
<a href="#top">(inicio)</a>

## Texto explicativo
<a href="#top">(inicio)</a>

Inclusão de um campo que irá trazer uma breve explicação do conteúdo da consulta.  

##### Atributos do campo<br><br> Exemplo: [Página Inicial - Consulta Acordo Judicial de Reparação da Vale](https://www.transparencia.mg.gov.br/eventos-extraordinarios/acordo-judicial-reparacao-vale?task=estado_recursosvale.listarExecucoes&amp;ano=&amp;dataInicio=01/01/2021&amp;dataFim=31/12/2022&amp;consulta=2&amp;filtro=)


1. O usuário poderá exibir mais detalhes do texto ao clicar em ***Mais*** ou ocultar ao clicar ***Menos***;
2. A funcionalidade deverá permitir a visualização de *tooltip* ao posicionar o mouse sobre uma palavra ou termo;
3. Ao clicar sobre a palavra ou termo o PdT deverá abrir um um *pop-up* em forma de glossário. [eg. pop-up](https://www.usaspending.gov/)
4. O PdT deverá permitir que por meio da área administrativa do Portal a equipe DTA inclua ou altere os dados desse campo incluindo os *tooltips*.


##### Texto Introdutório

- Tooltip de termos


## Leiaute - Barra de navegação
<a href="#top">(inicio)</a>

A barra de navegação superior será composta pelos seguintes campos:

* Início (dd/mm/aaaa)
* Fim (dd/mm/aaaa)
* Botão *'Pesquisar'*

###### Observações:

* No campo da data o usuário poderá selecionar ou digitar a data na caixa.

`EXEMPLO`

* O campo período será no formato **dd/mm/aaaa** composto por início e fim (eg. 01/04/2021 a 30/12/2021);

#### Leiaute - Tabelas navegação
<a href="#top">(inicio)</a>

* A pesquisa básica irá apresentar como padrão a tabela de resultados com os dados do exercício vigente e os dados da consulta 'Por Projeto'.

* A data de atualização dos dados (*Dados atualizados em*), o período, o ícone *Exibir Gráfico* ou *Fechar Gráfico*, Download, Compartilhar serão exibidos acima do gráfico/tabela de resultados.(MELHORAR)

* Como padrão os dados serão exibidos no formato de tabela e caso o usuário queira visualizar os dados em forma de gráfico deve clicar em '*Exibir Gráfico*' e os dados da tabela serão deslocados para baixo. Para retornar a exibição apenas no formato tabela o usuário deve clicar em '*Fechar Gráfico*'

* A barra de pesquisa da tabela de resultado deverá retornar os dados a medida que o usuário for digitando. O atributo *placeholder* deve ser aplicado na barra de pesquisa.

* A opção de 'Exibir linhas' (quantidade de linhas) será exibida na parte superior da tabela.

* Os valores TOTAL GERAL e o SUBTOTAL serão exibidos na tabela de resultados de acordo com o comportamento do usuário:

  * **TOTAL GERAL:** quando o usuário não aplicar nenhum filtro na tabela ou quanto todos os dados forem exibidos em uma única página, ou seja, sem paginação;
  * **SUBTOTAL:** quando o usuário aplicar qualquer filtro na tabela através da barra de pesquisa ou quando houver paginação na tabela de resultado, ou seja, houver mais de uma página de resultado.


##### Estrutura de design das tabelas de resultados da Pesquisa básica

 * Cabeçalho fixo - Fixer Header ([eg. Consulta de Remuneração do PdT](https://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-faixa/202112/3/1094/4022/C/3569184/995/26150365));
 * Rolagem horizontal - Horizontal Scroll. Quando o número de colunas ultrapassar o limite da página o PdT deve possibilizar a rolagem horizontal;
 * Colunas movíveis e classificáveis conforme ocorre atualmente;
 * Paginação e seleção da quantidade de linhas a serem exibidas, conforme ocorre atualmente;
 * O texto deve ser ajustável nas colunas, ou seja, caso seja necessário pode haver quebra de linha;
 * A tabela apresentará campos clicáveis (com link) que irá direcionar o usuário para o próximo nível da consulta.
 * Os campos clicáveis serão destacados conforme o layout já adotado pelo PdT - [Consulta Acordo Judicial de Reparação da Vale](https://www.transparencia.mg.gov.br/eventos-extraordinarios/acordo-judicial-reparacao-vale?task=estado_recursosvale.listarExecucoes&amp;ano=&amp;dataInicio=01/01/2021&amp;dataFim=31/12/2022&amp;consulta=2&amp;filtro=).

#### Download dos dados:
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

#### Barra de pesquisa

A barra de pesquisa deve aceitar várias formas de preenchimento dos dados:

* Desconsiderar acentuação, letras maiúsculas/minúsculas;
* Desconsiderar palavras intermediárias (ex.: Ao digitar “gestao pública”, um dos resultados será “Gestão da Administração Pública”);
* O usuário poderá pesquisar por qualquer coluna na tabela de resultados.

#### Compartilhar dados:
<a href="#top">(inicio)</a>

O usuário poderá Compartilhar os link dos dados nos seguintes canais, no mínimo:

- Twitter
- Facebook
- WhatsApp
- Por e-mail
- Copiar *url*

#### Pesquisa básica - Navegação por filtros

* 1º NÍVEL
  - [Tipo]() -> ao clicar o usuário será direcionado para o 2º nível
  - Juros e Encargos da Dívida
  - Amortização da Dívida
  - Total Realizado<br>


* 2º NÍVEL
  * [Credor]() -> ao clicar o usuário será direcionado para o 3º nível
  - CNPJ
  - Juros e Encargos da Dívida
  - Amortização da Dívida
  - Total Realizado<br>

* 3º NÍVEL
- Número do contrato
- Número SIAFI
- Juros e Encargos da Dívida
- Amortização da Dívida
- Total Realizado<br>

#### Campos Pesquisa básica - Navegação por filtros


 Resumo das funcionalidades de área administrativa
