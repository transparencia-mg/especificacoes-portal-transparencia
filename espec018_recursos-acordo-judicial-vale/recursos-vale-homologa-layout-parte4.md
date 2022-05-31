

### O resultado da consulta não corresponde ao período selecionado


**Não corrigido** - Verificado em 26/05/2022

Ao selecionar apenas o período de 2022 para o órgão Controladoria Geral do Estado a tabela de resultados apresenta valores zerados e quando é clicado no detalhamento os empenhos listados correspondem ao exercício de 2021.

O empenho citado como exemplo apenas foi inscrito em RP em 2022 não havendo nenhuma execução referente a ele. Nesse sentido, ele deve ser exibido apenas quando houver liquidação e/ ou pagamento .

![](static/imagens/homologacao/empenho-nao-corresponde-periodo.gif)

----

### Trocar nome de 'todas' para 'todos', pois órgão é uma palavra masculina

![](static/imagens/homologacao/todas.png)


---

### Filtro favorecido da consulta por Execução

Ao clicar no filtro 'Favorecido por nome' ou Favorecido por CPF/CNPJ' e não escolher nenhum favorecido e clicar em pesquisar o usuário é direcionado para a página inicial da consulta Por Execução sem nenhuma mensagem.

Caso não seja possível a busca por todos os Favorecido o Portal deve apresentar uma mensagem informando que é preciso selecionar um favorecido, assim como ocorre atualmente nas consultas que se encontram em produção no PDT.

![](static/imagens/homologacao/filtro-favorecido.gif)


---
### Legenda da tabela ao selecionar o filtro favorecido

Ao selecionar um Favorecido a legenda da tabela de resultados não está sendo exibida.

Exemplo: [Consulta de Despesa](https://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-favorecidos/2022/01-01-2022/31-12-2022/0/CONSTRUTORA%20CENTRO%20LESTE%20ENGENHARIA/0/3)


![](static/imagens/homologacao/filtro-favorecido-legenda.gif)


---

### Formatação dos textos

As preposições da legenda das tabelas estão com a inicial em maiúsculo.
O fato está acontecendo no cabeçalho de todas as consultas.

![](static/imagens/homologacao/preposicoes.png)


---

### EXIBIR/OCULTAR FILTROS

Conforme sugestão, favor desabilitar o botão onde não há coluna a ser exibida.

Mensagem Prodemge

> Nota: Sugiro que o botão exibir/oculta código fique desabilitado ou invisível nas consultas onde não há coluna de código a ser exibida. Assim que confirmado, podemos realizar o ajuste

---


### SUBTOTAL

**Não corrigido** - Verificado em 26/05/2022

Conforme documentação a opção SUBTOTAL só deve aparecer quando for aplicado algum filtro ou houver paginação dos dados.

Exemplo 1 - Não existe paginação, porém ao usar algum filtro a opção subtotal não é exibida.

Exemplo 2 - Existe paginação, porém ao solicitar a exibição de todas as linhas o valor subtotal ainda é exibido.


**Exemplo 1**

![](static/imagens/homologacao/subtotal-paginacao.gif)


**Exemplo 2**

![](static/imagens/homologacao/subtotal-paginacao2.gif)

---
### Legenda do Gráfico

**Consulta Por Execução - Gráfico de barras:** Trocar a legenda valor liquidado para "Valor Total Pago", pois o gráfico refere-se ao valor total Pago

![](static/imagens/homologacao/legenda-grafico1.png)


**Consulta Transferência por Município - Gráfico de barras:** Trocar a legenda valor liquidado para "Valor Pago", pois o gráfico refere-se ao valor Pago.

![](static/imagens/homologacao/legenda-grafico2.png)

**Consulta Por Receita - Gráfico de barras:**

1.  O gráfico deve-se referir a Classificação da Receita e não a Fonte de Recurso;
2.  Trocar a legenda valor liquidado para "Valor Arrecadado".

![](static/imagens/homologacao/legenda-grafico3.png)

---

### Título do Gráfico

O título dos gráficos de barra devem ser 'Série Histórica'

![](static/imagens/homologacao/legenda-grafico4.png)

---
### Valores do Gráfico

Os valores do gráfico de barras da consulta Transferência por Município não coincide com a tabela

![](static/imagens/homologacao/valor-grafico.gif)

### Campos clicáveis

A funcionalidade foi aplicada apenas na consulta básica a pesquisa avançada ainda está pendente


### MIGALHAS / CABEÇALHO

**Não corrigido** - Verificado em 26/05/2022

Ao selecionar um projeto pelo código na 'Consulta por Execução' tanto a árvore quanto o cabeçalho deve exibir o **Nome do projeto e o código do Projeto**, pois caso o usuário clique no projeto 9288133 e nesses campos apresentar apenas a descrição ele poderá ficar perdido onde está realmente.

Nesse questionamento foi realizado a alteração para exibição do Órgão. Essa alteração foi interessante, porém a descrição e código do Projeto norteia o cidadão no caminho por onde ele navegou.












### Filtro por Órgão

Ao selecionar o período de 01/01/2021 a 31/12/2021 e o órgão: 'Departamento de Edificações e Estradas de Rodagem do Estado De Minas Gerais' o PDT retorna a mensagem "*Nenhum resultado encontrado*", porém existem dados para o período selecionado quando solicita a exibição de todos os órgãos









O comportamento da barra de rolagem vertical não permite a vizualização dos dados do início da tabela #71
https://github.com/transparencia-mg/especificacoes-portal-transparencia/issues/71 [^]


-Link do Compartilhar > Copiar Linknão abre de detalhamento em novo formulário de acesso #72
https://github.com/transparencia-mg/especificacoes-portal-transparencia/issues/72 [^]

-Nome incorreto para seção Dados do Processo de Compra no formulário de detalhamento #73
https://github.com/transparencia-mg/especificacoes-portal-transparencia/issues/73 [^]


2- O campos clicáveis não estão em destaque, conforme ocorre atualmente no pdt. Assim o usuário poderá clicar tanto na lupa como no código o projeto, como por exemplo. (A FAZER)
