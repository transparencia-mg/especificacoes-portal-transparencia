---
contrato_manutencao:
proposta_comercial:
mantis:
pull_request: '[]()'
titulo: Transparência dos recursos da Vale - Execução de Restos a Pagar
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da demanda
<a href="#top">(inicio)</a>

Esta demanda tem como objetivo modificar a estrutura da consulta 'Acordo Judicial da Vale' no módulo de Execução, de modo a disponibilizar aos usuários informações sobre a execução dos restos a pagar. Especificamente, visa detalhar os cancelamentos em restos a pagar e o valor efetivo dos empenhos após os cancelamentos, reforços e anulações.

Em tempo também será alterada nomenclatura de alguns termos da consulta conforme determina a [Deliberação nº 19 -Atualizações de nomes e valores de iniciativas ](https://www.mg.gov.br/system/files/media/documento_detalhado/2024-06/Delibera%C3%A7%C3%A3o%20CS%2019.2024.pdf).


# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

Conforme consta no Processo SEI nº 1630.01.0000258/2024-25, Ofício SEPLAG/RAM - CB nº. 54/2024:

''*O Tribunal de Contas do Estado de Minas Gerais - TCE/MG, no âmbito da Representação TCE n. 1135458, encaminhou a diversos órgãos e entidades demandas de informações sobre execução dos projetos do Acordo Judicial Vale/Brumadinho implementados pelo Poder Executivo Estadual.*''

*A partir da referida Representação e em diálogo com as equipes do TCE/MG, inclusive com Plano de Ação definido entre as partes (86881253), observou-se a necessidade de aprimoramento das informações divulgadas sobre a execução dos recursos, o que envolve melhorias a serem realizadas no Portal da Transparência de forma a convergir as informações divulgadas pelo site do Comitê Pró-Brumadinho e o tratamento efetivamente dado aos valores dos projetos, conforme itens citados a seguir.*

*1. Divulgação do cancelamento e restabelecimento de restos a pagar e seus efeitos no “Valor empenhado efetivo”*

*Observa-se que o Portal da Transparência, na área específica de acompanhamento de “Eventos Extraordinários” -> “Acordo Judicial de Reparação da Vale", apresenta a execução (liquidação e pagamento) das despesas inscritas em Restos a Pagar. Porém, nessa seção do Portal da Transparência, não constam os valores de cancelamentos e restabelecimentos em Restos a Pagar e, com isso, o campo “Valor Empenhado” não considera tais efeitos (cancelamento e restabelecimento).*

*Nesse contexto, solicita–se que sejam realizados, no Portal da Transparência, na área específica do Acordo Judicial de Reparação da Vale, os ajustes e as parametrizações necessárias para que sejam explicitados os cancelamentos e restabelecimentos em Restos a Pagar, acrescido do campo, denominado, por exemplo, “Valor Empenhado Efetivo”, que considere os efeitos de cancelamento e restabelecimento em restos a pagar, de forma a garantir a correta representação do valor de fato executado orçamentariamente de cada projeto, considerado como referência para tal, o valor empenhado efetivo.*


# Especificação
<a href="#top">(inicio)</a>

Este documento é fundamentado pelas seguintes alterações:

- Inclusão das colunas: Valor Cancelado em Restos a Pagar e Valor Empenhado/Cancelado no Exercício
- Alteração da nomenclatura: Aonde estiver descrito Projeto substituir por Iniciativa
- Ajustes no layout e no formulário de detalhamento em decorrência das alterações mencionadas acima

## Página Inicial - Texto explicativo
<a href="#top">(inicio)</a>

Alteração do texto da Página Inicial para:

> Essa consulta tem por objetivo divulgar informações sobre os valores repassados ao Estado de Minas Gerais por meio do Acordo Judicial de Reparação firmado entre o Governo de Minas, o Ministério Público do Estado de Minas Gerais (MPMG), o Ministério Público Federal (MPF) e a Defensoria Pública de Minas Gerais (DPMG) com a Vale S.A., sob mediação do Tribunal de Justiça do Estado de Minas Gerais (TJMG).
>
> O Acordo foi assinado em 04 de fevereiro de 2021 e garantiu que a empresa Vale S.A. fosse responsabilizada pelos danos causados às regiões atingidas e à sociedade mineira pelo rompimento das barragens B-I, B-IV e B-IVA na Mina Córrego do Feijão, em Brumadinho, ocorrido em 25 de janeiro de 2019.
>
> O Acordo Judicial visa reparar os danos decorrentes do rompimento das barragens da Vale S.A. em Brumadinho e conta com um valor inicial total de R$ 37.689.767.329,00 (trinta e sete bilhões, seiscentos e oitenta e nove milhões, setecentos e sessenta e sete mil, trezentos e vinte e nove reais).
>
> É importante esclarecer que os valores constantes no Acordo Judicial de Reparação não serão, em sua integralidade, disponibilizados ao Governo de Minas. Dos R$ 37,68 bilhões, apenas R$ 11,06 bilhões efetivamente entrarão para os cofres do Estado. É esse o montante objeto da presente consulta as quais detalhamos em seguida.
>
> As consultas criadas para dar transparência aos repasses e aos gastos realizados no Acordo Judicial de Reparação contemplam quatro diferentes escopos:
>
> **1. Consulta por Iniciativa:** compreende a divulgação dos valores destinados as iniciativas previstas no Acordo Judicial de Reparação, seguindo cronograma de desembolso definido no Acordo e atualizados conforme [deliberações](https://www.mg.gov.br/pro-brumadinho/pagina/reparacao-brumadinho-legislacoes-e-publicacoes-oficiais-documentos-sobre-o-acordo-judicial) do Conselho Superior do Comitê Gestor Pró-Brumadinho no uso das atribuições conferidas pelo Decreto nº 48.183/2021.
>
> **2. Consulta por Execução:** é a consulta que permite a visualização dos gastos de cada iniciativa, contemplando nomes dos favorecidos e valores pagos.
>
>**3.Consulta por Município:** compreende o repasse de R$1.498.250.000,00 (um bilhão quatrocentos e noventa e oito milhões duzentos e cinquenta mil reais) para o fortalecimento dos serviços públicos e as melhorias de infraestrutura e de mobilidade nos municípios. As quantias foram determinadas proporcionalmente à população total, conforme dados de 2019 do IBGE.
>
>**4. Consulta por Receita:** é a visualização dos valores arrecadados em conta específica do Estado, bem como os seus respectivos valores de atualização monetária. Importante esclarecer que nessa consulta estão contempladas as correções e atualizações monetárias da Fonte de Recurso 95 que compreende recursos recebidos por danos advindos de desastres socioambientais, não apenas relativos a esse Acordo Judicial.

Outras informações sobre o Acordo Judicial de Reparação podem ser consultadas na página do [Comitê Pró-Brumadinho](https://www.mg.gov.br/pro-brumadinho).

## Alteração de termos de "projeto" para "Iniciativas"

Em toda consulta (pesquisa básica, tabela de resultados, tooltip, pesquisa avançada, glossário e etc) deverá ser alterada a nomenclatura do termo 'Projeto' para 'Iniciativa'

## Inclusão do campo "Dados Atualizados em:" no formulário de detalhamento

Incluir na parte superior do formulário de detalhamento o campo "Dados atualizados em:"

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/bc8c0d83-ed8f-4ab6-a33f-6918b8879a52)

## Campos Pesquisa básica - Navegação por filtros

####  Por Iniciativa (Por  projeto)
<a href="#top">(inicio)</a>

Como a nomenclatura da tabela origem será alterada será necessário se atentar para a mudança do mapa de carga para a correta extração do Portal de Dados Abertos.

#### Consulta por Execução
<a href="#top">(inicio)</a>

  * 1º NÍVEL
    * [Código Iniciativa]() -> ao clicar o usuário será direcionado para o 2º nível
    * Código Órgão -> apenas quando o usuário clicar em 'Exibir Código e Descrição'           
    * Órgão               
    * Valor Empenhado            
    * Valor Liquidado         
    * Valor Pago
    * Valor Liquidado em Restos a Pagar
    * Valor Cancelado em Restos a Pagar
    * Valor Empenhado/Cancelado no Exercício
    * Valor Pago em Restos a Pagar
    * Valor Total Pago     

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/54c32e31-971d-4813-a010-ad677a95b8c4)

  * 2º NÍVEL
    * [Empenho]() -> ao clicar o usuário será direcionado para o 3º nível - Formulário de Detalhamento
    * Ano
    * Data de Registro do Empenho
    * CNPJ/CPF Favorecido
    * Favorecido
    * Valor Empenhado            
    * Valor Liquidado         
    * Valor Pago
    * Valor Liquidado em Restos a Pagar
    * Valor Cancelado em Restos a Pagar
    * Valor Empenhado/Cancelado no Exercício
    * Valor Pago em Restos a Pagar
    * Valor Total Pago  

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/4f84c30a-75eb-4248-b582-49e1fbb3aaa0)

  * 3º NÍVEL - Formulário de Detalhamento

