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
| Ano |Ano de exercício| SIAFI - Período Contábil| Pesquisa básica
| Ano de exercício |Ano de exercício| SIAFI - Período Contábil| Formulário de detalhamento|
| Ação| Projeto Atividade - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa
| Categoria Econômica| Categoria Econômica Despesa -Descrição| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada
| Código Categoria Econômica| Categoria Econômica Despesa - Código| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada
| Elemento de despesa| Elemento de Despesa - Descrição  |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada|
| Código Elemento de Despesa| Elemento de Despesa - Código |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada|
| Função| Função - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
| Código da Função| Função - Código |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa|
| Fonte de Recurso| Fonte de Recurso - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
| Código Fonte de Recurso| Fonte de Recurso - Código |Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
| Fonte de Recurso - Portaria STN nº 710| Descrição| Matriz de Correspondência (fonte_stn)- Portal de Dados Abertos
| Código Fonte de Recurso - Portaria STN nº710|Fonte_STN_COD| Matriz de Correspondência - Portal de Dados Abertos
| Grupo de Despesa| Grupo de Despesa - Descrição| SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada
| Código Grupo de Despesa| Grupo de Despesa - Código| SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada
| Item de despesa| Item de Despesa - Descrição  |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada|
| Código Item de Despesa| item de Despesa - Código |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada|
| Identificador de Procedência e uso| Procedência - Descrição| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
| Código Identificador de Procedência e uso| Procedência - Código| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
| Modalidade de Aplicação| Modalidade de Aplicação - Descrição| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
| Código Modalidade de Aplicação| Modalidade de Aplicação - Código| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
| Órgão| Unidade Orçamentária - Nome  |SIAFI - Unidade Orçamentária|
| Código Órgão| Unidade Orçamentária - Código  |SIAFI - Unidade Orçamentária|
| Programa |Programa - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa
| Código Programa| Programa - Código |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa |
| Subfunção |Subfunção - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa
| Código Subfunção| Subfunção - Código |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa |
| Unidade Executora| Unidade Executora - nome | SIAFI - Unidade Executora
| Código Unidade Executora| Unidade Executora - Código | SIAFI - Unidade Executora
| Empenho| Número Empenho |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Dados do Empenho - Despesa|
| Favorecido| Razão Social Credor  |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Credor - Despesa| Código e descrição no mesmo campo
| CPF/CNPJ| CNPJ_CPF credor numérico| SIAFI- Execução Orçamentária da Despesa >> Despesa Realizada >> Credor - Despesa Código e descrição no mesmo campo
| Data de registro do empenho| Data Registro Doc Empenho| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Dados do Empenho - Despesa
| Tipo de Empenho |Tipo Empenho  - Descrição| SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Dados do Empenho - Despesa
| Valor inicial da despesa empenhada| Valor Inicial Empenho| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada| Apenas no formulário de detalhamento
| Valor Atual do Empenho| Valor Despesa Empenhada| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada |Apenas no formulário de detalhamento
| Valor Empenhado | Valor Despesa Empenhada  |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada  |
| Valor Liquidado | Valor Despesa Liquidada  |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada  |
| Valor Pago | Valor Pago Financeiro  |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada |
| Valor Pago em Restos a Pagar | Valor Pago processado + Valor pago não processado  |SIAFI - Execução de Restos a pagar >> Restos a pagar |Essa coluna é representada pela soma das  Valor Pago processado + Valor pago não processado
|Descrição Histórico do Empenho|||Essa informação é retirada de uma planilha separada da SEF. Os dados já são exibidos no Portal.
|Data de Registro do Esforço | Data Reforço/Anulação |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Dados do reforço / Anulação - Despesa |
| Nº do Documento do Esforço| Campo SIAFI não disponível para visualização da DTA. Trazer o campo já utilizado no formulário de detalhamento da despesa. | |Essa informação já é exibida no Portal.
| Valor do Esforço| Valor Reforço Empenho |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada |
|Data de Registro da Anulação |Data Reforço/Anulação | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Dados do reforço / Anulação - Despesa|
| Nº do Documento de Anulação |Campo SIAFI não disponível para visualização da DTA. Trazer o campo já utilizado no formulário de detalhamento da despesa. | |Essa informação já é exibida no Portal.
| Valor Anulado| Valor Anulação Empenho | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada|
|Data de Registro em RP | Data de Registro Doc Empenho |SIAFI - Execução de Restos a pagar >> Restos a pagar >> Dados do Empenho - Restos a Pagar| Data de registro que o empenho foi inscrito em Restos a Pagar
| Tipo de Inscrição | Campo SIAFI não disponível para visualização da DTA. Trazer o campo já utilizado no formulário de detalhamento da consulta de Restos a pagar | |
| Valor Inscrito em RP| **SOMA** do Valor Inscrito Processado - Valor Cancelado Processado ou Valor Restabelecido Processado **OU** soma do Valor Inscrito Não Processado - Valor Cancelado Não Processado + Valor Restabelecido Não Processado |SIAFI - Execução de Restos a Pagar > Restos a Pagar |Cada linha deverá apresentar o valor corresponde ao tipo de inscrição em restos a pagar.
|Data de Registro da liquidação| Data Registro Doc Liquidação |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada >> Dados da Liquidação - Despesa |
| Nº do Documento da liquidação |Campo SIAFI não disponível para visualização da DTA. Trazer o campo já utilizado no formulário de detalhamento da liquidação.  | |
| Valor Liquidado| Valor Despesa Liquidada | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada|
|Data de Registro da Liquidação em RP | Data Registro Doc Liquidação | SIAFI - Execução de Restos a Pagar > Restos a Pagar > Dados da Liquidação - Restos a Pagar |
| Nº do Documento da Liquidação em RP |Campo SIAFI não disponível para visualização da DTA. Trazer o campo já utilizado no formulário de detalhamento da liquidação.  | |
| Valor Liquidado RP | Valor Despesa Liquidada |SIAFI - Execução de Restos a Pagar > Restos a Pagar| Valor liquidado do restos a pagar não processado
|Data de Registro do Pagamento | Data de Registro |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Dados da Ordem de Pagamento - Despesa |
| Nº do Documento de Pagamento | Número Docto Pagamento | |
|  Situação da Ordem de Pagamento| Situação Ordem de Pagamento - Descrição |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Dados da Ordem de Pagamento - Despesa |
|Valor Pago| Valor Pago Financeiro |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada|
|Data de Registro do Pagamento em RP| Data Registro | SIAFI - Execução de Restos a Pagar > Restos a Pagar > Dados da Ordem de Pagamento - Restos a Pagar|Data de registro que o restos a pagar foi pago.
| Nº do Documento de pagamento em RP |Número Ordem de Pagamento  |SIAFI - Execução de Restos a Pagar > Restos a Pagar > Dados da Ordem de Pagamento - Restos a Pagar |
| Situação da Ordem de Pagamento em RP| Situação Ordem de Pagamento - Descrição |SIAFI - Execução de Restos a Pagar > Restos a Pagar > Dados da Ordem de Pagamento - Restos a Pagar|
| Valor Pago em RP|Valor Pago processado + Valor pago não processado  |SIAFI - Execução de Restos a pagar >> Restos a pagar |
|Número do Processo de Compra|Número do Processo de Compra|SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Campo utilizado para cruzamento das informações empenho vs processo de compra. Ao identificar qual processo de compra está vinculado ao empenho os demais dados referente ao processo serão extraídos do Armazém SIADI - Portal de Compras - Módulo Compras
|Data de Cadastramento do Processo |Data criação do Processo |Armazém SIADI - Portal de Compras - Módulo Compras > Data criação do Processo|
|Procedimento de Contratação| Procedimento de Contratação - Detalhamento 1| Armazém SIADI - Portal de Compras - Módulo Compras > Procedimento de Contratação|
|Situação do Processo| Situação Processo| Armazém SIADI - Portal de Compras - Módulo Compras|
|Objeto do Processo| Objeto Processo| Armazém SIADI - Portal de Compras - Módulo Compras|
|Número do Contrato |Número Contrato| Armazém SIADI - Portal de Compras - Módulo Compras > Contrato|
|Data de Publicação do Contrato |Data Publicação Contrato |Armazém SIADI - Portal de Compras - Módulo Compras > Data Publicação Contrato|
|Situação do Contrato| Situação Contrato |Armazém SIADI - Portal de Compras - Módulo Compras > Contrato|
|Vigência Atualizada| Data Término Vigência Contrato| Armazém SIADI - Portal de Compras - Módulo Compras > Data Atualizada Término Vigência Contrato|
|Objeto do Contrato| Objeto Contrato |Armazém SIADI - Portal de Compras - Módulo Compras > Contrato|
|Número do Convênio/ Parceria SIAFI| Contrato Convênio Saída|SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Dados do Empenho - Despesa| Ao identificar que existe 'Contrato Convênio Saída' relacionado a um empenho deve-se realizar o cruzamento com a base de dados do Pdt consulta Convênio de Saída / Parceria de recursos e caso a informação conste na base de dados essas serão replicadas nesse formulário. Exemplo: Código SIAFI (Contrato Convênio Entrada) 9288133 >> Empenho (Número do Empenho) 367/2021 >> Número do Convênio / Parceria SIAFI (Contrato Convênio Saída) 9318584
|Data de publicação|Data Publicação| PdT - Consulta Convênios / Parceria de Saída de Recursos|
|Situação do Convênio / Parceria| Situação do Convênio / Parceria|PdT - Consulta Convênios / Parceria de Saída de Recursos|
|Vigência Atualizada| Vigência atualizada| PdT - Consulta Convênios / Parceria de Saída de Recursos|
|Título do Convênio / Parceria| Título do Convênio / Parceria| PdT - Consulta Convênios / Parceria de Saída de Recursos|

