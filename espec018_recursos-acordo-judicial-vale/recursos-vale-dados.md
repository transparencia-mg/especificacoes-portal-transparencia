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
- Armazém BO / Pastas públicas - SIAFI > SUPORTE- SIAFI > CGE > Consulta Vale Recursos Vale> Tela Projeto


#### Filtros da Consulta

Essa consulta será plurianual, ou seja, o usuário irá visualizar todos os projetos e valores independente do ano de cadastro o Convênio Código.


|    Fonte de Dados    | URL
|--------------------------|-----------------
|Portal de Dados Abertos|    

#### Campos da Tabela

| Portal de Dados Abertos | PdT | Tooltip - PdT | Exibição da Coluna
|------------|-----|--------------------|---|
| Códiso SIAFI| Código SIAFI            | Código do Projeto no armazém SIAFI (Sistema Integrado de Administração Financeira de Minas Gerais ) |default
| Anexo         | Anexo      |          Anexo ao qual o Projeto se refere conforme o Acordo de Reparação e de execução do Governo do Estado.  conforme      |default| Projeto            | Projeto                 | Descrição do Projeto conforme consta no Acordo de Reparação e de execução do Governo do Estado                 |default
| Unidade Orçamentária Código      | Código Órgão            |    Código da Unidade Orçamentária responsável pelo Projeto                | ao acionar o botão '*Exibir código e descrição*''
| Unidade Orçamentária Nome        | Órgão                   |    Descrição da Unidade Orçamentária responsável pelo Projeto                |default
| Valor Total do Projeto          | Valor Total    do Projeto       |          Valor Total destinado ao projeto          |default


![](static/imagens/tabela-projeto.png)

**Comportamento da Consulta:**

- Ao clicar no campo 'Código SIAFI' o usuário será direcionado para o 2º nível da consulta por órgão, ou seja, a tabela de empenhos. A consulta deverá exibir todos dos empenhos relacionados ao Código SIAFI selecionado independentemente do ano de registro do empenho.


### Por Órgão
<a href="#top">(inicio)</a>

Os dados dessa consulta serão extraídos do Universo BO SIAFI
-  Armazém BO / Pastas públicas - SIAFI > SUPORTE- SIAFI > CGE > Consulta Vale Recursos Vale> TELA ÓRGÃO

#### Filtros da Consulta

Essa consulta será anual, ou seja, o usuário irá visualizar a execução (Despesa e restos a Pagar) do projeto conforme o período selecionado.

|Dados| Armazém BO- SIAFI       |Dimensão SIAFI| Filtro  |
|--|--------------------------|----------|-------
| Despesa| Contrato Convênio Entrada |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Usar como filtro todos os 'Códigos SIAFI' listados na consulta Por Projeto |     
| Restos a Pagar| Contrato Convênio Entrada  | SIAFI - Execução de Restos a Pagar > Restos a Pagar | UUsar como filtro todos os 'Códigos SIAFI' listados na consulta Por Projeto
| | Ano de Exercício  | SIAFI - Período Contábil |


#### Campos da Tabela

##### Tabela 1º nível

|Dados| Campo armazém BO- SIAFI     | Dimensão SIAFI| Campo PdT | Tooltip - PdT           | Exibição da Coluna
|--|------|---|---------------|------------|---|
|Despesa| ContratoConvênio Entrada | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Código SIAFI            | Código do Projeto no armazém SIAFI (Sistema Integrado de Administração Financeira de Minas Gerais ) |default
|Despesa| Unidade Orçamentária-Código      |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Código Órgão            |    Código da Unidade Orçamentária responsável pelo Projeto                | ao acionar o botão '*Exibir código e descrição*''
|Despesa| Unidade Orçamentária-Nome        | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Órgão                   |    Descrição da Unidade Orçamentária responsável pelo Projeto                |default
|Despesa| Valor Despesa Empenhada             |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | Valor Empenhado       | Valor do orçamento reservado para cumprir o compromisso assumido com o fornecedor ou credor |default
|Despesa| Valor Despesa Liquidada            | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Valor Liquidado      | Valor que o fornecedor ou credor tem direito a receber referente ao produto ou serviço devidamente entregue       |default
|Despesa| Valor Pago Financeiro           |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | Valor Pago | Valor referente aos pagamentos efetuados, no exercício, através de movimentações bancárias, escriturais e apropriação contábil da despesa. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária  |default
|Restos a Pagar| Valor Despesa Liquidada             |SIAFI - Execução de Restos a Pagar > Restos a Pagar |Valor Liquidado em Restos a Pagar       | Valor que o fornecedor ou credor tem direito a receber referente ao produto ou serviço devidamente entregue referente a exercícios anteriores                    |default
|Restos a Pagar| -Valor Pago Processado<br> -Valor Pago não processado |  SIAFI - Execução de Restos a Pagar > Restos a Pagar | Valor Pago em Restos a Pagar     | Valor pago referente a exercícios anteriores efetuados através de movimentações bancárias, escriturais e apropriação contábil da despesa, referente a produtos e serviços realizados em exercícios anteriores. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária. |default
|Fórmula Portal|   | | Valor Total Pago   | Somatório dos valores pagos neste exercício e pagos em restos a pagar processados e não processados.           |default

