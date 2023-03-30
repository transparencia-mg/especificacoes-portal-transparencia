# Especificação de dados

Os dados dessa consulta serão extraídos dos Universos BO SIAFI, BO SIAD - Módulo Compras e SIGCON Saída:

- Armazém BO / ~tmp /novas Especificações / nova-espec-despesa

## Campos PDT x Campo Armazém BO

A consulta será anual, ou seja, o usuário irá visualizar a execução da Dívida Pública conforme o período selecionado.


| Armazém BO- SIAFI |Dimensão SIAFI| Filtro |
|----|----------|------------|
| Ano de exercício<br> |Período Contábil| Usar o período desejado |  



|Campo PDT| Campo Armazém BO |Dimensão Armazém | Observação
|---------|------------------|------|---|
|Ano |Ano de exercício| SIAFI -Período Contábil| Pesquisa básica
|Ano de exercício |Ano de exercício| SIAFI -Período Contábil| Formulário de detalhamento|
|Ação| Projeto Atividade - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa
|Código Elemento de Despesa| Elemento de Despesa - Código |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada|
|Código Item de Despesa| item de Despesa - Código |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada|
|Código Órgão| Unidade Orçamentária - Código  |SIAFI - Unidade Orçamentária|
|CPF/CNPJ| CNPJ_CPF credor numérico| SIAFI- Execução Orçamentária da Despesa >> Despesa Realizada >> Credor - Despesa
|Código da Função| Função - Código |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa|
|Código Subfunção| Subfunção - Código |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa |
|Código Programa| Programa - Código |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa |
|Código Ação| Projeto Atividade - Código |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa |
|Código Categoria Econômica| Categoria Econômica Despesa - Código| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada
|Código Grupo de Despesa| Grupo de Despesa - Código| SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada
|Código Identificador de Procedência e uso| Procedência - Código| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
|Código Modalidade de Aplicação| Modalidade de Aplicação - Código| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
|Código Fonte de Recurso| Fonte de Recurso - Código |Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
|Código Fonte de Recurso - Portaria STN nº710|Fonte_STN_COD| Matriz de Correspondência - Portal de Dados Abertos
|Categoria Econômica| Categoria Econômica Despesa -Descrição| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada
|Data de registro do empenho| Data Registro Doc Empenho| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Dados do Empenho - Despesa
|Elemento de despesa| Elemento de Despesa - Descrição  |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada|
|Empenho| Número Empenho |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Dados do Empenho - Despesa|
|Favorecido| Razão Social Credor  |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Credor - Despesa|
|Função| Função - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
|Fonte de Recurso| Fonte de Recurso - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
|Fonte de Recurso - Portaria STN nº 710| Descrição| Matriz de Correspondência (fonte_stn)- Portal de Dados Abertos
|Grupo de Despesa| Grupo de Despesa - Descrição| SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada
|Item de despesa| Item de Despesa - Descrição  |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada|
|Identificador de Procedência e uso| Procedência - Descrição| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
|Modalidade de Aplicação| Modalidade de Aplicação - Descrição| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
|Órgão| Unidade Orçamentária - Nome  |SIAFI - Unidade Orçamentária|
|Programa |Programa - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa
|Subfunção |Subfunção - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa
|Unidade Executora| Unidade Executora - nome | SIAFI - Unidade Executora
|Tipo de Empenho |Tipo Empenho  - Descrição| SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Dados do Empenho - Despesa
|Valor inicial da despesa empenhada| valor inicial Empenho| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada| Apenas no formulário de detalhamento
|Valor Atual do Empenho| Valor Despesa Empenhada| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada |Apenas no formulário de detalhamento
| Valor Empenhado | Valor Despesa Empenhada  |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada  |
| Valor Liquidado | Valor Despesa Liquidada  |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada  |
| Valor Pago | Valor Pago Financeiro  |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada |
| Valor Pago em Restos a Pagar | Valor Pago processado + Valor pago não processado  |SIAFI - Execução de Restos a pagar >> Restos a pagar |Essa coluna é representada pela soma das  Valor Pago processado + Valor pago não processado


Parei na Descrição do empenho


















### Pesquisa Avançada

***1º nível:***