|Campo PdT |Barra vertical| Campos Adicionar/remover colunas
|----|--|-----|
|Período<br> ***(Data)***|sim| ***NÃO*** |
|Período<br> ***(Apenas o ano)***|***NÃO***| sim |
|Unidade Executora|sim | sim||
Unidade de Programação de Gastos (UPG)|sim | sim||
|Função|sim | sim||
|Subfunção|sim | sim||
|Programa|sim | sim||
|Ação|sim | sim||
|Categoria Econômica da Despesa|sim | sim||
|Grupo de Despesa|sim | sim||
|Modalidade de Aplicação|sim | sim||
|Elemento de Despesa|sim | sim||
|Item de Despesa|sim | sim||
|Fonte de Recurso|sim | sim||
|Fonte de Recurso - Portaria STN nº 710|sim | sim||
|Indicador de Procedência e Uso (IPU)|sim | sim||
|Empenho|sim |sim|
|Número do Processo de Compra|sim | sim||
|Procedimento de Contratação|sim |sim|
|Objeto Processo|sim |sim|
|Número Contrato // Convênio/Parceria de recurso de saída|sim |sim|
|Objeto Contrato|sim |sim|
|Título do Convênio / Parceria|sim |sim|
|CNPJ/ CPF Favorecido<br>***Usar o atributo placeholder : Texto: 'apenas números'***|sim |sim|
|Favorecido<br>***Usar o atributo placeholder : Texto: 'informe pelo menos 3 caracteres'***|sim |sim|
|Número documento Pagamento|sim | sim||
|Data Registro do Empenho |***NÃO*** | sim|
|Data de Registro do Pagamento|***NÃO*** | sim||
|Tipo Empenho|***NÃO*** | sim||
|Situação Ordem de Pagamento| ***NÃO*** | sim||
|Data criação do Processo|***NÃO*** |sim|
|Situação Processo|***NÃO*** |sim|
|Data Publicação Contrato|***NÃO*** |sim|
|Data Vigência Atualizada do Contrato|***NÃO*** |sim|
|Data Publicação Convênio/ Parceria|***NÃO*** |sim|
|Situação do Convênio / Parceria|***NÃO*** |sim|
|Situação do Contrato|***NÃO*** |sim|
|Valor Empenhado|***NÃO***|sim|
|Valor Liquidado|***NÃO***|sim|
|Valor Pago|***NÃO***|sim|
|Valor Liquidado em RP |***NÃO***|sim|
|Valor Pago em Restos a Pagar|***NÃO***|sim|

