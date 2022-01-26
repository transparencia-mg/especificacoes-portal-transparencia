---
contrato_manutencao: nº 15210010062019 (INF. 3951)
proposta_comercial:
mantis:
pull_request: '[]()'
titulo: Transparência dos recursos da Vale - Acordo Judicial 04/02/2021
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da demanda
<a href="#top">(inicio)</a>

Essa demanda visa a criação de uma seção para possibilitar o acompanhamento das ações desenvolvidas pelo Governo do Estado de Minas Gerais com recursos provenientes do acordo judicial firmado com a Vale. Considerando a relevância e os valores envolvidos no acordo, a seção será um instrumento de transparência e prestação de contas colocando em evidência a execução do acordo.

Juntamente com a criação da nova seção será implementado no Portal da Transparência (PDT) algumas necessidades dos usuários identificadas durante o projeto 'Experiência do Usuário no Portal da Transparência', realizado em abril de 2021, como por exemplo:

- Alteração do Formulário de Detalhamento;
- Pesquisa básica mais intuitiva e dinâmica;
- Inclusão de novas informações;
- Consolidação dos dados de Despesa e RP em uma única consulta.


# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

O Governo de Minas, o Ministério Público de Minas Gerais (MPMG), o Ministério Público Federal (MPF) e a Defensoria Pública de Minas Gerais (DPMG) assinaram um termo de Medidas de Reparação, no dia 4 de fevereiro de 2021, que garante que a empresa Vale seja imediatamente responsabilizada pelos danos causados às regiões atingidas e à sociedade mineira pelo rompimento da barragem Mina Córrego do Feijão, em Brumadinho, no ano de 2019.

O documento define “obrigações de fazer” e “obrigações de pagar” da Vale e prevê um total de recursos a serem aplicados em reparação socioambiental e socioeconômica de R$ 37.689.767.329,00 (trinta e sete bilhões, seiscentos e oitenta e nove milhões, setecentos e sessenta e sete mil, trezentos e vinte e nove reais). Destes, R$11.060.000.000,00 (onze bilhões e sessenta milhões) serão de gestão do Poder Executivo estadual para execução de projetos de mobilidade (anexo III), fortalecimento do serviço público (anexo IV), segurança hídrica (anexo II.3) e ressarcimento de despesas decorrentes da execução do referido Termo Judicial.

