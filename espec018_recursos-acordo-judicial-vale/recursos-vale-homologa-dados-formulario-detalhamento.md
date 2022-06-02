---
contrato_manutencao: nº 15210010062019 (INF. 3951)
proposta_comercial: null
mantis: null
pull_request: '[]()'
titulo: Transparência dos recursos da Vale - Acordo Judicial 04/02/2021
output:
  html_document:
    theme: united
    toc: yes
  word_document:
    toc: yes
---

# Homologação dos dados da consulta - CONSULTA DE EXECUÇÃO + FORMULÁRIO DE DETALHAMENTO
<a href="#top">(inicio)</a>

<div class="alert alert-warning">

## CONSULTA PRO EXECUÇÃO
<a href="#top">(inicio)</a>

### Nível 1 - filtro 01/01/2021 a 31/12/2021 - OK
  
![image](https://user-images.githubusercontent.com/52920939/171457542-4c79b225-7063-4885-a55e-8c0fc4617a20.png)
  
### Nível 2 - filtro 01/01/2022 a 31/12/2022 - erro de valores em alguns projetos 
  Foram identificadas diferenças nos projetos de nº:
  
    - 9288133 (valor liquidado em restos a pagar)
  
    - 9288152 (valor da despesa liquidada e valor pago)
  
    - 9288191 (valor despesa liquidada em restos a pagar)

![image](https://user-images.githubusercontent.com/52920939/171651361-01c8b636-72d3-4c05-abff-5f910f34cb12.png)

 
### FORMULÁRIO DE DETALHAMENTO
### 1. Classificação Orçamentária - OK

### 2. Empenho - OK

### 3. Liquidação - OK
  
### 4. Pagamento - OK
  
### 5. Outras informações - OK
  
### FORMULÁRIO DE DETALHAMENTO - EXEMPLO EMPENHO 147 - PROJETO 9288134
  
#### CORREÇÃO 1 - 

Os empenhos que possuem pagamentos em mais de um ano devem ser visualizados os valores separados por ano.

Duplicando as linhas de acordo com a quantidade de ano daquele empenho.
  
  
Empenho 147 - Ano 2021 e 2022
  
Aparece uma linha só para ambos os anos
  
![image](https://user-images.githubusercontent.com/52920939/171652349-c8dd6943-cb7e-4047-a2f5-30654416b032.png)
  
#### Correção 2
  
Ao selecionar o fitlro de período 01/01/2021 e 31/12/2022, deve ser incluída uma coluna **ANO** depois do número do código do projeto para que o usuário identifique a qual ano se refere os pagamentos.
  
![image](https://user-images.githubusercontent.com/52920939/171651970-4fd94aa7-878f-47e6-86ab-73c0c4e7fc13.png)

#### Correção 3
  
Ao selecionar o fitlro de período 01/01/2021 e 31/12/2022, deve ser incluída uma coluna **ANO** depois do empenho para que o usuário identifique a qual ano se refere os pagamentos.

![image](https://user-images.githubusercontent.com/52920939/171653312-f29d3d82-ae18-4550-86ab-4fa381b2d5a7.png)


