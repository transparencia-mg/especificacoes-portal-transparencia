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

## Página Inicial da consulta - Pesquisa Básica
<a href="#top">(inicio)</a>

### Texto explicativo
<a href="#top">(inicio)</a>

O texto desse campo poderá sem incluído/alterado pela equipe DTA por meio da área administrativa do Portal.

### Barra de navegação - Menu Superior
<a href="#top">(inicio)</a>

#### Tipo de Consultas

**Por Projeto**: Os dados dessa consulta serão extraídos do Universo BO SIGCON- Entrada.
- Armazém BO - CONSULTA tmp> recursos-vale> despesa vs convenio

Tabelas:

| Armazém BO- SIGCON ENTRADA       | PdT | Tooltip - PdT           | Exibição da Coluna
|----------------------------------|-------------------------|--------------------|---|
| Convênio Número Sequencial SIAFI | Código SIAFI            | Código do Projeto no armazém SIAFI (Sistema Integrado de Administração Financeira de Minas Gerais ) |default
| Plano Trabalho Objeto            | Projeto                 | Descrição do Projeto conforme consta no Acordo de Reparação e de execução do Governo do Estado                 |default
| Unidade Orçamentária Código      | Código Órgão            |    Código da Unidade Orçamentária responsável pelo Projeto                | ao acionar o botão '*Exibir código e descrição*''
| Unidade Orçamentária Nome        | Órgão                   |    Descrição da Unidade Orçamentária responsável pelo Projeto                |default
| Valor Total Convênio             | Valor Total           |          Valor Total destinado ao projeto          |default

![](static/imagens/tabela-projeto.png)



**Por Órgão**: Os dados dessa consulta serão extraídos do Universo BO SIAFI
- Armazém BO - CONSULTA tmp> recursos-vale> despesa vs convenio

Tabela 1º nível

| Armazém BO- SIAFI     | Dimensão SIAFI| PdT | Tooltip - PdT           | Exibição da Coluna
|-------------------------------|---|-------------------------|--------------------|---|
| ContratoConvênio Entrada | |Código SIAFI            | Código do Projeto no armazém SIAFI (Sistema Integrado de Administração Financeira de Minas Gerais ) |default
| Unidade Orçamentária-Código      | |Código Órgão            |    Código da Unidade Orçamentária responsável pelo Projeto                | ao acionar o botão '*Exibir código e descrição*''
| Unidade Orçamentária-Nome        | | Órgão                   |    Descrição da Unidade Orçamentária responsável pelo Projeto                |default
| Valor Despesa Empenhada             | | Valor Empenhado       | Valor do orçamento reservado para cumprir o compromisso assumido com o fornecedor ou credor |default
| Valor Despesa Liquidada            | | Valor Liquidado      | Valor que o fornecedor ou credor tem direito a receber referente ao produto ou serviço devidamente entregue       |default
| Valor Pago Financeiro           | | Valor Pago          | Valor referente aos pagamentos efetuados através de movimentações bancárias, escriturais e apropriação contábil da despesa. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária  |default
| Valor Despesa Liquidada             | |Valor Liquidado em Restos a Pagar       | Valor que o fornecedor ou credor tem direito a receber referente ao produto ou serviço devidamente entregue referente a exercícios anteriores                    |default
| Valor Pago Processado + Valor Pago não processado           | |Valor Pago em Restos a Pagar     | Valor referente aos pagamentos efetuados através de movimentações bancárias, escriturais e apropriação contábil da despesa, referente a produtos e serviços realizados em exercícios anteriores. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária.                   |default
| Valor Pago Financeiro           | | Valor Total Pago         | Valor total pago efetuado através de movimentações bancárias, escriturais e apropriação contábil da despesa, referente a produtos e serviços, incluído os valores pagos em restos a pagar. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária.                  |default


![](static/imagens/tabela-orgao-1nivel.png)

Tabela 2º nível

