---
contrato_manutencao: Manutenção PDT - Contrato INF INF 4817
proposta_comercial:
mantis:
pull_request: '[]()'
titulo: Receita Acordo Judicial Vale
output:
  html_document:
    theme: united
    toc: yes
---

# Especificação - Dados da Consulta
<a href="#top">(inicio)</a>

Esse documento tem como base a alteração da consulta de receita do Acordo Judicial da Vale para atender uma demanda do Tribunal de Contas do Estado de Minas Gerais. A consulta deverá exibir a coluna de Rendimentos.

## Pesquisa Básica - Tipo de Consultas
<a href="#top">(inicio)</a>
______
### Por Receita
<a href="#top">(inicio)</a>

Os dados dessa consulta serão extraídos do Universo BO SIAFI.
- Armazém BO / Pastas públicas - SIAFI > SUPORTE- SIAFI > Consulta Vale Portal > Por Receita - rendimentos


#### Filtros da Consulta

Essa consulta será plurianual, ou seja, o usuário irá visualizar os valores arrecadados por ano.

| Armazém BO- SIAFI       | Filtro
|--------------------------|-----------------
|Fonte de Recurso| 95
Classificação Receita - Formatado (Universo **RECEITA ORÇAMENTÁRIA**| 2990.00.1.1.02.000<br>
Classificação Receita - Formatado (Universo **ARRECADAÇÃO**| 2990.00.1.1.02.000<br>
Portaria STN nº 710/2021| Portal Dados MG (https://dados.mg.gov.br/dataset/matriz-fonte-stn)<br>

#### Campos da Tabela - Universo Receita Orçamentária

#### Não haverá alteração nessa consulta, com as seguintes exceções:
- Inclusão de tooltip na coluna Código da Fonte de Recursos
- Alteração do campo Código da Classificação da Receita, para dados com campos formatados: Classificação Receita - Formatado

|Dados| Campo armazém BO- SIAFI     | Dimensão SIAFI| Campo PdT | Tooltip - PdT           | Exibição da Coluna
|-| -|---|---------------|------------|---|
|Receita| Ano de Exercício |SIAFI - Período Contábil|Ano de Exercício |Ano de exercício que ocorreu a arrecadação|*default*|
|Receita |Classificação Receita - Formatado |SIAFI - Execução Orçamentária da Receita > Receita Orçamentária > Classificação Receita Orçamentária a partir de 2018 > |Código da Classificação Receita|Classificação criada a fim de possibilitar a identificação detalhada dos recursos que ingressam nos cofres públicos. Os números representam, da esquerda para a direita: categoria econômica; origem da receita; espécie da receita; desdobramento 1 da receita, desdobramento 2 da receita, desdobramento 3 da receita, tipo da receita| *default*|
|Receita| Classificação Receita - Descrição |SIAFI - Execução Orçamentária da Receita > Receita Orçamentária > Classificação Receita Orçamentária a partir de 2018|Classificação Receita |Descrição da identificação detalhada dos recursos que ingressam nos cofres públicos |*default*|
|Receita| Fonte de Recurso - Código |SIAFI - Execução Orçamentária da Receita > Receita Orçamentária > Dados da Receita Orçamentária|Código da Fonte de Recurso|Indica o código da origem do dinheiro arrecadado. Combina a origem do dinheiro às despesas orçamentárias. Esta vinculação visa demonstrar o montante de dinheiro que já está comprometido com o atendimento de determinadas finalidades, e aquele que pode ser livremente alocado.|ao acionar o botão 'Exibir código e descrição'|
|Receita| Fonte de Recurso  |SIAFI - Execução Orçamentária da Receita > Receita Orçamentária > Dados da Receita Orçamentária| Fonte de Recurso |Indica a origem do dinheiro arrecadado. Combina a origem do dinheiro às despesas orçamentárias. Esta vinculação visa demonstrar o montante de dinheiro que já está comprometido com o atendimento de determinadas finalidades, e aquele que pode ser livremente alocado.|*default*|
|Receita| Valor Previsto Inicial |SIAFI - Execução Orçamentária da Receita > Receita Orçamentária | Valor Previsto Inicial| Valor estimado da arrecadação para o ano consultado, previsto na Lei Orçamentária Anual (LOA)|*default*|
|Receita|  Valor Previsto Atualizado|SIAFI - Execução Orçamentária da Receita > Receita Orçamentária |Valor Previsto Atualizado| Valor estimado inicial para arrecadação no ano consultado, previsto na Lei Orçamentária Anual, atualizado ao longo do ano.|*default*
|Receita| Valor Efetivado Ajustado |SIAFI - Execução Orçamentária da Receita > Receita Orçamentária |Valor Arrecadado| Valor financeiro que entrou nos cofres públicos no período consultado|*default*



#### Campos da Tabela - Portal Dados MG

#### Não haverá alteração nessa consulta, com as seguintes exceções:
- Inclusão de tooltip na coluna Código da Fonte de Recursos - Portaria STN nº 710/2021

|Dados| Campo armazém BO- SIAFI     | Dimensão SIAFI| Campo PdT | Tooltip - PdT           | Exibição da Coluna
|-| -|---|---------------|------------|---|
|Receita| Matriz de Correspondências - Receita |Portal Dados MG|Fonte de Recursos - Portaria STN nº 710/2021 - Código|Dados disponibilizados a partir de 2023. Indicam o código da fonte ou destinação de recursos utilizados pelos Estados, Distrito Federal e Municípios, conforme previsto na Portaria STN nº 710/2021|ao acionar o botão 'Exibir código e descrição'|
|Receita| Matriz de Correspondências - Receita |Portal Dados MG|Fonte de Recursos - Portaria STN nº 710/2021 -         |Dados disponibilizados a partir de 2023. Indicam a classificação das fontes ou destinações de recursos utilizados pelos Estados, Distrito Federal e Municípios, conforme previsto na Portaria STN nº 710/2021|*default*|


#### Campos da Tabela - Universo Arrecadação

#### Dados a serem incluídos. 
- Identificamos que o universo é Arrecadação, e temos dúvidas se será possível incluir esses campos na consulta.

|Dados| Campo armazém BO- SIAFI     | Dimensão SIAFI| Campo PdT | Tooltip - PdT           | Exibição da Coluna
|-| -|---|---------------|------------|---|
|Receita| Ano de Exercício |SIAFI - Período Contábil|Ano de Exercício |Ano de exercício que ocorreu a arrecadação|*default*|
|Receita |Classificação Receita - Formatado |SIAFI - Execução Orçamentária da Receita > Arrecadação > Classificação Receita Orçamentária a partir de 2018 > |Código da Classificação Receita|Classificação criada a fim de possibilitar a identificação detalhada dos recursos que ingressam nos cofres públicos. Os números representam, da esquerda para a direita: categoria econômica; origem da receita; espécie da receita; desdobramento 1 da receita, desdobramento 2 da receita, desdobramento 3 da receita, tipo da receita| *default*|
|Receita| Classificação Receita - Descrição |SIAFI - Execução Orçamentária da Receita > Arrecadação > Classificação Receita Orçamentária a partir de 2018|Classificação Receita |Descrição da identificação detalhada dos recursos que ingressam nos cofres públicos |*default*|
|Receita| Fonte de Recurso - Código |SIAFI - Execução Orçamentária da Receita > Arrecadação > Dados da Arrecadação|Código da Fonte de Recurso|Indica o código da origem do dinheiro arrecadado. Combina a origem do dinheiro às despesas orçamentárias. Esta vinculação visa demonstrar o montante de dinheiro que já está comprometido com o atendimento de determinadas finalidades, e aquele que pode ser livremente alocado.|ao acionar o botão 'Exibir código e descrição'|
|Receita| Fonte de Recurso  |SIAFI - Execução Orçamentária da Receita > Arrecadação > Dados da Arrecadação| Fonte de Recurso |Indica a origem do dinheiro arrecadado. Combina a origem do dinheiro às despesas orçamentárias. Esta vinculação visa demonstrar o montante de dinheiro que já está comprometido com o atendimento de determinadas finalidades, e aquele que pode ser livremente alocado.|*default*|
|Receita| Valor Arrecadado Líquido |SIAFI - Execução Orçamentária da Receita > Arrecadação |Rendimentos| Valor referente aos rendimentos dos recursos que entrarm nos cofres públicos no período consultado|*default*


![image](https://github.com/user-attachments/assets/f3ab0284-864f-4c1b-86b8-4f1ed7d95d19)

