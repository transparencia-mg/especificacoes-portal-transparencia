---
contrato_manutencao: nº 15210010062019 (INF. 3951)
proposta_comercial:
mantis:
pull_request:
titulo: Anonimização dos CPFs de todas as Consultas do Portal
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da demanda
<a href="#top">(inicio)</a>

Essa demanda visa anonimizar os CPFs de credores pessoas físicas nas seguintes consultas:

* Concursos Realizados;
* Despesa;
* Restos a Pagar;
* Diárias e
* Viagens.

O método de anonimização deve ser aplicado nos resultados de todas as consultas citadas que apresentem informação de CPF, bem como nas funcionalidades de exportação de dados.

As informações devem ser armazenadas de forma completa no banco de dados do Portal, permitindo inclusive a realização de buscas nos campos anonimizados.

# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

A divulgação do CPF está sendo objeto de questionamento frequente no canal “Fale Conosco” do Portal da transparência, principalmente após a publicação da Lei Federal nº 13.709, de 14 de agosto de 2018 (LGPD), que versa sobre a proteção de dados pessoais.

A aprovação da LGPD trouxe para a discussão o tema privacidade e proteção de dados pessoais, provocando a necessidade de um debate em torno dos limites do tratamento de dados pessoais pelo poder público e, por consequência, as implicações da aplicação da LGPD na política de transparência, em especial, para a CGE, em relação à forma de divulgação dessas informações no Portal.

Nesse sentido, o Grupo de Trabalho instituído pela Resolução Conjunta SEPLAG/CGE/SEF/AGE/PRODEMGE nº 10.064, de 29/7/2019, emitiu a Consulta Jurídica SEPLAG/SUBGOVES nº 01/2020, que versa sobre a publicização de dados pessoais no Portal da Transparência, à Advocacia Geral do Estado .

Em resposta ao Grupo de Trabalho, a Advocacia Geral do Estado emitiu o Parecer Jurídico AGE 16.248. Abaixo segue a conclusão da AGE quanto aos questionamentos do Grupo de Trabalho:

> **III. Da Consulta**
>
>21.(...)      
a) que o Portal de Transparência do Estado divulgue no módulo “Concursos Realizados”, em relação aos candidatos classificados, o nome completo somado ao CPF descaracterizado;
>
> b) a manutenção da publicização da íntegra dos contratos administrativos, descaracterizando-se ou ocultando-se dados pessoais que não o nome e o CPF do representante legal do órgão, entidade, ou contratado, quando houver, ao argumento de que outros dados pessoais, como o endereço residencial,
diferentemente do endereço institucional ou comercial, não decorrem da relação da pessoa com o Estado; e
>
> c) no caso das "Despesas, Restos a Pagar, Diárias e Viagens", a divulgação do nome completo, com a descaraterização do número do CPF do credor da despesa pública, inclusive no caso de folha de pagamento de pessoal e de benefícios previdenciários.
>
>**IV. Conclusão**
>
>Em conclusão, ao responder aos questionamentos que nos foram formulados, somos de **opinião favorável à adoção das soluções pensadas pela consulente**. Seja pela **descaracterização de parte do número CPF** e de outros documentos de identificação civil de **candidatos aprovados em concursos públicos, representantes de sociedades e entidades contratantes e credores do Estado**. Seja pela ocultação de dados pessoais adicionais constantes de termos negociais entabulados pelo Estado. Entendendo-as, quando avaliadas em sua razoabilidade e legalidade, adequadas a dar cumprimento a ditames que, à primeira vista, mas de forma meramente aparente, seriam contraditórios. Preservando-se, de tal modo, o dever de transparência sedimentado na Lei de Acesso à Informação e o dever de proteção  dados pessoais de que trata, de forma sistematizada, a Lei Geral de Proteção de Dados.

# Especificação
<a href="#top">(inicio)</a>

Inicialmente, cabe destacar que todos os registros devem ser carregados novamente na base de dados do Portal da Transparência, de forma que todos os CPFs fiquem anonimizados.

A anonimização deve ser aplicada em:

* Gráficos e tabelas do nível favorecido (ex. Despesa ; RP;  Diárias e Viagens);
* Formulários de detalhamento de documentos ex. Despesa ; RP;  Diárias e Viagens);
* Tabela do nível nome do classificado (ex. Concursos realizados);
* Pesquisa avançada;
* Imprimir página;
* Exportar para csv;
* Exportar para pdf.

## Concursos Realizados
<a href="#top">(inicio)</a>

### Método de anonimização

