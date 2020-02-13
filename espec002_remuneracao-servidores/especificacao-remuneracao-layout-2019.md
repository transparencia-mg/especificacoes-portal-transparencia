---
contrato_manutencao: nº 15210010062019 (INF. 3951)
proposta_comercial: nº 626584/19
pull_request:
title: Consulta Remuneração - Interface
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da Demanda
<a href="#top">(inicio)</a>

Essa demanda visa alterar a [consulta de remuneração](http://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores) para:

* divulgar o histórico da remuneração de múltiplos anos na mesma tela;
* adequar o leiaute da interface aos campos da planilha de remuneração;
* utilizar elementos visuais para facilitar o entendimento da composição da remuneração;
* acrescentar informações da remuneração bruta/líquida nas tabelas de resultados da navegação por filtros.

# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

O formato atual de divulgação da consulta de Remuneração no Portal da Transparência apresenta apenas o histórico da remuneração referentes ao ano corrente, o que tem sido objeto de dúvidas no Fale Conosco e no telefone 155, sobre a localização do histórico da remuneração dos anos anteriores.

A prática adotada pelo Portal da Transparência é a transferência dos dados ao final do ano corrente para a base de dados do Portal de Dados Abertos, e a consequente exclusão desse dados na consulta de Remuneração.

Em relação a interface de divulgação, a especificação da consulta de remuneração foi elaborada em 2012 quando da publicação do Decreto n 45.969/12 que obriga a publicação da remuneração e revista em 2015, quando da atualização e reformulação do Portal da Transparência.

A revisão em 2015 visou ofertar mais transparência com relação à vida funcional dos servidores e à composição dos proventos. A interface web da consulta de remuneração foi alterada com a inserção dos novos campos, mas não foi feita as demais adequações para viabilizar a divulgação. Desde então existem campos disponibilizados na interface web da consulta que não possuem dados preenchidos.

# Especificação
<a href="#top">(inicio)</a>

## Leiaute - Tabelas navegação por filtros
<a href="#top">(inicio)</a>

Incluir os campos ___cargo, remuneração bruta e remuneração líquida___ nas tabelas de resultado dos filtros

* [Nome do Servidor](http://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-filtros/201912/Robson%20Goncalves/0/0/0/0/0/0)
* [Cargo Efetivo](http://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-filtros/201912/0/0/3401/E/0/0/1)
* [Cargo em Comissão](http://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-filtros/201912/0/0/4007/C/0/0/2)
* [Órgão](http://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-filtros/201912/0/1066/0/0/0/0/3)

bem como no [quarto nível](http://transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-faixa/201911/4/1094/4028/C) da navegação default por [salários mínimos](http://transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-faixa/201911/3). Os campos na tabela de resultado devem ser

* Servidor
* Masp
* Cargo
* Órgão Exercício
* Remuneração Bruta
* Remuneração Líquida

Exemplo:

![](static/leiaute_tabelas_navegacao_filtros.png)

As tabelas devem possuir o comportamento padrão em relação a paginação, filtro, compartilhamento em redes sociais e exportação/impressão.

## Leiaute - Formulários detalhamento situação funcional e histórico de recebimentos
<a href="#top">(inicio)</a>

Após a seleção de um servidor utilizando qualquer um dos filtros da barra pesquisa, o Portal deve exibir o formulário da situação funcional e o histórico da recebimentos, conforme apresentado abaixo.

### Situação funcional

![](static/situacao-funcional.png)

Os dados da situação funcional devem refletir a situação do mês/ano selecionado no filtro da _[barra de pesquisa]_ da consulta.

___Exemplo:___ Caso o usuário selecione os filtros `Ano: 2015 Mês: Janeiro` na _[barra de pesquisa]_, a situação funcional apresentada na tabela _[situação funcional]_ será a correspondente ao período Jan/2015.

### Histórico de recebimentos

![](static/historico-recebimentos.png)

Algumas observações:

* Valores zero devem ser apresentados como "-"

* A coluna mês/ano deve ser apresentada no formato mês(3 caracteres)/ano(4 caracteres). ___Exemplo:___ Set/2019

* Os dados da coluna mês/ano devem ser exibidos de forma decrescente (mais recente para o mais antigo)

* Quando o número de linhas da tabela _[histórico da recebimentos]_ for superior ao limite da página deve ser aplicada paginação conforme padrão das demais consultas

* O cabeçalho da tabela histórico da recebimentos deve ser congelado, ou seja, quando o usuário usar a barra de rolagem horizontal o cabeçalho da tabela deve ficar sempre visível. ___Exemplo:___ [Cabeçalho fixo (_Fixed Header_)](https://uxdesign.cc/design-better-data-tables-4ecc99d23356#86cf)

![](static/fixed-header.gif)

* A tabela _[histórico da recebimentos]_ deve exibir a opção de classificar em todas as colunas conforme já ocorre nas demais consultas do Portal.

* Os dados apresentados na tabela _[histórico da recebimentos]_ devem refletir o primeiro mês da série histórica disponível até o mês/ano selecionado no início da pesquisa.  

    ___Exemplo:___ O servidor Luiz possui dados disponíveis de Mai/2015 a Out/2019. Caso o usuário selecione no filtro da _[barra de pesquisa]_ os dados de Out/2017, o Portal exibirá dos dados de Mai/2015 a Out/2017.

##### Glossário Interativo: TOOL TIP

O glossário interativo do histórico de recebimentos deve apresentar os seguintes textos:

1. __Mês/ano:__ Mês e ano de referência da remuneração;
2. __Remuneração Básica:__ É composta pela soma das parcelas remuneratórias correspondentes ao cargo efetivo, a função ou o cargo comissionado.
3. __Férias:__ Valores próprios desses direitos.
4. __Gratificação Natalina:__ Valores próprios desses direitos.
5. __Outros valores:__ Valores pagos em condições excepcionais e transitórias, tais como: Indenizações, Decisões Judiciais,  e outros valores de natureza eventual.
6. __Total:__ Soma dos valores da remuneração básica, férias, Gratificação Natalina e Outros Valores.
7. __Descontos:__ Valor referentes aos descontos obrigatórios e pagamentos indevidos, incluído os descontos que excedam o limite constituicional da remuneração. Não estão incluídos os descontos de caráter pessoal, tais como consignados, previdência complementar e pensão alimentícia.
8. __Remuneração líquida:__ Valor da remuneração do servidor deduzidos das deduções realizadas no mês. O valor líquido apresentado pode ser superior ao efetivamente recebido, em face de não estarem inseridos os descontos de caráter pessoal.
9. __Jetons Empresas:__ É a remuneração percebida por servidores públicos estaduais em razão da participação como representantes do Estado em Conselhos de Administração e Fiscal ou órgãos equivalentes de empresas controladas direta ou indiretamente pelo Estado

#### Formulário de detalhamento

A tabela histórico de recebimentos deve permitir que o usuário clique no mês/ano para detalhar as informações referente aqueles mês. A informação mês/ano virá em vermelho como forma de destacar a possibilidade de clique. 

Quando o usuário clicar em um desses campos o Portal exibe outra janela detalhando os valores do mês selecionado. Deve ser possível a seleção de múltiplos meses sem perda de contexto. 

___Exemplo:___ [Multi-Modal](https://uxdesign.cc/design-better-data-tables-4ecc99d23356#4a39)

![](static/multi-modal.gif)

Ao clicar no coluna mês/ano, linha Out/2019 o portal exibirá o detalhamento do mês de outubro, com cabeçalho detalhando nome do servidor e mês da pesquisa:

![](static/formulario-detalhamento.png)

Algumas observações:

* O formulário de detalhamento deve apresentar a opção de fechar (x)
* O usuário pode mover o formulário de detalhamento para qualquer parte da tela
* Valores zero devem ser apresentados como "-"
* A seção de detalhamento dos jetons empresas somente deve ocorrer para os casos em que os valores não forem zerados para o mês destacado. __Exemplo:__

![](static/formulario-detalhamento-jetons.png)

### Exportação de arquivos

Ao contrário da situação atual, a funcionalidade de impressão e exportação (CSV e PDF) deve existir tanto nas tabelas de navegação por filtros quanto nos formulários de detalhamento da situação funcional e histórico de recebimentos.

Nas tabelas de navegação por filtros as regras de exportação/impressão devem seguir o padrão das demais consultas. A seguir são destacadas as particularidades das regras exportação/impressão para os formulários de detalhamento da situação funcional e histórico de recebimentos:

* A opção exportar dados deve gerar a planilha completa em forma de tabela com todos os dados das tabelas _[situação funcional]_ e _[histórico da remuneração]_.

* Os dados de cada linha da planilha deve refletir a situação funcional e remuneração referente ao período (mês/ano).

      ___Exemplo 1___: A linha "Ago/2015" deve exibir a situação funcional e remuneração do servidor referente a agosto de 2015; A linha "Jan/2019" deve exibir a situação funcional e remuneração do servidor referente a janeiro/2019 e assim sucessivamente.

* O leiaute da planilha exportada deve serguir o formato da planilha de remuneração disponibilizada pela CGE com inserção de uma coluna `mes` no formato `YYYY-MM-01`. Vide [arquivo exemplo](static/csv-usuario.csv).

* Os valores zero devem ser exportados como valores númericos `0`
