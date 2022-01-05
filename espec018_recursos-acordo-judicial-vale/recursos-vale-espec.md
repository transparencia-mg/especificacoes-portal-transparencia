---
contrato_manutencao: nº 15210010062019 (INF. 3951)
proposta_comercial:
mantis:
pull_request: '[]()'
titulo: Transparência dos recursos da Vale - Acordo Judicial 04/02/2021
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da demanda
<a href="#top">(inicio)</a>

Essa demanda visa a criação de uma seção no Portal da Transparência para possibilitar o acompanhamento das ações desenvolvidas pelo Governo do Estado de Minas Gerais com recursos provenientes do acordo judicial firmado com a Vale. Considerando a relevância e os valores envolvidos no acordo, a seção será um instrumento de transparência e prestação de contas a sociedade colocando em evidência a execução do acordo.

Juntamente com a criação da nova seção será implementado no Portal da Transparência algumas necessidades dos usuários identificadas durante o projeto **Experiência do Usuário no Portal da Transparência**, realizado em abril de 2021, como por exemplo:

- Alteração do Formulário de Detalhamento;
- Pesquisa básica mais intuitiva e dinâmica;
- Inclusão de novas informações;
- Consolidação os dados de Despesa e RP em uma única consulta.


# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

O Governo de Minas, o Ministério Público de Minas Gerais (MPMG), o Ministério Público Federal (MPF) e a Defensoria Pública de Minas Gerais (DPMG) assinaram um termo de Medidas de Reparação, no dia 4 de fevereiro de 2021, que garante que a empresa Vale seja imediatamente responsabilizada pelos danos causados às regiões atingidas e à sociedade mineira pelo rompimento da barragem Mina Córrego do Feijão, em Brumadinho, no ano de 2019.

O documento define “obrigações de fazer” e “obrigações de pagar” da Vale e prevê um total de recursos a serem aplicados em reparação socioambiental e socioeconômica de R$37.689.767.329,00 (trinta e sete bilhões, seiscentos e oitenta e nove milhões, setecentos e sessenta e sete mil, trezentos e vinte e nove reais). Destes, R$11.060.000.000,00 (onze bilhões e sessenta milhões) serão utilizados pelo Poder Executivo estadual para execução de projetos de mobilidade (anexo III), fortalecimento do serviço público (anexo IV), segurança hídrica (anexo II.3) e ressarcimento de despesas decorrentes da execução do referido Termo Judicial.