A anonimização deve ser aplicada no nível 'Nome do Classificado' em todos os filtros da consulta [Concursos Realizados](http://transparencia.mg.gov.br/estado-pessoal/concursos-realizados/concursos-orgaos-demandantes/2018/01-01-2018/31-12-2018/1/17/17/97) que possuem informação de CPF.

O método de anonimização consiste em:

* Substituir o CPF do candidato classificado pelo valor "000.000.000-00".

As regras acima devem ser aplicadas inclusive no caso em que o nome e CPF sejam apresentados no mesmo campo. No banco de dados do Portal da Transparência, as informações de CPF devem ser armazenadas sem anonimização, permitindo filtros que utilizem essas informações.

#### Exemplo:

Ao acessar o nível 'Nome do Classificado', o Portal deverá exibir:

| Nome do Classificado | CPF |
|---|---|
ADRIA DE LIMA SOUSA|000.000.000-00|
* ***Obs: As demais colunas não sofrerão alterações***

![](static/espec-anonimizacao-concursos.png)

## Consultas Despesa, Restos a Pagar, Diárias e Viagens
<a href="#top">(inicio)</a>

### Método de anonimização

A anonimização deve ser aplicada no nível 'Favorecido' de todos os filtros das consultas [Despesa](http://transparencia.mg.gov.br/despesa-estado/despesa/despesa-orgaos/2020/01-01-2020/31-12-2020/4015/1914/533/20/42), [Diárias](http://transparencia.mg.gov.br/estado-pessoal/diarias/despesadiarias-programas/2020/01-01-2020/31-12-2020/4026), [Restos a Pagar](http://transparencia.mg.gov.br/despesa-estado/restos-a-pagar/restospagar-orgaos/2020/4015/533/42/20/2798/130/58) e [Viagens](http://transparencia.mg.gov.br/estado-pessoal/viagens/estado_viagens-consulta/21/01-01-2020/31-12-2020/2020) que possuem informação de CPF.

O método de anonimização consiste em:

* Substituir o CPF do credor (favorecido) pelo valor "000.000.000-00".

A regra acima devem ser aplicada inclusive no caso em que o nome e CPF sejam apresentados no mesmo campo. No banco de dados do Portal da Transparência, as informações de CPF devem ser armazenadas sem anonimização, permitindo filtros que utilizem essas informações.

**Exemplos**:

Ao acessar o nível 'Favorecido por nome' ou 'Favorecido por CNPJ/CPF' o Portal deverá exibir:

### Consulta Despesa
| Favorecido | CNPJ/CPF | Item de despesa | Valor Empenhado |Valor Liquidado| Valor Pago|
|---|---|---|---|---|---
MARCOS SAULO DE CARVALHO|000.000.000-00|DESPESAS MIUDAS DE PRONTO PAGAMENTO| 10.000,00|10.000,00|10.000,00|

![](static/espec-anonimizacao-despesa.png)

* **Formulários de detalhamento de documentos**

Ao acessar os formulários de detalhamento, os seguintes campos devem ser anonimizados:

=> Campo ___Razão Social do Credor, CNPJ/CPF e Descrição do Favorecido___ do formulário de empenho da despesa:

![](static/espec-anonimizacao-despesa-detalhamento.png)

### Consulta Restos a Pagar

| Favorecido | CNPJ/CPF | Número do empenho | Valor Inscrito Processado |Valor Inscrito não Processado| Valor Pago no ano| Valor a pagar
|---|---|---:|---:|---:|---:|---:
MARCOS SAULO DE CARVALHO|000.000.000-00|85| 10.000,00|30.000,00|10.000,00|20.000,00

![](static/espec-anonimizacao-restosapagar.png)

* **Formulários de detalhamento de documentos**

Ao acessar os formulários de detalhamento, os seguintes campos devem ser anonimizados:

=>Campo ___Razão Social do Credor, CNPJ/CPF e Descrição do Favorecido___ do formulário de empenho da despesa:

![](static/espec-anonimizacao-despesa-detalhamento.png)

### Consulta Diárias

|Favorecido| CNPJ/CPF|  Valor Empenhado |Valor Liquidado| Valor Pago|
|---|---|---:|---:|---:
MARCOS SAULO DE CARVALHO|000.000.000-00|10.000,00|10.000,00|10.000,00|

![](static/espec-anonimizacao-diarias.png)


* **Formulários de detalhamento de documentos**

Ao acessar os formulários de detalhamento, os seguintes campos devem ser anonimizados:

=> Campo ___Razão Social do Credor, CNPJ/CPF e Descrição do Favorecido___ do formulário de empenho da despesa:

![](static/espec-anonimizacao-despesa-detalhamento.png)

### Consulta Viagens

|Favorecido | CNPJ/CPF | Cargo | Órgão| Quantidade de Viagens| Quantidade de Diárias |Valor Pago Diárias|Valor Pago Passagens| Valor Total|
|---|---|---|---|---|---|---:|---:|--:
MARCOS SAULO DE CARVALHO|000.000.000-00| Auditor Fiscal| Secretária de Estado da Fazenda|1,00|1,00|0,00|0,00|0,00

![](static/espec-anonimizacao-viagens.png)

* **Formulários de detalhamento de documentos**

Ao acessar os formulários de detalhamento, os seguintes campos devem ser anonimizados:

![](static/espec-anonimizacao-viagem-detalhamento.png)


***OBSERVAÇÕES GERAIS***

* Na pesquisa avançada, a anonimização deve ocorrer quando o usuário marcar o campo ___exibir favorecidos___.

* Ao digitar o CPF de um favorecido na consulta 'Favorecido por CPF / CNPJ', o Portal deve exibir a consulta completa anonimizando os dados do favorecido.

* Os dados na migalha de pão (caminho da pesquisa) devem ser anonimizados quando exibir o número do CPF;

* Ao realizar uma anonimização, o Portal deve continuar a exibir as transações de forma separada.

* A anonimização deve ser aplicada na árvore da consultas

![](static/espec-anonimizacao-arvore.png)