#### Colunas padrões da tabela de resultado - Monte sua Pesquisa

***1º nível:***

- Detalhar
- Valor Empenhado
- valor Liquidado
- Valo Pago
- Valor Pago em restos a Pagar

A tabela de resultados do 1º nível terá como opção o botão *Detalhar* o qual direcionará o usuário para a lista de empenhos (2º nível) conforme os filtros selecionados e em seguida poderá ser direcionado para o formulário de detalhamento ao clicar em um dos empenhos da lista. Caso o usuário solicite a exibição da coluna empenho já no 1º nível e este for um valor único, o usuário será direcionado diretamente para o formulário de detalhamento relacionado ao empenho.

***2º nível:***

- Empenho
- Data de registro do empenho
- Unidade orçamentária
- Unidade Executora
- Favorecido
- CPF/CNPJ do Favorecido
- Valor Empenhado
- Valor Liquidado
- Valo Pago
- Valor Pago em restos a Pagar

O usuário poderá clicar no número do empenho para exibir o formulário de detalhamento relacionado ao empenho.

#### Campos *Exibir código/descrição*
Os campos referente aos códigos serão exibidos quando o usuário acionar o botão *Exibir código/descrição*  e na extração/download dos dados.

|Campo PdT (Códigos)
|- |
|Código Órgão|
|Código Unidade Executora|
|Código Unidade Programação de Gasto |
|Código Função|
|Código Subfunção
|Código Programa
|Código Ação|
|Código Categoria Econômica da Despesa
|Código Grupo de Despesa
|Código Modalidade de Aplicação
|Código Elemento de Despesa
|Código Item de Despesa
|Código Fonte de Recurso
|Fonte de Recurso - Portaria STN nº 710
|Código Indicador de Procedência e Uso (IPU)
