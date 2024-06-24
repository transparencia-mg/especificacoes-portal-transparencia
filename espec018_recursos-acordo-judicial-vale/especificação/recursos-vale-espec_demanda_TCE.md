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

Esta demanda tem como objetivo modificar a estrutura da consulta 'Acordo Judicial da Vale' no módulo de Execução, de modo a disponibilizar aos usuários informações sobre a execução dos restos a pagar. Especificamente, visa detalhar os cancelamentos dos restos a pagar e o valor efetivo do empenho após os cancelamentos, reforços e anulações.

Em tempo também será alterado a nomenclatura de alguns termos da consulta conforme determina a [Deliberação nº 19 -Atualizações de nomes e valores de iniciativas ](https://www.mg.gov.br/system/files/media/documento_detalhado/2024-06/Delibera%C3%A7%C3%A3o%20CS%2019.2024.pdf).


# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

Conforme consta no Processo SEI nº 1630.01.0000258/2024-25, Ofício SEPLAG/RAM - CB nº. 54/2024:

''*O Tribunal de Contas do Estado de Minas Gerais - TCE/MG, no âmbito da Representação TCE n. 1135458, encaminhou a diversos órgãos e entidades demandas de informações sobre execução dos projetos do Acordo Judicial Vale/Brumadinho implementados pelo Poder Executivo Estadual.*''

*A partir da referida Representação e em diálogo com as equipes do TCE/MG, inclusive com Plano de Ação definido entre as parte (86881253), observou-se a necessidade de aprimoramento das informações divulgadas sobre a execução dos recursos, o que envolve melhorias a serem realizadas no Portal da Transparência de forma a convergir as informações divulgadas pelo site do Comitê Pró-Brumadinho e o tratamento efetivamente dado aos valores dos projetos, conforme itens citados a seguir.*

*1. Divulgação do cancelamento e reestabelecimento de restos a pagar e seus efeitos no “Valor empenhado efetivo”*

*Observa-se que o Portal da Transparência, na área específica de acompanhamento de “Eventos Extraordinários” -> “Acordo Judicial de Reparação da Vale", apresenta a execução (liquidação e pagamento) de despesas inscritas em Restos a Pagar. Porém, nessa seção do Portal da Transparência, não constam os valores de cancelamento e reestabelecimentos de Restos a Pagar e, com isso, o campo “Valor Empenhado” não considera os efeitos de cancelamento e reestabelecimento de restos a pagar.*

*Nesse contexto, solicita–se que sejam realizados, no Portal da Transparência, na área específica do Acordo Judicial de Reparação da Vale, os ajustes e as parametrizações necessárias para que sejam explicitados os cancelamentos e reestabelecimentos de Restos a Pagar e acrescido campo, denominado, por exemplo, “Valor Empenhado Efetivo”, que considere os efeitos de cancelamento e reestabelecimento de restos a pagar, de forma a garantir a correta representação do valor de fato executado orçamentariamente de cada projeto, considerado como referência para tal o valor empenhado efetivo.*


# Especificação
<a href="#top">(inicio)</a>

Este documento é fundamentado pelas seguintes alterações:

- Inclusão das colunas: Valor Cancelado em Restos a Pagar e Valor Empenhado Efetivo.
- Alteração da nomenclatura de Projeto para Iniciativa.
-Ajustes no layout e no formulário de detalhamento em decorrência das alterações mencionadas acima

## Página Inicial - Texto explicativo
<a href="#top">(inicio)</a>

Alteração do texto da Página Inicial para:

> Essa consulta tem por objetivo divulgar informações sobre os valores repassados ao Estado de Minas Gerais por meio do Acordo Judicial de Reparação firmado entre o Governo de Minas, o Ministério Público de Minas Gerais (MPMG), o Ministério Público Federal (MPF) e a Defensoria Pública de Minas Gerais (DPMG) com a Vale S.A., sob mediação do Tribunal de Justiça de Minas Gerais (TJMG).
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
>**3.Consulta por Município:** compreende o repasse de R$1.498.250.000,00 (um bilhão quatrocentos e noventa e oito milhões duzentos e cinquenta mil reais) para o fortalecimento dos serviços públicos e as melhorias de infraestrutura e de mobilidade nos municípios. As quantias foram determinadas proporcionalmente à população total, conforme dados de 2019 do IBGE .
>
>**4. Consulta por Receita:** é a visualização dos valores arrecadados em conta específica do Estado, bem como os seus respectivos valores de atualização monetária. Importante esclarecer que nessa consulta estão contemplados as correções e atualizações monetárias da Fonte de Recurso 95 que compreende recursos recebidos por danos advindos de desastres socioambientais, não apenas relativos a esse Acordo Judicial.

Outras informações sobre o Acordo Judicial de Reparação podem ser consultadas na página do [Comitê Pró-Brumadinho](https://www.mg.gov.br/pro-brumadinho).

## Alteração de termos de "Projeto" para "Iniciativas"

Em toda consulta (pesquisa básica, tabela de resultados, tooltip, pesquisa avançada, glossário e etc) deverá ser alterado a nomenclatura do termo 'Projeto' para 'Iniciativa'

## Campos Pesquisa básica - Navegação por filtros

#### Consulta por Execução

  * 1º NÍVEL
    * [Código Iniciativa]() -> ao clicar o usuário será direcionado para o 2º nível
    * Código Órgão -> -> apenas quando o usuário clicar em 'Exibir Código e Descrição'           
    * Órgão               
    * Valor Despesa Empenhada            
    * Valor Despesa Liquidada         
    * Valor Pago
    * Valor Cancelado em restos a pagar
    * Valor Liquidado em restos a pagar
    * Valor Empenhado Efetivo
    * Valor Pago em Restos a Pagar
    * Valor Total Pago     

COLOCAR IMAGEM

  * 2º NÍVEL
    * [Empenho]() -> ao clicar o usuário será direcionado para o 3º nível - Formulário de Detalhamento
    * Data de Registro do Empenho
    * Ano
    * CNPJ/CPF Favorecido
    * Valor Despesa Empenhada            
    * Valor Despesa Liquidada         
    * Valor Pago
    * Valor Cancelado em restos a pagar
    * Valor Liquidado em restos a pagar
    * Valor Empenhado Efetivo
    * Valor Pago em Restos a Pagar
    * Valor Total Pago  

COLOCAR IMAGEM

  * 3º NÍVEL - Formulário de Detalhamento

Ao clicar no campo clicável da tabela de resultados o usuário será direcionado para o formulário de detalhamento, que será composto pelos seguintes atributos:


* Empenho
COLOCAR IMAGEM


## Monte sua consulta
<a href="#top">(inicio)</a>


### Tabela de resultados
<a href="#top">(inicio)</a>

As colunas definidas como padrão ficarão marcadas na tabela ***Adicionar/Remover Colunas*** podendo o usuário desativá-las.
* Colunas padrões 1º NÍVEL:

  * [Detalhar]() => ao clicar na lupa o usuário será direcionado para o 2º nível da tabela da pesquisa avançada
  * Ano
  * Código da Iniciativa
  * Valor Despesa Empenhada            
  * Valor Despesa Liquidada         
  * Valor Pago
  * Valor Cancelado em restos a pagar
  * Valor Liquidado em restos a pagar
  * Valor Empenhado Efetivo
  * Valor Pago em Restos a Pagar
  * Valor Total Pago


* Colunas padrões 2º NÍVEL:
  * [Empenho]() -> ao clicar o usuário será direcionado para o 3º nível - Formulário de Detalhamento
  * Data de Registro do Empenho
  * Unidade orçamentária
  * Unidade Executora
  * Favorecido
  * CNPJ/CPF Favorecido
  * Valor Despesa Empenhada            
  * Valor Despesa Liquidada         
  * Valor Pago
  * Valor Cancelado em restos a pagar
  * Valor Liquidado em restos a pagar
  * Valor Empenhado Efetivo
  * Valor Pago em Restos a Pagar
  * Valor Total Pago  


* Ao inserir qualquer coluna da  tabela ***Adicionar/Remover Colunas***  essas serão incluídas antes das colunas de valores. E caso seja incluída alguma coluna de valor o portal deverá manter a ordem da execução orçamentária (Valor empenhado, valor liquidado, valor pago, Valor Cancelado em restos a pagar, valor liquidado em RP, Valor Empenhado Efetivo, Valor Pago em RP, Valor Total Pago).

COLOCAR IMAGEM
