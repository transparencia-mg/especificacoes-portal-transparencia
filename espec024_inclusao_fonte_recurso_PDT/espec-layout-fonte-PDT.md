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



## 9. Diárias

### Formulário de Detalhamento
* Favor se atentar para a alteração da ordem dos campos.

  ![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/a45f2aa1-4d54-4d72-88ac-37022840c316)



## 10. Viagens

### Formulário de Detalhamento
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/c575019f-1861-41c4-959f-47cb13e772be)



## 11. Programação e Execução do PPAG por Programa

### Programação Orçamentária e Financeira do Programa
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/6d37ca8d-b839-443c-b6d9-7c57b222fc9d)



### Execução Orçamentária e Financeira do Programa

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/f5b15cac-40b9-48c3-aaa4-3551540285c5)




### Dados Gerais da Ação
![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/ac741339-8065-465f-9a86-d3dc9ad94c58)




## 12. Compras e Contratos

### Nota de Empenho - Formulário de detalhamento do Processo Compra

* Favor se atentar para a alteração da ordem dos campos.

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/728d249a-a8fe-4940-85ed-8b1d86e850e3)



# Tooltip

Nas colunas acrescentadas, deverá aparecer o tooltip ao passar o mouse sobre o Ponto de Interrogação, assim como já ocorre nas demais colunas:

![image](https://user-images.githubusercontent.com/52920939/228567608-4bf89b22-44f7-4814-84e9-204df37b5521.png)

### Tooltip 1: Coluna Fonte de Financiamento - Portaria STN nº 710: 

***Indicam a classificação das fontes ou destinações de recursos utilizados pelos Estados, Distrito Federal e Municípios, conforme previsto na Portaria STN nº 710/2021***

### Tooltip 2: Código da Fonte de Financiamento - Portaria STN nº 710: 

***Indicam o código das fontes ou destinações de recursos utilizados pelos Estados, Distrito Federal e Municípios, conforme previsto na Portaria STN nº 710/2021***



