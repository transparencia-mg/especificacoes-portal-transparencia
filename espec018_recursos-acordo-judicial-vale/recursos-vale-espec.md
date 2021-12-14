---
contrato_manutencao: nº 15210010062019 (INF. 3951)
proposta_comercial:
mantis:
pull_request: '[]()'
titulo: Transparência dos recursos da Vale - Acordo Judicial 04/02/2021
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da demanda
<a href="#top">(inicio)</a>

Essa demanda visa a criação de uma seção que busca possibilitar o acompanhamento das ações desenvolvidas pelo governo do estado com recursos provenientes do acordo judicial firmado com a Vale. Considerando a relevância e os valores envolvidos no acordo, a seção será um instrumento de transparência e prestação de contas colocando em evidência a execução do acordo.

Juntamente com a criação da nova seção será implementado no PDT algumas necessidades dos usuários identificadas durante o projeto 'Experiência do Usuário no Portal da Transparência', como por exemplo:

- Alteração do Formulário de Detalhamento;
- Uma pesquisa básica mais intuitiva e dinâmica;
- Inclusão de informações;
- Consolidação os dados de Despesa e RP em uma única consulta.


# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

O Governo de Minas, o Ministério Público de Minas Gerais (MPMG), o Ministério Público Federal (MPF) e a Defensoria Pública de Minas Gerais (DPMG) assinaram um termo de Medidas de Reparação, no dia 4 de fevereiro de 2021, que garante que a empresa Vale seja imediatamente responsabilizada pelos danos causados às regiões atingidas e à sociedade mineira pelo rompimento da barragem Mina Córrego do Feijão, em Brumadinho, em 2019.

O documento define “obrigações de fazer” e “obrigações de pagar” da Vale e prevê um total de recursos a serem aplicados em reparação socioambiental e socioeconômica de R$ 37.689.767.329,00 (trinta e sete bilhões, seiscentos e oitenta e nove milhões, setecentos e sessenta e sete mil, trezentos e vinte e nove reais). Destes, R$11.060.000.000,00 (onze bilhões e sessenta milhões) serão de gestão do Poder Executivo estadual para execução de projetos de mobilidade (anexo III), fortalecimento do serviço público (anexo IV), segurança hídrica (anexo II.3) e ressarcimento de despesas decorrentes da execução do referido Termo Judicial.

A Lei nº 23.830/2021, publicada em 28/07/2021, autorizou abertura de crédito suplementar ao orçamento do Estado em função dos recursos previstos no Termo de Reparação que deverão ser alocados conforme consta no Acordo Judicial.


# Especificação
<a href="#top">(inicio)</a>

Esse documento tem como base a criação de uma nova consulta possibilitar o acompanhamento das ações desenvolvidas pelo governo do estado com recursos provenientes do acordo judicial firmado com a Vale .

## Página Inicial da consulta - Pesquisa Básica
<a href="#top">(inicio)</a>

### Texto explicativo
<a href="#top">(inicio)</a>

Inclusão de um campo que irá trazer uma breve explicação do conteúdo da consulta.  

Atributos do campo:

* O usuário poderá exibir mais detalhes do texto ao clicar em "*Saiba Mais*" ou ocultar ao clicar "*Ocultar*". [eg. Leroy Merlin](https://www.leroymerlin.com.br/materiais-hidraulicos).

* A funcionalidade deverá permitir a visualização de *tooltip* ao posicionar o mouse sobre uma palavra ou termo. [eg. tooltips](https://getbootstrap.com.br/docs/4.1/components/tooltips/)

* Ao clicar sobre a palavra ou termo da funcionalidade anterior o PdT deverá abrir um um *pop-up* qem forma de glossário. [eg. pop-up](https://www.usaspending.gov/)

* O PdT deverá permitir que por meio da área administrativa do Portal a equipe DTA inclua ou altere os dados desse campo incluindo os *tooltips*.

### Leiaute - Barra de navegação
<a href="#top">(inicio)</a>

A barra de navegação será composta pelos seguintes campos:

* Tipo de consulta;
* Período (início/fim): formato mmmm/aaaa
* Opção de filtrar conforme o tipo de consulta selecionado;
* Botão *'Monte sua consulta'*



### Leiaute - Tabelas navegação por filtros
