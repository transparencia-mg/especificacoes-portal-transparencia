---
contrato_manutencao: nº  (INF. )
proposta_comercial:
mantis:
pull_request: '[]()'
titulo: Despesa Pública
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da demanda
<a href="#top">(inicio)</a>


# Motivação / contexto da demanda
<a href="#top">(inicio)</a>


# Especificação
<a href="#top">(inicio)</a>


## Página Inicial - Pesquisa Básica
<a href="#top">(inicio)</a>

### Texto explicativo
<a href="#top">(inicio)</a>

Inclusão de um campo que irá trazer uma breve explicação do conteúdo da consulta.

#### Atributos do campo<br><br> Exemplo: [Página Inicial - Consulta Acordo Judicial de Reparação da Vale](https://www.transparencia.mg.gov.br/eventos-extraordinarios/acordo-judicial-reparacao-vale?task=estado_recursosvale.listarExecucoes&amp;ano=&amp;dataInicio=01/01/2021&amp;dataFim=31/12/2022&amp;consulta=2&amp;filtro=)


1. Seguir o padrão adotado na consulta Acordo Judicial de Reparação da Vale
2. O PdT deverá permitir que por meio da área administrativa do Portal a equipe DTA inclua ou altere os dados desse campo incluindo os *tooltips*.


##### Texto Introdutório

>

##### Tooltip dos termos destacados dentro do texto inicial

-

- **Observação:**<br> Ao clicar em qualquer termo destacado o usuário será direcionado para o termo especifico dentro do glossário do Portal.


## Leiaute - Barra de navegação
<a href="#top">(inicio)</a>

A barra de navegação superior será composta pelos seguintes campos:

* Ícones por tipo de Consulta;
* Período;
* Opção de *'Filtrar por'*;
* Botão *'Monte sua consulta'*

#### Atributos do campo<br>

