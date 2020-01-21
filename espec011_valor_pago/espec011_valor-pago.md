
# Visão Geral da Intervenção

Essa demanda visa adequar no Portal da Transparência a regra de divulgação dos dados de pagamento, mais especificamente, a inclusão a Data de Pagamento no formulário de detalhamento da despesa. alteração do nome das tabelas e alteração da conceito do valor pago das consultas de Despesa, Diárias e Restos a Pagar.

A alteração também será realizada na consulta de Convênios, e será alterada a regra de extração dos dados para a divulgação dos valores pagos.

# Motivação / Contexto da Intervenção

De acordo com as regras de registro de Ordem de Pagamento (OP) no SIAFI é possível ocorrer diversas situações identificadas no armazém BO para o campo Situação Ordem de Pagamento, que são:

1. Paga
2. Acatada pelo banco
3. Pendente de transmissão aos bancos
4. Sujeita a compensação bancária
5. Quitada
6. Cancelada
7. Cancelada pelo operador
8. Cancelada -TED
9. Transmitida ao banco - Pendente de confirmação
10. Cancelada sem cancelamento do IRRP retido _TED_

Dentre essas situações, ressaltamos as situações 2 (acatada pelo banco), 3 (pendente de transmissão aos bancos) e situação 4 (sujeita a compensação bancária).

Atualmente, o Portal de Transparência apresenta os dados relativos a OP utilizando como variável para divulgação do valor pago a ___Data de Registro___ no SIAFI.

Nesse sentido o Portal divulga uma despesa como paga, mas que ainda não percorreu todas as etapas de pagamento, ou seja, assinatura pelo ordenador de despesa, transmissão ao banco e a compensação bancária, o que gera dúvidas para os credores sobre o efetivo depósito dos valores registrados no Portal como pagos.

Etapas da Ordem de Pagamento:

![](static/fluxograma.jpg)

  Para elucidar, trazemos como exemplo o empenho 1387 (UE 1500002) - OP 1599 consultado no SIAFI na data de 17/12/2019, cujo registro da OP ocorreu no dia 28/11/2019, com data de pagamento registrada no SIAFI para 29/11/2019.

![](static/siafi_1599.jpg)

E conforme tela do SIAFI, consta na [Situação] a informação de PENDENTE PARA BANCO. AGUARDANDO ASSINATURA DIGITAL.

Essa mesma OP consultada no Portal da Transparência consta como paga no formulário de detalhamento de despesa, desde o dia 28/11/2019 (código do documento 1599), no valor de R$268,45.

![](static/portal_1599.jpg)

Assim, apesar de constar como paga no Portal da Transparência desde o dia 28/11/2019, a OP 1599 ainda não percorreu todas as etapas de pagamento.

A mesma situação ocorre na consulta de Restos a Pagar.
Exemplo é a consulta de restos a pagar referente ao Restos a Pagar 2018/3. Conforme tela do SIAFI a data de registro da OP ocorreu em 01/03/2019, mas o efetivo pagamento da despesa ocorreu em 07/03/2019.

![](static/restosapagarsiafi.jpg)

No Portal da Transparência, a mesma OP 22, consta que o pagamento foi realizado no 01/03/2019, quando na verdade, a data em que o valor foi acatado pelo banco ocorreu somente no dia 07/03/2019.

![](static/restosapagarportal.jpg)

Outra consulta com impacto direto na divulgação de dados sobre o pagamento é a consulta de Convênios/Parcerias de Saída de Recursos, que diferentemente das demais consultas não possui a informação de Data de Registro da OP.

![](static/conveniossaida.jpg)

A regra adotada pelo Portal da Transparência para a Consulta de Convênios / Parcerias de Saída de Recursos é a mesma aplicada as demais consultas, que é a informação de valor repassado tendo como critério o Valor Pago Financeiro, Valor Pago Processado e Valor Pago Não Processado de acordo com a Data de Registro da OP, que traz para o Portal, a informação de valor repassado, mesmo que a despesa não tenha percorrido todas as suas fases.

[Convênios de Saída](static/conveniossaida.xls)

Como exemplo, temos o convênio 9220736, cuja OP 192 foi registrada no dia 17/12/2019, e com data de pagamento para 20/12/2019.

![](static/convenios.jpg)

No entanto, conforme consulta ao armazém consta na Situação Ordem Pagamento - Descrição: Transmitida ao banco - pendente de confirmação. Essa situação indica que o depósito no valor de R$45.000,00 ainda não foi realizado na conta do convenente. Apesar do Portal da Transparência informar que o valor já foi repassado ao convenente.

![](static/portalconvenios.jpg)

A tela do SIAFI, confirma que o OP 192 ainda depende de compensação bancária, estando o depósito sujeita a confirmação pelo banco.

![](static/siaficonvenios.jpg)