![](static/imagens/tabela-orgao-1nivel.png)

**Comportamento da Consulta:**

- Ao clicar no campo 'Código SIAFI' o usuário será direcionado para o 2º nível da consulta, ou seja, tabela de empenhos.
____

##### Tabela 2º nível

- Armazém BO / Pastas públicas - SIAFI > SUPORTE- SIAFI > CGE > Consulta Vale Recursos Vale> TELA ÓRGÃO - nível 2

Ao clicar em algum dado do campo 'Código SIAFI' o usuário será direciona ao segundo nível da consulta, lista de empenhos correspondente ao código SIAFI selecionado.

|Dados|  Campo Armazém BO- SIAFI     | Dimensão SIAFI| Campo PdT | Tooltip - PdT           | Exibição da Coluna
|--|-----------------------------|---|-------------------------|--------------------|---|
|Despesa| Número Empenho| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Empenho           | Número de identificação do documento de empenho no SIAFI (Sistema Integrado de Administração Financeira de Minas Gerais )  |default
|Despesa| Data Registro Doc Empenho | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Data de Registro do Empenho  | Data de registro do documento de empenho   |default
|Despesa|  CNPJ_CPF Credor - Formatado    |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |CNPJ/ CPF  Favorecido  | Número de identificação: Pessoa Física (CPF) e Pessoa Jurídica (CNPJ) | default
| Despesa|  Razão Social Credor   |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | Favorecido    | Nome de quem recebeu recursos públicos estaduais pela prestação de serviço ou entrega do produto. Ex: prefeituras, servidores, empresas, entidades do terceiro setor, etc.  |default
| Despesa| Valor Despesa Empenhada |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | Valor Empenhado| Valor do orçamento reservado para cumprir o compromisso assumido com o fornecedor ou credor |default
| Despesa| Valor Despesa Liquidada  | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Valor Liquidado      | Valor que o fornecedor ou credor tem direito a receber referente ao produto ou serviço devidamente entregue        |default
| Despesa| Valor Pago Financeiro  | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Valor Pago  | Valor referente aos pagamentos efetuados, no exercício, através de movimentações bancárias, escriturais e apropriação contábil da despesa. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária |default
|Restos a Pagar| Valor Despesa Liquidada   |SIAFI - Execução de Restos a Pagar > Restos a Pagar |Valor Liquidado em Restos a Pagar       | Valor que o fornecedor ou credor tem direito a receber referente ao produto ou serviço devidamente entregue referente a exercícios anteriores |default
|Restos a Pagar| - Valor Pago Processado<br> - Valor Pago não processado |  SIAFI - Execução de Restos a Pagar > Restos a Pagar | Valor Pago em Restos a Pagar     | Valor pago referente a exercícios anteriores efetuados através de movimentações bancárias, escriturais e apropriação contábil da despesa, referente a produtos e serviços realizados em exercícios anteriores. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária. |default                 |default
|Fórmula Portal|   | | Valor Total Pago   |   Somatório dos valores pagos neste exercício e pagos em restos a pagar processados e não processados.           |default

![](static/imagens/tabela-empenho.png)

