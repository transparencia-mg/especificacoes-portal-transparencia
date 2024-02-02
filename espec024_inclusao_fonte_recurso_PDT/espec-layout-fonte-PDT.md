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
- Diárias
- Viagens
- Programação e Execução do PPAG por Programa
- Compras e Contratos


# Especificação
<a href="#top">(inicio)</a>

Cabe destacar que os dados deverão sem implementados apenas nas informações disponibilizadas a partir de 2023. As alterações deverão ser aplicadas nas consultas básicas, formulários de detalhamento e pesquisas avançadas. Ou seja, a nova coluna será exibida no PDT a depender do ano selecionado pelo usuário.

Os dados devem ser aplicados apenas a partir de 2023, ou seja, isso reflete na questão de layout também. A coluna fonte de recurso, tanto na pesquisa básica, formulário de detalhamento e pesquisa avançada só devem ser exibidos com dados a partir de 2023.

Caso a informação (coluna) apareça em registros anteriores o usuário pode entender que não existe a informação e que o Portal apresenta um erro.

## 1. Acordo Judicial de Reparação da Vale
<a href="#top">(inicio)</a>

### Pesquisa básica

##### FILTRO : Por Receita

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/48bbb4b1-1d58-432c-b337-7e9b23cf6210)


### Formulário de Detalhamento

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/1c2c90e6-6aff-4adc-898e-0d1e8d90dff6)



### Pesquisa Avançada

##### Barra de Navegação Vertical

* Deverá ser exibido código e descrição conforme padrão adotado no PDT.


![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/e0aaaa68-4631-4b7e-9d1f-aa06c316f15e)


##### Tabela de Resultados

* Quando o usuário selecionar qualquer um dos tipos de fontes de recursos, o PDT deverá exibir as duas colunas na tabela de resultados.

  Por exemplo, caso o usuário marque a opção adicionar "Fonte de Recurso" automaticamente a outra opção "Fonte de Recurso - Portaria STN 710" será selecionada.

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/d9b6b976-2154-4169-be50-aee91a2ff592)


![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/308c315a-d53c-4162-a869-2c8339c98a7e)


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
![image](https://user-images.githubusercontent.com/53793354/228533321-67582029-b38c-4ea9-8a64-eb8092ed8888.png)

## 4. Receita

### Pesquisa básica
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/60c3549b-f894-4f35-82c9-83157b4d1857)


### Pesquisa Avançada

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/db59493c-8b7e-4342-8a41-989c4b15f481)


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

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/d84912e8-66cc-4889-8419-ff10f88da361)


### Pesquisa Avançada
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/21d890c4-1e3a-47cd-974c-524f4927e249)


## 8. Crédito Orçamentário

### Pesquisa básica

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/5ec1f819-dd68-47e9-9a26-db4c9efbfbfd)


### Pesquisa Avançada
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/8e20c547-b2ee-446b-892e-4983f44e10ce)


## 9. Diárias

### Formulário de Detalhamento
* Favor se atentar para a alteração da ordem dos campos.

  ![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/b5e1e1a2-adcc-4841-ae3a-d84fbc7d03c0)


## 10. Viagens

### Formulário de Detalhamento
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/6bece99a-963c-48d3-b077-76447fd52823)


## 11. Programação e Execução do PPAG por Programa

### Programação Orçamentária e Financeira do Programa
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/bda4778f-ca78-45e2-91b8-a6a590cce475)


### Execução Orçamentária e Financeira do Programa

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/183403f7-9cc2-4129-8bf6-edb677eb1d95)



### Dados Gerais da Ação
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/3147168c-9114-4e7c-b8d9-89d141871c02)



## 12. Compras e Contratos

### Nota de Empenho - Formulário de detalhamento do Processo Compra

* Favor se atentar para a alteração da ordem dos campos.

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/526e3bfe-4006-4501-a64d-8a983a17f75c)


# Tooltip

Nas colunas acrescentadas, deverá aparecer o tooltip ao passar o mouse sobre o Ponto de Interrogação, assim como já ocorre nas demais colunas:

![image](https://user-images.githubusercontent.com/52920939/228567608-4bf89b22-44f7-4814-84e9-204df37b5521.png)

### Tooltip 1: Coluna Fonte de Financiamento - Portaria STN nº 710: 

***Indicam a classificação das fontes ou destinações de recursos utilizados pelos Estados, Distrito Federal e Municípios, conforme previsto na Portaria STN nº 710/2021***

### Tooltip 2: Código da Fonte de Financiamento - Portaria STN nº 710: 

***Indicam o código das fontes ou destinações de recursos utilizados pelos Estados, Distrito Federal e Municípios, conforme previsto na Portaria STN nº 710/2021***



