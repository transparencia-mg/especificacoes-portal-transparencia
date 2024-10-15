---
contrato_manutencao: INF 4504
mantis:
pull_request: '[]()'
titulo: Atualização da Consulta Despesa Pública
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da demanda
<a href="#top">(inicio)</a>

Reestruturação da consulta de Despesa para incluir numa mesma consulta todas as informações de um mesmo empenho. A consulta conterá dados de toda execução financeira do empenho, incluindo dados de restos a pagar, processos de compras, contratos e convênios vinculados.

# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

A alteração faz-se necessária para atender à demandas dos usuários em correlacionar as informacões dentro de uma única consulta.

Atualmente, no Portal da Transparência, para ter acesso a informações de execução financeira, incluindo restos a pagar, compras e contratos, o usuário precisa realizar a consulta em três locais diferentes (consulta de Despesa, consulta de Restos a Pagar, Consulta de Compras e Contratos, além da consulta de Convênios, quando aplicável), sendo que nem sempre os dados são de fácil compreensão por parte do usuário.

Para essa reestruturação, o objetivo será trazer todas as informações para uma mesma consulta, além de tornar a consulta mais intuitiva, com possibilidade do usuário estruturar a sua consulta, incluir ou retirar colunas, além de reduzir a quantidade de cliques para chegar a informação desejada.


# Especificação
<a href="#top">(inicio)</a>

Esse documento tem como objetivo apresentar as alterações que deverão ser implementadas na pesquisa básica e na pesquisa avançada da consulta de Despesa Pública.

## Observações Gerais:

1. Todas as páginas da consulta deverão exibir ícones com links para compartilhar as  consultas. O usuário poderá compartilhar os links dos dados nos seguintes canais, no mínimo:
**CORRETO**
     * Twitter
     * Facebook
     * WhatsApp
     * Instagram
     * Copiar url

