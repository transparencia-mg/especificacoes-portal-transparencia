---
Título: "Homologação do layout - Consulta Remuneração"
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

## Homologação finalizada em 11/08/2020.


[VERSÃO HTML](http://htmlpreview.github.io/?https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/master/espec002_remuneracao-servidores/especificacao-remuneracao-layout-2019-homologa-layout.html)

# Homologação do layout
<a href="#top">(inicio)</a>


## Leiaute - Tabelas navegação por filtros
<a href="#top">(inicio)</a>

Incluir os campos ___remuneração bruta e remuneração líquida___ nas tabelas de resultado dos filtros

* [Nome do Servidor]()  

<div class="alert alert-success">

 __CONFERE__

![](static/layout-tabela-filtro-servidor.png)
</div>


* [Cargo Efetivo]()

<div class="alert alert-success">

__CONFERE__

![](static/layout-tabela-filtro-cargo-efetivo.png)
</div>

* [Cargo em Comissão]()

<div class="alert alert-success">

__CONFERE__

![](static/layout-tabela-filtro-cargo-comissao.png)
</div>

* [Órgão]()

<div class="alert alert-success">

__CONFERE__

![](static/layout-tabela-filtro-orgao.png)

</div>

bem como no [quarto nível]() da navegação default por [salários mínimos](http://transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-faixa/201911/3). Os campos na tabela de resultado devem ser

* Servidor
* Masp
* Órgão Exercício
* Remuneração Bruta
* Remuneração Líquida

Exemplo:

![](static/leiaute_tabelas_navegacao_filtros.png)

<div class="alert alert-success">

__CONFERE__

![](static/layout-leiaute_tabelas_navegacao_filtros.png)

</div>

* O campo remuneração bruta refere-se ao campo _[Total]_ da tabela histórico recebimentos;

<div class="alert alert-success">

__CORRIGIDO__

<s>O portal não está exibindo os valores referente ao campo _[Total]_ na remuneração bruta. Os valores que estão sendo exibidos refere-se ao campo remuneração básica</s>

![](static/layout-remuneracao-bruta-tabela-corrigido.png)

**Valores corretos a serem exibidos:**

![](static/layout-remuneracao-bruta.png)

</div>


* O campo remuneração líquida refere-se ao campo _[Remuneração Líquida]_ da tabela histórico recebimentos.
__CONFERE__

* As tabelas devem possuir o comportamento padrão em relação a paginação, filtro, compartilhamento em redes sociais e exportação/impressão.

<div class="alert alert-info">

**Não é possível aplicar essa funcionalidade**

Mensagem da PRODEMGE (Alan):

"*Na tela de listagem de Servidores não é possível ter opção Exibir Todos pois se trata de uma tela com paginação pelo servidor justamente pela grande quantidade de registros que ela pode trazer, travando a página caso tente exibir todos os dados.*"

A opção "todas" não está ativa em nenhuma consulta conforme ocorre na consulta de despesa
--
![](static/layout-paginacao.png)

--
</div>

<div class="alert alert-success">

__CORRIGIDO__

<s>Ao realizar a classificação de valores o "TOTAL GERAL" é considerado na classificação</s>

![](static/layout-classificar-valor-total-corrigido.png)

</div>

<div class="alert alert-success">

__CORRIGIDO__

<s>O "TOTAL GERAL" não está sendo exibido no fim da tabela</s>


![](static/layout-valor-total-fim-tabela-corrigido.png)

</div>

<div class="alert alert-success">

__CORRIGIDO__

<s>O campo "TOTAL GERAL"deve vir em negrito</s>


![](static/layout-valor-total-negrito-corrigido.png)
</div>


<div class="alert alert-success">

__CORRIGIDO__

<s>Considerando a estrutura padrão do portal ao utilizar o campo "filtrar" o Portal de deve apresentar como "TOTAL GERAL" o valor total do filtro inicial da pesquisa.</s>

Filtro utilizado na pesquisa: ***Fontenelle***


![](static/layout-valor-total-fitro-resultado-corrigido.png)

Resultado utilizando o campo [filtrar]: ***Rodrigo***

![](static/layout-valor-total-fitro-corrigido.png)


</div>

<div class="alert alert-info">

**Ficou definido pela DTA que a tabela de remuneração deve seguir o padrão do portal, conforme sugestão da PRODEMGE.**

Mensagem PRODEMGE (Alan):

"*Peço que reconsiderem as cores da tela de Detalhamento, pois as cores verde e amerela não são padrão do site, quase todas as telas de detalhamento não possuem cores, exceto a até então tela de remuneração e a de viagens.*"

Inserir as cores padrões na planilha


![](static/layout-cor-situacao-funcional.png)

![](static/layout-cor-historico-remuneracao.png)

![](static/layout-cor-popup.png)

</div>

<div class="alert alert-success">

__CORRIGIDO__

<s>Colocar os Cabeçalhos em negrito</s>


![](static/layout-cabecalho-negrito-corrigido.png)

</div>

* Quando a base de dados (tabela de dados) apresentar o mesmo servidor com dois ou mais vínculos, o Portal deve apresentar cada vínculo em uma linha com os seus respectivos valores, ou seja, cada linha da planilha deve refletir uma linha no Portal.

<div class="alert alert-success">

__CONFERE__

Mês Fevereiro
--

![](static/layout-zulma-goncalves-planilha.png)

![](static/layout-zulma-goncalves-planilha-csv.png)

Resultado ao clicar na linha de valor: 2.657,67
--

![](static/layout-zulma-goncalves-detalhamento-linha1.png)

Resultado ao clicar na linha de valor: 2.491,56
--
![](static/layout-zulma-goncalves-detalhamento-linha2.png)

</div>


  __Exemplo:__ Servidora: ZULMA GONCALVES DE AGUIAR - JAN/2019 -

  Atualmente o Portal apresenta a servidora em linhas distintas, no entanto ao solicitar a exibição do detalhamento da remuneração o Portal duplica a informação de um vínculo desconsiderando as informações do segundo vínculo.

![](static/zulma-goncalves-planilha.png)

![](static/zulma-goncalves-portal.png)

Resultado após clicar em qualquer um dos vínculos

![](static/zulma-goncalves-detalhamento.png)


### Glossário Interativo: TOOL TIP

O glossário interativo das tabelas de navegação deve apresentar os seguintes textos:

1. __Servidor:__ Nome do servidor civil ou militar conforme registrado nos Sistemas de Pagamento de Pessoal do Estado de Minas Gerais.

<div class="alert alert-success">

__CONFERE__

![](static/layout-tooltip-servidor.png)
</div>

1. __Masp:__ Matrícula do servidor civil ou militar de Minas Gerais.

<div class="alert alert-success">

__CONFERE__

![](static/layout-tooltip-masp.png)
</div>

1. __Órgão Exercício:__ Órgão ou entidade de exercício do servidor.

<div class="alert alert-success">

__CONFERE__

![](static/layout-tooltip-orgao-exercicio.png)
</div>

1. __Remuneração Bruta:__ Composta pela soma das parcelas remuneratórias correspondentes ao cargo efetivo, a função ou cargo comissionado, bem como gratificações de qualquer natureza e vantagens pecuniárias de caráter temporário ou permanente (gratificação natalina, férias e etc).

<div class="alert alert-success">

__CONFERE__

![](static/layout-tooltip-remuneracao-bruta.png)
</div>

1. __Remuneração Líquida:__ Valor da remuneração do servidor após deduções obrigatórias realizadas no mês. O valor líquido apresentado pode ser superior ao efetivamente recebido, em face de não estarem inseridos os descontos de caráter pessoal.

<div class="alert alert-success">

__CONFERE__

![](static/layout-tooltip-remuneracao-liquida.png)
</div>


## Leiaute - Formulários detalhamento situação funcional e histórico de recebimentos
<a href="#top">(inicio)</a>

Após a seleção de um servidor utilizando qualquer um dos filtros da barra pesquisa, o Portal deve exibir o formulário da situação funcional e o histórico de recebimentos, conforme apresentado abaixo.

### Situação funcional

![](static/situacao-funcional.png)

<div class="alert alert-success">

__CONFERE__

![](static/layout-situacao-funcional.png)
</div>

Os dados da situação funcional devem refletir a situação do mês/ano selecionado no filtro da _[barra de pesquisa]_ da consulta.

<div class="alert alert-success">

__CONFERE__

Dados foram conferidos tomando como exemplo a Servidora: zulma-goncalves

![](static/layout-zulma-goncalves-planilha.png)

![](static/layout-zulma-goncalves-planilha-csv.png)

Resultado ao clicar na linha de valor: 2.657,67
--

![](static/layout-zulma-goncalves-detalhamento-linha1.png)

Resultado ao clicar na linha de valor: 2.491,56
--

![](static/layout-zulma-goncalves-detalhamento-linha2.png)

</div>

___Exemplo:___ Caso o usuário selecione os filtros `Ano: 2015 Mês: Janeiro` na _[barra de pesquisa]_, a situação funcional apresentada na tabela _[situação funcional]_ será a correspondente ao período Jan/2015.

<div class="alert alert-warning">

**OBS:** Testes referente a mais anos serão verificados em produção, pois no ambiente de homologação estão disponíveis apenas 3 meses.
--
</div>


### Histórico recebimentos

![](static/historico-recebimentos.png)

<div class="alert alert-success">

__CORRIGIDO__

<s>O nome da tabela é **Histórico de Recebimentos**</s>


![](static/layout-historico-recebimentos-corrigido.png)

</div>

Observações:

* Valores zero devem ser apresentados como "-";

<div class="alert alert-success">

__CORRIGIDO__

<s>Valores zero devem ser apresentados como "-"</s>

![](static/layout-valores-zerados-corrigido.png)

</div>

* A coluna mês/ano deve ser apresentada no formato mês(3 caracteres)/ano(4 caracteres). ___Exemplo:___ Set/2019;

<div class="alert alert-success">

__CORRIGIDO__

<s>O mês deve ser descritivo</s>

![](static/layout-mes-descritivo-corrigido.png)

**EXEMPLO**
![](static/historico-recebimentos.png)
</div>

* Os dados da coluna mês/ano devem ser exibidos de forma decrescente (mais recente para o mais antigo);

<div class="alert alert-success">

__CORRIGIDO__

***Foram testados apenas 3 meses***
--

<s>Ao utilizar a opção classificar  da coluna mês ano a funcionalidade não retorna a classificação correta - Como a descrição do mês encontra-se incorreta, não foi possível verificar esse item.</s>


<s>**No entanto ao classificar os dados deves obedecer a ordem decrescente**</s>

A ordem correta seria:

*  __<Fev/2020>; <Jan/2020>; <Dez/2019>__ : como padrão
     ou  
* __<Dez/2019>; <Jan/2020>; <Fev/2020>__ ao realizar a classificação.

![](static/layout-mes-descritivo-corrigido.png)

</div>

* Quando o número de linhas da tabela _[histórico recebimentos]_ for superior ao limite da página deve ser aplicada paginação conforme padrão das demais consultas;

<div class="alert alert-warning">

**OBS** Não é possível verificar essa funcionalidade (paginação) em homologação, pois a base de dados disponibilizada corresponde a apenas 3 meses. Dados serão verificados em produção.
--

</div>


* O cabeçalho da tabela histórico recebimentos deve ser congelado, ou seja, quando o usuário usar a barra de rolagem vertical o cabeçalho da tabela deve ficar sempre visível. ___Exemplo:___ [Cabeçalho fixo (_Fixed Header_)](https://uxdesign.cc/design-better-data-tables-4ecc99d23356#86cf);

<div class="alert alert-warning">

**OBS** Não é possível verificar essa funcionalidade (*Cabeçalho fixo (Fixed Header)* em homologação, pois a base de dados disponibilizada corresponde a apenas 3 meses. Dados serão verificados em produção.
--

</div>

__OBSERVAÇÃO:__ Essa funcionalidade não deve apresentar outra barra de rolagem dentro da tabela histórico recebimentos.
<div class="alert alert-warning">

**OBS**: Não é possível verificar essa funcionalidade (*não apresentar barra de rolagem*) em homologação, pois a base de dados disponibilizada corresponde a apenas 3 meses. Dados serão verificados em produção.
--

</div>

Exemplo: [stackoverflow](https://stackoverflow.com/questions/4709390/table-header-to-stay-fixed-at-the-top-when-user-scrolls-it-out-of-view-with-jque)

![](static/fixed-header.gif)

* A tabela _[histórico recebimentos]_ deve exibir a opção de classificar em todas as colunas conforme já ocorre nas demais consultas do Portal;

<div class="alert alert-success">

__CONFERE__

![](static/layout-filtro-historico-recebimento.png)

</div>

* Os dados apresentados na tabela _[histórico recebimentos]_ devem refletir o primeiro mês da série histórica disponível até o mês/ano selecionado no início da pesquisa.

<div class="alert alert-warning">

**OBS**: Não é possível verificar essa funcionalidade em homologação, pois a base de dados disponibilizada corresponde a apenas 3 meses. Dados serão verificados em produção.
--
</div>

    ___Exemplo:___ O servidor Luiz possui dados disponíveis de Mai/2015 a Out/2019. Caso o usuário selecione no filtro da _[barra de pesquisa]_ os dados de Out/2017, o Portal exibirá dos dados de Mai/2015 a Out/2017.

##### Glossário Interativo: TOOL TIP

O glossário interativo do histórico recebimentos deve apresentar os seguintes textos:

1. __Mês/ano:__ Mês e ano de referência da folha de pagamento. O pagamento ocorre conforme cronograma do Governo do Estado de Minas Gerais;

<div class="alert alert-success">

__CONFERE__

![](static/layout-tooltip-mes-ano.png)
</div>

1. __Básica:__ Composta pela soma das parcelas remuneratórias correspondentes ao cargo efetivo,  função gratificada ou cargo comissionado;

<div class="alert alert-success">

__CONFERE__

![](static/layout-tooltip-basica.png)
</div>

1. __Férias:__ Adicional pago ao servidor, por ocasião das férias regulamentares, correspondentes a 1/3 (um terço) da remuneração do período de férias;

<div class="alert alert-success">

__CONFERE__

![](static/layout-tooltip-ferias.png)
</div>

1. __Gratificação Natalina:__ Gratificação assegurada ao servidor civil ou militar a título de décimo terceiro salário;

<div class="alert alert-success">

__CONFERE__

![](static/layout-tooltip-gratificacao-natalina.png)
</div>

1. __Outros valores:__ Valores pagos em condições excepcionais e transitórias, tais como: Indenizações, Decisões Judiciais, Ajuda de Custo, Alimentação e outros valores de natureza eventual.

<div class="alert alert-success">

__CONFERE__

![](static/layout-tooltip-outros-valores.png)
</div>


1. __Total:__ Composta pela soma das parcelas remuneratórias correspondentes a remuneração básica e vantagens pecuniárias de caráter temporário ou permanente (gratificação natalina, férias e etc);

<div class="alert alert-success">

__CONFERE__

![](static/layout-tooltip-total.png)
</div>


1. __Descontos:__ Valor referentes aos descontos obrigatórios, incluído os descontos que excedam o limite constitucional da remuneração. Não estão incluídos os descontos de caráter pessoal, tais como consignados, previdência complementar e pensão alimentícia.

<div class="alert alert-success">

__CONFERE__

![](static/layout-tooltip-desconto.png)
</div>

1. __Remuneração líquida:__ Valor da remuneração do servidor após deduções realizadas no mês. O valor líquido apresentado pode ser superior ao efetivamente recebido, em face de não estarem inseridos os descontos de caráter pessoal.

<div class="alert alert-success">

__CONFERE__

![](static/layout-tooltip-remuneracao-liquida-historico.png)
</div>

1. __Jetons Empresas:__ É a remuneração percebida por servidores públicos estaduais em razão da participação como representantes do Estado em Conselhos de Administração e Fiscal ou órgãos equivalentes de empresas controladas direta ou indiretamente pelo Estado

<div class="alert alert-success">

__CONFERE__

![](static/layout-tooltip-jetons.png)
</div>

#### Formulário de detalhamento

A tabela histórico recebimentos deve permitir que o usuário clique no mês/ano para detalhar as informações referente aqueles mês. A informação mês/ano virá em vermelho como forma de destacar a possibilidade de clique.

<div class="alert alert-success">

__CONFERE__

![](static/layout-destaque-mes.png)
</div>

Quando o usuário clicar em um desses campos o Portal exibe outra janela detalhando os valores do mês selecionado. Deve ser possível a seleção de múltiplos meses sem perda de contexto.

___Exemplo:___ [Multi-Modal](https://uxdesign.cc/design-better-data-tables-4ecc99d23356#4a39)

![](static/multi-modal.gif)

<div class="alert alert-success">

__CONFERE__
![](static/layout-formulario-detalhamento.png)

  </div>

Ao clicar na coluna mês/ano, linha Out/2019 o portal exibirá o detalhamento do mês de outubro, com cabeçalho detalhando nome do servidor e mês da pesquisa: __OK__

![](static/formulario-detalhamento.png)

<div class="alert alert-success">

__CONFERE__

![](static/layout--formulario-detalhamento-jetons.png)

  </div>

<div class="alert alert-success">

__CORRIGIDO__

<s>A tabela histórico de remuneração não está exibindo os valores de jetons</s>


![](static/layout-historico-jetons-corrigido.png)
</div>

<div class="alert alert-success">

__CORRIGIDO__

<s>Os valores estão incorretos. Para o servidor em questão não existe valores na planilha "Jetons Administração Direta". Os valores são correspondentes a Jetons empresas apenas.</s>


![](static/layout-valores-errados-jetons-portal-corrigido.png)

![](static/layout-valores-errados-jetons-planilha.png)

</div>

<div class="alert alert-success">

__CORRIGIDO__

O campo **[Outros valores]** é composto pela soma dos campos (Prêmio de Produtividade + Férias Prêmio + Jetons Administração Direta + Demais Eventuais).


O campo **[Total]** é composto pela soma (básica + férias+ gratificação natalina + outros valores)

![](static/layout-erros-outros-valores-corrigido.png)


</div>

Algumas observações:

* O formulário de detalhamento deve apresentar a opção de fechar (x)

<div class="alert alert-success">

__CONFERE__
![](static/layout-opcao-fechar.png)
</div>

* O usuário pode mover o formulário de detalhamento para qualquer parte da tela

<div class="alert alert-success">

__CONFERE__
![](static/layout-mover-formulario.png)
</div>

* Valores zero devem ser apresentados como "-"

<div class="alert alert-success">

__CORRIGIDO__

<s>Corrigir valores zerados para "-"</s>

![](static/layout--formulario-detalhamento-valor-zerado-corrigido.png)
</div>

* A seção de detalhamento dos jetons empresas somente deve ocorrer para os casos em que os valores não forem zerados para o mês destacado. __Exemplo:__

![](static/formulario-detalhamento-jetons.png)

<div class="alert alert-success">

__CONFERE__

![](static/layout-valor-zerado-jetons.png)
</div>

<div class="alert alert-success">

__CORRIGIDO__

<s>Corrigir nome de Total Jetons Empresa para **Total Jetons Empresas**</s>

![](static/layout-altera-texto-empresa-corrigido.png)
</div>

<div class="alert alert-success">

__CORRIGIDO__

<s>Incluir o "R$" no local indicado</s>


![](static/layout--formulario-detalhamento-r$-corrigido.png)
</div>

Exportação de arquivos

Ao contrário da situação atual, a funcionalidade de impressão e exportação (CSV e PDF) deve existir tanto nas tabelas de navegação por filtros quanto nos formulários de detalhamento da situação funcional e histórico de recebimentos.

<div class="alert alert-success">

* Tabelas de Navegação - __CONFERE__

![](static/layout-exportacao-tabela-navegacao.png)

--
* **IMPRIMIR**- Tabelas de Navegação

![](static/layout-exportacao-tabela-navegacao-imprimir.png)

--
* **PDF** - Tabelas de Navegação

![](static/layout-exportacao-tabela-navegacao-pdf.png)

--
* **CSV** - Tabelas de Navegação

![](static/layout-exportacao-tabela-navegacao-csv.png)

</div>

Nas tabelas de navegação por filtros as regras de exportação/impressão devem seguir o padrão das demais consultas. A seguir são destacadas as particularidades das regras exportação/impressão para os formulários de detalhamento da situação funcional e histórico de recebimentos:

<div class="alert alert-success">

 __CONFERE__

![](static/layout-exportacao-detalhamento-remuneracao.png)

</div>

* A opção exportar dados deve gerar a planilha completa em forma de tabela com todos os dados das tabelas _[situação funcional]_ e _[histórico de recebimentos]_.

* Os dados de cada linha da planilha deve refletir a situação funcional e remuneração referente ao período (mês/ano).

___Exemplo 1___: A linha "Ago/2015" deve exibir a situação funcional e remuneração do servidor referente a agosto de 2015; A linha "Jan/2019" deve exibir a situação funcional e remuneração do servidor referente a janeiro/2019 e assim sucessivamente.

<div class="alert alert-success">

__CORRIGIDO__

<s>Não foi possível verificar esse erro, pois ao gerar o csv o Portal está apresentando apenas o mês vigente.</s>

<s>=> A funcionalidade destacada no exemplo acima (Exemplo 1) não está funcionando.</s>


**Exemplo**: A Joana Darc Aparecida de Faria Lopes em dez/2019 estava lotada na "SUPERINTENDENCIA CENTRAL DE ANALISE E"  e em fev/2020 estava lotada em "DIRETORIA CENTRAL DE FISCALIZACAO DE" ao gerar o csv o Portal retorna os mesmos dados para todos os períodos. Esse fato também ocorre para os outros campos, como por exemplo cargo em comissão.


* **Dezembro/2019**
![](static/layout-exportacao-detalhamento-remuneracao-csv1.png)

--
* **Fevereiro/2020**
![](static/layout-exportacao-detalhamento-remuneracao-csv2.png)

* **CSV gerado** - CSV gerado no dia 16/07/2020

![](static/layout-exportacao-detalhamento-remuneracao-csv3-corrigido.png)

</div>

<div class="alert alert-success">

__CORRIGIDO__

<s>Ao solicitar a extração em csv é gerado as informações de apenas um cargo.</s>

![](static/layout-zulma-goncalves-detalhamento-fev-csv-corrigido.png)

![](static/layout-zulma-goncalves-detalhamento-linha2.png)
</div>

<div class="alert alert-warning">

**Observações Luiz:**

***O servidor ACI ALVES DOS SANTOS possui dois cargos com cargas horárias distintas, sendo assim o processo de carga permite distinguir os cargos e exibir o histórico para cada cargo, de forma correta. Ou seja, os dados apresentados estão corretos.
Em alguns casos, quando o servidor possui alterações na carga horária entre meses ou cargas horários idênticas são os momentos em que os valores no histórico de recebimentos poderá exibir valores de diferentes caros que o servidor possui.***
***No caso da servidora ZULMA GONCALVES DE AGUIAR, ela possui a mesma carga horária, sendo assim, as informações são apresentadas de forma idêntica em ambos os cargos.
Esse é um dos problemas de não haver o número de admissão, como deveria ser no projeto original.***


O servidor ACI ALVES DOS SANTOS apresenta 02 cargos, no entanto apenas 01 está sendo exibido na tabela histórico de recebimentos.

[link porta- ACI ALVES DOS SANTOS](http://homologa3.prodemge.gov.br/age7/estado-pessoal/remuneracao-dos-servidores/remuneracao-filtros/202002/ACI%20ALVES%20DOS%20SANTOS/0/0/0/0/0/0/9/0/0/0)

![](static/layout-exportacao-aci-alves1.png)
--
![](static/layout-exportacao-aci-alves2.png)

Exemplo: A servidora ZULMA GONCALVES DE AGUIAR também apresenta 02 cargos e no entanto a informação dela é exibida na tabela.

[Link Portal - ZULMA](http://homologa3.prodemge.gov.br/age7/estado-pessoal/remuneracao-dos-servidores/remuneracao-filtros/202002/ZULMA%20GONCALVES%20DE%20AGUIAR/0/0/0/0/0/0/9/0/0/0)

</div>

<div class="alert alert-success">

__CONFERE__

* **IMPRIMIR**

![](static/layout-exportacao-detalhamento-remuneracao-imprimir.png)

--

* **PDF**

![](static/layout-exportacao-detalhamento-remuneracao-pdf.png)

</div>


* O leiaute da planilha exportada deve seguir o formato da planilha de remuneração disponibilizada pela CGE com inserção de uma coluna `mes` no formato `YYYY-MM-01`. Vide [arquivo exemplo](static/csv-usuario.csv). __OK__

<div class="alert alert-success">

__CORRIGIDO__

<s>A ordem da planilha a partir das empresa ainda encontra-se incorreto. A nome EMPI é a última coluna</s>

A ordem e o layout da planilha extraída em csv do Portal não está conforme o solicitado pela CGE.


![](static/layout-csv-historico-remuneracao-empresa-empi-corrigido.png)

![](static/espec-arquivo-csv.png)

</div>

* Os valores zero devem ser exportados como valores numéricos `0`

<div class="alert alert-success">

__CORRIGIDO__

<s>Os valores não estão no formato solicitado</s>

![](static/layout-valores-planilha-incorretos.png)

</div>