* Detalhar
* Valor Empenhado
* valor Liquidado
* Valo Pago
* Valor Pago em restos a Pagar

***2º nível:*** Essa tabela não será modal

* Empenho
* Data de registro do empenho
* Unidade orçamentária
* Unidade Executora
* Favorecido
* CPF/CNPJ do Favorecido
* Valor Empenhado
* valor Liquidado
* Valo Pago
* Valor Pago em restos a Pagar

* O usuário poderá clicar no número do empenho para exibir o formulário de detalhamento relacionado ao empenho.
* Exceção: Quando o usuário utilizar o filtro ***"Número da Ordem de Pagamento"*** na barra de filtro vertical as colunas abaixo deverão ser exibidas em formato desabilitado, sem a exibição de dados: Valor empenhado e Valor liquidado.
* Caso o filtro "Número da Ordem de Pagamento seja retirado da barra de filtros aplicados a formatação e exibição dos valores dessas colunas seguirá o padrão.
















| Armazém BO- SIAFI |Dimensão SIAFI| Filtro |
|----|----------|------------|
| Ano de exercício<br> |Período Contábil| Usar o período desejado |  

### Consulta por Órgão
_______
  1º nível - [Órgão]()<br>
  2º nível - Órgão > [Elemento]()<br>
  3º nível - Órgão > Elemento > [Favorecido]()<br>
  4º nível - Órgão > Elemento > Favorecido > [Empenho]()<br>
  5º nível - Órgão > Elemento > Favorecido > Empenho > [Formulário de Detalhamento]()<br>
___________

##### 1º NÍVEL