Assim, com o objetivo de melhorar a divulgação de dados sobre pagamentos, sugere-se a alteração no formulário de detalhamento da despesa (opções Empenho e Pagamento) para que apresente não somente a data de registro da OP, mas também a data de pagamento de uma determinada OP (paga, acatada pelo banco e sujeita a compensação bancária), respeitado o prazo de atualização de D+1 estabelecido pelo Decreto Federal n° 7.185, de 2010.

Além dessa alteração, sugere-se a alteração na descrição do valor pago que consta no glossário interativo das colunas "Valor pago" das consultas de Despesa, Diárias e Restos a Pagar, para que seja esclarecido a sociedade as situações que compõem o campo valor pago.

Atualmente, o glossário do portal e o tool tip trazem a seguinte definição: valor referente aos pagamentos efetuados através de movimentações bancárias, escriturais e apropriação contábil da despesa.



# Especificação

## Consulta Despesa e Diárias

__1. Alterar descrição do campo "Valor Pago" no glossário interativo__

Alterar a descrição do _tool tip_ da coluna valor pago que passará a exibir o seguinte texto ao passar o cursor sobre o ponto de interrogação:

* Valor Pago: Valor referente aos pagamentos efetuados através de movimentações bancárias, escriturais e apropriação contábil da despesa. O efetivo pagamento pode estar pendente de assinatura do ordenador de despesa e/ou sujeito a compensação bancária.

![](static/valor_pago.jpg)

___Observação___: Essas alterações aplicam-se a toda base de dados da consulta de Despesas e Diárias disponíveis no Portal da Transparência.


__2. Alterar o texto das colunas Data e Número de Documento__


Alterar o texto e descrição das [colunas] "DATA" e "NUMERO DO DOCUMENTO" das consultas de Despesas e Diárias.

 __Situação 1:__ ao clicar no [Valor Empenhado](http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-orgaos/2020/01-01-2020/31-12-2020/4009/1910/457/20/42/1264408/2771/empenhado), o próximo nível deverá apresentar a informação:

  - Data de Registro (no lugar de Data): Data de Registro do documento de empenho no SIAFI (Sistema Integrado de Administração Financeira).

  - Número do Empenho (no lugar de Número Documento): Número de identificação do documento de empenho no SIAFI (Sistema Integrado de Administração Financeira).

  ![](static/empenho.jpg)


__Situação 2:__ ao clicar no [Valor Liquidado](http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-orgaos/2020/01-01-2020/31-12-2020/4009/1910/457/20/42/1264408/2771/liquidado), o próximo nível deverá apresentar a informação:

  - Data do Registro (no lugar de Data): Data de registro da liquidação no SIAFI (Sistema Integrado de Administração Financeira).

  - Número da Liquidação (no lugar de Número Documento): Número de identificação do documento de  liquidação no SIAFI (Sistema Integrado de Administração Financeira);

![](static/liquidacao.jpg)

__Situação 3:__ ao clicar no [Valor Pago](http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-orgaos/2020/01-01-2020/31-12-2020/4009/1910/457/20/42/1264408/2771/pago), o próximo nível deverá apresentar a informação:

  - Data de Registro (no lugar de Data): Data de registro da ordem de pagamento no SIAFI (Sistema Integrado de Administração Financeira).

  - Número da Ordem Pagamento (no lugar de Número Documento): Número de identificação do documento da ordem de pagamento no SIAFI (Sistema Integrado de Administração Financeira).

![](static/pagamentos.jpg)


___Observação___: Essas alterações aplicam-se a toda base de dados da consulta de Despesas e Diárias disponíveis no Portal da Transparência.


Abaixo segue as consultas realizadas no armazém SIAFI para cada alteração sugerida.

![](static/nomenclaturas.jpg)

[Planilha Pagamentos](static/pagamentos_2019.xls)

__3. Alteração do Formulário de Detalhamento de Despesa e Diárias__

No formulário de detalhamento da consulta de despesa e diárias, opções de empenho e pagamento, serão alteradas as seguintes informações:

 __Situação:__ Ao clicar no [Número do documento do Empenho, Número Documento Liquidação ou Número do Documento Pagamento](http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-orgaos/2020/01-01-2020/31-12-2020/4009/1910/457/20/42/1264408/2771/empenhado/16/12589445/0/0), o próximo nível deverá apresentar a informação:

* Substituir o texto "Data" para "Data Registro" no formulário de pagamento (sem alteração na extração de dados no Armazém);

* Incluir a coluna de "Data Pagamento" no formulário de pagamento (após a coluna data de registro).

![](static/formulario_emp_pag.jpg)


__Observação__: Importante ressaltar que serão consideradas apenas as data de pagamento com valores válidos. Informações em branco ou informações inválidas não serão trazidas para o portal.

[formulario_detalhamento_despesa](static/formulario_detalhamento_despesa.xls)

## Consulta Restos a Pagar

__1. Formulário de Detalhamento de Despesa__

