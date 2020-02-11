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

Cabe ressaltar que o[Acórdão TCU 2154-2019 Plenário](https://pesquisa.apps.tcu.gov.br/#/redireciona/acordao-completo/%22ACORDAO-COMPLETO-2320372%22) afastou quaisquer eventuais dúvidas sobre a legalidade de divulgação dessas informações, 

Essa demanda vai possibilitar uma melhor navegação e busca quando estiverem sendo divulgados no Portal servidores ativos, inativos, pensionistas entre outros.

Na opção de Consulta: deverá ser excluída a opção Cargo Comissionado, e substituída por:
- Comissionado com vínculo efetivo;
- Comissioando sem vínculo efetivo.

# Especificação

## Barra de pesquisa

Considerando a inclusão do campo ___Situação___ e as alterações propostas na especificação referente ao layout da remuneração, a barra de pesquisa deverá apresentar a seguinte estrutura:

* Ano: Todo o histórico anual da remuneração;

* Mês: Todos os meses do (Janeiro a Dezembro);
* ___Situação:___ Ativo, Inativo, Pensionista, Designado ao Serviço Ativo e outros (o Portal deve exibir todos os tipos de vínculo que estiverem na planilha de remuneração);
* ___Consulta___: Nome do servidor, Cargo efetivo, Comissionado com vínculo efetivo,Comissioando sem vínculo efetivo, órgão;
* Nome: manter as regras atuais
* Pesquisar;
* Download planilha completa;


![](static/barradepesquisa.jpg)


### Observações gerais

* Caso o cidadão não escolha nenhum tipo de filtro no campo ___Situação___ o Portal deverá exibir o resultado considerando todos os tipos de vínculos existentes.

* Nos filtro situação do servidor, órgão, cargo efetivo e cargo em comissão devem possuir funcionalidade de seleção múltipla como na pesquisa avançada da consulta de despesa.

* No filtro o campo órgão deve permitir buscas por sigla sem que essa informação seja exibida.

* O portal deve exibir todos os tipos de situação funcional do servidor que estiverem na planilha de remuneração.
