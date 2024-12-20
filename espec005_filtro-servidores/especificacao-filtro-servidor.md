---
contrato_manutencao: nº 15210010062019 (INF. 3951)
proposta_comercial: nº nº 626584/19
pull_request: '[espec005](https://github.com/transparencia-mg/especificacoes-portal-transparencia/pull/7)'
titulo: Especificação filtro servidor
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da demanda
<a href="#top">(inicio)</a>

Essa demanda visa criar o filtro ___Situação___ na página inicial da consulta de [Remuneração de Servidores](http://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores) para a possibilitar a consulta de servidores ativos, inativos, pensionistas entre outros.

# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

A Diretoria Central de Transparência Ativa (DTA) recebe de forma recorrente questionamentos sobre o local de divulgação, no Portal da Transparência, de servidores inativos. Atualmente essa informação não é divulgada, mas existe previsão de divulgação ainda em 2020. 

Cabe ressaltar que o [Acórdão TCU 2154-2019 Plenário](https://pesquisa.apps.tcu.gov.br/#/redireciona/acordao-completo/%22ACORDAO-COMPLETO-2320372%22) afastou quaisquer eventuais dúvidas sobre a legalidade de divulgação dessas informações, 

Essa demanda vai possibilitar uma melhor navegação e busca quando estiverem sendo divulgados no Portal servidores ativos, inativos, pensionistas entre outros.

# Especificação

Na barra de pesquisa deve ser incluída um novo filtro em um campo específico que permita pesquisa pesquisas a partir dos valores da variável `Descrição Situação do Servidor`/`descsitser`. A barra de pesquisa deverá apresentar a seguinte estrutura:

![](static/barra_pesquisa.png)


## Observações

* Caso o cidadão não escolha nenhum tipo de filtro no campo ___Situação___ o Portal deverá exibir o resultado considerando todos os tipos de vínculos existentes.

* O portal deve exibir todos os tipos de situação funcional do servidor que estiverem na planilha de remuneração.