A [Lei nº 23.830/2021](https://www.almg.gov.br/consulte/legislacao/completa/completa.html?tipo=LEI&num=23830&comp=&ano=2021), publicada em 28/07/2021, autorizou abertura de crédito suplementar ao orçamento do Estado em função dos recursos previstos no Termo de Reparação que deverão ser alocados conforme consta no Acordo Judicial.


# Especificação
<a href="#top">(inicio)</a>

Esse documento tem como base a criação de uma nova consulta para possibilitar o acompanhamento das ações desenvolvidas pelo Governo do Estado de Minas Gerais com recursos provenientes do acordo judicial firmado com a Vale.

## Página Inicial da consulta - Pesquisa Básica
<a href="#top">(inicio)</a>

#### Texto explicativo
<a href="#top">(inicio)</a>

Inclusão de um campo que irá trazer uma breve explicação do conteúdo da consulta.  

Atributos do campo:

* O usuário poderá exibir mais detalhes do texto ao clicar em "*Saiba Mais*" ou ocultar ao clicar "*Ocultar*". [eg. Leroy Merlin](https://www.leroymerlin.com.br/materiais-hidraulicos).
* A funcionalidade deverá permitir a visualização de *tooltip* ao posicionar o mouse sobre uma palavra ou termo. [eg. tooltips](https://getbootstrap.com.br/docs/4.1/components/tooltips/)
* Ao clicar sobre a palavra ou termo o PdT deverá abrir um um *pop-up* em forma de glossário. [eg. pop-up](https://www.usaspending.gov/)
* O PdT deverá permitir que por meio da área administrativa do Portal a equipe DTA inclua ou altere os dados desse campo incluindo os *tooltips*.

Exemplos:  
- Saiba Mais
![](static/imagens/texto-explicativo.png)
____

- Tooltip de termos
![](static/imagens/texto-explicativo-ocultar.png)
___

- Pop-up
![](static/imagens/texto-explicativo-glossario.png)


#### Leiaute - Barra de navegação
<a href="#top">(inicio)</a>

A barra de navegação superior será composta pelos seguintes campos:

* Ícones por tipo de consulta;
* Período (mm/aaaa)
* Opção de *'Filtrar por'*;
* Botão *'Monte sua consulta'*

###### Observações:

* A pesquisa básica será composta, inicialmente, por 4 ícones de tipo de consultas:
  * Por projeto
  * Por Órgão
  * Por Receita
  * Transferência por Município

* Os ícones serão clicáveis. Quando o usuário posicionar o mouse sobre o ícone será exibido um *tooltip* com uma breve descrição da consulta.

* O campo período será no formato **mm/aaaa** composto por início e fim (eg. 04/2021 a 12/2021);
* O comportamento da opção *'Filtrar por'* será conforme o tipo de consulta selecionada e como padrão será exibido a opção 'Todos'
  * **Por Projeto**: Ao selecionar essa opção o usuário poderá escolher o Projeto a ser exibido.
  * **Por Órgão**: Ao selecionar esse tipo de consulta no campo *"Filtrar por"* o usuário poderá escolher se a busca será realizada pelo nome do Favorecido ou pelo CPF/CNPJ.
  * **Por Receita**:
  * **Transferência por Município**:

![](static/imagens/barra-navegacao-superior.png)


#### Leiaute - Tabelas navegação
<a href="#top">(inicio)</a>

* A tabela de resultado levará em consideração os parâmetros dos filtros aplicados.

* A pesquisa básica irá apresentar como padrão a tabela de resultados com os dados do exercício vigente e os dados da consulta 'Por Projeto'.

* A data de atualização dos dados (*Dados atualizados em*), o período e o ícone *Exibir Gráfico* ou *Exibir Tabela* serão exibidos acima da tabela de resultados.

* Como padrão os dados serão exibidos no formato de tabela e caso o usuário queira visualizar os dados em forma de gráfico deve clicar em '*Exibir Gráfico*'. Para retornar a exibição no formato tabela o usuário deve clicar em '*Exibir Tabela*'

* A barra de pesquisa da tabela de resultado deverá retornar os dados a medida que o usuário for digitando. O atributo *placeholder* deve ser aplicado na barra de pesquisa.

* Os valores TOTAL GERAL e o SUBTOTAL serão exibidos na tabela de resultados de acordo com o comportamento do usuário:

  * **TOTAL GERAL:** quando o usuário não aplicar nenhum filtro na tabela ou quanto todos os dados forem exibidos em uma única página, ou seja, sem paginação;
  * **SUBTOTAL:** quando o usuário aplicar qualquer filtros na tabela através da barra de pesquisa ou quando houver paginação no tabela de resultado, ou seja, houver mais de uma página de resultado.

* O usuário poderá solicitar a exibição dos dados com código e descrição. Ao clicar no botão '*Exibir código e descrição*' uma nova coluna será adicionada a esquerda de cada coluna que tenha a descrição.

![](static/imagens/tabela-resultados-parte-superior.png)


##### Estrutura de design das tabelas de resultados

 * Cabeçalho fixo - Fixer Header (eg. Consulta de Remuneração do PdT);
 * Rolagem horizontal - Horizontal Scroll. Quando o número de colunas ultrapassar o limite da página o PdT deve possibilizar a rolagem horizontal;
 * Colunas movíveis e classificáveis conforme ocorre atualmente;
 * Paginação e seleção da quantidade de linhas a serem exibidas, conforme ocorre atualmente;
 * O texto deve ser ajustável nas colunas, ou seja, caso seja necessário pode haver quebra de linha;
 * A tabela apresentará campos clicáveis (com link) que irá direcionar o usuário para o formulário de detalhamento ou para o próximo nível da consulta.
 * Os campos clicáveis serão destacados conforme o layout já adotado pelo PdT e terão a imagem de uma lupa.

#### Download dos dados:
<a href="#top">(inicio)</a>

* **Download PDF:** O documento gerado em PDF deverá exibir:
 * logo do Portal de Transparência no início da página e
 * *URL*, paginação e a data no fim da página.
 * O arquivo gerado irá exibir os mesmos dados apresentados na tela considerando todos os filtros aplicados e inclusive o TOTAL GERAL ou SUBTOTAL conforme o comportamento do usuário.


* **Download tabela:**
Será exibido a tabela completa de todas as páginas no formato CSV, independente do filtro aplicado. O campo TOTAL GERAL também deverá ser exibido.      
 Exibir código e descrição em campos distintos, independente de o usuário selecionar a opção '*Exibir código e descrição*'

* **Download base completa:** O usuário será direcionado para o conjunto de dados da respectiva consulta no Portal de Dados Abertos. O PdT deverá permitir que a equipe DTA inclua/altere a *url* desse campo através da área administrativa do Portal.                  
O PdT deverá permitir que por meio da área administrativa do Portal a equipe DTA decida se o campo Download Base Completa será exibido ou não na parte superior da tabela de resultado.

##### Barra de pesquisa

A barra de pesquisa deve aceitar várias formas de preenchimento dos dados:

* Desconsiderar acentuação, letras maiúsculas/minúsculas;
* Desconsiderar palavras intermediárias (ex.: Ao digitar “gestao pública”, um dos resultados será “Gestão da Administração Pública”);
* O usuário poderá pesquisar por qualquer coluna na tabela de resultados.

#### Leiaute - Formulário de Detalhamento
<a href="#top">(inicio)</a>

Ao clicar no campo clicável da tabela de resultados e o usuário for direcionado para o formulário de detalhamento, esse será composto pelos seguintes atributos:

* As tabelas que compõe o formulário de detalhamento será exibidas em formato de guias (eg. [*Tabs*](https://www.w3schools.com/howto/howto_js_tabs.asp))

* O usuário poderá exportar as informações do formulário de detalhamento ao clicar no botão '*Exportar*'.
         Definir se a exportação será em pdf ou tabela

## Monte sua consulta
<a href="#top">(inicio)</a>

A estrutura da pesquisa avançada está descrita na documentação [Remodelagem da Pesquisa Avançada](https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/espec016_remodelagem-pesquisa-avancada/espec016_remodelagem-pesquisa-avancada/pesquisa-avandada-espec.md).