| Armazém BO- SIAFI     | Dimensão SIAFI| PdT | Tooltip - PdT           | Exibição da Coluna
|-------------------------------|---|-------------------------|--------------------|---|
| Número Empenho| |Empenho           | Número de identificação do documento de empenho   |default
|  CNPJ_CPF Credor - Formatado    | |CNPJ/ CPF  Favorecido           | Número de identificação: Pessoa Física (CPF) e Pessoa Jurídica (CNPJ) | default
|   Razão Social Credor   | | Favorecido                   | Nome de quem recebeu recursos públicos estaduais pela prestação de serviço ou entrega do produto. Ex: prefeituras, servidores, empresas, entidades do terceiro setor, etc.  |default
| Valor Despesa Empenhada             | | Valor Empenhado       | Valor do orçamento reservado para cumprir o compromisso assumido com o fornecedor ou credor |default
| Valor Despesa Liquidada            | | Valor Liquidado      | Valor que o fornecedor ou credor tem direito a receber referente ao produto ou serviço devidamente entregue        |default
| Valor Pago Financeiro           | | Valor Pago          | Valor referente aos pagamentos efetuados através de movimentações bancárias, escriturais e apropriação contábil da despesa. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária |default
| Valor Despesa Liquidada             | |Valor Liquidado em Restos a Pagar       | Valor que o fornecedor ou credor tem direito a receber referente ao produto ou serviço devidamente entregue referente a exercícios anteriores |default
| Valor Pago Processado + Valor Pago não processado           | |Valor Pago em Restos a Pagar     | Valor referente aos pagamentos efetuados através de movimentações bancárias, escriturais e apropriação contábil da despesa, referente a produtos e serviços realizados em exercícios anteriores. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária. |default
| Valor Pago Financeiro           | | Valor Total Pago         | Valor total pago efetuado através de movimentações bancárias, escriturais e apropriação contábil da despesa, referente a produtos e serviços, incluído os valores pagos em restos a pagar. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária. |default

![](static/imagens/tabela-empenho.png)

**Por Município**: Os dados dessa consulta serão extraídos do Universo BO SIGCON- Entrada.
- Armazém BO - CONSULTA tmp> recursos-vale> despesa vs convenio

Tabelas:
| Armazém BO- SIAFI     | Dimensão SIAFI| PdT | Tooltip - PdT           | Exibição da Coluna
|-------------------------------|---|-------------------------|--------------------|---|
| Município Credor - Descrição | | Município           | Nome do município que recebeu o recurso   |default
| Valor Despesa Empenhada             | | Valor Empenhado       | Valor do orçamento reservado para cumprir o compromisso assumido com o fornecedor ou credor |default
| Valor Despesa Liquidada            | | Valor Liquidado      | Valor que o fornecedor ou credor tem direito a receber referente ao produto ou serviço devidamente entregue        |default
| Valor Pago Financeiro           | | Valor Pago          | Valor referente aos pagamentos efetuados através de movimentações bancárias, escriturais e apropriação contábil da despesa. O efetivo pagamento pode estar pendente de transmissão bancária e/ou sujeita a compensação bancária |default

