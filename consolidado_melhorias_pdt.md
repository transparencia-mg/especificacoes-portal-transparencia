# Consolidado de melhorias a serem implementadas no Portal de Transparência

## Dívida Pública
<a href="#top">(inicio)</a>

Foi questionado pela equipe da SEF - Diretoria Central de Gestão da Dívida Pública  que os valores publicados no portal da Transparência, ano 2021, referentes aos valores da Dívida Pública do Estado MG encontram divergentes dos valores publicados no portal da dívida.
Nesse sentido a DTA realizou um comparativo entre as informações disponibilizadas pela SEF e PDT e foi identificado a utilização de outros filtros(campos) diferente dos utilizados pela DTA.

A nova especificação conforme dados da SEF está disponível em - [Especificação](https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/espec021_divida-publica/espec021_divida-publica/especificacao-divida-publica.md) <br>

## Concursos Realizados
<a href="#top">(inicio)</a>

#### Problema 1:
O PDT não apresenta a data da nomeação de candidatos nomeados judicialmente.  

Exemplo: Candidato Carlos Henrique de Oliveira -Edital SEPLAG/SED nº 08/2013 - 
[Portal da Transparência](https://www.transparencia.mg.gov.br/estado-pessoal/concursos-realizados/concursos-orgaos-demandantes/2013/01-01-2013/31-12-2013/1/3/3/43)

![Screenshot_1](https://user-images.githubusercontent.com/53793354/192311745-bb831f53-866b-45be-b385-af6d8c6c1f99.png)


## Despesa
<a href="#top">(inicio)</a>

## Restos a Pagar
<a href="#top">(inicio)</a>

## Receita
<a href="#top">(inicio)</a>

## Compras e Contratos
<a href="#top">(inicio)</a>

#### Problema 1:
Consulta de Compras e contratos apresenta apenas os contratos, para uma melhor transparência dos dados seria necessário apresentar informações de autorização de serviço e ordem de serviço do Portal de Compras para os processos que não possuem contrato.  

Exemplo: PROCESSO CGE 1521001 000011/2022 https://www1.compras.mg.gov.br/processocompra/processo/abaHistoricoOsAf.html?aba=abaHistoricoOsAf&id=612610&metodo=visualizar

#### Problema 2:
O formulário de detalhamento da apresenta apenas os dados dos empenhos. Para adequação as normas é necessário apresentar também a liquidação e pagamento de todos os empenhos relacionados aos contratos.

A solução proposta é a adequação do formulário de detalhamento nos moldes da consulta da Vale que ao clicar no nº do empenho o usuário terá acesso a toda a execução.

#### Problema 3:
Ao clicar no número do processo de compra no formulário de detalhamento o usuário é direcionado para o Edital do processo quando a informação é existente, porém o PDT não é claro quanto a qual informação será exibida. A sugestão é a alteração do formulário de forma que fique claro qual dado será exibido ao clicar no campo "Processo de Compra" 

[Nº do Processo de Compra: 1261556 000089/2022](https://www.transparencia.mg.gov.br/compras-e-patrimonio/compras-e-contratos/comprasecontratos-procedimento/0/2022/01-01-2022/27-09-2022/1831044/7/0/0/17/3/379/301/17564/3010031/94354/1015/375425/1261556000089-2022)

![image](https://user-images.githubusercontent.com/53793354/192615838-7db5e071-8ed9-4c30-bec4-8df265b3c537.png)

#### Problema 4:

 - Inclusão do número da Nota Fiscal e chave de acesso;
 - Incluir a vigência do Contrato nas tabelas - Consulta de Compras e Contratos;


## Convênio de Entrada
<a href="#top">(inicio)</a>

#### Problema 1:
A inclusão será realizada alterando o layout do formulário de detalhamento e incluindo o item do SIAFI - Data Registro Doc Arrecadação. 
**NOTA** Essa alteração deverá ser incluída na reformulação do formulário de detalhamento.

![image](https://user-images.githubusercontent.com/52920939/188449968-37862f4f-a151-404c-9c5a-9812e04dd1d2.png)

#### Problema 2:
- Atualmente o PDT apresenta apenas os convênios de entrada com Plano de Trabalho SIAFI tipo: Convênio de entrada, porém existem outros tipos. Verificar a transparência desses outros tipos.
- 
![image](https://user-images.githubusercontent.com/53793354/188454054-9434e31a-a27c-435a-9b46-ad5635ea734a.png)


## Convênio de Saída
<a href="#top">(inicio)</a>

#### Problema 1: 
Alguns valores dos convênios que estão no PDT estão classificados como "recurso de emenda parlamentar", mas deveriam estar classificados como "recurso concedente". As divergências ocorrem porque o  campo "VALOR PARLAMENTAR ATUAL' do sistema transacional SIGCON-SAÍDA é utilizado tanto  para recursos de emendas parlamentares e para convênios celebrados com recursos concedentede uma fonte especifica. Como o PDT extrai a informação diretamente do SIGCON não é possível atualmente fazer essa diferenciação entre os valores pois na view disponibilizada eles estão na mesma categoria.

Nesse sentido, segundo ainda a SEGOV será necessário é alterar alguma regra de leitura do dado no momento da disponibilização no Portal.

[Detalhes do problema](https://trello.com/c/uFIGPEC1/1081)

## Remuneração
<a href="#top">(inicio)</a>

#### Problema 1: 
Perda do histórico da remubnetação do servidor.
Atualmente quando o servidor troca de nome, por exemplo, acrescenta ou retira algum nome, o Portal de Transparência não consegue resgatar e apresentar todo os histórico de sua remuneração. O mesmo erro ocorre quando o servidor possui mais de um cargo no estado.
Isso é devido pois o PDT utiliza como chave além da carga horária o nome do servidor para apresentar o histórico.

Para solucionar esse problema deverá ser incluido funcionalidade de número de admissão como chave primária na tabela do portal. Atualmente todas as planilhas rececebidas pea DTA já possuem essa coluna.

#### Problema 2: 
Equalizar as informações disponibilizadas no PDT com as informações do TCE - CAPMG.
A ideia inicial é alterar a fórmula de cálculo dos descontos do PDT para apresentarmos as mesmas informações do TCE.

#### Problema 3: 
Inserir no PDT a lista de todos os servidores por carreira independente da remuneração

#### Problema 4: 
Criar uma nova opção "Carreiras" dentro do menu de acesso rápido na consulta de Remuneração
Essa opção pode ser incluída na remodelagem das página intermediárias

## Despesa de Pessoal
<a href="#top">(inicio)</a>

#### Problema 1:
Atualmente a consulta de despesa de pessoal d PDT encontra-se divergente da dados disponibilizados pela Secretaria de Fazenda. Nesse sentido será necessário a intervenção nessa consulta

Ajustamos os dados da consulta no armazém e passando a apresentar todas as despesas do Grupo Despesa: Pessoal e Encargos Sociais, a consulta evidenciou um valor bem mais próximo do que o divulgado no [Relatório de Gestão Fiscal de 2021](http://www.fazenda.mg.gov.br/governo/contadoria_geral/gestaofiscal/ano2021/):
![image](https://user-images.githubusercontent.com/52920939/194880144-b3c04eb7-7f2c-4284-8592-dfb076da3b7c.png)

Necessitando agora entender quais os elementos itens de despesa devem ser descartados da consulta do portal.
![image](https://user-images.githubusercontent.com/52920939/194880260-083f3661-d792-48c5-a179-44269fc9f2a6.png)
![image](https://user-images.githubusercontent.com/52920939/194880318-e3594ad6-15be-4e8c-9657-642057a660a1.png)


## Acordo Judicial de Reparação da Vale
<a href="#top">(inicio)</a>

#### Problema 1:
Trocar a ordem das colunas para: Valor empenhado, Valor Liquidado, Valor Liquidado RP, Valor Pago, Valor Pago RP, Valor Total Pago

## PPAG
<a href="#top">(inicio)</a>

## Proposta e Lei Orçamentária
<a href="#top">(inicio)</a>

## Diárias
<a href="#top">(inicio)</a>

#### Problema 1:
A consulta de diárias apresenta apenas o nome do CPF administrativos dos servidores civis.
Para solucionar esse problma será preciso alterar o credor beneficiário da Diária, passando a trazer informações do Credor beneficiário e não mais do CPF administrativo.

## Viagens
<a href="#top">(inicio)</a>

## Layout - Pesquisa Avançada

A remodelagem e a elaboração da pesquisa avançada deverá seguir os moldes da pesquisa avançada da consulta 'Acordo Judicial de Reparação da Vale'.

- Remodelagem
  - Despesa
  - Restos a pagar
  - Receita
  - Proposta Orçamentária
  - Alteração Orçamentária
  - Crédito Orçamentário
  - Obras Orçadas

- Elaboração
  - Concursos Realizados
  - Diárias
  - Emendas
  - PPAG

## Layout - Página Inicial

O objetivo é torná-la autoexplicativa. Para isso, tanto o design a quanto navegação, devem ser intuitivos, de forma a deixar claro para o usuário como o PdT funciona.

A página inicial deve reduzir ao máximo os pontos intermediários de interação para que, com poucos cliques, os usuários cheguem às informações desejadas permitindo assim que ele veja claramente quais dados estão disponíveis. Abaixo segue as principais intervenções:

1) Alterar e melhorar a navegabilidade do menu superior e do menu de acesso rápido:

  - Alteração do menu superior, reorganizando as informações para possibilitar o acesso a todo conteúdo de forma mais rápida.  eg. 	Menu no formato *dropdown*;
  - diferenciar quais informações são internas (eg. consulta do PdT - Despesas) e quais são externas (eg. Obras Públicas)
  - Criar novos ícones para as consultas;
  - Inclusão da barra de acessibilidade;

2) Reorganizar as informações da página inicial:
  - Alterar a cor de fundo;
  - Criar menu de acesso rápido (consultas mais acessadas);
  - Centralização dos canais de atendimento.
  - Alteração do menu de acesso de rápido de forma que o usuário visualize todos os dados com menor número de cliques possíveis;
  - Reorganização da área de notícias

3) Barra de Busca:
  - o campo deve possibilitar que um determinado dado seja encontrado
 de forma mais rápida e por vários caminhos possíveis;
  - inclusão da ferramenta *placeholder* indicando o que o usuário pode buscar, como órgão, Município, CNPJ de empresa conveniada ou nome de servidor.

4) Acesso à área administrativa pela DTA
  - Essa funcionalidade permitirá que a equipe DTA realize alterações e acrescente informações a serem exibidas no painel de destaque da página inicial. A área administrativa do Portal deverá permitir que a equipe da DTA altere o texto explicativo das pesquisa básica, bem como os termos que ficarão em destaque

5) Criação do Mapa do site
  - O mapa do sítio deve ser disponibilizado em forma de lista hierárquica (utilizando os elementos de lista do HTML), podendo conter quantos níveis forem necessários

6) Barra de Início Fixa
  - Fixar a barra inicial ao rolar página das consultas

7) Fale Conosco:
  - inserir o link de dúvidas frequentes na página do formulário do fale conosco e o link do fale conosco próximo ao dúvidas frequentes.

8) Corrigir a lentidão na pesquisa avançada da consulta Receita Pública

## Layout - Remodelagem das páginas intermediárias do Portal

As páginas intermediárias deverão seguir o mesmo padrão das páginas intermediarias do menu de acesso rápido.

Todas as consultas deverão ter página intermediárias, incluindo as páginas quee possuem apenas uma sessão, como por exemplo a consulta da Receita.

A área administrativa do Portal deverá permitir que a DTA altere o conteúdo de todas as páginas intermediárias.

> Pensar na questão da data de atualização do conteúdo estático das páginas intermediárias

## Layout - Remodelagem da Pesquisa Básica

A Remodelagem deverá seguir os moldes da pesquisa 'Acordo Judicial de Reparação da Vale' nas seguintes consultas:

1) COVID-19    
- Compras - Programa de enfrentamento COVID 19.

2) Despesa  
- Despesa;
- Restos a Pagar;
- Mapa de Investimento;

3) Receita

