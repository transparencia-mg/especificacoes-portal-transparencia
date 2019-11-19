---
titulo: "Filtro do Servidor"
pull_request: https://github.com/transparencia-mg/especificacoes-portal-transparencia/blob/feat/especificacao-filtro-servidor/espec005_filtro-servidores/especificacao-filtro-servidor.md
---
  
# Visão geral da demanda

Essa demanda visa criar o filtro *vínculo do servidor* na página inicial da consulta de **Remuneração de Servidores** para a possiblitar a consulta de servidores ativos, inativos e pensionistas.


# Motivação / contexto da demanda
A criação do filtro vínculo do servidor é importante para atender a uma demanda da sociedade, via Fale Conosco e 59622, que necessita realizar consultas de servidores inativos e pensionistas.

O formato atual de divulgação no Portal da Transparência apresenta apenas a lista total dos servidores, não diferenciando os servidores ativos e inativos.

![](static/filtro.png)

Só se conhece a sitaução funcional de servidor (ativo ou inativo), quando se acessa o detalhamento dos dados funcionais desse servidor (Situação Funcional - Descrição Situação do Servidor).

![](static/detalhamento_servidor.jpg)

Assim, ao criar o filtro Vínculo do Servidor, será possível visualizar a quantidade de servidores ativos, inativos e pensionsitas.

#Especificação

## Filtro Vínculo do Servidor

### Página Inicial

O cidadão seleciona na consulta os filtros 
- Nome do Servidor
- Cargo Efetivo
- Cargo em Comissão
- Órgão
- Situação do Servidor


No filtro "Nome", será possível escolher umas das 4 opções abaixo:
- Ativo
- Inativo
- Pensionista
- Designado ao serviço ativo

![](static/filtro.png)

Ao clicar em pesquisar, a consulta exibirá a lista do servidores que se encontram no filtro pesquisado.

Dependências / Integrações
Não se aplica

Exemplos / Pesquisa

Governo do [Distrito Federal](http://www.transparencia.df.gov.br/#/servidores/remuneracao)
![](static/distritofederal.jpg)

Prfeitura de [Curitiba](https://www.transparencia.curitiba.pr.gov.br/meta4/servidores.aspx)
![](static/curitiba.jpg)

![](static/filtros.jpg)

![](static/exemplos.jpg)

Dúvidas

