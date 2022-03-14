---
contrato_manutencao: nº 15210010062019 (INF. 3951)
proposta_comercial:
mantis:
pull_request: '[]()'
titulo: Correção "valor a pagar" da consulta de Restos a Pagar
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da demanda
<a href="#top">(inicio)</a>

Atualmente a informação da coluna “Valor a pagar” da consulta do Portal de Transparência é construída através do cálculo:
Valor Inscrito Processado + Valor Inscrito Não Processado – Valor Pago no Ano, porém quando ocorre retenções a soma não reflete o valor correto do saldo a pagar na consulta de restos a pagar.

Com o objetivo de corrigir essa inconsistência no Portal, o correto é que a coluna “Valor a pagar” extraia as informações diretamente do Armazém SIAFI e que os valores retidos também sejam exibidos na consulta de restos a pagar para melhor compreensão do usuário.


# Homologação - LAYOUT
<a href="#top">(inicio)</a>

## Consulta Restos a pagar

#### ITENS PARA CORREÇÃO

**14- Incluir a coluna "Valor Retido" - consulta avançada** - **CORRIGIR**

**Não foi localizada a coluna Valor Retido na consulta avançada.**

![](static/consulta-avancada.png)



#### ITENS APROVADOS

**1- Incluir a coluna "Valor Retido" - tela inicial** - **OK**

![](static/tela-inicial.png)


**2- Incluir a coluna "Valor Retido" - consulta por órgão** - **OK**

![](static/orgao.png)


**3- Incluir a coluna "Valor Retido" - consulta por órgão - elemento** - **OK**

![](static/orgao-elemento.png)


**4- Incluir a coluna "Valor Retido" - consulta por órgão - elemento item** - **OK**

![](static/orgao-elemento-item.png)


**5- Incluir a coluna "Valor Retido" - consulta por órgão - elemento item - empenho** - **OK**

![](static/orgao-elementoitemempenho.png)


**6- Incluir a coluna "Valor Retido" - consulta por favorecido** - **OK**

![](static/favorecido.png)


**7- Incluir a coluna "Valor Retido" - consulta por Favorecido - elemento** - **OK**

![](static/favorecido-elemento.png)


**8- Incluir a coluna "Valor Retido" - consulta por Favorecido - elemento item** - **OK**

![](static/favorecido-elementoitem.png)


**9- Incluir a coluna "Valor Retido" - consulta por Favorecido - elemento item - órgão** - **OK**

![](static/favorecido-elementoitemorgao.png)


**10- Incluir a coluna "Valor Retido" - consulta por Favorecido - elemento item - órgão documento** - **OK**

![](static/favorecido-elementoitemorgaodocumento.png)