4) Planejamento e Resultados
  - Proposta Orçamentária
  - Emendas Orçamentária
  - Alteração Orçamentária
  - Obras Orçadas
  - Crédito Orçamentário
  - PPAG Consolidado
  - PPAG por Programa

5) Pessoal
  - Despesa com Pessoal
  - Remuneração dos Servidores
  - Diárias
  - Viagens
  - Concursos Realizados

6) Convênios e Parcerias
  - Convênios de Entrada
  - Convênio de Saída

7) Transferência de Impostos a Municípios

8) Compra e Patrimônio
  - Compras e Contratos
  - Gestão da Frota
  -  Patrimônio

9) Dívida Pública
 - Execução da Dívida

A remodelagem deve considerar a alteração dos formulários de detalhamento de todas as consultas com as seguintes novas funcionalidades:
  - modal
  - uma aba para cada conjunto de informações (classificação orçamentária, empenho, liquidação, pagamento, outras informações)
  - visualização dos dados de despesa e restos a pagar de acordo agrupados por estágio de despesa (empenho, liquidação e pagamento)

## Layout - Partição dos anos

O Portal de Transparência deverá permitir que o cidadão busque informações, na pesquisa avançada, por mais de um exercício simultaneamente, a exemplo do modelo implantado na Pesquisa Avançada da Consulta da Vale.

