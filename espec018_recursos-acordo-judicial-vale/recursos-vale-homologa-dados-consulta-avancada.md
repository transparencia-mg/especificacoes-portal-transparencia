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

 
### RELATO DOS ERROS
  
### 1. FILTROS 
  
* A medida que o usuário selecionar um parâmetro de qualquer filtro automaticamente apenas as opções que possuem relacionamento com o parâmetro selecionado será exibida nos demais filtros. Nos testes realizados foi verificado que esta funcionalidade não está ativa.
  
Exemplo: Ao selecionar o parâmetro projeto, apenas os dados daquele projeto devem estar disponíveis para seleção. Os demais devem estar inativados ou não devem aparecer. 
  
  - Foi selecionado o filtro 9288144, nesse caso deve estar habilitado ou aparecendo apenas o anexo IV.
  
  ![image](https://user-images.githubusercontent.com/52920939/168069982-9601af3e-da2a-40c3-a425-481ce28c3e23.png)

  - Foi selecionado o filtro 9288144, nesse caso deve estar habilitado ou aparecendo apenas o órgão polícia civil. 
  
  ![image](https://user-images.githubusercontent.com/52920939/168070150-fb0f31fe-79bb-4d21-88ce-df876ff75ef7.png)

O mesmo comportamento foi identificado nos demais filtros
  
### 2. EXIBIÇÃO DA CONSULTA
  
 * Ao aplicar os filtros e clicar em pesquisar não esta sendo exibindo na tela final os dados consultados.
  
Exemplo: No exemplo abaixo foi solicitado a exibição dos filtros: Projeto, Órgão e Função. Mas a consulta retorno apenas o período e valores. 
  
  - FITLROS APLICADOS:
  
  ![image](https://user-images.githubusercontent.com/52920939/168070612-9c68f6dc-f9a3-45b0-b0c9-3b32d6d80d2a.png)

  - RESULTADO DA CONSULTA
  ![image](https://user-images.githubusercontent.com/52920939/168070496-5e8044cf-990a-4077-bfff-62e57d48f5c7.png)

  
### 3. EXIBIR / OCULTAR CÓDIGO
  
 * Ao selecionar o botão exibir/ocultar código o portal não está apresentando diferença. O comportamento esta sendo o de exibir o código selecionando ou não o botão. 
  
- Ao selecionar o botão os códigos devem ser exibidos, colocando-se um coluna a esquerda.
 
  ![image](https://user-images.githubusercontent.com/52920939/168071132-a55695d7-de06-40f8-a9b3-936e0e78c89a.png)

 - Ao retirar o marcador do botão os códigos e as colunas devem desaparecer da coluna. Esse comportamento também deve ser o comportamento padrão.
  
  ![image](https://user-images.githubusercontent.com/52920939/168071312-4e0c1d7c-9159-4dae-b783-3f3a27f7ca52.png)
  
  
  
### 4. NÚMERO DE CONTRATO NÃO É EXIBIDO NO RESULTADO DA CONSULTA
  
 * Ao selecionar o número de um contrato na consulta o mesmo não aparece na tela de resultados.
  
- Exemplo: Foi selecionado o projeto 9288169 - na tela da consulta a coluna está vazia.
  
![image](https://user-images.githubusercontent.com/52920939/168076024-6053d7e0-4c15-4eb9-8854-21bfb7f9493a.png)

No entanto, ao solicitar o detalhamento, consta número de contrato para esse projeto 
  
![image](https://user-images.githubusercontent.com/52920939/168076145-059c24c4-c42a-482a-b4ea-4033711f2e8c.png)

  

### 4. FILTRO SEM NENHUM RESULTADO
  
Ao escolher um Favorecido, e clicar em pesquisar e em seguida detalhar, o portal abriu a caixa de diálogo com dados da página inicial
  
  SITUAÇÃO 1
  
 - FILTRO APLICADO
  
  ![image](https://user-images.githubusercontent.com/52920939/168071825-0b7eea7f-fa1e-4bfa-95e7-536dc981de59.png)

  - RESULTADO DA CONSULTA
  
  ![image](https://user-images.githubusercontent.com/52920939/168071757-ae886c94-82d1-4c47-854e-ffff096df56b.png)
  
  SITUAÇÃO 2
  FILTROS APLICADOS: 
  
  ![image](https://user-images.githubusercontent.com/52920939/168078077-dd06d01c-bd9b-40a8-8727-e2fc13454d06.png)

  RESULTADO DA CONSULTA:
  
  ![image](https://user-images.githubusercontent.com/52920939/168078180-6561a24f-3896-417e-8f60-41958fc8329d.png)
  
  ### 5. TABELA DE RESULTADOS TRAZ EMPENHOS DE OUTROS ANOS
  
  Ao filtrar o dado órgão 1521 - Controladoria Geral do Estado - no ano de 2022
  
  ![image](https://user-images.githubusercontent.com/52920939/168090958-ea497bd1-c98f-422b-9d4a-76d5e683bf5b.png)

  A tabela de resultados traz o empenho referente ao ano de 2021.
  
  ![image](https://user-images.githubusercontent.com/52920939/168091014-18bd9db1-f366-4841-8eff-4883da7225c5.png)

  
  
  ### 6. SEM INFORMAÇÕES DO PROCESSO DE COMPRA
  
  No projeto 9288155, foi verificado que a consulta não trouxe as informações referente ao processo de compra vinculado ao empenho 237/2022.
  
  TELA DA CONSULTA
  ![image](https://user-images.githubusercontent.com/52920939/168090033-46d8980c-b64c-44e2-b65a-bef89e4206a7.png)

  TELA DO PROCESSO DE COMPRA
  ![image](https://user-images.githubusercontent.com/52920939/168090233-36ddc3ce-7769-4b8e-b3a7-6a4bfc95d169.png)

  
  ### 7. SAIR
  Quando clicar em sair após a aplicação de um filtro, a página retorna para um erro. O correto é voltar para a página da consulta avançada.
  
  ![image](https://user-images.githubusercontent.com/52920939/168078283-602de1c0-8bf4-4eae-94cf-0e51e66271b6.png)

  

  