![image](https://user-images.githubusercontent.com/52920939/148783968-6ac2ab08-2b08-47e7-a996-466cd63981ec.png)


**Por Receita**: Os dados dessa consulta serão extraídos do Universo BO SIGCON- Entrada.
- Armazém BO - CONSULTA tmp> recursos-vale> despesa vs convenio

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

| Armazém BO- SIAFI     | Dimensão SIAFI| PdT |  Observações
|-------------------------------|---|-------------------------|--------------------|
| Unidade Orçamentária - Código Unidade Orçamentária - Nome| |Unidade Orçamentária           |  |
| | |Unidade Executora           |  |
| Função - Código   Função - Descrição| |Função           |  |
|Subfunção - Código   Subfunção - Descrição|  |    Subfunção      |  |  
|Programa - Código Programa - Descrição| |     Programa     |  |
|Projeto_Atividade - Código Projeto_Atividade - Descrição| |  Ação (Projeto Atividade)        |  |  
|Categoria Econômica Despesa -Código Categoria Econômica Despesa -Descrição| | Categoria Econômica          | |
|Grupo Despesa - Código Grupo Despesa - Descrição| | Grupo Despesa         |  |  
|Elemento Despesa - Código Elemento Despesa - Descrição| |   Elemento Despesa       |  |
|Item Despesa - Código Item Despesa - Descrição| | Item Despesa         |  |  
|Modalidade Aplicação - Código Modalidade Aplicação - Descrição| | Modalidade Aplicação         |  |
|Procedência - Código Procedência - Descrição| | Indicador de Procedência e Uso         |  |  
|Fonte Recurso - Código Fonte Recurso - Descrição| | Fonte Recurso         |  |

- Tela da Classificação Orçamentária - PDT

![image](https://user-images.githubusercontent.com/52920939/148776231-4dea4a15-42c5-4626-8eb0-916f3250a80c.png)


###### Tabela Empenho

- Tabela do Empenho

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
| Data Registro Doc Empenho | |  Data de Registro       |  Reforço do Empenho
| | |  Número do documento       |  Reforço do Empenho
| Valor Reforço Empenho | |   Valor  do reforço     | Reforço do Empenho
| | | Data de Registro        |  Anulação do Empenho
| | |  Número do documento        |  Anulação do Empenho
| | |  Valor Anulado      |  Anulação do Empenho
| | | Data de Registro        |  Inscrição em Restos a Pagar
| | |   Tipo      |  Inscrição em Restos a Pagar
| | |   Valor Inscrito      |  Inscrição em Restos a Pagar

- Telas do Empenho - PDT

![image](https://user-images.githubusercontent.com/52920939/148776192-5319e930-b8a8-481d-89c9-5e551c9e7513.png)

![image](https://user-images.githubusercontent.com/52920939/148775545-e494f5ff-5baf-438f-bf78-3639ee752524.png)


###### Tabela Liquidação

- Tabela Liquidação

| Armazém BO- SIAFI     | Dimensão SIAFI| PdT |  Observações
|-------------------------------|---|-------------------------|--------------------|
| | |Data de Registro         | |
| | |Número do Documento      | |
| CNPJ_CPF Credor - Formatado   Razão Social Credor | |  Favorecido
| | |Valor Liquidado        |   
| | | Data de Registro        |  Liquidação em Restos a Pagar
| | |  Número do documento     |  Liquidação em Restos a Pagar
| CNPJ_CPF Credor - Formatado   Razão Social Credor | |  Favorecido |  Liquidação em Restos a Pagar
| | |   Valor Inscrito      |  Liquidação em Restos a Pagar

- Tela da Liquidação - PDT

![image](https://user-images.githubusercontent.com/52920939/148775719-252e77a3-cfde-46d2-8926-f4fe4054cc36.png)


###### Tabela Pagamento

- Tabela Pagamento

| Armazém BO- SIAFI     | Dimensão SIAFI| PdT |  Observações
|-------------------------------|---|-------------------------|--------------------|
| | |Data de Registro         |
| | |Número do Documento         |  
|||Situação da Ordem de Pagamento|
| CNPJ_CPF Credor - Formatado   Razão Social Credor ||  Favorecido
| | |Valor Pago       |   
| | | Data de Registro        |  Pagamento em Restos a Pagar
| | |   Número do documento     |  Pagamento em Restos a Pagar
|||Situação da Ordem de Pagamento| Pagamento em Restos a Pagar
| CNPJ_CPF Credor - Formatado   Razão Social Credor | |  Favorecido | em Restos a Pagar
| | |   Valor Pago    |  Pagamento em Restos a Pagar

- Telas do Pagamento - PDT

![image](https://user-images.githubusercontent.com/52920939/148775790-f2ace5c3-7fb8-4777-9549-53b5c0ab5129.png)

###### Tabela Outras Informações

- Tabela Outras Informações

| Campo Armazém BO  | Dimensão SIAFI| PdT |  Observações
|-------------------------------|---|-------------------------|--------------------|
| Número Processo Compra SIAD | |Número do Processo de Compra         | link para o processo de compra no PdT
| | |Data de Cadastramento do Processo         |
| | |Procedimento de Contratação        |
| | |Situação         |
| | |Objeto         |
| | |Número do Contrato        | link para o Contrato no Portal de Compras
| | |Data de Publicação       |
| | |Situação        |
| | |Vigência Atualizada        |
| | |Objeto         |
| | |Número do Convênio / Parceria SIAFI       |link para o convênio no PdT
| | |Data de Publicação       |
| | |Situação do Convênio / Parceria       |
| | |Vigência Atualizada        |
| | |Título do Convênio / Parceria        |

- Tela Outras Informações

![image](https://user-images.githubusercontent.com/52920939/148776063-1c3f2d5b-544a-4659-92ce-32620863fcb2.png)