**PÁGINA INICIAL E INTERMEDIÁRIAS**
![image](https://github.com/user-attachments/assets/825dda51-a4c0-4aa7-b278-bc0fd043f54e)
**DETALHAMENTO** - LINKS FORAM ABERTOS PARA COMPARTILHAR
![image](https://github.com/user-attachments/assets/b9b87ed8-38c2-4bb9-b931-8ecac70ae687)


2. Todas as páginas deverão exibir cabeçalho da tabela para que o usuário identifique qual o caminho percorrido. Além do caminho percorrido pelo usuário o PDT deverá apresentar a data de atualização dos dados e o período selecionado. **CORRETO**

     * Período:
     * Dados atualizados em:
**CORRETO**  
![image](https://github.com/user-attachments/assets/13c98db2-be77-4d2e-94be-b27140fc21a6)

3. Todas as páginas deverão exibir as migalhas de pão (*Breadcrumbs navigation*): **CORRETO**

**CORRETO**
![image](https://github.com/user-attachments/assets/2249cbd5-aa8e-489c-880f-bb6775305855)


4. Os ícones '*Exibir Gráfico*/*Ocultar Gráfico*', '*Download*' e '*Compartilhar*' serão exibidos acima do gráfico/tabela de resultados. Sendo que, quando o usuário clicar em exibir gráfico o botão '*Download*' será deslocado para depois do gráfico. Esse comportamento já é adotado na consulta Acordo Judicial da Vale. **CORRETO**

**Exibir Gráfico/Ocultar Gráfico**
![image](https://github.com/user-attachments/assets/5731f183-49a6-465b-90b8-3292366dd72e)
**Gráfico de área ou barra**
![image](https://github.com/user-attachments/assets/60eb2ffd-fd02-4499-be22-b47138d9fff6)
![image](https://github.com/user-attachments/assets/4aef4340-17d4-49fc-a467-193caf71e02c)
**DOWNLOAD PDF**
![image](https://github.com/user-attachments/assets/f74c044f-e8cf-4e32-af83-b8fbe3a800e7)
**DOWNLOAD CSV**
![image](https://github.com/user-attachments/assets/2bd3449f-20d1-4731-972d-023c565c6ead)

**CORRIGIR LINK - DOWNLOAD BASE COMPLETA** - ALTERAR PARA REDIRECIONAR PARA A PÁGINA DA CONSULTA DE DESPESAS* https://dados.mg.gov.br/dataset/despesa
![image](https://github.com/user-attachments/assets/de9e7771-f648-45c1-afc1-f9e2bcb69410)

5. Todas as **barras de pesquisa** devem aceitar várias formas de preenchimento dos dados.**CORRETO**

**AUTO COMPLETAR** **CORRETO**
    * Autocompletar (*autocomplete* ) desde a primeira letra (eg. [Portal de Transparência MG](http://www.transparencia.mg.gov.br));
**CORRETO**  
![image](https://github.com/user-attachments/assets/b628fb0d-b10e-43d3-ae6b-ac1fb900736a)

**DESCONSIDERAR CARACTERES ESPECIAIS** **CORRETO**
    * Desconsiderar acentuação, letras maiúsculas e minúsculas;
**CORRETO**
![image](https://github.com/user-attachments/assets/2ec7134b-3821-49a8-8ad7-e1d22a0cd4d9)

**DESCONSIDERAR PALAVRAS INTERMEDIÁRIAS** **CORRETO**
    * Desconsiderar palavras intermediárias (ex.: Ao digitar “gestao pública”, um dos resultados será “Gestão da Administração Pública”);
**CORRETO**
![image](https://github.com/user-attachments/assets/0bba2e27-df4d-4c0b-bed8-66c8638b734c)

**PESQUISA AVANÇADA**   - **NÃO AVALIADA - SERÁ AVALIADA POSTERIORMENTE**
    * O usuário poderá pesquisar código ou descrição das classificações orçamentárias (eg. [Consulta Acordo Judicial da Vale - PdT MG](https://www.transparencia.mg.gov.br/eventos-extraordinarios/acordo-judicial-reparacao-vale?task=estado_recursosvale.consultaLivre)).  

**PESQUISA AVANÇADA**   - **NÃO AVALIADA - SERÁ AVALIADA POSTERIORMENTE**    
    *  O usuário poderá pesquisar por qualquer coluna na tabela de resultados.

6. O design de todas as tabelas de resultados da pesquisa básica deverá apresentar o seguinte comportamento:**CORRETO**
**CABEÇALHO FIXO**
    * Cabeçalho fixo - Fixer Header ([eg. Consulta de Remuneração do PdT](https://www.transparencia.mg.gov.br/estado-pessoal/remuneracao-dos-servidores/remuneracao-faixa/202112/3/1094/4022/C/3569184/995/26150365));
**CORRETO**  
![image](https://github.com/user-attachments/assets/53fb638f-f560-4d2e-8432-03a7da57ea8a)

**ROLAGEM HORIZONTAL** - **CORRETO - NÃO FOI NECESSÁRIA A ROLAGEM HORIZONTAL**
   * Rolagem horizontal - Horizontal Scroll. Quando o número de colunas ultrapassar o limite da página o PdT deve possibilitar a rolagem horizontal;

**COLUNAS MOVIVÉIS E CLASSIFICAVÉIS**
   * Colunas movíveis e classificáveis, conforme ocorre atualmente;
**CORRETO**
![image](https://github.com/user-attachments/assets/a6d22d6e-e808-4623-aef3-b7bef3188f3f)

**PAGINAÇÃO E SELEÇÃO DA QUANTIDADE DE LINHAS**
   * Paginação e seleção da quantidade de linhas a serem exibidas, conforme ocorre atualmente;
**CORRETO**
![image](https://github.com/user-attachments/assets/154a1dfc-4a37-400a-9d0a-d4746d72f539)

**TEXTO AJUSTÁVEL NAS COLUNAS**
   * O texto deve ser ajustável nas colunas, ou seja, caso seja necessário pode haver quebra de linha;
**CORRETO**
![image](https://github.com/user-attachments/assets/3899ba4b-6014-48e7-b295-2ffcae14e33e)

**CAMPOS CLICÁVEIS** MARCADOS EM VERMELHO
   * A tabela apresentará campos clicáveis (com link) que irão direcionar o usuário para o próximo nível da consulta.
**CORRETO**  
![image](https://github.com/user-attachments/assets/34a8b2e1-504e-4038-b097-540f1d2ae580)

**CAMPOS CLICÁVEIS** MARCADOS EM VERMELHO
   * Os campos clicáveis serão destacados conforme o layout já adotado pelo PdT - [Consulta Acordo Judicial de Reparação da Vale](https://www.transparencia.mg.gov.br/eventos-extraordinarios/acordo-judicial-reparacao-vale?task=estado_recursosvale.listarExecucoes&amp;ano=&amp;dataInicio=01/01/2021&amp;dataFim=31/12/2022&amp;consulta=2&amp;filtro=).
**CORRETO**  
![image](https://github.com/user-attachments/assets/34a8b2e1-504e-4038-b097-540f1d2ae580)

**TOOLTIP** - CONFERIDO SÓ A EXISTÊNCIA - AVALIAÇÃO DO TEXTO NO PRÓPRIO ARQUIVO DO TOOLTIP
   * Todos os termos das tabelas terão tooltip que serão exibidos quando o usuário passar o mouse sobre o ícone de "?"
   ![](static/tooltip-tabela.png)
**CORRETO**
![image](https://github.com/user-attachments/assets/28d1ce65-80fa-410b-b6dc-b46c99295a43)
**CORRETO**
![image](https://github.com/user-attachments/assets/117eabc1-c8ae-4863-b325-4f112e2a1cc7)


7. A descrição dos tooltips e os campos de cada tabela estão disponíveis em:
**AVALIADO NO PRÓPRIO DOCUMENTO DE TOOLTP**
    * [Especificação Tooltip](https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/espec020_filtros_consulta_despesa/espec020_filtros_consulta_despesa/especificacao-despesa-tooltip.md)
   * [Especificação Dados](https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/master/espec020_filtros_consulta_despesa/especificacao-despesa-dados.md)

9. Todas as funcionalidades não exemplificadas seguirão o mesmo padrão já adotado na consulta Acordo Judicial da Vale do Portal de Transparência. 

## Página Inicial - Pesquisa Básica
<a href="#top">(inicio)</a>

## 1. Texto Introdutório

Inclusão de um campo que irá trazer uma breve explicação do conteúdo da consulta. *Exemplo: [Consulta Acordo Judicial da Vale](https://www.transparencia.mg.gov.br/eventos-extraordinarios/acordo-judicial-reparacao-vale)* - **CORRETO**

![image](https://github.com/user-attachments/assets/44f1b33d-124e-472c-b902-5d28dc4eff3f)

### Atributos do campo<br>

1. O PdT deverá permitir que por meio da área administrativa do Portal a equipe da DTA inclua ou altere os dados de texto desse campo, incluindo os tooltips. **NÃO AVALIADO - SERÁ PRECISO VERIFICAR POSTERIORMENTE**
  
2. O usuário poderá exibir mais detalhes do texto ao clicar em **Mais** ou ocultar ao clicar **Menos**; **CORRETO**

**CORRETO**
![image](https://github.com/user-attachments/assets/44f1b33d-124e-472c-b902-5d28dc4eff3f)

3. A funcionalidade deverá permitir a visualização de tooltip ao posicionar o mouse sobre uma palavra ou termo;**CORRETO**
**CORRETO**
![image](https://github.com/user-attachments/assets/357b5778-88e2-4e90-972c-397965fc4451)

4. Ao clicar sobre a palavra ou termo o PdT deverá abrir um pop-up em forma de glossário. [eg. pop-up](https://www.usaspending.gov/)**CORRETO**
**CORRETO**
![image](https://user-images.githubusercontent.com/53793354/221929369-65f86c35-99da-49ae-b6e7-3a4a56e44776.png)

5. Ao clicar em qualquer termo destacado o usuário será direcionado para o termo específico dentro do glossário do Portal. **CORRETO**
![image](https://user-images.githubusercontent.com/53793354/222512320-2b637eb1-9b0c-4891-8f5e-dded28d3c0c2.png)

**CORRETO**
![image](https://github.com/user-attachments/assets/619d72f2-fc02-46c2-95d9-a79d4440eda2)

### Texto explicativo

* Ver  [Especificação Tooltip](https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/espec020_filtros_consulta_despesa/espec020_filtros_consulta_despesa/especificacao-despesa-tooltip.md) **AVALIADO NO PRÓPRIO DOCUMENTO DE TOOLTP**

## 2. Leiaute - Barra de navegação
<a href="#top">(inicio)</a>

A barra de navegação superior será composta pelos seguintes campos: **CORRETO**

  * Ícones por tipo de Consulta: Órgão, Favorecido, Programa e Função;
  * Ano;
  * Período (01/04/2021 a 30/12/2021);
  * Opção de *'Filtro*;
  * Botão *'Monte sua consulta'* **SERÁ INSERIDO POSTERIORMENTE**

![image](https://github.com/user-attachments/assets/6590c288-c58a-4152-9d52-ce6288a3852a)

**CORRETO**
![image](https://user-images.githubusercontent.com/53793354/221950181-bcab0ef7-f535-4495-94a4-4a66418ee89e.png)

### Atributos do campo<br>

1. O campo período será no formato **dd/mm/aaaa** composto por início e fim (eg. 01/04/2021 a 30/12/2021). Como padrão, o campo "Início/Fim" irá exibir o exercício vigente até o último dia de atualização dos dados. **ESTÁ EXIBINDO ATÉ 31/12/2024** - NÃO PREJUDICA A AVALIAÇÃO
![image](https://github.com/user-attachments/assets/c9839d04-64ea-4d02-a947-83a2220e0a78)

2. No campo da data o usuário poderá selecionar ou digitar a data na caixa.<br> Exemplo: [Portal de Transparêcia ES](https://transparencia.es.gov.br/Despesa);
**PARA DIGITAR A DATA, PRECISA CLICAR PARA SELECIONAR** - NÃO PREJUDICA, MAS PODE FACILITAR A DIGITAÇÃO - AO COLOCAR O CURSO NA DATA, ELE VAI PRO INÍCIO OU APAGA A DATA ATUAL
![image](https://github.com/user-attachments/assets/91122af5-300a-4e68-897c-00ba97657dca)

3. Caso o usuário digite uma data que ultrapasse o exercício financeiro o PdT deverá exibir uma mensagem orientando que a data esteja dentro do período do exercício financeiro.
**CORRETO**
![image](https://github.com/user-attachments/assets/bfde12d7-d63b-49c4-ab43-9a08d3db737c)

4. A busca poderá ser realizada por meio de 4 tipos de filtros:
**CORRETO**
  * Órgão
  * Favorecido (Nome ou CPF/CNPJ)
  * Função
  * Programa
![image](https://github.com/user-attachments/assets/5339abfb-d702-48ad-986d-42243de32079)

5. Quando o usuário posicionar o mouse sobre o ícone será exibido um tooltip com uma breve descrição.
**CORRETO**
![image](https://github.com/user-attachments/assets/6b5948f7-b2ba-4639-b6da-70f778be654a)


6. O comportamento do campo *'Filtro'* será conforme o tipo de consulta selecionada e como padrão será exibido a opção 'Todos':<br>
     - **Órgão, Função, Programa**:<br> Ao selecionar uma das opções o PDT irá permitir que o usuário selecione um item no campo filtro. Esse campo poderá ser selecionado através da barra de rolagem ou por digitação.
**CORRETO**
![image](https://github.com/user-attachments/assets/e66fdfd3-e42a-4385-a099-a68984e9949f)


      - **Favorecido**:<br> Ao selecionar esse tipo de consulta o usuário poderá escolher se a busca será realizada pelo nome do Favorecido ou pelo CPF/CNPJ. Nesse caso, deverá ser exibida uma barra em que o usuário irá digitar os dados.
**CORRETO** ALTERAR FUTURAMENTO PARA APARECER A INFORMAÇÃO *Digite o nome ou CPF/CNPJ
![image](https://github.com/user-attachments/assets/d9436e04-3a2b-4653-b04f-f3a00e480148)


6. A barra de pesquisa do campo filtro deverá possuir atributo [placeholder]
**CORRETO**
![image](https://github.com/user-attachments/assets/211fc4d9-5a7b-4259-aa98-9a8d0722f937)(https://www.w3schools.com/tags/att_input_placeholder.asp) para facilitar ou indicar como o campo deverá sem preenchido. Destaca-se que o campo favorecido nome e CNPJ serão obrigatórios para o usuário seguir na busca, conforme ocorre na consulta da Vale. Porém nos demais filtros (órgão, programa, função) a informação deverá ser retornada a medida que o usuário for digitando.<br> (Texto: *Digite o nome, parte do nome ou CPF/CNPJ*)

7. As demais funcionalidades serão as mesmas já adotadas na consulta 'Acordo Judicial de Reparação da Vale' (MELHOR TRAZER DA ESPECIFICAÇÃO DA CONSULTA DA VALE AQUI E REPETIR AS FUNCIONALIDADES QUE QUEREMOS QUE SEJAM IMPLEMENTADAS PFV)


## 3. Leiaute - Tabelas de Resultados
<a href="#top">(inicio)</a>

1. A tabela de resultado levará em consideração os parâmetros dos filtros aplicados pelo usuário. **CORRETO**
![image](https://github.com/user-attachments/assets/245df583-9f2a-429a-99e0-476e92ca66b7)
  
2. A pesquisa básica irá apresentar como padrão a tabela de resultados com os dados do exercício vigente por Órgão.
**CORRETO** - VERIFICADO SOMENTE 2024 - RETORNAR PARA VERIFICAR OUTROS ANOS
   
3.  Como padrão os dados serão exibidos no formato de tabela e caso o usuário queira visualizar os dados em forma de gráfico deve clicar em '*Exibir Gráfico*' e os dados da tabela serão deslocados para baixo. Para retornar a exibição para o formato tabela o usuário deve clicar em '*Ocultar Gráfico*'
**CORRETO**
![image](https://github.com/user-attachments/assets/ec0887a5-b778-4264-a772-bed7cfdb0385)
![image](https://github.com/user-attachments/assets/37a45339-ed5b-477a-988d-354dbbcdfc78)

4. A opção de 'Exibir linhas' (quantidade de linhas) será exibida na parte superior da tabela. 
**CORRETO**
![image](https://github.com/user-attachments/assets/3d717a75-d90c-4a19-8542-e165206aa1aa)
  
5. O usuário poderá solicitar a exibição dos dados com código e descrição. Ao clicar no botão *'Exibir/Ocultar Código'* uma nova coluna será adicionada a esquerda de cada coluna que tenha a descrição.
**CORRETO**
![image](https://github.com/user-attachments/assets/50baa39d-a9f5-4bac-9560-9c8bd9cb2225)

6. Os valores TOTAL GERAL e o SUBTOTAL serão exibidos na tabela de resultados de acordo com o comportamento do usuário:

  * **TOTAL GERAL:** quando o usuário não aplicar nenhum filtro na tabela ou quando todos os dados forem exibidos em uma única página, ou seja, sem paginação;
**CORRETO**
![image](https://github.com/user-attachments/assets/0f61017c-f0c6-4831-b97b-dfa82b764c19)

  * **SUBTOTAL:** quando o usuário aplicar qualquer filtro na tabela através da barra de pesquisa ou quando houver paginação na tabela de resultado, ou seja, houver mais de uma página de resultado.
**CORRETO**
![image](https://github.com/user-attachments/assets/0a513c45-8c30-4205-a43b-127f74bd5ea5)
![image](https://github.com/user-attachments/assets/c2237835-b413-4fa7-ba7f-f6e9137f0233)

    
7. Os campos clicáveis serão destacados conforme o layout já adotado pelo PdT e terão a imagem de uma lupa. Para exibir mais informações o usuário deverá clicar na lupa da coluna "detalhar":
**MELHORAR** LUPA APARECEU SOMENTE NA PÁGINA DO EMPENHO
![image](https://github.com/user-attachments/assets/7187a86b-5e66-46a3-b466-dab1c2a3659a)


8. Todos os parâmetros apresentados acima, podem ser verificados na consulta do Portal *'Acordo Judicial da Vale'*.

![tabela-resultados-pesquisa-basica](https://user-images.githubusercontent.com/53793354/222518746-af453a54-590d-4454-8722-53f6230c770b.gif)

![image](https://github.com/user-attachments/assets/27947b42-d5b8-4132-9c98-b50e53eccb72)

### Leiaute - Gráficos
<a href="#top">(inicio)</a>

* O usuário terá a opção de verificar a série histórica ao clicar no gráfico de barra;
**GRÁFICO ESTÃO SENDO EXIBIDOS ATÉ O SEGUNDO NÍVEL - A PARTIR DE EMPENHO NÃO APARECE** - VERIFICAR QUAL O COMPORTAMENTO CORRETO
![image](https://github.com/user-attachments/assets/d58e3a2e-15d3-4011-a2b7-a65f3f98226a)
  
* Os gráficos apresentaram os dados da coluna 'Valor Liquidado'.
**CORRETO**
![image](https://github.com/user-attachments/assets/b33c8824-2fac-4d7e-bd0c-4fc24ef667de)

* Todos os gráficos deverão apresentar títulos, conforme o usuário for navegando pela consulta.<br>
Exemplo: Consulta de Despesa 
**CORRETO**
![image](https://github.com/user-attachments/assets/0908e15c-59d6-4cde-af62-ba742a88b16b)
![image](https://github.com/user-attachments/assets/7e58fc01-55ad-4810-90dd-07c87530c635)

### Download dos dados:
<a href="#top">(inicio)</a>

  - **Download PDF:**

  * O documento gerado em PDF deverá exibir:
      * logo do Portal de Transparência no início da página;
**CORRETO**
![image](https://github.com/user-attachments/assets/38bb2ce3-92a3-4723-8160-cd9d040a221c)

      * *URL*, paginação e a data no fim da página (data em que a consulta foi realizada); 
**CORRETO** - TESTE REALIZADO NO LINK - DIRECIONOU PARA PÁGINA CORRETAMENTE
![image](https://github.com/user-attachments/assets/cae033f1-d466-4504-a0d6-af3263f48621)

      * O arquivo gerado irá exibir os mesmos dados apresentados na tela considerando todos os filtros aplicados, inclusive TOTAL GERAL ou SUBTOTAL conforme o comportamento do usuário. 

**SUBTOTAL APARECEU APENAS NA ÚLTIMA PÁGINA - E COM VALORES INCORRETOS**
![image](https://github.com/user-attachments/assets/6a28e0a5-f369-44df-8434-f40d89a43101)

**SUBTOTAL APARECEU APENAS NA ÚLTIMA PÁGINA - E COM VALORES INCORRETOS**
![image](https://github.com/user-attachments/assets/db5f77b0-97bd-488d-86df-c3613be17d15)

      * ao selecionar essa opção o arquivo PDF deverá ser aberto em outra aba do navegador **NÃO SE APLICA MAIS, POIS ESTÁ BAIXANDO O ARQUIVO**
      * Período da consulta: 
**CORRIGIR - APARECE A DATA DO ARQUIVO, MAS NÃO APARECE O PERÍODO DA CONSULTA**
![image](https://github.com/user-attachments/assets/f7ea05eb-f375-4a5a-aa29-3dcb8347692c)

  - **Download Planilha (CSV):** 

  * O documento gerado em CSV deverá:
      * Exibir a tabela completa de todas as páginas no formato CSV, independente do filtro aplicado. 
**CORRETO**
![image](https://github.com/user-attachments/assets/5dd06c60-f7bf-4c6c-b18a-4253f669bf8a)

  - **Exibir código e descrição** 
      * Exibir código e descrição em campos distintos, independente do usuário selecionar a opção '*Exibir/Ocultar código*'
  **CORRETO**
![image](https://github.com/user-attachments/assets/baca816b-4e7c-4e70-a650-ce93487a0763)


  - **Download base completa:** **CORRIGIR**

  * O download da base completa:
      * O usuário será direcionado para o conjunto de dados da respectiva consulta no Portal de Dados Abertos.
**CORRIGIR O LINK - DIRECIONANDO PARA A PÁGINA INICIAL DO DADOS MG** CORRIGIR PARA O CONJUNTO DE DADOS DA DESPESA
![image](https://github.com/user-attachments/assets/c8698548-b1e2-4dfb-8205-fb68af51ff08)

      * O PdT deverá permitir que a equipe DTA inclua/altere a *url* desse campo através da área administrativa do Portal.
**NÃO FOI VERIFICADO SOBRE A ÁREA ADMINISTRATIVA**                 

## 4. Pesquisa básica - Navegação por filtros
<a href="#top">(inicio)</a>


### CONSULTA POR ÓRGÃO - Página Inicial
<a href="#top">(inicio)</a>

Essa consulta será composta por 5 níveis:
_______
  1º nível - [Órgão]()<br>
  2º nível - Órgão > [Elemento de despesa]()<br>
  3º nível - Órgão > Elemento de despesa > [Favorecido]()<br>
  4º nível - Órgão > Elemento de despesa > Favorecido > [Empenho]()<br>
  5º nível - Órgão > Elemento de despesa > Favorecido > Empenho > [Formulário de Detalhamento]()<br>
___________

##### 1º NÍVEL **CORRETO**
  - Código do Órgão
  - [Órgão]() -> ao clicar o usuário será direcionado para o 2º nível **CORRETO**
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/200358592-fd3046ee-1c02-4cfc-b320-93a0bc1990bc.png)
**CORRETO**
![image](https://github.com/user-attachments/assets/18f98e38-143c-48ef-a42f-2b4565e974b0)


##### 2º NÍVEL **CORRETO**
  - [Elemento de despesa]() -> ao clicar o usuário será direcionado para o 3º nível **CORRETO**
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/76428a3d-d4cf-4c0f-889a-c01edf606c0a)

**CORRETO**
![image](https://github.com/user-attachments/assets/7ff91592-a93d-4de5-8ea6-dfcb09c86454)

##### 3º NÍVEL **CORRETO**
  - [Favorecido]() -> ao clicar o usuário será direcionado para o 4º nível **CORRETO**
  - CPF / CNPJ
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![](static/tabela_3_favorecido_orgão.png)

**CORRETO**
![image](https://github.com/user-attachments/assets/0666c0c1-f364-45df-b8bb-a9775f6681dc)


##### 4º NÍVEL **CORRETO**
  - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento **CORRETO**
  - Data de registro do Empenho
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/225976978-08433f80-ad38-42db-add6-7fa7dc5a88b9.png)

**CORRETO**
![image](https://github.com/user-attachments/assets/6aa355ed-c38c-41f4-a408-287711732dc0)


##### 5º NÍVEL

 - **Formulário de Detalhamento** **VÁRIOS ITENS A SEREM CORRIGIDOS**

  Ao clicar no número do empenho o usuário será direcionado para o formulário de detalhamento, que será composto pelos seguintes atributos: **CORRETO**
    * As tabelas que compõem o formulário de detalhamento serão exibidas em formato de guias. **CORRETO**
    * O usuário poderá fazer o Download das informações do formulário de detalhamento ao clicar no botão 'Download'. **NÃO LOCALIZADO - CORRIGIR** 
  
![image](https://github.com/user-attachments/assets/b63ec9a1-162b-4f6b-ab41-fcbfd3eb59c8)


**OBS:**O usuário poderá fazer o Download das informações do formulário de detalhamento ao clicar no botão 'Download'. A exportação em planilha (CSV) deverá ser estruturada em formato de tabela. Cada campo em uma coluna. **NÃO LOCALIZADO - CORRIGIR** 


##### Campos do formulário de detalhamento 

###### Classificação Orçamentária **CORRETO**

![image](https://github.com/transparencia-mg/especificacoes-portal-transparencia/assets/53793354/49cd8d38-6fa0-42aa-b77c-4842ab982ae4)

**CORRETO**
![image](https://github.com/user-attachments/assets/493ffb5b-2e73-4087-b346-410f247de402)

###### Empenho **CORRETO**
- O formulário de detalhamento deverá exibir a inscrição, liquidação e pagamento dos valores em restos a pagar referente ao todos os exercícios. **CORRETO**
- Exemplo:
  * Ano de registro do Empenho: 2020
  * Inscrição em Restos a Pagar: 2021
  * Reinscrito em Restos e Pagar: 2022
![image](https://github.com/user-attachments/assets/17383fd6-d310-4bc4-9cd3-36541545b7ee)


###### Liquidação **CORRETO**
**CORRETO**
![image](https://github.com/user-attachments/assets/7bd89771-cdbc-4cce-ab03-e2e75a1edc19)

###### Pagamento **CORRETO**

**CORRETO**
![image](https://github.com/user-attachments/assets/379fdd5b-6767-4c0d-86e7-8d49c5d0ce76)
**CORRETO**
![image](https://github.com/user-attachments/assets/54644cfd-1594-4f8e-ac19-2c043f46f0ac)

###### Outras Informações
**Comportamento da Consulta:**CORRETO**

- Ao clicar no campo 'Número do Processo de Compra' o usuário será direcionado o [formulário de detalhamento da consulta Compras e Contratos](https://www.transparencia.mg.gov.br/licitacoes-e-contratos/compras-e-contratos/comprasecontratos-procedimento/99/2024/01-01-2024/17-04-2024/1831084/5/0/0/17/3/175/305/6976/3050203/92592/1872/409049/2301762000001-2024).

**CORRETO - NÃO ENTANTO PODEMOS ENCURTAR O CAMINHO DO USUÁRIO E ENVIAR DIRETO PARA O LINK DO PORTAL DE COMPRAS**

![image](https://github.com/user-attachments/assets/b8dbf4f4-af1b-44f1-97c7-15b18a32f071)

- Ao clicar no campo 'Número do Contrato' o usuário o usuário será direcionado o [formulário de detalhamento da consulta Contratos](https://www.transparencia.mg.gov.br/licitacoes-e-contratos/compras-e-contratos/comprasecontratos-filtros/5/2024/01-01-2024/17-04-2024/90/85413).

**CORRETO - NÃO ENTANTO PODEMOS ENCURTAR O CAMINHO DO USUÁRIO E ENVIAR DIRETO PARA O LINK DO PORTAL DE COMPRAS**
![image](https://github.com/user-attachments/assets/9fdf1be9-47d2-429f-b276-0538f040d472)

- Ao clicar no campo 'Número do Convênio / Parceria SIAFI' o usuário será direcionado o formulário de detalhamento da consulta [Consulta Convênios / Parceria de Saída de Recursos](https://www.transparencia.mg.gov.br/convenios/convenios-de-saida-de-recursos/convenios-de-saida/convenios-orgao-detalhesconv/2/2024/01-01-2024/31-12-2024/20/4674/74024)

**CORRETO - MAS NÃO FOI LOCALIZADO NENHUM CONVENIO PARA SER VERIFICADO**
![image](https://github.com/user-attachments/assets/7e080013-9619-4acf-b16d-68da3c3d3276)


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
**CORRETO**

  - [Função]() -> ao clicar o usuário será direcionado para o 2º nível **CORRETO**
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/200358699-3acd5a01-9948-437c-96b6-fa2f06726f5a.png)

**CORRETO**
![image](https://github.com/user-attachments/assets/4c4be56c-f9e4-4081-a810-e30e8e3eeb3f)


##### 2º NÍVEL 
**CORRETO**
  - Código do Subfunção
  - [Subfunção]() -> ao clicar o usuário será direcionado para o 3º nível  **CORRETO**
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/200358762-207b6b03-df53-471b-be0a-dd07e358c58f.png)
**CORRETO**
![image](https://github.com/user-attachments/assets/3f489b53-81f7-48a0-b584-867eaa4b4868)

##### 3º NÍVEL 
**CORRETO**
  - [Favorecido]() -> ao clicar o usuário será direcionado para o 4º nível **CORRETO**
  - CPF / CNPJ
  - Código do Órgão -> Apenas quando o usuário clicar em *'Exibir/Ocultar Código'*)
  - Órgão
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/234644755-f9b5a04d-9eb9-42eb-84fd-e931777ba3d8.png)

**CORRETO**
![image](https://github.com/user-attachments/assets/49ebdd8a-b594-4a6a-96a6-d1713be28986)


##### 4º NÍVEL
  - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento
  - Data de registro do Empenho
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/225976859-3d1378d1-9134-40ae-b6c4-1accc71b130a.png)
**CORRETO**
![image](https://github.com/user-attachments/assets/1ef5911c-2fca-47e1-9207-fcfc3fc54802)



##### 5º NÍVEL

- Formulário de Detalhamento - **INFORMAÇÕES DE CORREÇÕES, VERIFICAR NA CONSULTA POR ÓRGÃO**

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

##### 1º NÍVEL **CORRETO**
  - Código da Programa
  - [Programa]() -> ao clicar o usuário será direcionado para o 2º nível **CORRETO**
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/200358865-cd1aee56-75a1-42c9-aa95-fafcda4db320.png)

**CORRETO**
![image](https://github.com/user-attachments/assets/85599188-2361-42e3-bb48-d3be3816094f)

##### 2º NÍVEL **CORRETO**
  - Código do Ação
  - [Ação]() -> ao clicar o usuário será direcionado para o 3º nível **CORRETO**
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/200358964-74159e14-a951-4c49-b6a0-4bd377975681.png)

**CORRETO**
![image](https://github.com/user-attachments/assets/527feecc-8ed4-4071-b27f-e7a7ef0906c5)

##### 3º NÍVEL **CORRETO**
  - [Favorecido]() -> ao clicar o usuário será direcionado para o 4º nível **CORRETO**
  - CPF / CNPJ
  - Código do Órgão -> Apenas quando o usuário clicar em *'Exibir/Ocultar Código'*)
  - Órgão
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/234645101-99df10fb-bd8a-44a3-acbd-23ccd5da215b.png)

**CORRETO**
![image](https://github.com/user-attachments/assets/84946482-3fbb-4c31-94d3-145aa9afdaf8)

##### 4º NÍVEL **CORRETO** 
  - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento **CORRETO**
  - Data de registro do Empenho
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/225976711-22009c8c-796d-46bd-aae3-626578119991.png)

**CORRETO**
![image](https://github.com/user-attachments/assets/7e640766-a76b-4488-9010-ecfe939ebacd)

##### 5º NÍVEL

- Formulário de Detalhamento **INFORMAÇÕES DE CORREÇÕES, VERIFICAR NA CONSULTA POR ÓRGÃO**


### CONSULTA POR FAVORECIDO (NOME E CPF/CNPJ) **CORRETO** 
<a href="#top">(inicio)</a>

Essa consulta será composta por 3 níveis: **CORRETO** 
_______
  1º nível - [Favorecido]()<br>
  2º nível - Favorecido > [Empenho]()<br>
  3º nível - Favorecido > Empenho > Formulário de Detalhamento<br>
___________

##### 1º NÍVEL
  - [Favorecido]() -> ao clicar o usuário será direcionado para o 4º nível **CORRETO** 
  - CPF / CNPJ
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/228915058-9da50a39-f7e5-41a2-8471-72ea369b32ca.png)

**CORRETO** 
![image](https://github.com/user-attachments/assets/1a3a45e8-001f-4084-9b27-18d8054d359f)


##### 2º NÍVEL **CORRETO** 
 - [Empenho]() -> ao clicar o usuário será direcionado para o formulário de detalhamento **CORRETO** 
  - Data de registro do Empenho
  - Código do Órgão -> Apenas quando o usuário clicar em *'Exibir/Ocultar Código'*)
  - Órgão
  - Valor Empenhado
  - Valor Liquidado
  - Valor Pago
  - Valor Pago de Restos a Pagar<br>

![image](https://user-images.githubusercontent.com/53793354/228915644-9b4db1ef-4db0-4d27-9540-254f95e12e22.png)

**CORRETO** 
![image](https://github.com/user-attachments/assets/7cb07be7-b1ac-444d-b094-8cfe9cf1a42f)


##### 3º NÍVEL

- Formulário de Detalhamento **INFORMAÇÕES DE CORREÇÕES, VERIFICAR NA CONSULTA POR ÓRGÃO**


**SERÁ AVALIADA EM OUTRO MOMENTO**
## Pesquisa Avançada - Monte sua consulta - 
<a href="#top">(inicio)</a>

A pesquisa será composta pelos seguintes componentes:

* Barra de navegação vertical com filtros;
* Filtros Aplicados;
* Tabela de Resultado;

### Barra de Navegação Vertical
<a href="#top">(inicio)</a>

 Atributos da barra de navegação vertical:

* Todos os filtros deverão apresentar uma breve descrição.
* Todos os campos da barra vertical poderão ser consultados por descrição ou código, assim como ocorre na [Consulta Avançada do PdT -Acordo Judicial da Vale](https://www.transparencia.mg.gov.br/eventos-extraordinarios/acordo-judicial-reparacao-vale?task=estado_recursosvale.consultaLivre) na qual é possível digitar o nome ou código nos filtros.
* A lista de filtros será localizada a esquerda da tela. Caso a quantidade de filtros ultrapasse o limite da tela deverá ser utilizada a barra de rolagem.
[Consulta Avançada do PdT -Acordo Judicial da Vale](https://www.transparencia.mg.gov.br/eventos-extraordinarios/acordo-judicial-reparacao-vale?task=estado_recursosvale.consultaLivre)
* O usuário poderá realizar a busca de qualquer filtro na **barra de pesquisa**. A barra de pesquisa deverá possuir atributo [placeholder](https://www.w3schools.com/tags/att_input_placeholder.asp) para facilitar ou indicar como o campo deverá ser preenchido.
* Alguns filtros da barra de navegação também deverão possuir atributos *placeholder*.
* A barra de navegação poderá ser **ocultada/exibida** ([*collapsed Sidebar*](https://www.w3schools.com/howto/howto_js_collapse_sidebar.asp)) a partir dos comandos.
    *	Ocultada => ao clicar no botão **[Ocultar Filtros]**;
    * Exibida => ao clicar no botão **[Mostrar Filtros]**
    * **OBSERVAÇÃO**: Ao ocultar a barra de navegação vertical dos demais conteúdos (tabela de resultados, campos aplicados e etc) serão reajustados na página.

* Ao clicar no símbolo '(⋮) 'será exibida uma outra barra de filtros onde o usuário poderá selecionar outros parâmetros da pesquisa.
* A barra deslizante só será exibida se o usuário clicar em algum filtro  da barra de navegação vertical.
* A barra deslizante será **ocultada** ao clicar em outro filtro.
* Quando a barra deslizante for ocultada e as opções forem selecionadas, a seção em que o usuário se encontra deverá apresentar a quantidade de filtros selecionados.
* Ao clicar sob a **barra de pesquisa** será exibida uma lista suspensa com todos os parâmetros referente ao filtro. Para selecionar o parâmetro desejado o usuário poderá usar a barra de rolagem ou a barra de pesquisa.  
* A barra deslizante deverá listar os parâmetros selecionados com a opção ***['x']() (excluir)***. O usuário poderá remover os parâmetros não desejados clicando no ***['x']()***.
* O usuário poderá combinar vários parâmetros para o mesmo filtro (selecionar mais de um item) ou selecionar a opção ***[Exibir Todos]*** ou ainda clicar no símbolo (⋮)
* Ao selecionar ***[Exibir Todos]***, abrirá uma tela modal exibindo todos os parâmetros daquele filtro com as opções *Selecionar tudo, Limpar Seleção, Inverter seleção*. O usuário poderá remover os parâmetros não desejados ao assinalar com tique a opção.  
* Os botões **Atualizar, Pesquisar e Limpar tudo** devem ser estilisticamente diferenciados (eg. [*Differentiate button types*](https://medium.com/nextux/design-better-buttons-6b64eb7f13bc#aj%20la%20lb))
* Ao selecionar o período específico a barra deslizante de cada filtro irá exibir como parâmetro apenas as classificações orçamentárias vigentes no ano da pesquisa. A exceção será para a consulta de Restos a Pagar, onde os parâmetros da barra deslizante irão refletir apenas as classificações orçamentárias inscritas em restos a pagar, e não a classificação orçamentária vigente no ano.
* A medida que o usuário selecionar um parâmetro de qualquer filtro, automaticamente apenas as opções que possuem relacionamento com o parâmetro selecionado serão exibida nos demais filtros.
  * **Exemplo**:   
Ao selecionar o parâmetro '1521- Controladoria-Geral do Estado' no filtro *Órgão* e em seguida clicar no filtro *Programa* apenas os programas que tiveram execução na Controladoria-Geral do Estado naquele ano serão exibidos.
* Todos os parâmetros selecionados serão exibidos no campo **Filtros Aplicados**.

-> Todas as funcionalidade listadas acima estão disponíveis na consulta do Portal - Acordo Judicial da Vale

![](static/barra-lateral.gif)


### Filtros Aplicados
<a href="#top">(inicio)</a>

* O usuário poderá **ocultar/exibir** o conteúdo do campo filtros aplicados a partir do comandos:
  * **[^]**: Exibir o conteúdo do campo;
  * **[v]**: Ocultar o conteúdo do campo. Ao ocultar os dados do campo, os demais conteúdos da tela serão ajustados na página.


* Como padrão o filtro **Período** será exibido no campo filtros aplicados. O campo será no formato dd/mm/aaaa composto por início e fim (eg. 01/04/2021 a 30/12/2021). Como padrão o campo "Início/Fim" irá exibir exercício vigente até o último dia de atualização dos dados. No campo da data o usuário poderá selecionar ou digitar a data na caixa. Exemplo: Portal de Transparêcia ES;
* O campo filtro aplicados será composto pelos botões: Pesquisar, Atualizar e Limpar Tudo localizados na parte superior:
* A posição na tela dos botões Pesquisar e Atualizar será a mesma, sendo a exibição de um ou outro realizada de acordo com as regras abaixo.
  - **Pesquisar**: será exibido após o usuário selecionar qualquer parâmetro na barra deslizante.  O Usuário deverá clicar em pesquisar para exibir o resultado desejado.
  - **Atualizar**: será exibido quando o usuário remover/adicionar algum parâmetro, ou seja, fizer qualquer alteração no campo filtros aplicados.
  - **Limpar Tudo**: ficará disponível sempre que houver pelo menos um parâmetro selecionado. Ao clicar nesse botão será excluído todo o conteúdo desse campo.

  OBS: Os botões **Pesquisar/Atualizar/Limpar Tudo** devem ser estilisticamente diferenciados (eg. [*Differentiate button types*](https://medium.com/nextux/design-better-buttons-6b64eb7f13bc#aj%20la%20lb))
* O usuário poderá excluir um filtro por completo. Por exemplo, caso o usuário queira excluir o campo 'Órgãos' ele poderá fazer isso sem a necessidade de excluir os filtros um a um. Ele poderá excluir o campo "ÓRGÃO"
* Casos os parâmetros selecionados não retornem nenhuma informação, o PdT deverá apresentar a seguinte mensagem:  '*Não há dados a serem exibidos com os parâmetros selecionados.*''
* Os parâmetros selecionados na barra deslizante deverão ser exibidos na ordem que o usuário escolheu.
* Todos os parâmetros serão representados no campo filtros aplicados da seguinte forma:
  * **Filtro** (*nome do filtro*): **Parâmentro** (*nome do parâmetro*)-(**[X]()**)(*excluir*);
* À medida que o usuário for incluindo parâmetros na pesquisa, a tabela de resultados será deslocada para baixo quando ultrapassar o limite da tela (eg. [Portal de Transparência Federal](http://www.portaltransparencia.gov.br/despesas/programa-e-acao?ordenarPor=programa&direcao=asc)).
* Caso o usuário selecione uma grande quantidade de filtros será acrescida a opção *Ver mais* abaixo da lista de filtros.

-> Todas as funcionalidade listadas acima estão disponíveis na consulta do Portal - Acordo Judicial da Vale

### Tabela de resultados
<a href="#top">(inicio)</a>

* A tabela de resultado levará em consideração os parâmetros do campo filtros aplicados.
* A tabela apresentará colunas padrão que serão exibidas independentemente de o usuário selecionar/aplicar algum filtro.
  **Ver [Especificação Dados](https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/master/espec020_filtros_consulta_despesa/especificacao-despesa-dados.md)**

* A data de atualização dos dados, opção de compartilhamento e download serão exibidos acima da tabela de resultados.

* Os valores **TOTAL GERAL** e o **SUBTOTAL** serão exibidos na tabela de resultados de acordo com o comportamento do usuário. Conforme descrito na pesquisa básica.
* A **barra de pesquisa** da tabela de resultado deverá retornar os dados da tabela que estão exibidos.
A medida que o usuário for digitando os dados a busca será acionada. O atributo *placeholder*: deve ser aplicado na barra de pesquisa.

* O usuário poderá adicionar ou remover colunas - [*hide/show columns*](https://ux.stackexchange.com/a/110079) na tabela de resultados. Ao clicar em **Adicionar/Remover colunas** será exibida uma barra lateral a direta com todas as colunas que poderão ser adicionadas ou removidas.
* Ao exibir ou ocultar alguma coluna a tabela de resultados será atualizada automaticamente (eg.[Column Toggle Table](https://ux.stackexchange.com/questions/110077/best-practices-to-allow-user-to-hide-show-columns-in-a-data-table/110079#110079)).

* O ícone **Adicionar/Remover Colunas** além dos filtros pré-determinados pela DTA terá uma barra de pesquisa onde o usuário poderá digitar o filtro desejado.

* As colunas definidas como padrão ficarão marcadas na tabela ***Adicionar/Remover Colunas*** podendo o usuário desativá-las.<br> Ver [Especificação Dados](https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/master/espec020_filtros_consulta_despesa/especificacao-despesa-dados.md)

* Ao inserir qualquer coluna essas serão incluídas antes das colunas de valores. E caso seja incluída alguma coluna de valor o portal deverá manter a ordem da execução orçamentária (Valor empenhado, valor liquidado, valor pago, valor pago em restos a pagar).

* Os campos clicáveis serão destacados conforme o layout já adotado  pelo PdT e terão a imagem de uma lupa. Para exibir mais informações o usuário deverá clicar na lupa da coluna "detalhar":
  * O 1º nível terá como opção o botão Detalhar o qual direcionará o usuário para o segundo nível, conforme os filtros selecionados, e, em seguida, poderá ser direcionado para o próximo nível e assim por diante.
  * No caso especifico da Consulta de Despesa o último nível da consulta será sempre o formulário de detalhamento que será acessado após o usuário clicar em algum empenho.

  * **OBS** Caso o usuário solicite a exibição da coluna empenho já no 1º nível e este for um valor único, o usuário será direcionado diretamente para o formulário de detalhamento relacionado ao empenho.
  * **Exceção:** Quando o usuário utilizar o filtro ***"Número da Ordem de Pagamento"*** na barra de filtro vertical as colunas abaixo deverão ser exibidas em formato desabilitado, sem a exibição de dados: Valor empenhado e Valor liquidado.
  * Caso o filtro ***"Número da Ordem de Pagamento"*** seja retirado da barra de filtros aplicados a formatação e exibição dos valores dessas colunas seguirá o padrão.

* A única tabela que deverá ser exibida no estilo modal será o formulário de detalhamento. A navegação pelos níveis será exibida normalmente, conforme ocorre na pesquisa básica.

* Todos os filtros selecionados serão exibidos na tabela de resultado.

* A exibição de código e descrição será diferente em cada seção:
  * Barra de pesquisa e filtros aplicados: exibir código e descrição no mesmo campo;
  * Tabela de resultado: exibir apenas descrição. Os códigos serão exibidos apenas se o usuário adicionar a coluna código;

#### Download dos dados:
  * Como regra geral deverá seguir o padrão da pesquisa básica.
  * Opção exportar Planilha (CSV): exibir código e descrição em colunas distintas, independente de o usuário selecionar a opção código na tabela de resultado. O período selecionado deverá ser exibido na primeira coluna da planilha;


#### Observação
- Os dados/tabelas da pesquisa avançada serão os mesmos que constam nas tabelas da pesquisa básica, porém será necessário verificar a granularidade para os devidos cruzamentos. Ver [Especificação de Dados](https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/master/espec020_filtros_consulta_despesa/especificacao-despesa-dados.md)
