---
title: "Data de Repasse - Consulta Convênio/Parceria de recursos de Saída"
Mantis:
contrato_manutencao: INF 4504
output:
  html_document:
    theme: united
    toc: yes
  word_document:
    toc: yes

---

# Visão geral da Demanda
<a href="#top">(inicio)</a>

Essa demanda visa incluir no formulário de detalhamento da Consulta Convênio/Parceria de Recursos de Saída outras informações denominadas **Execução da Despesa do Convênio/Parceira** que apresente todos os empenhos, liquidações e pagamentos, com as respectivas datas, referentes ao convênio.

# Motivação / contexto da demanda
<a href="#top">(inicio)</a>


# Especificação
<a href="#top">(inicio)</a>

## Formulário de Detalhamento
<a href="#top">(inicio)</a>

Deverá ser acrescido no formulário de detalhamento da Consulta as seguintes informações: **Execução da Despesa do Convênio/Parceria**.

As novas informações deverão ser exibidas logo abaixo do formulário "Alterações do Convênio", conforme exemplo:

![image](https://user-images.githubusercontent.com/53793354/230954817-7d16c263-c55d-46fc-ba24-762f7a4efb42.png)


#### Formulário: Execução da Despesa do Convênio/Parceria

1. As informações deverão ser exibidas a partir do ano de 2007.
2. O 'Valor Total Pago' será representado por: Valor Pago no Exercício + Valores Pagos em Restos a Pagar.
3. Os dados só devem ser exibidos quando houver informação de pagamento, ou seja, caso haja registro do empenho e liquidação e não houver pagamento, a informação não deve ser exibida.


![image](https://user-images.githubusercontent.com/53793354/230952965-b0c27d6a-294a-461e-bc22-ed362060698f.png)


##### Consulta BO - Filtro:

| Armazém BO- SIAFI |Dimensão SIAFI| Filtro |
|-------------------|--------------|--------|
| Contrato Convênio Saída <br> | **- Exercício**<br> Execução Orçamentária da Despesa >> Despesa Realizada >> Dado do Empenho - Despesa<br><br>**- Restos a Pagar**<br>Execução de Restos a Pagar >> Restos a Pagar >> Dados de Restos a Pagar| Usar o número SIAFI para buscar os dados da execução da despesa |  

##### Consulta BO - Campos:

|Campo PDT| Campo SIAFI | Dimensão Armazém | Observação
|---------|-----------------|------|-----------|
|Data de Registro do Empenho | Data Registro Doc Empenho| **- Exercício**<br> Execução Orçamentária da Despesa >> Despesa Realizada >> Dado do Empenho - Despesa<br><br>**- Restos a Pagar**<br>Execução de Restos a Pagar >> Restos a Pagar >> Dados de Restos a Pagar||
|Empenho |Número Empenho|  **- Exercício**<br> Execução Orçamentária da Despesa >> Despesa Realizada >> Dado do Empenho - Despesa<br><br>**- Restos a Pagar**<br>Execução de Restos a Pagar >> Restos a Pagar >> Dados de Restos a Pagar
|Convenente / OSC Parceira |- CNPJ_CPF Credor - Numérico<br> - Razão Social Credor |**- Exercício**<br> Execução Orçamentária da Despesa >> Despesa Realizada >>Credor - Despesa<br><br>**- Restos a Pagar**<br>Execução de Restos a Pagar >> Restos a Pagar >> Credor - Restos a Pagar | Os dados nesse campo deverão ser concatenados
|Data de Registro do Pagamento| Data de Registro|**- Exercício**<br> Execução Orçamentária da Despesa >> Despesa Realizada >> Dados da Ordem de Pagamento - Despesa<br><br>**- Restos a Pagar**<br>Execução de Restos a Pagar >> Restos a Pagar >> Dados da Ordem de Pagamento -  Restos a Pagar |
|Número do Documento de Pagamento |**- Exercício** Número Docto Pagamento<br><br>**- Restos a Pagar**<br> Número Ordem de Pagamento|**- Exercício**<br> Execução Orçamentária da Despesa >> Despesa Realizada >> Dados da Ordem de Pagamento - Despesa<br><br>**- Restos a Pagar**<br>Execução de Restos a Pagar >> Restos a Pagar >> Dados da Ordem de Pagamento -  Restos a Pagar |  |
|Valor Pago |**- Exercício**<br>Valor Pago Financeiro<br><br>**- Restos a Pagar**<br>Valor Pago Processado + Valor Pago Não Processado| **- Exercício**<br> Execução Orçamentária da Despesa >> Despesa Realizada<br><br>**- Restos a Pagar**<br>Execução de Restos a Pagar >> Restos a Pagar| Cada pagamento deverá ser lançado em uma única linha
|Total || |Esse campo será representado pela soma dos valores pagos no exercício mais a soma dos valores pagos em Restos a pagar (Processados e Não Processados)
