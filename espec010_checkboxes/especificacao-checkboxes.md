---
contrato_manutencao: nº 15210010062019 (INF. 3951)
proposta_comercial: nº 626584/19
pull_request: '[espec010](https://github.com/transparencia-mg/especificacoes-portal-transparencia/pull/10)'
titulo: Marcar e desmarcar todos os checkboxes nas pesquisas avançadas
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da demanda
<a href="#top">(inicio)</a>

Essa demanda visa incluir nas consultas que possuem pesquisas avançadas a opção de marcar e desmarcar as caixas de seleção ___checkboxes___, de forma que o usuário possa selecionar todas as opções da pesquisa avançada sem a necessidade de selecionar todas as opções exibir.

# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

Atualmente, a pesquisa avançada das consultas do Portal da Transparência possui a funcionalidade de exibir os itens da pesquisa. No entanto, para que o usuário possa visualizar os itens da pesquisa é necessário que ele selecione um a um os campos "_exibir_" que serão mostrados na consulta.

Para facilitar a navegação do usuário, sugere-se a inclusão do item “___Exibir Todos___” no início da consulta, possibilitando ao usuário selecionar com apenas um clique todos os itens da consulta.

# Especificação
<a href="#top">(inicio)</a>

__1. Consultas que sofrerão alterações__

A opção “___Exibir todos___” deverá ser incluída em todas as consultas que possuem “Pesquisa Avançada”:

- [Despesa](http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-pesquisa-avancada);
- Restos a Pagar (incluir essa funcionalidade na reformulação que será implementada) ;
- [Viagens](http://www.transparencia.mg.gov.br/estado-pessoal/viagens/estado_viagens-pesquisa-avancada);
- [Receita](http://www.transparencia.mg.gov.br/estado-receita/receita-pesquisa-avancada);
- [Proposta orçamentária](http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/proposta-orcamentaria/proposta-pesquisa-avancada);
- [Alteração orçamentária](http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/alteracao-orcamentaria/altorcam-pesquisa-avancada);
- [Obras orçadas](http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/obras-orcadas/obras-pesquisa-avancada);
- [Crédito orçamentário](http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/credito-orcamentario/credorcam-pesquisa-avancada);
- [Programação e Execução PPAG por Programa](http://www.transparencia.mg.gov.br/planejamento-e-resultados/planejamento-e-monitoramento/programacao-execucao-ppag-programa?task=estado_ppagprograma.consultaLivre);
- [Convênios/Parcerias de Saída de Recursos](http://www.transparencia.mg.gov.br/convenios/convenios-de-saida/convenios-pesquisa-avancada);
- [Convênios de Entrada de Recursos](http://www.transparencia.mg.gov.br/convenios/convenio-entrada/convenios-entrada-pesquisa-avancada);
- [Compras e Contratos](http://www.transparencia.mg.gov.br/compras-e-patrimonio/compras-e-contratos/comprasecontratos-pesquisa-avancada);
- [Gestão de Frota](http://www.transparencia.mg.gov.br/compras-e-patrimonio/gestao-de-frota/frota-pesquisa-avancada);
- [Patrimônio](http://www.transparencia.mg.gov.br/compras-e-patrimonio/patrimonio/patrimonio-pesquisa-avancada).


**2. Layout da inclusão da opção "*Exibir Todos/Não Exibir Todos*" nas pesquisas avançadas**

* Deverá ser incluído a caixa de seleção _"Exibir todos”_ e _"Não Exibir Todos"_ ;
* A caixa de seleção deverá ser localizada antes da seleção das opções da consulta avançada;

![](static/exibir_todos.jpg)


# Dúvidas
<a href="#top">(inicio)</a>

1.	Boa Prática
Muitos portais utilizam a opção na pesquisa de exibir todos ou selecionar todos, sem a necessidade de ficar marcando a caixa de seleção “Exibir”. Dessa forma a seleção só é alterada, caso o usuário tenha interesse em exibir apenas um item específico.

- Estados que utilizam a opção exibir todas:

[CEARÁ](https://cearatransparente.ce.gov.br/portal-da-transparencia/despesas/despesas-do-poder-executivo?locale=pt-BR&__=__)

![](static/ceara.jpg)

[Distrito Federal](http://www.transparencia.df.gov.br/#/despesas/credor)

![](static/distrito_federal.jpg)

2. Podemos deixar como padrão a opção "Exibir todos" sem ativado. Assim caso algum usu
