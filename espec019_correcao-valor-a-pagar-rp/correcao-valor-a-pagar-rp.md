---
contrato_manutencao: nº 15210010062019 (INF. 395)
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




# Motivação / contexto da demanda
<a href="#top">(inicio)</a>



# Especificação
<a href="#top">(inicio)</a>

## Consulta Restos a pagar

**1- Incluir a coluna "Valor Retido"**

| Campo SIAFI| Universo| Campo PdT | Tooltip |
|---|---|-|--|
| Valor Liquidado Retido |  SIAFI > Execução de Restos a Pagar > Restos a Pagar | Valor Retido| Valor em reais referente às retenções (parte da liquidação a favor de terceiros).

**2- Alterar a fórmula de cálculo da coluna "Valor a Pagar"**




|Campo PdT| Campo SIAFI|Universo| Fórmula|
|---|---|-|--|
| Valor a Pagar | - Saldo Restos a Pagar   Processado<br>  - Saldo Restos a Pagar não Processado | | Somar os valores das Colunas 'saldo Restos a Pagar   Processado' e 'Saldo Restos a Pagar não Processado'


**3- Resultado Portal de Transparência"**
