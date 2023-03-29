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

Inclusão de uma nova coluna denominada 'Fonte de Recurso - Portaria STN nº 710' em todas as consultas do Portal de Transparência que possuem a informação Fonte de Recurso. A alteração será implementada nas consultas básicas, formulários de detalhamentos e pesquisas avançadas.

# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

Foi solicitado pela SEPLAG a inclusão de uma nova coluna no Portal de Transparência que representasse a descrição/código das novas fontes de recursos para atender o disposto na Portaria STN nº 710/2021 do Governo Federal.

Abaixo segue as 12 consultas impactadas pela alteração:
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

Cabe destacar que os dados deverão sem implementados apenas nas informações disponibilizadas a partir de 2023. As alterações deverão ser aplicadas nas consultas básicas, formulários de detalhamentos e pesquisas avançadas.

## 1. Acordo Judicial de Reparação da Vale
<a href="#top">(inicio)</a>

### Pesquisa básica

##### FILTRO : Por Receita

![image](https://user-images.githubusercontent.com/53793354/228531669-a563c655-67f1-46ec-a34a-ee086c95523d.png)

### Formulário de Detalhamento

![image](https://user-images.githubusercontent.com/53793354/228533056-d84cea10-668f-4e47-88f6-3ba0cdc04e85.png)


### Pesquisa Avançada

##### Barra de Navegação Vertical

* Deverá ser exibido código e descrição conforme padrão adotado no PDT.


![image](https://user-images.githubusercontent.com/53793354/228532348-21f2d57f-fa8b-4eee-8aa0-642011e92a99.png)

##### Tabela de Resultados

* Quando o usuário selecionar qualquer um dos tipos de fontes de recursos, o PDT deverá exibir as duas colunas na tabela de resultados.

  Por exemplo, caso o usuário marque a opção adicionar "Fonte de Recurso" automaticamente a outra opção "Fonte de Recurso - Portaria STN 710" será selecionada.

![image](https://user-images.githubusercontent.com/53793354/228558868-f4e7bb64-f9a9-48c1-8d24-4eda219d7156.png)


![image](https://user-images.githubusercontent.com/53793354/228532231-14fa5421-6779-4172-89c7-84d73219e363.png)

## 2. Despesa

### Pesquisa básica

![image](https://user-images.githubusercontent.com/53793354/228532796-9dc2850b-ed0d-494a-b282-67b4b680ca33.png)

### Formulário de Detalhamento

* Favor se atentar para a alteração da ordem dos campos.

![image](https://user-images.githubusercontent.com/53793354/228533216-4f2603c8-7a85-45cd-bd53-c01796abd065.png)

### Pesquisa Avançada
![image](https://user-images.githubusercontent.com/53793354/228533321-67582029-b38c-4ea9-8a64-eb8092ed8888.png)


## 3. Restos a Pagar

### Pesquisa básica
![image](https://user-images.githubusercontent.com/53793354/228533582-ee9cd4b4-a3cb-49f8-83e4-f4c823b4c65b.png)


### Formulário de Detalhamento

* Favor se atentar para a alteração da ordem dos campos.

![image](https://user-images.githubusercontent.com/53793354/228533512-58ae1c36-a3db-4914-8912-480144b29d86.png)

### Pesquisa Avançada
![image](https://user-images.githubusercontent.com/53793354/228533321-67582029-b38c-4ea9-8a64-eb8092ed8888.png)

## 4. Receita

### Pesquisa básica
![image](https://user-images.githubusercontent.com/53793354/228533791-e6718110-401e-42c7-987c-3de02249033c.png)

### Pesquisa Avançada

![image](https://user-images.githubusercontent.com/53793354/228533717-c75b402b-9d13-47dc-ae63-3daa8107d06b.png)


## 5. Proposta Orçamentária

### Pesquisa básica
![image](https://user-images.githubusercontent.com/53793354/228534157-cad938e6-8048-4ca6-8b64-608326389f65.png)

### Pesquisa Avançada
![image](https://user-images.githubusercontent.com/53793354/228534110-6fb9e567-29cc-4398-ab12-7f6bff87a28c.png)



## 6. Emenda Orçamentária

### Pesquisa básica

![image](https://user-images.githubusercontent.com/53793354/228534304-6986301f-3222-4b7c-80bd-430021943d50.png)


## 7. Alteração Orçamentária

### Pesquisa básica

![image](https://user-images.githubusercontent.com/53793354/228534938-e4c56878-4e85-43d6-8be2-31377d1db196.png)

### Formulário de Detalhamento
* Favor se atentar para a alteração da ordem dos campos.

![image](https://user-images.githubusercontent.com/53793354/228534886-f1584c29-f366-4648-9703-b05daf846e6d.png)

### Pesquisa Avançada
![image](https://user-images.githubusercontent.com/53793354/228534484-873ca691-fc41-4483-b48e-0ad09b9ee484.png)


## 8. Crédito Orçamentário

### Pesquisa básica

![image](https://user-images.githubusercontent.com/53793354/228535152-3cc49e7d-9820-4df4-ba74-1e369ff8cc3a.png)


### Pesquisa Avançada
![image](https://user-images.githubusercontent.com/53793354/228535066-d76c99c6-da02-4bb1-a388-0e1e7e094c59.png)

## 9. Diárias

### Formulário de Detalhamento
* Favor se atentar para a alteração da ordem dos campos.

![image](https://user-images.githubusercontent.com/53793354/228535354-02a48d14-abef-45f8-a6af-1aa17fd38f76.png)

### Pesquisa Avançada
![image](https://user-images.githubusercontent.com/53793354/228535458-9272de51-4a93-4886-ab94-52013f9a460f.png)


## 10. Viagens

### Formulário de Detalhamento
![image](https://user-images.githubusercontent.com/53793354/228535536-9a39f046-6c80-48a4-9193-52de65e1cb1c.png)


## 11. Programação e Execução do PPAG por Programa

### Programação Orçamentária e Financeira do Programa
![image](https://user-images.githubusercontent.com/53793354/228548823-d6c2459b-8fda-4fdb-9a43-c1b174016ebb.png)

### Execução Orçamentária e Financeira do Programa

![image](https://user-images.githubusercontent.com/53793354/228545971-088c1ee3-3983-4a80-8ac0-1e55efd97a25.png)


### Dados Gerais da Ação
![image](https://user-images.githubusercontent.com/53793354/228550183-6acf8c0c-e7e0-4d0c-90da-c89deefbd835.png)


## 12. Compras e Contratos

### Nota de Empenho - Formulário de detalhamento do Processo Compra

* Favor se atentar para a alteração da ordem dos campos.

![image](https://user-images.githubusercontent.com/53793354/228559021-5660dab6-98b1-4a0e-aebd-46dae96b6914.png)