Ao clicar no campo clicável da tabela de resultados o usuário será direcionado para o formulário de detalhamento, que será composto pelos seguintes atributos:

- Se atentar para a alteração/nome da coluna 'Valor Empenhado Efetivo:
  - Calculo da Coluna:
    = Valor Despesa Empenhada **-**[ (Valor Cancelado Processado **+** Valor Cancelado Não Processado) **-** (Valor Reestabelecido Processado **+** Valor Reestabelecido Não Processado)]

**EMPENHO**

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/3caaa656-5122-481a-adba-a9be338e5c96)
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/e397377c-ccfc-4478-b69f-80fc1096ae20)


**LIQUIDAÇÃO**

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/f91a34b9-1ba5-4715-8732-f36696fc825e)
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/af2463cf-abf7-483a-80d3-8446e314d8be)

**PAGAMENTO**

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/93bac370-e0dc-4572-b119-ca2513e5ce39)
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/e4c8634d-e7cc-4b7e-9c17-bf27d4c56381)


## Monte sua consulta
<a href="#top">(inicio)</a>


### Tabela de resultados
<a href="#top">(inicio)</a>

As colunas definidas como padrão ficarão marcadas na tabela ***Adicionar/Remover Colunas*** podendo o usuário desativá-las.
* Colunas padrões 1º NÍVEL:

  * [Detalhar]() => ao clicar na lupa o usuário será direcionado para o 2º nível da tabela da pesquisa avançada
  * Ano
  * Valor Empenhado            
  * Valor Liquidado         
  * Valor Pago
  * Valor Liquidado em Restos a Pagar
  * Valor Cancelado em Restos a Ppagar
  * Valor Empenhado/Cancelado no Exercício
  * Valor Pago em Restos a Pagar
  * Valor Total Pago

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/52920939/30e93a57-0b5b-4700-ab1b-26a5f4bc483d)