* O campo período será no formato **dd/mm/aaaa** composto por início e fim (eg. 01/04/2021 a 30/12/2021);<br><br>
* No campo da data o usuário poderá selecionar ou digitar a data na caixa.<br>Exemplo: [Portal de Transparêcia ES](https://transparencia.es.gov.br/Despesa)

![](static/formato-data.gif)

* A pesquisa básica será composta por 4 ícones de tipo de consultas:
  * Órgão: xxxxxxxx
  * Função: xxxxxxxx
  * Programa: xxxxxxx
  * Favorecido: xxxxxx


* Os ícones serão clicáveis. Quando o usuário posicionar o mouse sobre o ícone será exibido um tooltip com uma breve descrição da consulta.

* O comportamento da opção *'Filtro'* será conforme o tipo de consulta selecionada e como padrão será exibido a opção 'Todos':
  - Órgão, Função, Programa: padrão já adotado no PdT
  ![](static/filtros.png)

  - Favorecido: Ao selecionar esse tipo de consulta o usuário poderá escolher se a busca será realizada pelo nome do Favorecido ou pelo CPF/CNPJ. Nesse caso deverá ser exibido uma barra onde o usuário irá digitar os dados, conforme já ocorre atualmente no PdT.
![](static/filtro-favorecido.png)

## Leiaute - Cabeçalho da tabelas
<a href="#top">(inicio)</a>

* A data de atualização dos dados (*Dados atualizados em*), o período, o ícone *Exibir Gráfico* ou *Fechar Gráfico*, Download, Compartilhar serão exibidos acima do gráfico/tabela de resultados.(MELHORAR)


## Leiaute - Tabelas navegação
<a href="#top">(inicio)</a>

* A pesquisa básica irá apresentar como padrão a tabela de resultados com os dados do exercício vigente por Órgão.

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
* O usuário terá a opção de verificar série histórica ao clicar no gráfico de barra.
* Os gráficos apresentaram os dados da coluna 'Valor Liquidado'


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

### CONSULTA POR ÓRGÃO
<a href="#top">(inicio)</a>

Essa consulta será composta por 5 níveis:
_______
  1º nível - [Órgão]()<br>
  2º nível - Órgão > [Elemento]()<br>
  3º nível - Órgão > Elemento > [Favorecido]()<br>
  4º nível - Órgão > Elemento > Favorecido > [Empenho]()<br>
  5º nível - Órgão > Elemento > Favorecido > Empenho > [Formulário de Detalhamento]()<br>
___________

##### 1º NÍVEL
  - Código do Órgão
  - [Órgão]() -> ao clicar o usuário será direcionado para o 2º nível
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>
  
  ![image](https://user-images.githubusercontent.com/53793354/200358592-fd3046ee-1c02-4cfc-b320-93a0bc1990bc.png)


##### 2º NÍVEL
  - [Elemento]() -> ao clicar o usuário será direcionado para o 3º nível
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

  ![image](https://user-images.githubusercontent.com/53793354/200359119-2bc8ec40-da77-40d5-b455-fbc7092aaf0c.png)


##### 3º NÍVEL
  - [Favorecido]() -> ao clicar o usuário será direcionado para o 4º nível
  - CPF / CNPJ
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

  ![image](https://user-images.githubusercontent.com/53793354/200358491-87bb0982-39ab-4880-8c12-3b4f2a73d9d6.png)


##### 4º NÍVEL
  - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento
  - Data de registro do Empenho
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/200358187-8ece2a7c-6631-491c-9691-bc24b30a86de.png)


##### 5º NÍVEL

 - Formulário de Detalhamento

Ao clicar no número do empenho o usuário será direcionado para o formulário de detalhamento, que será composto pelos seguintes atributos:
  * As tabelas que compõe o formulário de detalhamento serão exibidas em formato de guias (eg. Tabs)
  * O usuário poderá fazer o Download das informações do formulário de detalhamento ao clicar no botão 'Download'.

### CONSULTA POR FUNÇÃO
<a href="#top">(inicio)</a>

Essa consulta será composta por 4 níveis:
_______
  1º nível - [Função]()<br>
  2º nível - Função > [Subfunção]()<br>
  3º nível - Função > Subfunção > [Favorecido]()<br>
  4º nível - Função > Subfunção > Favorecido > [Empenho]()<br>
  5º nível - Função > Subfunção > Favorecido > Empenho > [Formulário de Detalhamento]()<br>
___________

##### 1º NÍVEL
  - Código da Função
  - [Função]() -> ao clicar o usuário será direcionado para o 2º nível
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

  ![image](https://user-images.githubusercontent.com/53793354/200358699-3acd5a01-9948-437c-96b6-fa2f06726f5a.png)


##### 2º NÍVEL
  - Código do Subfunção
  - [Subfunção]() -> ao clicar o usuário será direcionado para o 3º nível
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

  ![image](https://user-images.githubusercontent.com/53793354/200358762-207b6b03-df53-471b-be0a-dd07e358c58f.png)

  
##### 3º NÍVEL
  - [Favorecido]() -> ao clicar o usuário será direcionado para o 4º nível
  - CPF / CNPJ
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

  ![image](https://user-images.githubusercontent.com/53793354/200358449-0858169f-08d3-433c-bf94-31d3bbdfac3d.png) 


##### 4º NÍVEL
  - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento
  - Data de registro do Empenho
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/200358222-32287309-16be-48ea-92ef-fa941c975271.png)


##### 5º NÍVEL

- Formulário de Detalhamento

### CONSULTA POR PROGRAMA
<a href="#top">(inicio)</a>

Essa consulta será composta por 5 níveis:
_______
  1º nível - [Programa]()<br>
  2º nível - Programa > [Ação]()<br>
  3º nível - Programa > Ação > [Favorecido]()<br>
  4º nível - Programa > Ação > Favorecido > [Empenho]() ><br>
  5º nível - Programa > Ação > Favorecido > Empenho > Formulário de Detalhamento<br>
___________

##### 1º NÍVEL
  - Código da Programa
  - [Programa]() -> ao clicar o usuário será direcionado para o 2º nível
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

  ![image](https://user-images.githubusercontent.com/53793354/200358865-cd1aee56-75a1-42c9-aa95-fafcda4db320.png)


##### 2º NÍVEL
  - Código do Ação
  - [Ação]() -> ao clicar o usuário será direcionado para o 3º nível
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

  ![image](https://user-images.githubusercontent.com/53793354/200358964-74159e14-a951-4c49-b6a0-4bd377975681.png)


##### 3º NÍVEL
  - [Favorecido]() -> ao clicar o usuário será direcionado para o 4º nível
  - CPF / CNPJ
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>
  
  ![image](https://user-images.githubusercontent.com/53793354/200358390-eb905243-e139-4538-a84e-a006c4123d0d.png)


##### 4º NÍVEL
  - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento
  - Data de registro do Empenho
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/200358241-b7811142-0bee-4068-ad93-c3f3378bbf8a.png)

##### 5º NÍVEL

- Formulário de Detalhamento


### CONSULTA POR FAVORECIDO (NOME E CPF/CNPJ)
<a href="#top">(inicio)</a>

Essa consulta será composta por 5 níveis:
_______
  1º nível - [Favorecido]()<br>
  2º nível - Favorecido > [Empenho]()<br>
  3º nível - Favorecido > Empenho > Formulário de Detalhamento<br>
___________

##### 1º NÍVEL
  - [Favorecido]() -> ao clicar o usuário será direcionado para o 4º nível
  - CPF / CNPJ
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

  ![image](https://user-images.githubusercontent.com/53793354/200358337-66705311-e9ed-432a-a373-ef1fdf8dbf7d.png)


##### 2º NÍVEL
  - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento
  - Data de registro do Empenho
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

  ![image](https://user-images.githubusercontent.com/53793354/200358252-cadc7f6c-cc98-45a7-808d-50b30195afcb.png)

##### 3º NÍVEL

- Formulário de Detalhamento



## Campos Pesquisa básica - Navegação por filtros
<a href="#top">(inicio)</a>

Os dados dessa consulta serão extraídos do Universo BO SIAFI:
  * Armazém BO / ~tmp /nova-espec-despesa

#### Filtros da Consulta
