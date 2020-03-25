---
contrato_manutencao: nº 15210010062019 (INF. 3951)
proposta_comercial: nº 626584/19
Disponível na URL: http://homologa3.prodemge.gov.br/age7/despesa-estado/restos-a-pagar
titulo: Homologa layout adiciona modos consulta restos a pagar
output:
  html_document:
    theme: united
    toc: yes
---

# Homologação do Layout

[LINK HTML](http://htmlpreview.github.io/?https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/master/espec003_consulta-restos-a-pagar/inclusao-novos-filtros-consulta-restos-a-pagar-homologa-layout.html)
<div class="alert alert-warning">

___Todas as divergências apontadas pela CGE na homologação do dia 05/02/2020 foram corrigidas pela PRODEMGE___  

  </div>

## Página Inicial e Navegação por nível

Para contemplar a inclusão dos modos de pesquisa adicionais a barra de pesquisa da página inicial deve ser:

<div class="alert alert-success">

__Tipos de Consultas OK__

![](static/layout-barra-pagina-inicial.png)
  </div>

<div class="alert alert-success">

__1__. Ao selecionar o tipo de consulta [ÓRGÃO] o campo a ser exibido deve ser [FILTRO], conforme padrão já utilizado nas demais consultas

![](static/layout-barra-navegacao-corrigido.png)

----

__2.__ Falta no ano no título do gráfico de pizza

![](static/layout-nome-grafico-pizza-corrigido.png)
</div>

Após uma pesquisa bem sucedida utilizando o filtro favorecido por nome ou CPF/CNPJ devem ser apresentados um gráfico _treemap_ e uma tabela, __ambos navegáveis__, por meio de duplo clique. O primeiro nível de navegação após a realização de uma busca utilizando o filtro favorecido é

<div class="alert alert-success">

![](static/1-nivel-favorecido.png)

---
__Dados da tabela 1º nível OK__
![](static/layout-tabela-1-nivel.png)
</div>

A ordem de navegação para os demais níveis e os campos descritivos que compõe o _treemap_ e a tabela são:

* 1º nível: | [Favorecido](#)      | CPF/CNPJ |
* 2º nível: | Categoria Econômica	| Grupo de Despesa | [Elemento de Despesa](#) |
* 3º nível: | Fonte de Recursos	  | Modalidade de Aplicação	| [Item de Despesa](#) |
* 4º nível: | Código              | [Órgão](#)	|
* 5º nível: | Data                | [Número do Empenho](#)	|

<div class="alert alert-success">

__Dados OK__

![](static/layout-tabela-2-nivel.png)
![](static/layout-tabela-3-nivel.png)
![](static/layout-tabela-4-nivel.png)
![](static/layout-tabela-5-nivel.png)

Somente os campos marcados como _hyperlink_ permitem a navegação nas tabelas. Nas tabelas do 1º ao 5º nível os seguinte campos numéricos devem ser apresentados:

* Valor Inscrito Processado,
* Valor Inscrito não Processado,
* Valor Pago no Ano,
* Valor a pagar
---
__O campo filtrar permiti pesquisar qualquer dado da tabela - OK__

 ![](static/layout-campo-filtrar.png)

</div>

<div class="alert alert-success">

O 5º nível do número do documento não possui gráfico _treemap_
http://homologa3.prodemge.gov.br/age7/despesa-estado/restos-a-pagar/restospagar-favorecidos/2020/2811340/autentica/0/3/566/25/51/3106/154/560/9804

 ![](static/layout-gráfico-5-nivel-corrigido.png)

 ---
 Os dados abaixo da tabela não estão sendo carregados

![](static/layout-rodapel-corrigido.png)
</div>

<div class="alert alert-success">

Ao clicar no campo _[Número do empenho]_ no 5º nível, o Portal exibirá o [formulário de detalhamento](http://www.transparencia.mg.gov.br/despesa-estado/restos-a-pagar/restospagar-orgaos/2019/3887/477/42/20/2768/130/58/5839139), já utilizado na consulta por órgão:

__Formulário de detalhamento RP OK__

![](static/layout-formulario-detalhamento.png)
  </div>

  <div class="alert alert-success">

Ao selecionar um favorecido pelo número do CPF/CNPJ o Portal exibe o favorecido corretamente, no entanto ao tentar avançar para o próximo nível o usuário é direcionado a página inicial. __CORRIGIDO__
http://homologa3.prodemge.gov.br/age7/despesa-estado/restos-a-pagar/restospagar-favorecidos/2020/0/0/27520617000194/4

  </div>



### Observações

<div class="alert alert-success">

* O gráfico _treemap_ deve utilizar a métrica "Valor Pago no Ano" em todos os níveis; __CONFERE__
![](static/layout-valor-grafico-treemap.png)
---
* O título do gráfico _treemap_ em cada nível deve ser o valor da classificação orçamentária selecionada no nível anterior; __CONFERE__
  </div>

  <div class="alert alert-success">

* O campo _[Data]_ exibido no 5º nível deve fazer referência a data de registro inicial do empenho.

O Portal está apresentando a data de registro em restos a pagar e não a data inicial do documento de empenho __CORRIGIDO__

![](static/layout-data-corrigido.png)

  </div>


* O filtro favorecido por nome deve ter a opção de autocomplete a partir de 3 letras. A menos que seja tecnicamente inviável os resultados devem ser retornados sem a necessidade do usuário clicar no ícone pesquisar;

<div class="alert alert-info">

__Observação enviada pelo Luiz (PRODEMGE)__: A funcionalidade de autocomplete não foi atendida, para evitar possíveis problemas de desempenho;
  </div>

<div class="alert alert-success">

* O filtro favorecido por nome deve permitir que o cidadão digite no mínimo 3 letras consecutivas de qualquer parte do nome do favorecido e o portal retornará todos os itens que encaixem na pesquisa; __CONFERE__
  </div>


* O preenchimento obrigatório dos filtros favorecido por nome e por CPF/CNPJ somente deve ser necessário em caso de inviabilidade técnica ou prejuízo de desempenho para o Portal.

<div class="alert alert-info">

__Observação enviada pelo Luiz (PRODEMGE)__ A obrigatoriedade de preenchimento do campo persiste, para evitar possíveis problemas de desempenho;
  </div>

<div class="alert alert-success">

* O filtro favorecido por CPF/CNPJ deve realizar a busca com CPFs/CNPJs formatados ou númericos.

A pesquisa por CNPJ/CPF quando utilizado o número formatado não retorna nenhum dado __CORRIGIDO__

CNPJ pesquisado: 04.602.789/0001-01  - DATEN TECNOLOGIA LTDA
![](static/layout-busca-cnpj-corrigido.png)

---

* No filtro o campo órgão deve permitir buscas por sigla sem que essa informação seja exibida.

Luiz, conforme sugerido por você a CGE aprova a inclusão da sigla logo após o nome do órgão na caixa de pesquisa. Porém, favor colocar a sigla em caixa alta __IMPLEMENTADO__

![](static/layout-sigla-orgao.png)

</div>

* Os filtros dos três modos de pesquisa devem possuir funcionalidade de seleção múltipla como na pesquisa avançada.

<div class="alert alert-info">

__Observação enviada pelo Luiz (PRODEMGE)__:	A seleção múltipla nos filtros não foi atendida. Aplicar este recurso somente nas consultas de Despesa e Restos a Pagar irá sair do padrão do site, causa uma possível redução do uso da Pesquisa Avançada, além de possíveis problemas no layout e desempenho;
 </div>

## Pesquisa Avançada
<a href="#top">(inicio)</a>

A consulta avançada terá 12 campos de filtro e parâmetro de ano:

1.  Órgão
2.  Função
3.  Subfunção
4.  Programas
5.  Ação
6.  Categoria Econômica
7.  Grupo de Despesa
8.  Modalidade de Aplicação
9.  Elemento de despesa
10.  Item de Despesa
11.  Fonte de Recursos
12.  Identificador de Procedência e Uso (IPU)

O usuário poderá escolher em exibir ou não a lista dos favorecidos. Como padrão o portal não exibirá os favorecidos.

Favorecidos

 <input type="checkbox" disabled=""> Exibir favorecidos
 <input type="checkbox" disabled="" checked=""> Não exibir Favorecidos

 <div class="alert alert-success">

__CONFERE__

![](static/layout-tabela-pesquisa-avancada.png)
![](static/layout-tabela-pesquisa-avancada2.png)

   </div>

### Observações

<div class="alert alert-success">
* O campo órgão da pesquisa avançada deve permitir buscas por sigla sem que essa informação seja exibida.

Se possível aplicar a mesma regra. O campo busca pode exibir o nome e sigla (nessa ordem) sem exibir na tabela. __IMPLEMENTADO__

![](static/layout-sigla-orgao-pesquisa-avancada.png)


 </div>

 <div class="alert alert-success">
*  A Pesquisa Avançada deve possuir um botão de marcar/desmarcar todas as colunas conforme demanda [especificação checkboxes](https://github.com/transparencia-mg/especificacoes-portal-transparencia/tree/feat/especificacao_checkboxes/espec010_checkboxes).

__Funcionalidade está OK na consulta de restos a pagar, as demais serão verificadas depois__

---

*   O autocomplete da pesquisa avançada deve possuir código e descrição das classificações orçamentárias ([eg. consulta proposta orçamentária](http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/proposta-orcamentaria/proposta-pesquisa-avancada));

![](static/layout-pesquisa-avancada-codigo.png)

---

* A exibição de código e descrição deve ser diferente em cada seção da pesquisa  avançada:
  * Campos dos filtros: exibir  código e descrição no mesmo campo ([eg. consulta proposta orçamentária](http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/proposta-orcamentaria/proposta-pesquisa-avancada)); __CONFERE__

  * Tabela de resultado: exibir apenas descrição; __CONFERE__
  * Opções imprimir e PDF: exibir apenas descrição; e __CONFERE__
![](static/layout-imprimir-pdf.png)
![](static/layout-imprimir.png)

  * Opção exportar CSV.: exibir código e descrição em campos distintos. __CONFERE__
![](static/layout-imprimir-csv.png)

 ---

*   Ao exibir o favorecido o Portal deverá retornar o nome e CNPJ/CPF do favorecido, conforme já ocorre na [Consulta de despesa](http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-resultado-pesquisa-avancada/2019/01-01-2019/31-12-2019/3853/0/3684/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/1/0).

![](static/layout-pesquisa-avancada-favorecido.png)

---

*   O Portal dever ter a funcionalidade de autocompletar (desde a primeira letra), desconsiderando acentuação, letras maiúsculas/minúsculas e palavras intermediárias (ex.: Ao digitar "gestao pública", um dos resultados será "Gestão da Administração Pública"). __CONFERE__


*   O cidadão poderá informar mais de um valor para cada filtro. Ao informar um valor de filtro, listar todas as opções. Se o cidadão não informar um valor para cada filtro, o Portal considerará todos os valores possíveis para cada filtro não informado. __CONFERE__

*   O cidadão poderá escolher os campos que ele quer que apareça no resultado (seguir modelo das demais consultas). __CONFERE__

*   O cidadão deverá escolher o ano da pesquisa. __CONFERE__

*   Ao exibir o resultado na tabela a consulta deverá retornar as colunas valor inscrito processado, valor inscrito não processado, valor pago no ano e valor a pagar. __CONFERE__

</div>
