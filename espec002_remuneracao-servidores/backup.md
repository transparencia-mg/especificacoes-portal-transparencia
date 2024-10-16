---
title: Consulta Remuneração - Interface
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da Demanda
<a href="#top">(inicio)</a>

Essa demanda visa divulgar alterar a [consulta de remuneração](http://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores) para:

* divulgar o histórico da recebimentos de múltiplos anos na mesma tela;
* adequar o leiaute da interface aos campos da planilha de remuneração;
* utilizar elementos visuais para facilitar o entendimento da composição da remuneração;
* acrescentar informações da remuneração bruta/líquida nas tabelas de resultados da navegação por filtros.

# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

O formato atual de divulgação da consulta de Remuneração no Portal da Transparência apresenta apenas o histórico da recebimentos referentes ao ano corrente, o que tem sido objeto de dúvidas no Fale Conosco e no telefone 155, sobre a localização do histórico da recebimentos dos anos anteriores.

A prática adotada pelo Portal da Transparência é a transferência dos dados ao final do ano corrente para a base de dados do Portal de Dados Abertos, e a consequente exclusão desse dados na consulta de Remuneração.

Em relação a interface de divulgação, a especificação da consulta de remuneração foi elaborada em 2012 quando da publicação do decreto 45.969/12 que obriga a publicação da remuneração e revista em 2015, quando da atualização e reformulação do Portal da Transparência.

A revisão em 2015 visou dar mais transparência com relação à vida funcional dos servidores e à composição dos proventos. A interface web da consulta de remuneração foi alterada com a inserção dos novos campos, mas não foi feita as demais adequações para viabilizar a divulgação. Desde então existem campos disponibilizados na interface web da consulta que não possuem dados preenchidos.

# Especificação
<a href="#top">(inicio)</a>

## Leiaute - Tabelas navegação por filtros
<a href="#top">(inicio)</a>

Nas tabelas de resultado dos filtros

* [Nome do Servidor](http://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-filtros/201912/Robson%20Goncalves/0/0/0/0/0/0)
* [Cargo Efetivo](http://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-filtros/201912/0/0/3401/E/0/0/1)
* [Cargo em Comissão](http://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-filtros/201912/0/0/4007/C/0/0/2)
* [Órgão](http://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-filtros/201912/0/1066/0/0/0/0/3)

bem como no [quarto nível](http://transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-faixa/201911/4/1094/4028/C) da navegação default por [salários mínimos](http://transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-faixa/201911/3) os campos na tabela de resultado devem ser 

* Servidor
* Masp
* Cargo
* Órgão Exercício
* Remuneração Bruta
* Remuneração Líquida

Exemplo:

![](static/leiaute_tabelas_navegacao_filtros.png)

Atualmente somente são exibidos os campos Servidor, Masp e Órgão Exercício.

## Leiaute - Formulários detalhamento situação funcional e histórico da recebimentos
<a href="#top">(inicio)</a>

Após a seleção de um servidor utilizando qualquer um dos filtros da barra pesquisa, o Portal exibe o formulário da situação funcional e o histórico da recebimentos, conforme apresentado abaixo.

### Situação funcional

![](static/situacao_funcional.png)

* Os dados da situação funcional devem refletir a situação do mês/ano selecionado no filtro da _[barra de pesquisa]_ da consulta.

    ___Exemplo:___ Caso o usuário selecione os filtros `Ano: 2015 Mês: Janeiro` na _[barra de pesquisa]_, a situação funcional apresentada na tabela _[situação funcional]_ será a correspondente ao período Jan/2015.

### Histórico de recebimentos

![](static/historico_recebimentos.png)

* A coluna mês/ano será apresentada no formato mês(3 caracteres)/ano(4 caracteres).

    ___Exemplo:___ Set/2019

* Os dados da coluna mês/ano devem ser exibidos de forma decrescente (mais recente para o mais antigo);

* Quando o número de linhas da tabela _[histórico da recebimentos]_ for superior ao limite da página deve ser aplicada paginação conforme padrão das demais consultas.

* O cabeçalho da tabela histórico da recebimentos deve ser congelado, ou seja, quando o usuário usar a barra de rolagem horizontal o cabeçalho da tabela deve ficar sempre visível.                    
    ___Exemplo:___ [Cabeçalho fixo (_Fixed Header_)](https://uxdesign.cc/design-better-data-tables-4ecc99d23356#86cf)

    ![](https://miro.medium.com/max/800/1*kXEEaxvKP_9xRT0HuqScTQ.gif)

* A tabela _[histórico da recebimentos]_ deve exibir a opção de classificar em todas as colunas conforme já ocorre nas demais consultas do Portal.

* Os dados apresentados na tabela _[histórico da recebimentos]_ devem refletir o primeiro mês da série histórica disponível até o mês/ano selecionado no início da pesquisa.  

   ___Exemplo:___ O servidor Luiz possui dados disponíveis de Mai/2015 a Out/2019. Caso o usuário selecione no filtro da _[barra de pesquisa]_ os dados de Out/2017, o Portal exibirá dos dados de Mai/2015 a Out/2017.


### Formulário de detalhamento

A tabela histórico de recebimentos deve permitir que o usuário clique no mês/ano para detalhar as informações referente aqueles mês. A informação mês/ano virá em vermelho. 

Quando o usuário clicar em um desses campos o Portal exibe outra tabela detalhando os valores do mês selecionado. Deve ser possível a seleção de múltiplos meses.

___Exemplo:___ [Multi-Modal](https://uxdesign.cc/design-better-data-tables-4ecc99d23356#4a39)

![](https://miro.medium.com/max/800/1*Bu6hCcWjrXR0k_F5jEJO8g.gif)

Ao clicar no coluna mês/ano, linha Out/2019 o portal exibirá o detalhamento do mês de outubro, com cabeçalho detalhando nome do servidor e mês da pesquisa:

![](static/tabelamesano.jpg)

Algumas observações:

* O formulário de detalhamento deve apresentar a opção de fechar (x);
* O usuário pode mover o formulário de detalhamento para qualquer parte da tela.
* Considerando que do período de 2012 a 2019 não existe detalhamento dos dados da Remuneração e Deduções, o Portal não terá a opção do usuário exibir a tabela multi-modal nesse período.


### Exportação de arquivos

#### Exportar CSV

* A opção exportar dados deve gerar a planilha completa em forma de tabela com todos os dados das tabelas _[situação funcional]_ e _[histórico da recebimentos]_.

* Os dados de cada linha da planilha deve refletir a situação funcional e remuneração referente ao período (mês/ano). Ver: Modelo da Planilha CSV

    ___Exemplo 1___: A linha "Ago/2015" deve exibir a situação funcional e remuneração do servidor referente a agosto de 2015; A linha "Jan/2019" deve exibir a situação funcional e remuneração do servidor referente a janeiro/2019 e assim sucessivamente.

* Caso o usuário tenha selecionado um período específico na barra de pesquisa inicial o portal exporta apenas o histórico da recebimentos considerando o primeiro mês da série histórica disponível até o mês selecionado.

    ___Exemplo 2___:  O servidor Aroldo possui dados disponíveis de Mai/2012 a Out/2019. Caso o usuário selecione o mês janeiro/2019 na barra de pesquisa inicial do Portal. O Portal exibe e exporta para CSV o primeiro mês da série histórica disponível até o mês de Jan/2019 (Mai/2012 a Jan/2019).

    ___Exemplo 3___: Considerando ainda o servidor Aroldo. O mês atual é Out/2019. O Usuário não realizou nenhum filtro na barra de pesquisa inicial do Portal que por default utilizou o mês corrente (Out/2019). O Portal exibe e exporta para CSV o primeiro mês da série histórica disponível até o mês de Out/2019 (Mai/2012 a Out/2019).

#### Exportar PDF e imprimir

  * A opção deve permitir que o cidadão imprima ou gere o pdf dos dados exibidos na tela conforme já ocorre nas demais consultas do Portal.  


### Glossário Interativo: TOOL TIP

1. Mês/ano: Mês e ano de referência da remuneração
2. Vantagens: É composta pela soma das parcelas remuneratórias recebidas pelo servidor em razão do cargo, função ou emprego público, o que inclui adicionais, gratificações e vantagens pessoais.
3. 13º Salário e Férias: Valores próprios desses direitos.
4. Indenizações: Valores pagos a título de auxílio alimentação, auxílio transporte, ajuda de custose parcelas indenizatórias que não caracterizam como despesas de pessoal.
5. Atrasados: Valores pagos posteriormente ao fato gerador
6. Outros Valores: Valores pagos em condições excepcionais e transitórias, tais como: Indenizações, Decisões Judiciais e outros valores de natureza eventual.
7. Remuneração Bruta: Todos os valores devidos ao servidor no mês
8. Deduções: Valor referentes aos descontos obrigatórios e pagamentos indevidos, incluído os descontos que excedam o limite constituicional da remuneração. Não estão incluídos os descontos de caráter pessoal, tais como consignados, previdência complementar e pensão alimentícia. 
9. Remuneração Líquida: Valor da remuneração do servidor deduzidos das deduções realizadas no mês. O valor líquido apresentado pode ser superior ao efetivamente recebido, em face de não estarem inseridos os descontos de caráter pessoal.
10. Jetons empresas: É a remuneração percebida por servidores públicos estaduais em razão da participação como representantes do Estado em Conselhos de Administração e Fiscal ou órgãos equivalentes de empresas controladas direta ou indiretamente pelo Estado