* Colunas padrões 2º NÍVEL:
  * [Empenho]() -> ao clicar o usuário será direcionado para o 3º nível - Formulário de Detalhamento
  * Data de Registro do Empenho
  * Unidade orçamentária
  * Unidade Executora
  * CNPJ/CPF Favorecido
  * Favorecido
  * Valor Empenhado            
  * Valor Liquidado         
  * Valor Pago
  * Valor Liquidado em Restos a Pagar
  * Valor Cancelado em Restos a Pagar
  * Valor Empenhado/Cancelado no Exercício
  * Valor Pago em Restos a Pagar
  * Valor Total Pago  
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/4fd70501-a075-4f62-881a-c11e8d198959)


* Ao inserir qualquer coluna da  tabela ***Adicionar/Remover Colunas***  essas serão incluídas antes das colunas de valores. E caso seja incluída alguma coluna de valor o portal deverá manter a ordem da execução orçamentária (Valor Empenhado, Valor Liquidado, Valor Pago, Valor Liquidado em RP, Valor Cancelado em Restos a Pagar, Valor Empenhado/Cancelado no Exercício, Valor Pago em RP, Valor Total Pago).

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/86b6219c-21df-4a52-bc7c-8624642ba8f4)


# Especificação - Dados da Consulta
<a href="#top">(inicio)</a>

## Por Iniciativa
<a href="#top">(inicio)</a>

Como a nomenclatura da tabela origem será alterada será necessário se atentar para a mudança do mapa de carga para a correta extração do Portal de Dados Abertos.

*Para não comprometer a atualização dos dados no ambiente de produção, será disponibilizado no ambiente de homologaão do Portal de Dados Abertos a cópia dos dados com os ajustes de nomenclatura das colunas.*

#### Filtros da Consulta
Essa consulta será plurianual, ou seja, o usuário irá visualizar todas as iniciativas e valores independente do ano.


|    Fonte de Dados    | URL
|--------------------------|-----------------
|Portal de Dados Abertos|    https://dados.mg.gov.br/dataset/acordo-judicial-reparacacao-vale-Iniciativas

*Para não comprometer a atualização dos dados no ambiente de produção, será disponibilizado no ambiente de homologaão do Portal de Dados Abertos a cópia dos dados com os ajustes de nomenclatura das colunas.*

#### Campos da Tabela

| Portal de Dados Abertos | PdT | Tooltip - PdT | Exibição da Coluna
|------------|-----|--------------------|---|
| Código Iniciativa| Código Iniciativa          | Código da Iniciativa no armazém SIAFI (Sistema Integrado de Administração Financeira de Minas Gerais ) |default
| Iniciativa     |Iniciativa               | Descrição da Iniciativa conforme consta no Acordo de Reparação e de execução do Governo do Estado                 |default
| Anexo         | Anexo      |          Anexo ao qual a Iniciativa se refere conforme o Acordo de Reparação      |default
| Valor da Iniciativa         | Valor da Iniciativa       |          Valor total destinado a Iniciativa        |default


## Por Execução
<a href="#top">(inicio)</a>