**Comportamento da Consulta:**

- Ao clicar no campo 'Empenho' o usuário será direcionado o formulário de detalhamento.

-----

##### Formulário de Detalhamento

- Armazém BO / Pastas públicas - SIAFI > SUPORTE- SIAFI > CGE > Consulta Vale Recursos Vale> > Formulário de Detalhamento

O formulário de detalhamento deverá exibir a inscrição, liquidação e pagamento dos valores em restos a pagar referente ao todos os exercícios.
Exemplo:
- Ano de registro do Empenho: 2020
- Inscrição em Restos a Pagar: 2021
- Reinscrito em Restos e Pagar: 2022

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

![](static/imagens/formulario-empenho.png)


_______

**3- Formulário Liquidação**


|Dados|  Campo Armazém BO- SIAFI     | Dimensão SIAFI| Campo PdT | Observações
|--|-----------------------------|---|-------------------------|----|
|Detalhamento da Liquidação| | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Nº do documento| Campo SIAFI não disponível para visualização da DTA. Trazer o campo já utilizado no formulário de detalhamento da liquidação.
|Detalhamento da Liquidação| Data Registro Doc Liquidação | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Data de Registro||Despesa| Data Registro Doc Empenho | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Data de Registro|
|Detalhamento da Liquidação|  CNPJ_CPF Credor - Formatado    |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada || Código e descrição no mesmo campo
| Detalhamento da Liquidação|  Razão Social Credor   |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | CNPJ/ CPF e Descrição do  Favorecido | Código e descrição no mesmo campo
| Detalhamento da Liquidação|  Valor Despesa Liquidada   |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Valor Liquidado |
|Liquidação em Restos a Pagar| Data Registro Doc Liquidação  | SIAFI - Execução de Restos a Pagar > Restos a Pagar > Dados da Liquidação - Restos a Pagar |Data de Registro| Data de registro que o restos a pagar não processado foi liquidado.
|Liquidação em Restos a Pagar|  CNPJ_CPF Credor - Numérico   | SIAFI - Execução de Restos a Pagar > Restos a Pagar || Código e descrição no mesmo campo
| Liquidação em Restos a Pagar|  Razão Social Credor   | SIAFI - Execução de Restos a Pagar > Restos a Pagar | CNPJ/ CPF e Descrição do  Favorecido | Código e descrição no mesmo campo
| Liquidação em Restos a Pagar|  Valor Despesa Liquidada   |SIAFI - Execução de Restos a Pagar > Restos a Pagar |Valor Liquidado RP| Valor liquidado do restos a pagar não processado

![](static/imagens/formulario-liquidacao.png)

_______

**4- Formulário Pagamento**


|Dados|  Campo Armazém BO- SIAFI     | Dimensão SIAFI| Campo PdT | Observações
|--|-----------------------------|---|-------------------------|----|
|Detalhamento do Pagamento| Data de Registro| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Dados da Ordem de Pagamento - Despesa| Data de Registro|
|Detalhamento do Pagamento| Número Docto Pagamento | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Dados da Ordem de Pagamento - Despesa |Nº do documento|
|Detalhamento do Pagamento| Situação Ordem de Pagamento - Descrição | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Dados da Ordem de Pagamento - Despesa |Situação da Ordem de Pagamento|
|Detalhamento do Pagamento|  CNPJ_CPF Credor - Formatado    |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada || Código e descrição no mesmo campo
| Detalhamento do Pagamento|  Razão Social Credor   |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | CNPJ/ CPF e Descrição do  Favorecido | Código e descrição no mesmo campo
| Detalhamento do Pagamento|  Valor Pago Financeiro  |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Valor Pago |
|Pagamento em Restos a Pagar| Data Registro | SIAFI - Execução de Restos a Pagar > Restos a Pagar > Dados da Ordem de Pagamento - Restos a Pagar |Data de Registro| Data de registro que o restos a pagar foi pago.
|Pagamento em Restos a Pagar| Número Ordem de Pagamento | SIAFI - Execução de Restos a Pagar > Restos a Pagar > Dados da Ordem de Pagamento - Restos a Pagar |Nº do documento|
|Detalhamento do Pagamento| Situação Ordem de Pagamento - Descrição |  SIAFI - Execução de Restos a Pagar > Restos a Pagar > Dados da Ordem de Pagamento - Restos a Pagar |Situação da Ordem de Pagamento|
|Pagamento em Restos a Pagar|  CNPJ_CPF Credor - Numérico   | SIAFI - Execução de Restos a Pagar > Restos a Pagar || Código e descrição no mesmo campo
| Pagamento em Restos a Pagar|  Razão Social Credor   | SIAFI - Execução de Restos a Pagar > Restos a Pagar | CNPJ/ CPF e Descrição do  Favorecido | Código e descrição no mesmo campo
| Pagamento em Restos a Pagar|  Valor Pago Processado ou Valor Pago não processado |SIAFI - Execução de Restos a Pagar > Restos a Pagar |Valor Pago em RP |

