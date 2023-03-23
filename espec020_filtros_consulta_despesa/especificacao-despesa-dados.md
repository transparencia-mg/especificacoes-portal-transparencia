# Especificação de dados

Os dados dessa consulta serão extraídos dos Universos BO SIAFI, BO SIAD - Módulo Compras e SIGCON Saída:
- Armazém BO / Pastas públicas - SIAFI > SUPORTE- SIAFI > CGE >

## Filtros da Consulta

### Consulta por Órgão

_______
  1º nível - [Órgão]()<br>
  2º nível - Órgão > [Elemento]()<br>
  3º nível - Órgão > Elemento > [Favorecido]()<br>
  4º nível - Órgão > Elemento > Favorecido > [Empenho]()<br>
  5º nível - Órgão > Elemento > Favorecido > Empenho > [Formulário de Detalhamento]()<br>
___________
A consulta será anual, ou seja, o usuário irá visualizar a execução da Dívida Pública conforme o período selecionado.

| Armazém BO- SIAFI |Dimensão SIAFI| Filtro |
|----|----------|------------|
| Ano de exercício<br> |Período Contábil| Usar o período desejado |  


##### 1º NÍVEL


![image](https://user-images.githubusercontent.com/53793354/200358592-fd3046ee-1c02-4cfc-b320-93a0bc1990bc.png)

#### Campos da Tabela

|Campo PDT| Campo Armazém BO |Dimensão Armazém BO SIAFI| Exibição da Coluna| Observação
|---------|------------------|------|---|-|
| [Órgão]()| Unidade Orçamentária - Nome  |SIAFI - Unidade Orçamentária|
 Código Órgão| Unidade Orçamentária - Código  |SIAFI - Unidade Orçamentária| ao acionar o botão *'Exibir/Ocultar Código'*|
| Valor Empenhado | Valor Despesa Empenhada  |SIAFI - |
| Valor Liquidado | Valor Despesa Liquidada  |SIAFI - |
| Valor Pago | Valor Pago Financeiro  |SIAFI - |
| Valor Pago em Restos a Pagar | Valor Despesa Empenhada  |SIAFI - || Verificar se existe o campo no BO|

##### 2º NÍVEL

![image](https://user-images.githubusercontent.com/53793354/200359119-2bc8ec40-da77-40d5-b455-fbc7092aaf0c.png)

#### Campos da Tabela

|Campo PDT| Campo Armazém BO |Dimensão Armazém BO SIAFI| Exibição da Coluna| Observação
|---------|------------------|------|---|-|
| [Elemento]()|   |SIAFI -|
| ***Os campos referente a valores serão os mesmos do 1º nível***

PAREI AQUI SILVIANA

##### 3º NÍVEL
  - [Favorecido]() -> ao clicar o usuário será direcionado para o 4º nível
  - CPF / CNPJ
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/200358491-87bb0982-39ab-4880-8c12-3b4f2a73d9d6.png)


##### 4º NÍVEL
  - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento
  - Data de registro do Empenho
  - Unidade Executora
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/222240159-6b60cd86-8482-47e4-9055-0547efd02acb.png)


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

Essa consulta será composta por 5 níveis:
_______
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


##### 2º NÍVEL
  - Código do Subfunção
  - [Subfunção]() -> ao clicar o usuário será direcionado para o 3º nível
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/200358762-207b6b03-df53-471b-be0a-dd07e358c58f.png)


##### 3º NÍVEL
  - [Favorecido]() -> ao clicar o usuário será direcionado para o 4º nível
  - CPF / CNPJ
  - Código do Órgão -> Apenas quando o usuário clicar em *'Exibir/Ocultar Código'*)
  - Órgão
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>


##### 4º NÍVEL
  - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento
  - Data de registro do Empenho
  - Unidade Executora
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/222240202-d983cb56-1191-4666-aa48-0df4864f3d4b.png)


##### 5º NÍVEL

- Formulário de Detalhamento

### CONSULTA POR PROGRAMA
<a href="#top">(inicio)</a>

Essa consulta será composta por 5 níveis:
_______
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


##### 2º NÍVEL
  - Código do Ação
  - [Ação]() -> ao clicar o usuário será direcionado para o 3º nível
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/200358964-74159e14-a951-4c49-b6a0-4bd377975681.png)


##### 3º NÍVEL
  - [Favorecido]() -> ao clicar o usuário será direcionado para o 4º nível
  - CPF / CNPJ
  - Código do Órgão -> Apenas quando o usuário clicar em *'Exibir/Ocultar Código'*)
  - Órgão
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>




##### 4º NÍVEL
  - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento
  - Data de registro do Empenho
  - Unidade Executora
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/222240258-bf01a336-22dc-4c57-be52-0f313f0e896d.png)

##### 5º NÍVEL

- Formulário de Detalhamento


### CONSULTA POR FAVORECIDO (NOME E CPF/CNPJ)
<a href="#top">(inicio)</a>

Essa consulta será composta por 5 níveis:
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

  ![image](https://user-images.githubusercontent.com/53793354/200358337-66705311-e9ed-432a-a373-ef1fdf8dbf7d.png)


##### 2º NÍVEL
  - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento
  - Data de registro do Empenho
  - Código do Órgão -> Apenas quando o usuário clicar em *'Exibir/Ocultar Código'*)
  - Órgão
  - Unidade Executora
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>


##### 3º NÍVEL

- Formulário de Detalhamento





### Níveis

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
