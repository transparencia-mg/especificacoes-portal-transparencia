# Especificação de dados

Os dados dessa consulta serão extraídos dos Universos BO SIAFI, BO SIAD - Módulo Compras e SIGCON Saída:

- Armazém BO / ~tmp /novas Especificações / nova-espec-despesa

## Campos PDT x Campo Armazém BO

A consulta será anual, ou seja, o usuário irá visualizar a execução da Dívida Pública conforme o período selecionado.


| Armazém BO- SIAFI |Dimensão SIAFI| Filtro |
|----|----------|------------|
| Ano de exercício<br> |Período Contábil| Usar o período desejado |  



|Campo PDT| Campo Armazém BO |Dimensão Armazém | Observação
|---------|------------------|------|---|
|Ano |Ano de exercício| SIAFI -Período Contábil| Pesquisa básica
|Ano de exercício |Ano de exercício| SIAFI -Período Contábil| Formulário de detalhamento|
|Ação| Projeto Atividade - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa
|Código Elemento de Despesa| Elemento de Despesa - Código |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada|
|Código Item de Despesa| item de Despesa - Código |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada|
|Código Órgão| Unidade Orçamentária - Código  |SIAFI - Unidade Orçamentária|
|CPF/CNPJ| CNPJ_CPF credor numérico| SIAFI- Execução Orçamentária da Despesa >> Despesa Realizada >> Credor - Despesa
|Código da Função| Função - Código |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa|
|Código Subfunção| Subfunção - Código |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa |
|Código Programa| Programa - Código |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa |
|Código Ação| Projeto Atividade - Código |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa |
|Código Categoria Econômica| Categoria Econômica Despesa - Código| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada
|Código Grupo de Despesa| Grupo de Despesa - Código| SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada
|Código Identificador de Procedência e uso| Procedência - Código| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
|Código Modalidade de Aplicação| Modalidade de Aplicação - Código| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
|Código Fonte de Recurso| Fonte de Recurso - Código |Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
|Código Fonte de Recurso - Portaria STN nº710|Fonte_STN_COD| Matriz de Correspondência - Portal de Dados Abertos
|Categoria Econômica| Categoria Econômica Despesa -Descrição| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada
|Data de registro do empenho| Data Registro Doc Empenho| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Dados do Empenho - Despesa
|Elemento de despesa| Elemento de Despesa - Descrição  |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada|
|Empenho| Número Empenho |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Dados do Empenho - Despesa|
|Favorecido| Razão Social Credor  |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Credor - Despesa|
|Função| Função - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
|Fonte de Recurso| Fonte de Recurso - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
|Fonte de Recurso - Portaria STN nº 710| Descrição| Matriz de Correspondência (fonte_stn)- Portal de Dados Abertos
|Grupo de Despesa| Grupo de Despesa - Descrição| SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada
|Item de despesa| Item de Despesa - Descrição  |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada|
|Identificador de Procedência e uso| Procedência - Descrição| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
|Modalidade de Aplicação| Modalidade de Aplicação - Descrição| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
|Órgão| Unidade Orçamentária - Nome  |SIAFI - Unidade Orçamentária|
|Programa |Programa - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa
|Subfunção |Subfunção - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa
|Unidade Executora| Unidade Executora - nome | SIAFI - Unidade Executora
|Tipo de Empenho |Tipo Empenho  - Descrição| SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Dados do Empenho - Despesa
|Valor inicial da despesa empenhada| valor inicial Empenho| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada| Apenas no formulário de detalhamento
|Valor Atual do Empenho| Valor Despesa Empenhada| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada |Apenas no formulário de detalhamento
| Valor Empenhado | Valor Despesa Empenhada  |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada  |
| Valor Liquidado | Valor Despesa Liquidada  |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada  |
| Valor Pago | Valor Pago Financeiro  |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada |
| Valor Pago em Restos a Pagar | Valor Pago processado + Valor pago não processado  |SIAFI - Execução de Restos a pagar >> Restos a pagar |Essa coluna é representada pela soma das  Valor Pago processado + Valor pago não processado


Parei na Descrição do empenho


















* O usuário poderá clicar no número do empenho para exibir o formulário de detalhamento relacionado ao empenho.
* Exceção: Quando o usuário utilizar o filtro ***"Número da Ordem de Pagamento"*** na barra de filtro vertical as colunas abaixo deverão ser exibidas em formato desabilitado, sem a exibição de dados: Valor empenhado e Valor liquidado.
* Caso o filtro "Número da Ordem de Pagamento seja retirado da barra de filtros aplicados a formatação e exibição dos valores dessas colunas seguirá o padrão.