Por exemplo, na consulta de despesa, o usuário poderá comparar dados de programa, função, UO, Ação e etc entre exercícios distintos, bem como poderá pesquisar os valores pagos a um determinado credor em um intervalo de tempo.

Exemplo: [Portal de Transparência de Linhares](https://linhares-es.portaltp.com.br/consultas/despesas/empenhos.aspx)


## Consolidar os dados de Despesa e RP em uma única consulta

Remodelagem das consultas despesas e restos a pagar de forma que as todas as etapas (empenho, liquidação, pagamento do exercício corrente e pagamento dos valores inscritos em RP) sejam apresentadas em uma única consulta.

Exemplo:
- [Portal de Transparência Distrito Federal](http://www.transparencia.df.gov.br/#/despesas/acao)

- [Portal de Transparência Federal](http://www.portaltransparencia.gov.br/despesas/orgao?ordenarPor=orgaoSuperior&direcao=asc)

## Restos a Pagar

 - Alterar a consulta (fórmula de cálculo das colunas) para alinhar com as informações com os dados disponibilizados pela Secretaria de EStado de Fazendo no Relatório Resumido de Execução Orçamentária - [RREO](http://www.fazenda.mg.gov.br/governo/contadoria_geral/lrf/2021/).


## Possibilidade do usuário consultar todas as etapas da Programação Orçamentária

Possibilitar que o usuário verifique todas as etapas (Crédito Inicial + Alteração + Empenho + Liquidação + Pagamento + RP) da Programação e Execução Orçamentária em um único local.

A sugestão que esses dados possam ser verificados na pesquisa avançada e na pesquisa básica de despesa.

Exemplo:
- [Portal de Transparência do Estado de São Paulo](https://www.fazenda.sp.gov.br/SigeoLei131/Paginas/FlexConsDespesa.aspx)

![](static/programa-execu-orcamentaria.png)


## Layout - Inclusão da barra de dúvidas e canais de atendimento

A barra de dúvidas e canais de atendimento devem estar presentes em todas as páginas do PdT assim com ocorre com o ícone de acessibilidade.
 - Barra de dúvidas: o usuário pode procurar qualquer assunto.  
      - Ao clicar no ícone dúvidas será aberto um popup para o usuário digite o termo que deseja pesquisar. Inicialmente a busca será realizada no glossário, perguntas frequentes e no manual de navegação.

Exemplo: [Portal de Transparência Federal](http://www.portaltransparencia.gov.br/despesas/orgao?ordenarPor=orgaoSuperior&direcao=asc)

![](static/barra-duvidas.png)

 - Canais de atendimento:	O usuário será direcionado para a página canais de atendimento do PdT

## Layout - Inclusão de novo canal de compartilhamento

Inclusão do canal de compartilhamento pela rede social WhatsApp em todas as páginas do PdT.

## Layout - Implementação da ferramenta de feedback

Implementação da ferramenta de feedback para o PdT, com o objetivo de coletar informações dos usuários do Portal sobre o que eles querem e o que eles precisam.

A ferramenta proposta pretende por meio de coleta de informações dos usuários identificar erros, melhorias e evoluções necessárias para o atendimento das demandas da sociedade. 

Exemplo: [Portal de Transparência Distrito Federal](http://www.transparencia.df.gov.br/#/despesas/acao)

![](static/feedback1.png)

![](static/feedback2.png)