![](static/imagens/formulario-pagamento.png)

_______

**4- Formulário Outras Informações**


|Dados|  Campo Armazém BO     | Dimensão Armazém BO| Campo PdT | Observações
|--|-----------------------------|---|-------------------------|----|
|Dados do Processo de Compra| Número do Processo de Compra| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada | Número do Processo de Compra| Campo utilizado para cruzamento das informações empenho vs processo de compra. Ao identificar qual processo de compra está vinculado ao empenho os demais dados referente ao processo serão extraídos do Armazém SIADI - Portal de Compras - Módulo Compras
|Dados do Processo de Compra| Data criação do Processo | Armazém SIADI - Portal de Compras - Módulo Compras > Data criação do Processo| Data de Cadastramento do Processo|
|Dados do Processo de Compra| Procedimento de Contratação - Detalhamento 1 | Armazém SIADI - Portal de Compras - Módulo Compras > Procedimento de Contratação| Procedimento de Contratação|
|Dados do Processo de Compra| Situação Processo | Armazém SIADI - Portal de Compras - Módulo Compras | Situação do Processo|
|Dados do Processo de Compra| Objeto Processo | Armazém SIADI - Portal de Compras - Módulo Compras | Objeto do Processo|
|Dados Contrato| Número Contrato| Armazém SIADI - Portal de Compras - Módulo Compras > Contrato | Número do Contrato|
|Dados Contrato| Data Publicação Contrato | Armazém SIADI - Portal de Compras - Módulo Compras > Data Publicação Contrato| Data de Publicação|
|Dados Contrato| Data Término Vigência Contrato | Armazém SIADI - Portal de Compras - Módulo Compras > Data Atualizada Término Vigência Contrato| Vigência atualizada |
|Dados Contrato| Situação Contrato | Armazém SIADI - Portal de Compras - Módulo Compras > Contrato | Situação do Contrato|
|Dados Contrato| Objeto Contrato | Armazém SIADI - Portal de Compras - Módulo Compras > Contrato | Objeto do Contrato|
|Dados do Convênio  / Parceria de Saída Recursos| Contrato Convênio Saída| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Dados do Empenho - Despesa | Número do Convênio / Parceria SIAFI| Ao identificar que existe 'Contrato Convênio Saída' relacionado a um empenho deve-se realizar o cruzamento com a base de dados do Pdt consulta Convênio de Saída / Parceria de recursos e caso a informação conste na base de dados essas serão replicadas nesse formulário. Exemplo: Código SIAFI (Contrato Convênio Entrada) 9288133 >> Empenho (Número do Empenho) 367/2021 >> Número do Convênio / Parceria SIAFI (Contrato Convênio Saída) [9318584](https://www.transparencia.mg.gov.br/convenios/convenios-de-saida/convenios-conslivre-detalhesconv/2021/01-01-2021/31-12-2021/61691)
|Dados do Convênio/Parceria de Saída Recursos| Data Publicação |PdT - Consulta Convênios / Parceria de Saída de Recursos | Data de Publicação|
|Dados do Convênio/Parceria de Saída Recursos| Vigência atualizada | PdT - Consulta Convênios / Parceria de Saída de Recursos| Vigência atualizada |
|Dados do Convênio/Parceria de Saída Recursos| Situação do Convênio / Parceria| PdT - Consulta Convênios / Parceria de Saída de Recursos | Situação do Convênio / Parceria|
|Dados do Convênio/Parceria de Saída Recursos| Título do Convênio / Parceria | PdT - Consulta Convênios / Parceria de Saída de Recursos| Título do Convênio / Parceria|

![](static/imagens/formulario-outras-informacoes.png)

**Comportamento da Consulta:**

- Ao clicar no campo 'Número do Processo de Compra' o usuário será direcionado o formulário de detalhamento da consulta [Compras e Contratos](https://www.transparencia.mg.gov.br/compras-e-patrimonio/compras-e-contratos/comprasecontratos-detalhe-proccompra/2021/20210101/20211231/352133).

- Ao clicar no campo 'Número do Contrato' o usuário poderá fazer o [download do contrato](https://www1.compras.mg.gov.br/contrato/gestaocontratos/arquivosContrato.html?idContrato=170153).

- Ao clicar no campo 'Número do Convênio / Parceria SIAFI' o usuário será direcionado o formulário de detalhamento da consulta [Consulta Convênios / Parceria de Saída de Recursos](https://www.transparencia.mg.gov.br/convenios/convenios-de-saida/convenios-conslivre-detalhesconv/2021/01-01-2021/31-12-2021/61691)


_______
### Por Município
<a href="#top">(inicio)</a>

Os dados dessa consulta serão extraídos do Universo BO SIAFI.
- Armazém BO / Pastas públicas - SIAFI > SUPORTE- SIAFI > CGE > Consulta Vale Recursos Vale> Tela Município


#### Filtros da Consulta

Essa consulta será plurianual, ou seja, o usuário irá visualizar todos repasses referente ao Município independentemente do ano de repasse.

| Armazém BO- SIAFI       | Filtro
|--------------------------|-----------------
|Contrato Convênio Entrada | 9288130    


#### Campos da Tabela

|Dados| Campo armazém BO- SIAFI     | Dimensão SIAFI| Campo PdT | Tooltip - PdT           | Exibição da Coluna
|-|------|---|---------------|------------|---|
|Município |Ano de Exercício |Período Contábil| Ano do Repasse|Ano de exercício que o repasse ocorreu|---|
|Município |Município Credor - Descrição| SIAFI - Execução Orçamentária da Despesa - Despesa Realizada > Credor - Despesa |Município |Nome do Município que recebeu os repasses do Acordo Judicial conforme art. 5º e anexo V da Lei Estadual nº 23.830/2021|*default*
|Município |Número Empenho| SIAFI - Execução Orçamentária da Despesa - Despesa Realizada|Empenho| Número de identificação do documento de empenho no SIAFI (Sistema Integrado de Administração Financeira de Minas Gerais )|*default*|
|Município |Data Registro| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Dados da Ordem de Pagamento - Despesa| Data de Registro|Data de Registro do Pagamento no SIAFI (Sistema Integrado de Administração Financeira de Minas Gerais )|*default*|
|Município |Situação Ordem de Pagamento - Descrição |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada > Dados da Ordem de Pagamento - Despesa |Situação da Ordem de Pagamento| Situação da Ordem de Pagament conforme consta no SIAFI (Sistema Integrado de Administração Financeira de Minas Gerais )|*default*|
|Município |Valor Pago Financeiro| SIAFI - Execução Orçamentária da Despesa > Despesa Realizada |Valor Pago| Valor referente aos repasses efetuados conforme art. 5º e anexo V da Lei Estadual nº 23.830/2021 do Acordo Judicial|*default*|

![](static/imagens/tabela-municipio.png)

**Comportamento da Consulta:**

- Ao clicar no campo 'Empenho' o usuário será direcionado o formulário de detalhamento referente ao empenho.

______
### Por Receita
<a href="#top">(inicio)</a>

Os dados dessa consulta serão extraídos do Universo BO SIAFI.
- Armazém BO / Pastas públicas - SIAFI > SUPORTE- SIAFI > CGE > Consulta Vale Recursos Vale> Tela Receita


#### Filtros da Consulta

Essa consulta será plurianual, ou seja, o usuário irá visualizar os valores arrecadados por ano.

| Armazém BO- SIAFI       | Filtro
|--------------------------|-----------------
|Fonte de Recurso| 95
Classificação Receita - Formatado| 2990.00.1.1.02.000


#### Campos da Tabela

|Dados| Campo armazém BO- SIAFI     | Dimensão SIAFI| Campo PdT | Tooltip - PdT           | Exibição da Coluna
|-| -|---|---------------|------------|---|
|Receita| Ano de Exercício |SIAFI - Período Contábil|Ano de Exercício |Ano de exercício que ocorreu a arrecadação|*default*|
|Receita |Classificação Receita - Formatado |SIAFI - Execução Orçamentária da Receita > Receita Orçamentária > Classificação Receita Orçamentária a partir de 2018 > |Código da Classificação Receita|Classificação criada a fim de possibilitar a identificação detalhada dos recursos que ingressam nos cofres públicos. Os números representam, da esquerda para a direita: categoria econômica; origem da receita; espécie da receita; desdobramento 1 da receita, desdobramento 2 da receita, desdobramento 3 da receita, tipo da receita| ao acionar o botão 'Exibir código e descrição'|
|Receita| Classificação Receita - Descrição |SIAFI - Execução Orçamentária da Receita > Receita Orçamentária > Classificação Receita Orçamentária a partir de 2018|Classificação Receita |Descrição da identificação detalhada dos recursos que ingressam nos cofres públicos |*default*|
|Receita| Fonte de Recurso - Código |SIAFI - Execução Orçamentária da Receita > Receita Orçamentária > Classificação Receita Orçamentária a partir de 2018|Código da Fonte de Recurso||ao acionar o botão 'Exibir código e descrição'|
|Receita| Fonte de Recurso -  |SIAFI - Execução Orçamentária da Receita > Receita Orçamentária > Classificação Receita Orçamentária a partir de 2018|Fonte de Recurso |Indica a origem do dinheiro arrecadado. Combina a origem do dinheiro às despesas orçamentárias. Esta vinculação visa demonstrar o montante de dinheiro que já está comprometido com o atendimento de determinadas finalidades, e aquele que pode ser livremente alocado.|*default*|
|Receita| Valor Previsto Inicial |SIAFI - Execução Orçamentária da Receita > Receita Orçamentária > Classificação Receita Orçamentária a partir de 2018| Valor Previsto Inicial| Valor estimado da arrecadação para o ano consultado, previsto na Lei Orçamentária Anual (LOA)|*default*|
|Receita|  Valor Previsto Atualizado|SIAFI - Execução Orçamentária da Receita > Receita Orçamentária > Classificação Receita Orçamentária a partir de 2018|Valor Previsto Atualizado| Valor estimado inicial para arrecadação no ano consultado, previsto na Lei Orçamentária Anual, atualizado ao longo do ano.|*default*
|Receita| Valor Efetivado Ajustado |SIAFI - Execução Orçamentária da Receita > Receita Orçamentária > Classificação Receita Orçamentária a partir de 2018|Valor Arrecadado| Valor financeiro que entrou nos cofres públicos no período consultado|*default*

![](static/imagens/tabela-receita.png)

## Ponto de Destaque

A pesquisa básica deve permitir que novas informações possam ser incluídas através da integração de fontes estáticas, ou seja, fonte que não seja o Armazém BO.


## Monte sua pesquisa - Pesquisa Avançada
<a href="#top">(inicio)</a>

Os dados/tabelas da pesquisa avançada serão os mesmos que constam nas tabelas da pesquisa básica, porém será necessário verificar a granularidade para os devidos cruzamentos.

|Filtro barra vertical| Filtro Tabela de resultado | Comportamento ao selecionar o filtro na barra vertical
|--------|--|--------|
|Período| não |- Como padrão o período será o do ano corrente até a última data de atualização<br> - Usuário é obrigado a selecionar o período<br>
|Código SIAFI|sim ||
|Órgão|sim ||
|Código SIAFI|sim ||
|Órgão|sim ||
|Código SIAFI|sim ||
|Órgão|sim |Esse campo deverá possibilitar a busca por nome ou descrição| 
|Código SIAFI|sim ||
|Órgão|sim ||
|Código SIAFI|sim ||
|Órgão|sim ||