![image](https://user-images.githubusercontent.com/53793354/200358592-fd3046ee-1c02-4cfc-b320-93a0bc1990bc.png)

#### Campos da Tabela

|Campo PDT| Campo Armazém BO |Dimensão Armazém BO SIAFI| Observação
|---------|------------------|------|---|
| [Órgão]()| Unidade Orçamentária - Nome  |SIAFI - Unidade Orçamentária|
 Código Órgão| Unidade Orçamentária - Código  |SIAFI - Unidade Orçamentária|
| Valor Empenhado | Valor Despesa Empenhada  |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada  |
| Valor Liquidado | Valor Despesa Liquidada  |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada  |
| Valor Pago | Valor Pago Financeiro  |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada |
| Valor Pago em Restos a Pagar | Valor Pago processado + Valor pago não processado  |SIAFI - Execução de Restos a pagar >> Restos a pagar |Essa coluna é representada pela soma das  Valor Pago processado + Valor pago não processado

##### 2º NÍVEL

![image](https://user-images.githubusercontent.com/53793354/200359119-2bc8ec40-da77-40d5-b455-fbc7092aaf0c.png)

#### Campos da Tabela

|Campo PDT| Campo Armazém BO |Dimensão Armazém BO SIAFI|
|---------|------------------|------
| [Elemento]()| Elemento de Despesa - Descrição  |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Natureza da Despesa Realizada|
| ***Os campos referente a valores serão os mesmos do 1º nível***

##### 3º NÍVEL
  - [Favorecido]() -> ao clicar o usuário será direcionado para o 4º nível
  - CPF / CNPJ
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![](static/tabela_3_favorecido_orgão.png)

|Campo PDT| Campo Armazém BO |Dimensão Armazém BO SIAFI|
|---------|------------------|------
| [Favorecido]()|Razão Social Credor  |SIAFI -Execução Orçamentária da Despesa >> Despesa Realizada >> Credor - Despesa|
|CPF/CNPJ| CNPJ_CPF credor numérico| SIAFI- Execução Orçamentária da Despesa >> Despesa Realizada >> Credor - Despesa
| ***Os campos referente a valores serão os mesmos do 1º nível***

##### 4º NÍVEL
  - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento
  - Data de registro do Empenho
  - Unidade Executora
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/222240159-6b60cd86-8482-47e4-9055-0547efd02acb.png)

|Campo PDT| Campo Armazém BO |Dimensão Armazém BO SIAFI|
|---------|------------------|------
| [Empenho]()| Número Empenho |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Dados do Empenho - Despesa|
|Data de registro do empenho| Data Registro Doc Empenho| SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Dados do Empenho - Despesa
|Unidade Executora| Unidade Executora - nome | SIAFI - Unidade Executora
| ***Os campos referente a valores serão os mesmos do 1º nível***

##### 5º NÍVEL

 - Formulário de Detalhamento

Ao clicar no número do empenho o usuário será direcionado para o formulário de detalhamento, que será composto pelos seguintes atributos:
  * As tabelas que compõe o formulário de detalhamento serão exibidas em formato de guias
  * O usuário poderá fazer o Download das informações do formulário de detalhamento ao clicar no botão 'Download'.
````
O usuário poderá fazer o Download das informações do formulário de detalhamento ao clicar no botão 'Download'. A exportação em planilha (CSV) deverá ser em formato de tabela. Cada campo em uma coluna.
``````

###### Campos do formulário de detalhamento

* Classificação Orçamentária



* Empenho



* Liquidação

 ![image](https://user-images.githubusercontent.com/52920939/220975288-35fbd2c2-85bf-4976-bd6e-d3ea955d1ada.png)

* Pagamento

 ![image](https://user-images.githubusercontent.com/52920939/220975331-2532a423-f6b6-4bd1-8ecb-39dab9428796.png)

* Outras Informações

  ![image](https://user-images.githubusercontent.com/52920939/220975555-95c2866f-2523-4f99-a3de-1a907992d56d.png)

### CONSULTA POR FUNÇÃO
<a href="#top">(inicio)</a>

______
  1º nível - [Função]()<br>
  2º nível - Função > [Subfunção]()<br>
  3º nível - Função > Subfunção > [Favorecido]()<br>
  4º nível - Função > Subfunção > Favorecido > [Empenho]()<br>
  5º nível - Função > Subfunção > Favorecido > Empenho > [Formulário de Detalhamento]()<br>
___________

##### 1º NÍVEL
  - Código da Função
  - [Função]() -> ao clicar o usuário será direcionado para o 2º nível
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/200358699-3acd5a01-9948-437c-96b6-fa2f06726f5a.png)

|Campo PDT| Campo Armazém BO |Dimensão Armazém BO SIAFI|
|---------|------------------|------
|Código da Função| Função - Código |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa|
|[Função]()|Função - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> GMIFP - Despesa
|***Os campos referente a valores serão os mesmos do 1º nível da consulta por Órgão***

##### 2º NÍVEL
  - Código do Subfunção
  - [Subfunção]() -> ao clicar o usuário será direcionado para o 3º nível
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/200358762-207b6b03-df53-471b-be0a-dd07e358c58f.png)

|Campo PDT| Campo Armazém BO |Dimensão Armazém BO SIAFI|
|---------|------------------|------
|Código Subfunção| Subfunção - Código |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa |
|[Subfunção]()|Subfunção - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa
|***Os campos referente a valores serão os mesmos do 1º nível da consulta por Órgão***


##### 3º NÍVEL

  - [Favorecido]() -> ao clicar o usuário será direcionado para o 4º nível
  - CPF / CNPJ
  - Código do Órgão -> Apenas quando o usuário clicar em *'Exibir/Ocultar Código'*)
  - Órgão
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![](static/favorecido-orgao.png)

***OS CAMPOS SERÃO OS MESMOS DA CONSULTA POR ÓRGÃO***

##### 4º NÍVEL
  - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento
  - Data de registro do Empenho
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/225976859-3d1378d1-9134-40ae-b6c4-1accc71b130a.png)

***OS CAMPOS SERÃO OS MESMOS DA CONSULTA POR ÓRGÃO***

##### 5º NÍVEL

- Formulário de Detalhamento

***OS CAMPOS SERÃO OS MESMOS DA CONSULTA POR ÓRGÃO***

### CONSULTA POR PROGRAMA
<a href="#top">(inicio)</a>
______
  1º nível - [Programa]()<br>
  2º nível - Programa > [Ação]()<br>
  3º nível - Programa > Ação > [Favorecido]()<br>
  4º nível - Programa > Ação > Favorecido > [Empenho]() ><br>
  5º nível - Programa > Ação > Favorecido > Empenho > Formulário de Detalhamento<br>
___________

