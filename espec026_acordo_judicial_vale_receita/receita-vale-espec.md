---
contrato_manutencao: Manutenção PDT - Contrato INF INF 4817
proposta_comercial:
mantis:
pull_request: '[]()'
titulo: Receita Acordo Judicial Vale
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da demanda
<a href="#top">(inicio)</a>

Essa demanda visa a alteração da consulta de Receita do Acordo Judicial da Vale no Portal da Transparência para possibilitar o acompanhamento das ações desenvolvidas pelo Governo do Estado de Minas Gerais com recursos provenientes do acordo judicial firmado com a Vale. Considerando a relevância e os valores envolvidos no acordo, a seção será um instrumento de transparência e prestação de contas a sociedade colocando em evidência a execução do acordo.

# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

Ao longo do processo de pagamento do Acordo Judicial da Vale, melhorias na consulta do Acordo Judicial da Vale tem sido solicitadas pela SEPLAG e TCE, dentre elas a melhoria que trata da inclusão da coluna de Rendimentos na consulta de Receita: https://www.transparencia.mg.gov.br/eventos-extraordinarios/acordo-judicial/acordo-judicial-reparacao-vale?task=estado_recursosvale.listarReceitas&amp;ano=&amp;dataInicio=01/01/2021&amp;dataFim=31/12/2025&amp;consulta=4&amp;filtro=


# Especificação
<a href="#top">(inicio)</a>

Esse documento tem como base a alteração da consulta de Receita do Acordo Judicial da Vale



## Página Inicial da consulta - Pesquisa Básica
<a href="#top">(inicio)</a>

#### Leiaute - Barra de navegação - sem alteração
<a href="#top">(inicio)</a>

A barra de navegação superior será composta pelos seguintes campos:

* Ícones por tipo de consulta;
* Período (dd/mm/aaaa)
* Opção de *'Filtrar por'*;
* Botão *'Monte sua consulta'*

###### Observações:

* Os ícones serão clicáveis. Quando o usuário posicionar o mouse sobre o ícone será exibido um *tooltip* com uma breve descrição da consulta.

* O campo período será no formato **dd/mm/aaaa** composto por início e fim (eg. 01/04/2021 a 30/12/2021);
  * **Por Receita**:

#### Leiaute - Tabelas navegação - sem alteração
<a href="#top">(inicio)</a>

* A tabela de resultado levará em consideração os parâmetros dos filtros aplicados.

* A data de atualização dos dados (*Dados atualizados em*), o período, o ícone *Exibir Gráfico* ou *Fechar Gráfico*, Download, Compartilhar serão exibidos acima do gráfico/tabela de resultados.

* Como padrão os dados serão exibidos no formato de tabela e caso o usuário queira visualizar os dados em forma de gráfico deve clicar em '*Exibir Gráfico*' e os dados da tabela serão deslocados para baixo. Para retornar a exibição apenas no formato tabela o usuário deve clicar em '*Fechar Gráfico*'

* A barra de pesquisa da tabela de resultado deverá retornar os dados a medida que o usuário for digitando. O atributo *placeholder* deve ser aplicado na barra de pesquisa.

* A opção de 'Exibir linhas' (quantidade de linhas) será exibida na parte superior da tabela.

* O usuário poderá solicitar a exibição dos dados com código e descrição. Ao clicar no botão '*Exibir código e descrição*' uma nova coluna será adicionada a esquerda de cada coluna que tenha a descrição.

* Os valores TOTAL GERAL e o SUBTOTAL serão exibidos na tabela de resultados de acordo com o comportamento do usuário:

  * **TOTAL GERAL:** quando o usuário não aplicar nenhum filtro na tabela ou quanto todos os dados forem exibidos em uma única página, ou seja, sem paginação;
  * **SUBTOTAL:** quando o usuário aplicar qualquer filtro na tabela através da barra de pesquisa ou quando houver paginação na tabela de resultado, ou seja, houver mais de uma página de resultado.


![](static/imagens/tabela-resultados-parte-superior.png)


