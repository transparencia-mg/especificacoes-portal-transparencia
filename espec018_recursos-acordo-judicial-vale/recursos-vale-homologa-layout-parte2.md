---
contrato_manutencao: nº 15210010062019 (INF. 3951)
Link html: http://htmlpreview.github.io/?https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/master/espec018_recursos-acordo-judicial-vale/recursos-vale-homologa-layout-parte2.html
mantis: 165193
pull_request: '[]()'
titulo: Transparência dos recursos da Vale - Acordo Judicial 04/02/2021
output:
  html_document:
    theme: united
    toc: yes
  word_document:
    toc: yes
---

# Homologação do Layout - parte 2
<a href="#top">(inicio)</a>


##### Estrutura de design das tabelas de resultados da Pesquisa básica

<div class="alert alert-success">

* **OK** Cabeçalho fixo - *[Fixer Header](https://medium.com/nextux/design-better-data-tables-4ecc99d23356#86cf)* (eg. [Consulta de Remuneração do PdT](http://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-faixa/202103/1/1038/4158/C/3251081/986/23239313));

![](static/imagens/homologacao/cabecalho-fixo.png)

</div>

<div class="alert alert-danger">


 * Rolagem horizontal - Horizontal Scroll. Quando o número de colunas ultrapassar o limite da página o PdT deve possibilizar a rolagem horizontal;


- A funcionalidade não está funcionado;
- Se não existe paginação o valor subtotal não precisa ser exibido

![](static/imagens/homologacao/paginacao.gif)

 </div>

<div class="alert alert-success">

OK
--

 *  **OK** Colunas movíveis e classificáveis conforme ocorre atualmente;
 * **OK** Paginação e seleção da quantidade de linhas a serem exibidas, conforme ocorre atualmente;
 *  **OK** O texto deve ser ajustável nas colunas, ou seja, caso seja necessário pode haver quebra de linha;

  </div>

* A tabela apresentará campos clicáveis (com link) que irá direcionar o usuário para o formulário de detalhamento ou para o próximo nível da consulta.


<div class="alert alert-danger">

* Os campos clicáveis serão destacados conforme o layout já adotado pelo PdT e terão a imagem de uma lupa.


**CORRGIR**

1- Em algumas páginas é exibido uma lupa em outras um olho. Padronizar para LUPA.
2- O campos clicáveis não estão em destaque

![](static/imagens/homologacao/lupa.png)

![](static/imagens/homologacao/olho.png)

  </div>

<div class="alert alert-danger">

**CORRIGIR**

 1- O título do gráfico da consulta de município está como 'Sem informação'

![](static/imagens/homologacao/titulo-grafico.png)

----
2- Alinhar nome do órgão a esquerda da tela

![](static/imagens/homologacao/alinhar-nome-orgao.png)

---

3- A tabela do segundo nível da consulta está desformatada.

![](static/imagens/homologacao/tabela-desformatada.png)

---


4- Ao selecionar um projeto pelo código na consulta de execução tanto a arvoré quanto o cabeçalho deve exibir além do nome do projeto o código, pois caso o usuário clique no projeto 9288133 e nesses campos apresentar apenas a descrição ele poderá ficar perdido onde está realmente.

![](static/imagens/homologacao/arvore-execucao.png)

 </div>

#### Download dos dados:
<a href="#top">(inicio)</a>

* **Download PDF:** O documento gerado em PDF deverá exibir:

<div class="alert alert-danger">

**CORRIGIR**

1-  A URL* não está sendo exibida

2- o arquivo gerado em PDF não está sendo exibido em outra aba do navegador e sim está fazendo o downolad

3- O arquivo gerado irá exibir os mesmos dados apresentados na tela considerando todos os filtros aplicados e inclusive o TOTAL GERAL ou SUBTOTAL conforme o comportamento do usuário. **Não é possível verificar, pois o download não está exibindo os dados**

![](static/imagens/homologacao/pdf-municipios.png)

 </div>

 * **OK** logo do Portal de Transparência no início da página e
 * **CORRIGIR** *URL*, paginação e a data no fim da página.
 * **CORRIGIR** O arquivo gerado irá exibir os mesmos dados apresentados na tela considerando todos os filtros aplicados e inclusive o TOTAL GERAL ou SUBTOTAL conforme o comportamento do usuário.
 * **CORRIGIR** ao selecionar essa opção o arquivo PDF deverá ser aberto em outra aba do navegador


* **Download Planilha (CSV):**

<div class="alert alert-danger">

**CORRIGIR**

1- Não está funcionando - O campo TOTAL GERAL também deverá ser exibido
2- Não está funcionando Exibir código e descrição em campos distintos, independente de o usuário selecionar a opção '*Exibir código e descrição*'

![](static/imagens/homologacao/csv-execucao.png)


 </div>

 * **OK** Será exibido a tabela completa de todas as páginas no formato CSV, independente do filtro aplicado.
 * O campo TOTAL GERAL também deverá ser exibido.  Não    
 * Exibir código e descrição em campos distintos, independente de o usuário selecionar a opção '*Exibir código e descrição*'

* **Download base completa:**

<div class="alert alert-danger">

**CORRIGIR**

Iremos informar o link do dataset para direcionamento.
Como ainda não temos o dataset de todos os conjuntos, o usuário será direcionado para o conjunto principal da consultado

</div>

 * O usuário será direcionado para o conjunto de dados da respectiva consulta no Portal de Dados Abertos.
 *O PdT deverá permitir que a equipe DTA inclua/altere a *url* desse campo através da área administrativa do Portal.                  
 * O PdT deverá permitir que por meio da área administrativa do Portal a equipe DTA decida se o campo Download Base Completa será exibido ou não na parte superior da tabela de resultado.

#### Barra de pesquisa

A barra de pesquisa deve aceitar várias formas de preenchimento dos dados:

* Desconsiderar acentuação, letras maiúsculas/minúsculas;
* Desconsiderar palavras intermediárias (ex.: Ao digitar “gestao pública”, um dos resultados será “Gestão da Administração Pública”);
* O usuário poderá pesquisar por qualquer coluna na tabela de resultados.

<div class="alert alert-success">

#### Compartilhar dados: OK
<a href="#top">(inicio)</a>

O usuário poderá Compartilhar os link dos dados nos seguintes canais, no mínimo:

- Twitter **OK**
- Facebook **OK**
- WhatsApp **OK**
- Por e-mail
- Copiar *url* **OK**

</div>

#### Campos Pesquisa básica - Navegação por filtros

###### Consulta por Projeto

* 1º NÍVEL
  - [Código Projeto]() -> ao clicar o usuário será direcionado para o 2º nível
  - Projeto
  - Anexo
  - Valor do Projeto


<div class="alert alert-danger">

**CORRIGIR**

1- Está faltando a coluna anexo

2- Corrigir o nome da coluna para 'Valor do Projeto'

![](static/imagens/homologacao/tabela-projeto.png)


</div>

* 2º NÍVEL

  * [Empenho]() -> ao clicar o usuário será direcionado para o 3º nível
  * Data de Registro do Empenho
  * Código Órgão - > apenas quando o usuário clicar em 'Exibir Código e Descrição'         
  * Órgão
  * CNPJ/CPF Favorecido
  * Favorecido
  * Valor Despesa Empenhada            
  * Valor Despesa Liquidada         
  * Valor Pago
  * Valor Liquidado em Restos a Pagar
  * Valor Pago em Restos a Pagar
  * Valor Total Pago


<div class="alert alert-danger">

**CORRIGIR**

1- A funcionalidade 'exibir código/descrição' não está aparecendo na tela


![](static/imagens/homologacao/atributos-tabela.png)

 </div>

* 3º NÍVEL
    - Formulário de Detalhamento

###### Consulta por Execução

  * 1º NÍVEL

    * [Código Projeto]() -> ao clicar o usuário será direcionado para o 2º nível
    * Código Órgão -> apenas quando o usuário clicar em 'Exibir Código e Descrição'           
    * Órgão               
    * Valor Despesa Empenhada            
    * Valor Despesa Liquidada         
    * Valor Pago
    * Valor Liquidado em RP
    * Valor Pago em Restos a Pagar
    * Valor Total Pago     

<div class="alert alert-danger">

**CORRIGIR**

- Esta faltando o código do órgão ao selecionar o campo 'Exibir código/descrição'
- Corrigir o texto da coluna "Valor total pago" e não valor a pagar

![](static/imagens/homologacao/tabela-orgao.png)

</div>

  * 2º NÍVEL **OK**
    * [Empenho]() -> ao clicar o usuário será direcionado para o 3º nível
    * Data de Registro do Empenho
    * CNPJ/CPF Favorecido
    * Favorecido
    * Valor Despesa Empenhada            
    * Valor Despesa Liquidada         
    * Valor Pago
    * Valor Liquidado em Restos a Pagar
    * Valor Pago em Restos a Pagar
    * Valor Total Pago

<div class="alert alert-danger">

**CORRIGIR**

- O segundo nível da consulta por execução não possui a coluna órgão;
- Corrigir o texto da coluna "Valor total pago" e não valor a pagar

![](static/imagens/homologacao/tabela-orgao-segundo-nivel.png)

</div>

  * 3º NÍVEL - Formulário de Detalhamento

###### Consulta por Município

<div class="alert alert-success">

  * 1º NÍVEL  
    * Ano  do Repasse    
    * Município           
    * [Empenho]()       
    * Data de Registro do Pagamento
    * Situação da Ordem de Pagamento
    * Valor Pago

</div>

<div class="alert alert-danger">

**CORRIGIR**

- Alinhar situação da ordem de pagamento a esquerda      

![](static/imagens/homologacao/tela-municipio-alinhar-coluna.png)


</div>

* 2º NÍVEL

<div class="alert alert-danger">

**CORRIGIR**

- Ao clicar no número do empenho o usuário deverá ser direcionado diretamente para o formulário de detalhamento.    


</div>

* 3º NÍVEL
    - Formulário de Detalhamento

###### Consulta por Receita

  * 1º NÍVEL       
    * Ano de Exercício     
    * Código da Classificação da Receita -> apenas quando o usuário clicar em 'Exibir Código e Descrição'   
    * Classificação da Receita
    * Código da Fonte de Recurso -> apenas quando o usuário clicar em 'Exibir Código e Descrição'   
    * Fonte de Recurso
    * Valor Previsto Inicial
    * Valor Previsto Atualizado
    * Valor Arrecadado

<div class="alert alert-danger">

**CORRIGIR**

- Ao Código da fonte de recurso não está sendo exibido

![](static/imagens/homologacao/tela-receita-código.png)

</div>

#### Leiaute - Formulário de Detalhamento
<a href="#top">(inicio)</a>

Ao clicar em campo clicável da tabela de resultados o usuário será direcionado para o formulário de detalhamento, que será composto pelos seguintes atributos:

* As tabelas que compõe o formulário de detalhamento serão exibidas em formato de guias (eg. [*Tabs*](https://www.w3schools.com/howto/howto_js_tabs.asp))

* O usuário poderá fazer o Download das informações do formulário de detalhamento ao clicar no botão '*Download*'.
A exportação em planilha (CSV) deverá ser em formato de tabela. Cada campo em uma coluna.

##### Campos do formulário de detalhamento OK

* Classificação Orçamentária
 ![](static/imagens/formulario-classificacao-orcamentaria.png)


<div class="alert alert-danger">

**CORRIGIR**

 - Alterar nome de  Classificação para **Classificação Orçamentária**
 - Alterar nome de empenho para **Número do Empenho**
 - A ordem dos campos deve ser a mesma solicitada

![](static/imagens/homologacao/formulario-classificacao.png)

</div>


* Empenho
 ![](static/imagens/formulario-empenho.png)


 <div class="alert alert-danger">

 **CORRIGIR**

  - A ordem dos campos deve ser a mesma solicitada;
  - Colocar os dados alinhados

![](static/imagens/homologacao/formulario-empenho.png)

</div>

 <div class="alert alert-success">

 OK
 --

* Liquidação
![](static/imagens/formulario-liquidacao.png)

----          
![](static/imagens/homologacao/detalhamento-liquidacao.png)

 </div>

* Pagamento
 ![](static/imagens/formulario-pagamento.png)

<div class="alert alert-danger">

 **CORRIGIR**

  - A quebra de linha no campo valor pago não é interessante, já que existe a quebra no favorecido acredito que podemos manter o valor pago sem quebra de linha.


![](static/imagens/homologacao/formulario-pagamento.png).

 </div>

* Outras Informações
  ![](static/imagens/formulario-outras-informacoes.png)


<div class="alert alert-danger">

   **CORRIGIR**

- Os campos estão trocados
- Se não há informações de convênios o formulário deve permanecer sem dados.

![](static/imagens/homologacao/formulario-outras-informacoes.png)

 </div>


<div class="alert alert-danger">

**CORRIGIR**

Ao exportar o formulário de detalhamento o arquivo zipado esta vindo por tabela e não por bloco.

![](static/imagens/homologacao/exporta-detalhamento.png)

 </div>