##### 1º NÍVEL
  - Código da Programa
  - [Programa]() -> ao clicar o usuário será direcionado para o 2º nível
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/200358865-cd1aee56-75a1-42c9-aa95-fafcda4db320.png)

|Campo PDT| Campo Armazém BO |Dimensão Armazém BO SIAFI|
|---------|------------------|------
|Código Programa| Programa - Código |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa |
|[Programa]()|Programa - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa
|***Os campos referente a valores serão os mesmos do 1º nível da consulta por Órgão***


##### 2º NÍVEL
  - Código do Ação
  - [Ação]() -> ao clicar o usuário será direcionado para o 3º nível
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/200358964-74159e14-a951-4c49-b6a0-4bd377975681.png)

|Campo PDT| Campo Armazém BO |Dimensão Armazém BO SIAFI|
|---------|------------------|------
|Código Ação| Projeto Atividade - Código |SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa |
|[Ação]()|Projeto Atividade - Descrição | SIAFI - Execução Orçamentária da Despesa >> Despesa Realizada >> Programa de Trabalho - Despesa
|***Os campos referente a valores serão os mesmos do 1º nível da consulta por Órgão***

##### 3º NÍVEL
  - [Favorecido]() -> ao clicar o usuário será direcionado para o 4º nível
  - CPF / CNPJ
  - Código do Órgão -> Apenas quando o usuário clicar em *'Exibir/Ocultar Código'*)
  - Órgão
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![](static/favorecido-orgao.png)

***OS CAMPOS SERÃO OS MESMOS DA CONSULTA POR ÓRGÃO***


##### 4º NÍVEL
  - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento
  - Data de registro do Empenho
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/225976711-22009c8c-796d-46bd-aae3-626578119991.png)

***OS CAMPOS SERÃO OS MESMOS DA CONSULTA POR ÓRGÃO***

##### 5º NÍVEL

- Formulário de Detalhamento

***OS CAMPOS SERÃO OS MESMOS DA CONSULTA POR ÓRGÃO***


### CONSULTA POR FAVORECIDO (NOME E CPF/CNPJ)
<a href="#top">(inicio)</a>

_______
  1º nível - [Favorecido]()<br>
  2º nível - Favorecido > [Empenho]()<br>
  3º nível - Favorecido > Empenho > Formulário de Detalhamento<br>
___________

##### 1º NÍVEL

- [Favorecido]() -> ao clicar o usuário será direcionado para o 4º nível
- CPF / CNPJ
- Valor Empenhado
- Valor Liquidado
- Valor Pago
- Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/228915058-9da50a39-f7e5-41a2-8471-72ea369b32ca.png)

***OS CAMPOS SERÃO OS MESMOS DA CONSULTA POR ÓRGÃO***

##### 2º NÍVEL
  - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento
  - Data de registro do Empenho
  - Código do Órgão -> Apenas quando o usuário clicar em *'Exibir/Ocultar Código'*)
  - Órgão
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/228915644-9b4db1ef-4db0-4d27-9540-254f95e12e22.png)

***OS CAMPOS SERÃO OS MESMOS DA CONSULTA POR ÓRGÃO***

##### 3º NÍVEL

- Formulário de Detalhamento


### Pesquisa Avançada

***1º nível:***

* Detalhar
* Valor Empenhado
* valor Liquidado
* Valo Pago
* Valor Pago em restos a Pagar

***2º nível:*** Essa tabela não será modal

* Empenho
* Data de registro do empenho
* Unidade orçamentária
* Unidade Executora
* Favorecido
* CPF/CNPJ do Favorecido
* Valor Empenhado
* valor Liquidado
* Valo Pago
* Valor Pago em restos a Pagar

* O usuário poderá clicar no número do empenho para exibir o formulário de detalhamento relacionado ao empenho.
* Exceção: Quando o usuário utilizar o filtro ***"Número da Ordem de Pagamento"*** na barra de filtro vertical as colunas abaixo deverão ser exibidas em formato desabilitado, sem a exibição de dados: Valor empenhado e Valor liquidado.
* Caso o filtro "Número da Ordem de Pagamento seja retirado da barra de filtros aplicados a formatação e exibição dos valores dessas colunas seguirá o padrão.