Os dados dessa consulta serão extraídos do Universo BO SIAFI
-  Armazém BO / Pastas públicas - SIAFI > SUPORTE- SIAFI > CGE > Campos BO das consultas do Portal da Transparência > Campos BO - Portal da Transparência > Eventos Extraordinários > Acordo Judicial Vale > Execução - PROPOSTA TCE

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/52920939/87ac8997-f5eb-4fb5-ac6d-dccfd833e932)


#### Filtros da Consulta

Essa consulta será anual, ou seja, o usuário irá visualizar a execução (Despesa e restos a Pagar) da Iniciativa conforme o período selecionado.

|Dados| Armazém BO- SIAFI       |Dimensão SIAFI| Filtro  |
|--|--------------------------|----------|-------
| Despesa| Contrato Convênio Entrada |SIAFI - Execução Orçamentária da Despesa > Despesa Realizada| Usar como filtro todos os 'Código Iniciativa' listados na consulta Por Iniciativa |     
| Restos a Pagar| Contrato Convênio Entrada  | SIAFI - Execução de Restos a Pagar > Restos a Pagar | Usar como filtro todos os 'Código Iniciativa' listados na consulta Por Iniciativa
| | Ano de Exercício  | SIAFI - Período Contábil |


#### Campos da Tabela

##### Tabela - Novas Colunas

|Dados| Campo armazém BO- SIAFI     | Dimensão SIAFI| Campo PdT | Tooltip - PdT           | Fórmula Portal
|--|------|---|---------------|------------|---|
|Portal de Dados Abertos| Código Iniciativa | Portal de Dados Abertos |Código Iniciativa            | Código da Iniciativa no armazém SIAFI (Sistema Integrado de Administração Financeira de Minas Gerais ) |
|Fórmula Portal| -Valor Cancelado Processado<br> -Valor Cancelado Não Processado<br> -Valor Reestabelecido Processado<br> -Valor Reestabelecido não Processado<br>        |SIAFI - Execução de Restos a Pagar > Restos a Pagar |Valor Cancelado em restos a pagar    |         | = (Valor Cancelado processado + Valor Cancelado Não Processado) - (Valor Reestabelecido processado + Valor Reestabelecido  Não Processado)           
|Fórmula Portal| -Valor Despesa Empenhada<br> -Valor Cancelado Processado<br> -Valor Cancelado Não Processado<br> -Valor Restabelecido Processado<br> -Valor Restabelecido não Processado<br>        | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada <br>-SIAFI - Execução de Restos a Pagar > Restos a Pagar |Valor Empenhado/cancelado no exercício    |                       |= Valor Empenhado - Valor Cancelado em restos a pagar (nova coluna do PDT)


##### Formulário de Detalhamento

O formulário de detalhamento deverá exibir a inscrição, liquidação e pagamento dos valores em restos a pagar referente ao todos os exercícios.
Exemplo:
- Ano de registro do Empenho: 2020
- Inscrição em Restos a Pagar: 2021
- Cancelamento em Restos a  Pagar:2021
- Reinscrito em Restos e Pagar: 2022

_______

**2- Formulário Empenho**

|Dados|  Campo Armazém BO- SIAFI     | Dimensão SIAFI| Campo PdT | Observações
|--|-----------------------------|---|-------------------------|----|
|Inscrição em Restos a Pagar| Data Registro Doc Empenho  | SIAFI - Execução de Restos a Pagar > Restos a Pagar > Dados do Empenho - Restos a Pagar |Data de Registro| Data de registro que o empenho foi inscrito em Restos a Pagar
|Fórmula Portal| -Valor Despesa Empenhada<br> -Valor Cancelado Processado<br> -Valor Cancelado Não Processado<br> -Valor Restabelecido Processado<br> -Valor Restabelecido não Processado<br>        | SIAFI - Execução Orçamentária da Despesa > Despesa Realizada <br>-SIAFI - Execução de Restos a Pagar > Restos a Pagar |Valor Empenhado Efetivo    | = Valor Empenhado - Valor Cancelado em restos a pagar (nova coluna do PDT)                      
|Inscrição em Restos a Pagar|   |  | Descrição| Campo SIAFI não disponível para visualização da DTA. Trazer o campo já utilizado no formulário de detalhamento da consulta de Restos a pagar
|Inscrição em Restos a Pagar|- Valor Inscrito Processado<br> - Valor Cancelado Processado<br> -Valor Restabelecido Processado<br> - Valor Inscrito Não Processado<br> -Valor Cancelado Não Processado<br> - Valor Restabelecido Não Processado<br>   |  SIAFI - Execução de Restos a Pagar > Restos a Pagar| Valor| Cada linha deverá apresentar o valor corresponde ao tipo de inscrição, cancelamento ou reestabelecimento em restos a pagar.