No [Formulário de Detalhamento da Despesa](http://transparencia.mg.gov.br/despesa-estado/restos-a-pagar/restospagar-orgaos/2019/3853/546/42/20/3065/130/58/5933374) da Consulta de Restos a Pagar, será alterada a mesma informação já especificada para a consulta de Despesas e Diárias, que é:

1. Substituir o texto "Data" para "Data Registro" (sem alteração na extração de dados no Armazém);

2. Incluir a coluna de "Data Pagamento" no formulário de pagamento (após a coluna data de registro).

![](static/formulario_emp_pag.jpg)

  __Observação__: Importante ressaltar que serão consideradas apenas as data de pagamento com valores válidos. Informações em branco ou informações inválidas não serão trazidas para o portal.

[Restos a Pagar](static/restosapagar.xls)


__2. Alterar descrição do campo "Valor Pago no Ano" no glossário interativo__

Alterar a descrição do _tooltip_ da coluna "valor pago no ano" da consulta de Restos a Pagar, que passará a exibir o seguinte texto ao passar o cursor sobre o ponto de interrogação:

  - Valor Pago no Ano: Soma do valor de restos a pagar processados e não processados referentes aos pagamentos efetuados através de movimentações bancárias, escriturais e apropriação contábil da despesa. O efetivo pagamento pode estar pendente de assinatura do ordenador de despesa e/ou sujeito a compensação bancária.

![](static/valorpagonoano.jpg)


## Consulta Convênios de Saída

__1. Alterar descrição do campo "Valor Repassado pelo Concedente/Órgão ou Entidade Estadual Parceiro" no glossário interativo__

Alterar a descrição do _tooltip_ da coluna "valor Repassado pelo Concedente/Órgão ou Entidade Estadual Parceiro" da consulta de Convênios/Parcerias Saída de Recursos, que passará a exibir o seguinte texto ao passar o cursor sobre o ponto de interrogação:

  - __Valor Repassado pelo Concedente/Órgão ou Entidade Estadual Parceiro:__ Valor financeiro repassado pelo concedente/órgão ou entidade estadual parceiro ao convenente / Organização da Sociedade Civil (OSC) parceria, referente ao(s) convênios(s)/ parceria(s) firmado(s) entre as partes por meio de pagamento via SIAFI. Abrange o valor do concedente / órgão ou entidade estadual parceiro, das emendas parlamentares e outras fontes. O efetivo pagamento pode estar sujeito a compensação bancária.

![](static/valorrepassadoalter.jpg)


__2. Alterar Formulário de Detalhamento do Convênio__

Para obter o real valor repassado deve-se utilizar a fórmula: (Valor Pago Financeiro - Valor Pago pendente =  Valor repassado) conforme campos do armazém BO.

Campos do Armazém BO:
![](static/valor-repassado-convenio-saida.png)

Exemplos:

Dados disponíveis no Portal de Transparência atualmente:

![](static/valor-repassado-portal.png)

O Portal apresenta como repassado o valor total de R$ 35.000,00 no entanto, conforme consta no SIAFI transacional o valor encontra-se __"pendente para o banco- aguardando assinatura digital"__. Com as novas regras o Portal deve apresentar o valor efetivamente repassado (Valor Pago Financeiro - Valor Pago pendente).

![](static/convenio-op-1547-.png)

__Nome da Consulta Armazém (BO):__ valor_repassado_conv_saida

Na extração dos dados do armazém para a divulgação do Valor Repassado pelo Concedente/Órgão ou Entidade Estadual Parceiro, será considerado para divulgação dos valores repassados o Valor Pago Financeiro menos o Valor Pago Pendente, nas segintes condições:

* Somente serão considerados os pagamentos cuja variável data de pagamento apresente uma data válida. Datas em branco ou datas inválidas não serão mostrados no Portal. Essa informação no Portal deve permanecer zerada até que a data de pagamento apresente uma data válida.

# Exemplos

1. Boa Prática:
O portal da Transparência do Distrito Federal traz a informação de Data de Emissão no lugar de data de pagamento.

![](static/distritofederal.jpg)

2. No Governo do [Paraná](http://www.transparencia.pr.gov.br/pte/pages/despesas/consultaCredor/exibir_extrato.jsf?windowId=8b8), é utilizado a expressão Nº do Documento, no entanto, a visualização das fases é apresentada numa única tela, não deixando dúvidas a que fase da despesa o documento se refere.

![](static/parana.jpg)

3. O [Governo Federal](http://transparencia.gov.br/despesas/favorecido?de=01/09/2019&ate=30/09/2019&funcaoSubfuncao=FN03&funcaoSubfuncao=SB092&programa=2130&acao=2674&programaGoverno=00&grupo=3&elemento=14&modalidade=90&orgaos=UG110581&ordenarPor=valor&direcao=desc) utiliza a expressão Documento, com visualização semelhante a do Paraná, com o número do documento acompanhado da fase a que se refere.

![](static/governofederal.jpg)
