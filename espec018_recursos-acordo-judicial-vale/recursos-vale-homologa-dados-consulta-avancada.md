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

# Homologação dos dados da consulta - CONSULTA AVANÇADA
<a href="#top">(inicio)</a>

<div class="alert alert-warning">

## CONSULTA AVANÇADA
<a href="#top">(inicio)</a>

## OBSERVAÇÃO: A consulta avançada não está gerando o formulário de detalhamento dos empenhos - está retornando para a página inicial.

  ![image](https://user-images.githubusercontent.com/52920939/171464475-586c92e1-7022-46d7-bf5b-b9ba131ce6d8.png)

  
### RELATO DOS ERROS
  
### 1. FILTROS 
  
* A medida que o usuário selecionar um parâmetro de qualquer filtro automaticamente apenas as opções que possuem relacionamento com o parâmetro selecionado será exibida nos demais filtros. Nos testes realizados foi verificado que esta funcionalidade não está ativa.
  
Exemplo: Ao selecionar o parâmetro projeto, apenas os dados daquele projeto devem estar disponíveis para seleção. Os demais devem estar inativados ou não devem aparecer. 
  
  - Foi selecionado o filtro 9288144, nesse caso deve estar habilitado ou aparecendo apenas o anexo IV. - **CORRIGIDO**
  
![image](https://user-images.githubusercontent.com/52920939/171460551-eaa785da-ab9b-4c00-87b9-343083cf7afa.png)


  - Foi selecionado o filtro 9288144, nesse caso deve estar habilitado ou aparecendo apenas o órgão polícia civil. - **CORRIGIDO**
  
![image](https://user-images.githubusercontent.com/52920939/171460587-093fbc3d-4e60-4735-9e6a-1459c650dc73.png)

O mesmo comportamento foi identificado nos demais filtros
  
### 2. EXIBIÇÃO DA CONSULTA
  
 * Ao aplicar os filtros e clicar em pesquisar não esta sendo exibindo na tela final os dados consultados - **CORRIGIDO**
  
Exemplo: No exemplo abaixo foi solicitado a exibição dos filtros: Projeto, Órgão e Função. Mas a consulta retorno apenas o período e valores. **CORRIGIDO**
    
  - FITLROS APLICADOS:
  
![image](https://user-images.githubusercontent.com/52920939/171461210-0cdcde0c-15e6-4e89-9a64-722c600d6ad5.png)

  - RESULTADO DA CONSULTA
![image](https://user-images.githubusercontent.com/52920939/171461288-a93c148a-0ab0-485b-b4dd-5d5b6dbf3f44.png)

  
### 3. EXIBIR / OCULTAR CÓDIGO - NÃO CORRIGIDO (AGUARDANDO RETORNO DO MANTIS)
  
 * Ao selecionar o botão exibir/ocultar código o portal não está apresentando diferença. O comportamento esta sendo o de exibir o código selecionando ou não o botão. 
  
- Ao selecionar o botão os códigos devem ser exibidos, colocando-se um coluna a esquerda.
 
  ![image](https://user-images.githubusercontent.com/52920939/168071132-a55695d7-de06-40f8-a9b3-936e0e78c89a.png)

 - Ao retirar o marcador do botão os códigos e as colunas devem desaparecer da coluna. Esse comportamento também deve ser o comportamento padrão.
  
  ![image](https://user-images.githubusercontent.com/52920939/168071312-4e0c1d7c-9159-4dae-b783-3f3a27f7ca52.png)
  
  
  
### 4. NÚMERO DE CONTRATO NÃO É EXIBIDO NO FILTRO DA CONSULTA - NÃO CORRIGIDO
    
 * Ao abrir o filtro de número de contrato o mesmo não aparece para seleção
  
- Exemplo: Foi selecionado o projeto 9288169 - na tela do filtro não consta valor.
  
![image](https://user-images.githubusercontent.com/52920939/171462022-4531ddb1-b4ee-451c-a986-c884bd8a5b97.png)

No entanto, ao solicitar o detalhamento, consta número de contrato para esse projeto 
  
![image](https://user-images.githubusercontent.com/52920939/168076145-059c24c4-c42a-482a-b4ea-4033711f2e8c.png)

  

### 4. FILTRO SEM NENHUM RESULTADO - CORRIGIDO
  
Ao escolher um Favorecido, e clicar em pesquisar e em seguida detalhar, o portal abriu a caixa de diálogo com dados da página inicial
  
  SITUAÇÃO 1
  
 - FILTRO APLICADO
  
  ![image](https://user-images.githubusercontent.com/52920939/168071825-0b7eea7f-fa1e-4bfa-95e7-536dc981de59.png)

  - RESULTADO DA CONSULTA
  
  ![image](https://user-images.githubusercontent.com/52920939/171462400-6d84690d-b237-4c02-a609-f5e95d6853b5.png)
  
  SITUAÇÃO 2
  FILTROS APLICADOS: 
  
 ![image](https://user-images.githubusercontent.com/52920939/171462606-5b2dbf1a-1155-4b45-bd26-8ec0ce1f7ce4.png) 

  RESULTADO DA CONSULTA:
  
  ![image](https://user-images.githubusercontent.com/52920939/171462652-20d19045-784c-4917-8973-7039d6acf62f.png)

  
  ### 5. TABELA DE RESULTADOS TRAZ EMPENHOS DE OUTROS ANOS - NÃO CORRIGIDO
  
  Ao filtrar o dado órgão 1521 - Controladoria Geral do Estado - no ano de 2022
  
  ![image](https://user-images.githubusercontent.com/52920939/168090958-ea497bd1-c98f-422b-9d4a-76d5e683bf5b.png)

  A tabela de resultados traz o empenho referente ao ano de 2021.
  
  ![image](https://user-images.githubusercontent.com/52920939/168091014-18bd9db1-f366-4841-8eff-4883da7225c5.png)

  
  
  ### 6. SEM INFORMAÇÕES DO PROCESSO DE COMPRA - NÃO FOI POSSÍVEL CONFERIR, POIS A CONSULTA AVANÇADA NÃO ESTÁ EXIBINDO RESULTADOS
  
  No projeto 9288155, foi verificado que a consulta não trouxe as informações referente ao processo de compra vinculado ao empenho 237/2022.
  
  TELA DA CONSULTA
  ![image](https://user-images.githubusercontent.com/52920939/168090033-46d8980c-b64c-44e2-b65a-bef89e4206a7.png)

  TELA DO PROCESSO DE COMPRA
  ![image](https://user-images.githubusercontent.com/52920939/168090233-36ddc3ce-7769-4b8e-b3a7-6a4bfc95d169.png)

  
  ### 7. SAIR - NÃO CORRIGIDO
  Quando clicar em sair após a aplicação de um filtro, a página retorna para um erro. O correto é voltar para a página da consulta avançada.
  
  ![image](https://user-images.githubusercontent.com/52920939/168078283-602de1c0-8bf4-4eae-94cf-0e51e66271b6.png)

  
  ### 8. BOTÃO LIMPAR FILTRO - NOVO ERRO
  Quando clicamos em limpar filtro, o botão apenas limpa os dados que estão na tela de filtros, e não realiza a limpeza do menu lateral a esquerda.
  
  Após realizar uma consulta, utilizei a opção limpar filtro. Os dados foram limpados da exibição, mas ao retornar para a pesquisa por código de projeto, o projeto q   estava selecionado, permaneceu com a seleção
  
  
![image](https://user-images.githubusercontent.com/52920939/171464921-2ae58ec8-7d68-43f8-aa89-a87330ccd747.png)

  