##### Estrutura de design das tabelas de resultados da Pesquisa básica - sem alteração

 * Cabeçalho fixo - Fixer Header ([eg. Consulta de Remuneração do PdT](https://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-faixa/202112/3/1094/4022/C/3569184/995/26150365));
 * Rolagem horizontal - Horizontal Scroll. Quando o número de colunas ultrapassar o limite da página o PdT deve possibilizar a rolagem horizontal;
 * Colunas movíveis e classificáveis conforme ocorre atualmente;
 * Paginação e seleção da quantidade de linhas a serem exibidas, conforme ocorre atualmente;
 * O texto deve ser ajustável nas colunas, ou seja, caso seja necessário pode haver quebra de linha;
 * A tabela apresentará campos clicáveis (com link) que irá direcionar o usuário para o formulário de detalhamento ou para o próximo nível da consulta.
 * Os campos clicáveis serão destacados conforme o layout já adotado pelo PdT e terão a imagem de uma lupa.

#### Download dos dados - sem alteração
<a href="#top">(inicio)</a>

* **Download PDF:** O documento gerado em PDF deverá exibir:
 * logo do Portal de Transparência no início da página e
 * *URL*, paginação e a data no fim da página.
 * O arquivo gerado irá exibir os mesmos dados apresentados na tela considerando todos os filtros aplicados e inclusive o TOTAL GERAL ou SUBTOTAL conforme o comportamento do usuário.
 * ao selecionar essa opção o arquivo PDF deverá ser aberto em outra aba do navegador


* **Download Planilha (CSV):**
 * Será exibido a tabela completa de todas as páginas no formato CSV, independente do filtro aplicado.
 * O campo TOTAL GERAL também deverá ser exibido.      
 * Exibir código e descrição em campos distintos, independente de o usuário selecionar a opção '*Exibir código e descrição*'


* **Download base completa:**
 * O usuário será direcionado para o conjunto de dados da respectiva consulta no Portal de Dados Abertos.
 *O PdT deverá permitir que a equipe DTA inclua/altere a *url* desse campo através da área administrativa do Portal.                  
 * O PdT deverá permitir que por meio da área administrativa do Portal a equipe DTA decida se o campo Download Base Completa será exibido ou não na parte superior da tabela de resultado.

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

#### Campos Pesquisa básica - Navegação por filtros

###### Consulta por Receita

  * 1º NÍVEL       
    * Ano de Exercício     
    * Código da Classificação da Receita -> apenas quando o usuário clicar em 'Exibir Código e Descrição'   
    * Classificação da Receita
    * Código da Fonte de Recurso -> apenas quando o usuário clicar em 'Exibir Código e Descrição'   
    * Fonte de Recurso
    * Fonte de Recursos - Portaria STUN nº 710/2021
    * Código da Fonte de Recursos - Portaria STUN nº 710/2021 -> apenas quando o usuário clicar em 'Exibir Código e Descrição'  
    * Valor Previsto Inicial
    * Valor Previsto Atualizado
    * Valor Arrecadado
    * Rendimentos



### Observações gerais:

* Todas as **barras de pesquisa** devem aceitar várias formas de preenchimento dos dados.
  * Autocompletar (*autocomplete* ) desde a primeira letra (eg. [Portal de Transparência MG](http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/proposta-orcamentaria/proposta-pesquisa-avancada));
  * Desconsiderar acentuação, letras maiúsculas/minúsculas;
  * Desconsiderar palavras intermediárias (ex.: Ao digitar “gestao pública”, um dos resultados será “Gestão da Administração Pública”);
  * O usuário poderá pesquisar código ou descrição das classificações orçamentárias (eg. [Proposta Orçamentára - PdT MG](http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/proposta-orcamentaria/proposta-pesquisa-avancada)).   

* Todos os filtros selecionados serão exibidos na tabela de resultado.

* A exibição de código e descrição será diferente em cada seção:

 * Barra de pesquisa e filtros aplicados: exibir código e descrição no mesmo campo (eg. [Proposta Orçamentára - PdT MG](http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/proposta-orcamentaria/proposta-pesquisa-avancada));

 * Tabela de resultado: exibir apenas descrição. Os códigos serão exibidos apenas se o usuário adicionar a coluna;

 * Opção exportar CSV.: exibir código e descrição em campos distintos, independente de o usuário selecionar a opção código na tabela de resultado.