A [Lei nº 23.830/2021](https://www.almg.gov.br/consulte/legislacao/completa/completa.html?tipo=LEI&num=23830&comp=&ano=2021), publicada em 28/07/2021, autorizou abertura de crédito suplementar ao orçamento do Estado em função dos recursos previstos no Termo de Reparação que deverão ser alocados conforme consta no Acordo Judicial.


# Especificação - Dados da Consulta
<a href="#top">(inicio)</a>

Esse documento tem como base a criação de uma nova consulta para possibilitar o acompanhamento das ações desenvolvidas pelo governo do estado com recursos provenientes do acordo judicial firmado com a Vale .

## Pesquisa Básica - Tipo de Consultas
<a href="#top">(inicio)</a>

### Por Projeto
<a href="#top">(inicio)</a>

Os dados dessa consulta serão extraídos do Universo BO SIGCON- Entrada.
- Armazém BO / Pastas públicas - SIAFI > CGE_Portal da Transparência > Recursos Vale> Tela Projeto


**Filtros da Consulta:**

| Armazém BO- SIGCON ENTRADA       | Filtro
|--------------------------|-----------------
|Convênio Código | Usar os filtros que constam no amazém BO     

------
verificar se existe a possibilidade de ser criado novos Convênios, se sim teremos que ver como a DTA irá proceder quanto a esses filtros.
-------

**Campos da Tabela:**

| Armazém BO- SIGCON ENTRADA       | PdT | Tooltip - PdT           | Exibição da Coluna
|----------------------------------|-------------------------|--------------------|---|
| Convênio Número Sequencial SIAFI | Código SIAFI            | Código do Projeto no armazém SIAFI (Sistema Integrado de Administração Financeira de Minas Gerais ) |default
| Plano Trabalho Objeto            | Projeto                 | Descrição do Projeto conforme consta no Acordo de Reparação e de execução do Governo do Estado                 |default
| Unidade Orçamentária Código      | Código Órgão            |    Código da Unidade Orçamentária responsável pelo Projeto                | ao acionar o botão '*Exibir código e descrição*''
| Unidade Orçamentária Nome        | Órgão                   |    Descrição da Unidade Orçamentária responsável pelo Projeto                |default
| Valor Total Convênio             | Valor Total           |          Valor Total destinado ao projeto          |default

![](static/imagens/tabela-projeto.png)

**Comportamento da Consulta:**

- Ao clicar no campo 'Código SIAFI' o usuário será direcionado para o 2º nível da consulta por órgão, ou seja, a tabela de empenhos. A consulta deverá exibir todos dos empenhos relacionados ao Código SIAFI selecionado independentemente do ano de registro do empenho.


### Por Órgão
<a href="#top">(inicio)</a>

Os dados dessa consulta serão extraídos do Universo BO SIAFI
- Armazém BO / Pastas públicas - SIAFI > CGE_Portal da Transparência > Recursos Vale> > TELA ÓRGÃO

**Filtros da Consulta:**

|Dados| Armazém BO- SIAFI       |Dimensão SIAFI| Filtro  |
|--|--------------------------|----------|-------
| Despesa| Contrato Convênio Entrada |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Usar como filtro todos os 'Convênio Número Sequencial SIAFI' listados na consulta Por Projeto extraídos do SIGCON-Entrada |     
| Restos a Pagar| Contrato Convênio Entrada  | SIAFI - Execução de Restos a Pagar > Restos a Pagar | Usar como filtro todos os Convênio Número Sequencial SIAFI listados na consulta Por Projeto extraídos do SIGCON-Entrada
| | Ano de Exercício  | SIAFI - Período Contábil |


**Campos da Tabela:**

**Tabela 1º nível**

|Dados| Campo armazém BO- SIAFI     | Dimensão SIAFI| Campo PdT | Tooltip - PdT           | Exibição da Coluna
|--|------|---|---------------|------------|---|
|Despesa| ContratoConvênio Entrada | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Código SIAFI            | Código do Projeto no armazém SIAFI (Sistema Integrado de Administração Financeira de Minas Gerais ) |default
|Despesa| Unidade Orçamentária-Código      |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Código Órgão            |    Código da Unidade Orçamentária responsável pelo Projeto                | ao acionar o botão '*Exibir código e descrição*''
|Despesa| Unidade Orçamentária-Nome        | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Órgão                   |    Descrição da Unidade Orçamentária responsável pelo Projeto                |default
|Despesa| Valor Despesa Empenhada             |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | Valor Empenhado       | Valor do orçamento reservado para cumprir o compromisso assumido com o fornecedor ou credor |default
|Despesa| Valor Despesa Liquidada            | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Valor Liquidado      | Valor que o fornecedor ou credor tem direito a receber referente ao produto ou serviço devidamente entregue       |default
|Despesa| Valor Pago Financeiro           |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | Valor Pago | Valor referente aos pagamentos efetuados, no exercício, através de movimentações bancárias, escriturais e apropriação contábil da despesa. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária  |default
|Restos a Pagar| Valor Despesa Liquidada             |SIAFI - Execução de Restos a Pagar > Restos a Pagar |Valor Liquidado em Restos a Pagar       | Valor que o fornecedor ou credor tem direito a receber referente ao produto ou serviço devidamente entregue referente a exercícios anteriores                    |default
|Restos a Pagar| Valor Pago Processado + Valor Pago não processado |  SIAFI - Execução de Restos a Pagar > Restos a Pagar | Valor Pago em Restos a Pagar     | Valor pago referente a exercícios anteriores efetuados através de movimentações bancárias, escriturais e apropriação contábil da despesa, referente a produtos e serviços realizados em exercícios anteriores. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária. |default
|Fórmula Portal|   | | Valor Total (Pago  + Pago RP )     |   Somatório dos valores pagos neste exercício e pagos em restos a pagar processados e não processados.           |default

**Comportamento da Consulta:**

- Ao clicar no campo 'Código SIAFI' o usuário será direcionado para o 2º nível da consulta, ou seja, tabela de empenhos.

![](static/imagens/tabela-orgao-1nivel.png)

____

**Tabela 2º nível**
- Armazém BO / Pastas públicas - SIAFI > CGE_Portal da Transparência > Recursos Vale > TELA ÓRGÃO - nível 2

Ao clicar em algum dado do campo 'Código SIAFI' o usuário será direciona ao segundo nível da consulta, lista de empenhos correspondente ao código SIAFI selecionado.

|Dados|  Campo Armazém BO- SIAFI     | Dimensão SIAFI| Campo PdT | Tooltip - PdT           | Exibição da Coluna
|--|-----------------------------|---|-------------------------|--------------------|---|
|Despesa| Número Empenho| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada|Empenho           | Número de identificação do documento de empenho no SIAFI (Sistema Integrado de Administração Financeira de Minas Gerais )  |default
|Despesa| Data Registro Doc Empenho | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada|Data de Registro do Empenho  | Data de registro do documento de empenho   |default
|Despesa|  CNPJ_CPF Credor - Formatado    |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |CNPJ/ CPF  Favorecido  | Número de identificação: Pessoa Física (CPF) e Pessoa Jurídica (CNPJ) | default
| Despesa|  Razão Social Credor   |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | Favorecido    | Nome de quem recebeu recursos públicos estaduais pela prestação de serviço ou entrega do produto. Ex: prefeituras, servidores, empresas, entidades do terceiro setor, etc.  |default
| Despesa| Valor Despesa Empenhada |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | Valor Empenhado| Valor do orçamento reservado para cumprir o compromisso assumido com o fornecedor ou credor |default
| Despesa| Valor Despesa Liquidada  | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Valor Liquidado      | Valor que o fornecedor ou credor tem direito a receber referente ao produto ou serviço devidamente entregue        |default
| Despesa| Valor Pago Financeiro  | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Valor Pago  | Valor referente aos pagamentos efetuados, no exercício, através de movimentações bancárias, escriturais e apropriação contábil da despesa. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária |default
|Restos a Pagar| Valor Despesa Liquidada   |SIAFI - Execução de Restos a Pagar > Restos a Pagar |Valor Liquidado em Restos a Pagar       | Valor que o fornecedor ou credor tem direito a receber referente ao produto ou serviço devidamente entregue referente a exercícios anteriores |default
|Restos a Pagar| Valor Pago Processado + Valor Pago não processado |  SIAFI - Execução de Restos a Pagar > Restos a Pagar | Valor Pago em Restos a Pagar     | Valor pago referente a exercícios anteriores efetuados através de movimentações bancárias, escriturais e apropriação contábil da despesa, referente a produtos e serviços realizados em exercícios anteriores. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária. |default                 |default
|Fórmula Portal|   | | Valor Total (Pago  + Pago RP )     |   Somatório dos valores pagos neste exercício e pagos em restos a pagar processados e não processados.           |default

**Comportamento da Consulta:**

- Ao clicar no campo 'Empenho' o usuário será direcionado o formulário de detalhamento.

![](static/imagens/tabela-empenho.png)


**Formulário de Detalhamento**
- Armazém BO / Pastas públicas - SIAFI > CGE_Portal da Transparência > Recursos Vale > Formulário de Detalhamento


**1- Formulário Classificação Orçamentária**

|Dados|  Campo Armazém BO- SIAFI     | Dimensão SIAFI| Campo PdT | Observações
|--|-----------------------------|---|-------------------------|----|
|Despesa| Número Empenho| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Empenho           |
|Despesa| Data Registro Doc Empenho | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Data de Registro|
|Despesa| Unidade Orçamentária - Código/Nome | SIAFI - Unidade Orçamentária |Unidade Orçamentária| Código  e descrição no mesmo campo
|Despesa| Unidade Executora - Código/Nome | SIAFI - Unidade Executora |Unidade Executora| Código e descrição no mesmo campo
|Despesa| Função - Descrição| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Programa de Trabalho - Despesa |Função| Código e descrição no mesmo campo
|Despesa| Função - Código| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Programa de Trabalho - Despesa || Código e descrição no mesmo campo
|Despesa| Subfunção - Descrição| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Programa de Trabalho - Despesa |Subfunção| Código e descrição no mesmo campo
|Despesa| Subfunção - Código| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Programa de Trabalho - Despesa || Código e descrição no mesmo campo
|Despesa| Programa - Descrição| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Programa de Trabalho - Despesa |Programa| Código e descrição no mesmo campo
|Despesa| Programa - Código| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Programa de Trabalho - Despesa || Código e descrição no mesmo campo
|Despesa| Projeto_Atividade - Descrição| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Programa de Trabalho - Despesa |Ação (Projeto Atividade)| Código e descrição no mesmo campo
|Despesa| Projeto_Atividade - Código| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Programa de Trabalho - Despesa || Código e descrição no mesmo campo
|Despesa| Categoria Econômica Despesa - Desc| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Natureza da Despesa Realizada |Categoria Econômica da Despesa| Código e descrição no mesmo campo
|Despesa| Categoria Econômica Despesa - Código| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Natureza da Despesa Realizada || Código e descrição no mesmo campo
|Despesa| Grupo Despesa - Descrição| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Natureza da Despesa Realizada | Grupo de Despesa| Código e descrição no mesmo campo
|Despesa| Grupo Despesa - Código| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Natureza da Despesa Realizada || Código e descrição no mesmo campo
|Despesa| Modalidade de Aplicação - Descrição| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Natureza da Despesa Realizada | Modalidade de Aplicação| Código e descrição no mesmo campo
|Despesa| Modalidade de Aplicação - Código| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Natureza da Despesa Realizada || Código e descrição no mesmo campo
|Despesa| Elemento Despesa - Descrição| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Natureza da Despesa Realizada | Elemento de Despesa| Código e descrição no mesmo campo
|Despesa| Elemento Despesa - Código| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Natureza da Despesa Realizada || Código e descrição no mesmo campo
|Despesa| Item Despesa - Descrição| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Natureza da Despesa Realizada | Item de Despesa| Código e descrição no mesmo campo
|Despesa| Item Despesa - Código| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Natureza da Despesa Realizada || Código e descrição no mesmo campo
|Despesa| Fonte Recurso - Descrição| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > GMIFP | Fonte de Recurso| Código e descrição no mesmo campo
|Despesa| Fonte Recurso - Código| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > GMIFP  || Código e descrição no mesmo campo
|Despesa| Procedência - Descrição| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > GMIFP | Indicador de Procedência e Uso (IPU)| Código e descrição no mesmo campo
|Despesa| Procedência - Código| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > GMIFP  || Código e descrição no mesmo campo


![](static/imagens/formulario-classificacao-orcamentaria.png)

_______

**2- Formulário Empenho**

|Dados|  Campo Armazém BO- SIAFI     | Dimensão SIAFI| Campo PdT | Observações
|--|-----------------------------|---|-------------------------|----|
|Detalhamento do Empenho| Número Empenho| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Empenho|
|Detalhamento do Empenho| Data Registro Doc Empenho | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Data de Registro||Despesa| Data Registro Doc Empenho | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Data de Registro|
|Detalhamento do Empenho| Ano de Exercício | SIAFI - Período Contábil |Ano de Exercício|
|Despesa |Tipo Empenho - Descrição| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Tipo de Empenho|
|Detalhamento do Empenho|  CNPJ_CPF Credor - Formatado    |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada || Código e descrição no mesmo campo
| Detalhamento do Empenho|  Razão Social Credor   |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | CNPJ/ CPF e Descrição do  Favorecido | Código e descrição no mesmo campo
| Detalhamento do Empenho|  Valor Inicial Empenho   |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | Valor inicial empenhado | | Despesa|     |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | Valor Atualizado do Empenho (reforço e anulação |
| Detalhamento do Empenho|  Valor Despesa Empenhada  |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | Valor atual do empenho (reforços e anulações) | |
| Detalhamento do Empenho|    ||Descrição Histórico do Empenho |Integração entre Portal e SIAFI |
| Reforço do Empenho|  Valor Reforço  Empenho |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Valor |
| Reforço do Empenho|  |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Nº do documento | Campo SIAFI não disponível para visualização da DTA. Trazer o campo já utilizado no formulário de detalhamento da despesa
| Reforço do Empenho|  Data Reforço/Anulação |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Data de Registro |
| Anulação do Empenho|  Valor Anulação Empenho  |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | Valor | |
| Anulação do Empenho|  |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Nº do documento | Campo SIAFI não disponível para visualização da DTA. Trazer o campo já utilizado no formulário de detalhamento da despesa.
| Anulação do Empenho|  Data Reforço/Anulação |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Data de Registro |
|Inscrição em Restos a Pagar| Data Registro Doc Empenho  | SIAFI - Execução de Restos a Pagar > Restos a Pagar > Dados do Empenho - Restos a Pagar |Data de Registro| Data de registro que o empenho foi inscrito em Restos a Pagar
|Inscrição em Restos a Pagar|   |  | Tipo de Inscrição| Campo SIAFI não disponível para visualização da DTA. Trazer o campo já utilizado no formulário de detalhamento da consulta de Restos a pagar
|Inscrição em Restos a Pagar|**soma** do Valor Inscrito Processado - Valor Cancelado Processado ou Valor Restabelecido Processado      **OU soma** do Valor Inscrito Não Processado - Valor Cancelado Não Processado + Valor Restabelecido Não Processado   |  SIAFI - Execução de Restos a Pagar > Restos a Pagar| Valor Inscrito| Cada linha deverá apresentar o valor corresponde ao tipo de inscrição em restos a pagar.



**Por Município**: Os dados dessa consulta serão extraídos do Universo BO SIGCON- Entrada.
- Armazém BO - CONSULTA tmp> recursos-vale> despesa vs convenio >MUNICIPIOS

Tabelas:
| Armazém BO- SIAFI     | Dimensão SIAFI| PdT | Tooltip - PdT           | Exibição da Coluna
|-------------------------------|---|-------------------------|--------------------|---|
| Município Credor - Descrição | | Município           | Nome do município que recebeu o recurso   |default
| Valor Despesa Empenhada             | | Valor Empenhado       | Valor do orçamento reservado para cumprir o compromisso assumido com o fornecedor ou credor |default
| Valor Despesa Liquidada            | | Valor Liquidado      | Valor que o fornecedor ou credor tem direito a receber referente ao produto ou serviço devidamente entregue        |default
| Valor Pago Financeiro           | | Valor Pago          | Valor referente aos pagamentos efetuados através de movimentações bancárias, escriturais e apropriação contábil da despesa. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária |default

![image](https://user-images.githubusercontent.com/52920939/148783968-6ac2ab08-2b08-47e7-a996-466cd63981ec.png)


**Por Receita**: Os dados dessa consulta serão extraídos do Universo BO SIGCON- Entrada.
- Armazém BO - CONSULTA tmp> recursos-vale> despesa vs convenio > RECEITA

Tabelas:
| Armazém BO- SIAFI     | Dimensão SIAFI| PdT | Tooltip - PdT           | Exibição da Coluna
|-------------------------------|---|-------------------------|--------------------|---|
| Classificação Receita - Formatado | | Classificação da Receita           | Classificação criada a fim de possibilitar a identificação detalhada dos recursos que ingressam nos cofres públicos. Os números representam, da esquerda para direita: categoria econômica, origem da receita; espécie da receita, desdobramento 1 da receita; desdobramento 2 da receita, desdobramento 3 da receita, tipo da receita |default
| Item Receita - Descrição | | Item da Receita       | Detalhamento da classificação orçamentária da receita referente ao tipo de receita |default
| Subitem Receita - Descrição    | | Subitem da Receita      | Detalhamento da classificação orçamentária da receita referente ao item de receita |default
| Fonte de Recurso - Descrição   | | Fonte de Recurso          | Indica a origem do dinheiro arrecadado. Combina a origem do dinheiro às despesas orçamentárias. Esta vinculação visa demonstrar o montante de dinheiro que já está comprometido com o atendimento de determinadas finalidades, e aquele que pode ser livremente alocado |default
| Valor Previsto Inicial             | | Valor Previsto Inicial       | Valor estimado da arrecadação para o ano consultado, previsto na Lei Orçamentária Anual (LOA) |default
| Valor Previsto Atualizado           | | Valor Previsto Atualizado     | Valor estimado inicial para arrecadação no ano consultado, previsto da Lei Orçamentária Anual, atualizado ao longo do ano |default
| Valor Efetivado Ajustado           | | Valor Arrecadado          | Valor financeiro que entrou nos cofres públicos no período consultado |default

![image](https://user-images.githubusercontent.com/52920939/148783938-35f2b895-feb0-4cb5-8577-6e3b635f9123.png)


**Formulário de Detalhamento**: Os dados dessa consulta serão extraídos do Universo BO SIAFI

- Tabela Classificação Orçamentária
- Armazém BO - CONSULTA tmp> recursos-vale> despesa > CLASSIFICAÇÃO ORÇAMENTÁRIA

| Armazém BO- SIAFI     | Dimensão SIAFI| PdT |  Observações
|-------------------------------|---|-------------------------|--------------------|
| Unidade Orçamentária - Código Unidade Orçamentária - Nome| |Unidade Orçamentária           |  |
| Unidade Executora - Código/Nome | |Unidade Executora           |  |
| Função - Código   Função - Descrição| |Função           |  |
| Subfunção - Código   Subfunção - Descrição|  |    Subfunção      |  |  
| Programa - Código Programa - Descrição| |     Programa     |  |
| Projeto_Atividade - Código Projeto_Atividade - Descrição| |  Ação (Projeto Atividade)        |  |  
| Categoria Econômica Despesa -Código Categoria Econômica Despesa -Descrição| | Categoria Econômica          | |
| Grupo Despesa - Código Grupo Despesa - Descrição| | Grupo Despesa         |  |  
| Elemento Despesa - Código Elemento Despesa - Descrição| |   Elemento Despesa       |  |
| Item Despesa - Código Item Despesa - Descrição| | Item Despesa         |  |  
| Modalidade Aplicação - Código Modalidade Aplicação - Descrição| | Modalidade Aplicação         |  |
| Procedência - Código Procedência - Descrição| | Indicador de Procedência e Uso         |  |  
| Fonte Recurso - Código Fonte Recurso - Descrição| | Fonte Recurso         |  |

- Tela da Classificação Orçamentária - PDT

![image](https://user-images.githubusercontent.com/52920939/148776231-4dea4a15-42c5-4626-8eb0-916f3250a80c.png)


###### Tabela Empenho

- Tabela do Empenho
- Armazém BO - CONSULTA tmp> recursos-vale> despesa > FORMULÁRIO EMPENHO

| Armazém BO- SIAFI     | Dimensão SIAFI| PdT |  Observações
|-------------------------------|---|-------------------------|--------------------|
| Número Empenho| |Número do Empenho           |  |
| Ano de Exercício| |  Ano de Exercício       |  |
| Data Registro Doc Empenho| |  Data do Registro       |  |
| Tipo Empenho - Descrição| | Tipo  de Empenho       |  |
| CNPJ_CPF Credor - Formatado   Razão Social Credor | |  Favorecido       |  |
| | | Descrição Histórico do Empenho        |  |
| Valor Inicial Empenho| |    Valor Inicial Empenhado     |  |
| Valor Despesa Empenhada | | Valor Empenhado Atualizado        |  |
| Data Registro / Cancelamento Apropriação | |  Data de Registro       |  Reforço do Empenho
| | |  Número do documento       |  Reforço do Empenho
| Valor Reforço Empenho | |   Valor  do reforço     | Reforço do Empenho
| Data Registro / Cancelamento Apropriação | | Data de Registro        |  Anulação do Empenho
| | |  Número do documento        |  Anulação do Empenho
| Valor Anulação Empenho | |  Valor Anulado      |  Anulação do Empenho
| Data Registro Doc Restos a Pagar | | Data de Registro        |  Inscrição em Restos a Pagar
| | |   Tipo      |  Inscrição em Restos a Pagar
| valor inscrito processado” (BO) – valor cancelado processado (BO) + valor restabelecido processado | |   Valor Inscrito      |  Inscrição em Restos a Pagar

- Telas do Empenho - PDT

![image](https://user-images.githubusercontent.com/52920939/148776192-5319e930-b8a8-481d-89c9-5e551c9e7513.png)

![image](https://user-images.githubusercontent.com/52920939/148775545-e494f5ff-5baf-438f-bf78-3639ee752524.png)


###### Tabela Liquidação

- Tabela Liquidação
- Armazém BO - CONSULTA tmp> recursos-vale> despesa > FORMULÁRIO LIQUIDAÇÃO

| Armazém BO- SIAFI     | Dimensão SIAFI| PdT |  Observações
|-------------------------------|---|-------------------------|--------------------|
| Data Registro Doc Liquidação  | |Data de Registro         | |
| | |Número do Documento      | |
| CNPJ_CPF Credor - Formatado   Razão Social Credor | |  Favorecido
| Valor Despesa Liquidada | |Valor Liquidado        |   
| Data Registro Doc Liquidação | | Data de Registro        |  Liquidação em Restos a Pagar
| | |  Número do documento     |  Liquidação em Restos a Pagar
| CNPJ_CPF Credor - Formatado   Razão Social Credor | |  Favorecido |  Liquidação em Restos a Pagar
| | |   Valor Inscrito      |  Liquidação em Restos a Pagar

- Tela da Liquidação - PDT

![image](https://user-images.githubusercontent.com/52920939/148775719-252e77a3-cfde-46d2-8926-f4fe4054cc36.png)


###### Tabela Pagamento

- Tabela Pagamento
- Armazém BO - CONSULTA tmp> recursos-vale> despesa > FORMULÁRIO PAGAMENTO

| Armazém BO- SIAFI     | Dimensão SIAFI| PdT |  Observações
|-------------------------------|---|-------------------------|--------------------|
| Data Registro | |Data de Registro         |
| Número Docto Pagamento | |Número do Documento         |  
| Situação Ordem Pagamento - Descrição ||Situação da Ordem de Pagamento|
| CNPJ_CPF Credor - Formatado   Razão Social Credor ||  Favorecido
| Valor Pago Financeiro | |Valor Pago       |   
| Data Registro Doc Restos a Pagar  | | Data de Registro        |  Pagamento em Restos a Pagar
| Número Ordem Pagamento | |   Número do documento     |  Pagamento em Restos a Pagar
|||Situação da Ordem de Pagamento| Pagamento em Restos a Pagar
| CNPJ_CPF Credor - Formatado   Razão Social Credor | |  Favorecido | em Restos a Pagar
| valor pago processado (BO) + valor pago não processado (BO) | |   Valor Pago    |  Pagamento em Restos a Pagar

- Telas do Pagamento - PDT

![image](https://user-images.githubusercontent.com/52920939/148775790-f2ace5c3-7fb8-4777-9549-53b5c0ab5129.png)

###### Tabela Outras Informações

- Tabela Outras Informações
- Armazém BO - CONSULTA tmp> recursos-vale> despesa vs convenio > TABELA OUTRAS INFORMAÇÕES
- Armazém BO - CONSULTA tmp> recursos-vale> despesa vs convenio > PROCESSO DE COMPRA E CONTRATO


| Campo Armazém BO  | Dimensão SIAFI| PdT |  Observações
|-------------------------------|---|-------------------------|--------------------|
| Número Processo -  Formatado | |Número do Processo de Compra         | link para o processo de compra no PdT
| Data Criação Processo| |Data de Cadastramento do Processo         |
| Procedimento Contratação - Detalhamento 1 | |Procedimento de Contratação        |
| Situação Processo| |Situação         |
| Objeto Processo| |Objeto         |
| Número Contrato| |Número do Contrato        | link para o Contrato no Portal de Compras
| Data Publicação Contrato| |Data de Publicação       |
| Situação Contrato| |Situação        |
| Data Término Vigência Contrato| |Vigência Atualizada        |
| Objeto Contrato| |Objeto         |
| Número Convênio | |Número do Convênio / Parceria SIAFI       |link para o convênio no PdT
| Data Publicação Convênio | |Data de Publicação       |
| | |Situação do Convênio / Parceria       | Sigcon Saída
| Data Final VigênciaConvênio | |Vigência Atualizada        |
| Convênio - Título do Convênio | |Título do Convênio / Parceria        |

- Tela Outras Informações

![image](https://user-images.githubusercontent.com/52920939/148776063-1c3f2d5b-544a-4659-92ce-32620863fcb2.png)
