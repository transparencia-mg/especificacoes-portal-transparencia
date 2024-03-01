---
contrato_manutencao: INFº 4504
mantis: 0171436
titulo: Inclusão da coluna Fonte de Recurso conforme Portaria STN
output:
  html_document:
    theme: united
    toc: yes
  pdf_document:
    toc: yes
---
# Alteração da Espefificação conforme reunião do dia 29/02/2024
> 
> Conforme acordado em reunião de alinhamento realizada em 29/02/24 entre a SEPLAG, a CGE e a PRODEMGE, encaminho-lhes para registro e formalização os seguintes pontos:
> 1. Remoção da Informação da Fonte de Recurso STN: A informação da Fonte de Recurso STN será removida das seguintes consultas:
>
> Diárias
> Viagens
> PPAG
> Compras e Contratos
> 
> 2. Atualização diária com carga completa: As seguintes consultas serão atualizadas diariamente com a carga completa, incluindo dados desde janeiro de 2023:
> Despesa
> Restos a Pagar
> Receita
> Proposta Orçamentária
> Emendas Orçamentárias
> Alteração Orçamentária
> Crédito Orçamentário
> 
> 3. Atualização incremental da consulta do Acordo Judicial da Vale: A consulta do Acordo Judicial da Vale será atualizada diariamente com carga incremental.
> Conforme informado pela SEPLAG a Fonte de Recurso 95 sempre será a 899.

# Visão geral da demanda
<a href="#top">(inicio)</a>

Inclusão de uma nova coluna denominada 'Fonte de Recurso - Portaria STN nº 710' em todas as consultas do Portal de Transparência - PDT que possuem a informação Fonte de Recurso. A alteração será implementada nas consultas básicas, formulários de detalhamento e pesquisas avançadas.

# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

Foi solicitado, pela SEPLAG, a inclusão de uma nova coluna no Portal da Transparência que apresentasse a descrição/código das novas fontes de recursos para atender o disposto na Portaria STN nº 710/2021 do Governo Federal.

Abaixo seguem as 12 consultas impactadas pela alteração:
- Receita
- Despesa
- Restos a pagar
- Acordo Judicial da Vale
- Proposta Orçamentária
- Emenda Orçamentária
- Alteração Orçamentária
- Crédito Orçamentário

# Especificação
<a href="#top">(inicio)</a>

Cabe destacar que os dados deverão sem implementados apenas nas informações disponibilizadas a partir de 2023. As alterações deverão ser aplicadas nas consultas básicas, formulários de detalhamento e pesquisas avançadas. Ou seja, a nova coluna será exibida no PDT a depender do ano selecionado pelo usuário.

Os dados devem ser aplicados apenas a partir de 2023, ou seja, isso reflete na questão de layout também. A coluna fonte de recurso, tanto na pesquisa básica, formulário de detalhamento e pesquisa avançada só devem ser exibidos com dados a partir de 2023.

Caso a informação (coluna) apareça em registros anteriores o usuário pode entender que não existe a informação e que o Portal apresenta um erro.

## Atualização da Consulta

 A atualização deverá ser diária com carga completa em todas as consultas com exceção da consulta Acordo Judicial da Vale
 
 - Carga completa - atualização diária incluindo dados desde janeiro de 2023: Todas as consultas
 - Carga incremental - atualização diária - Acordo Judicial da Vale

## 1. Acordo Judicial de Reparação da Vale
<a href="#top">(inicio)</a>

### Pesquisa básica

##### FILTRO : Por Receita

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/48bbb4b1-1d58-432c-b337-7e9b23cf6210)


### Formulário de Detalhamento

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/1c2c90e6-6aff-4adc-898e-0d1e8d90dff6)


## 2. Despesa

### Pesquisa básica - Favorecido

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/9ba8bf49-b943-464d-86c9-57a6aa295666)


### Formulário de Detalhamento

* Favor se atentar para a alteração da ordem dos campos.

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/d3077033-a413-4002-9745-14f28b461222)


### Pesquisa Avançada
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/3cf44322-49b9-4da5-b23e-6d56d3b3a2c3)



## 3. Restos a Pagar

### Pesquisa básica
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/5c89c82f-175b-4a23-b679-03c0bb51a07c)


### Formulário de Detalhamento

* Favor se atentar para a alteração da ordem dos campos.

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/ebdae4ea-cee5-41b0-9f7d-e4a132564e77)


### Pesquisa Avançada
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/ed2e2205-91d0-4f8f-8e9b-21bb6329699c)


## 4. Receita

### Pesquisa básica
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/60a3445b-22cc-4658-9a51-b07392e764b1)



### Pesquisa Avançada

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/1f11f889-8880-4e98-b232-9b269f49630d)


## 5. Proposta Orçamentária

### Pesquisa básica
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/bddeced6-08c0-4742-a29f-e2ae527474d5)


### Pesquisa Avançada
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/d4722a8f-235d-48df-bbea-c9f6f305935d)


## 6. Emenda Orçamentária

### Pesquisa básica

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/c1efb674-c61c-4b55-9ef9-b3fed8c910f6)

## 7. Alteração Orçamentária

### Pesquisa básica

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/e943f751-5b07-44e8-b1d6-1de2abd63cb8)


### Formulário de Detalhamento
* Favor se atentar para a alteração da ordem dos campos.

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/bc46898d-2d8c-4243-b028-4344c2633ec7)



### Pesquisa Avançada
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/da4e7245-64f1-4aa7-bda4-8970b5d09be7)

## 8. Crédito Orçamentário

### Pesquisa básica

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/cc18c49b-b96e-4256-b5d5-b8cc9c68ac08)


### Pesquisa Avançada
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/89b53eda-671d-4f6d-a42d-d988bc67e78a)


# Tooltip

Nas colunas acrescentadas, deverá aparecer o tooltip ao passar o mouse sobre o Ponto de Interrogação, assim como já ocorre nas demais colunas:

![image](https://user-images.githubusercontent.com/52920939/228567608-4bf89b22-44f7-4814-84e9-204df37b5521.png)

### Tooltip 1: Coluna Fonte de Financiamento - Portaria STN nº 710: 

***Indicam a classificação das fontes ou destinações de recursos utilizados pelos Estados, Distrito Federal e Municípios, conforme previsto na Portaria STN nº 710/2021***

### Tooltip 2: Código da Fonte de Financiamento - Portaria STN nº 710: 

***Indicam o código das fontes ou destinações de recursos utilizados pelos Estados, Distrito Federal e Municípios, conforme previsto na Portaria STN nº 710/2021***



