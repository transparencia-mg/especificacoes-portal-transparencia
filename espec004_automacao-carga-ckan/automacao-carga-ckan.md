---
pull_request: '[espec001](https://github.com/transparencia-mg/especificacoes-portal-transparencia/pull/1)'
titulo: Fluxo ETL no CKAN da CGE
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da demanda
<a href="#top">(inicio)</a>

Essa demanda visa especificar as ações necessárias e requisitos do processo de extração, transformação e carga (fluxo ETL) dos dados do Portal da Transparência para o [Portal de Dados Abertos](dados.mg.gov.br), de maneira automatizada e na mesma periodicidade de atualização das consultas originárias do Portal da Transparência.

As tabelas e visões do Portal da Transparência devem ser mapeadas para os recursos do CKAN, em múltiplos formatos (eg. csv e json), determinando o leiaute da divulgação.

## Premissas

Menor número possível de intervenções humanas manuais na interface gráfica do ckan - especialmente no fluxo de atualização de metadados (criação e exclusão de recursos e datasets são passíveis dessas intervenções)

Aproveitamento da maior parte das regras de boas práticas de dados já consolidadas e vocabulários preexistentes (tanto dos nomes de datasets, de recursos, de variáveis, de metadados) - corresponde à [Boa Prática 15 recomendada pela W3C](https://www.w3.org/TR/dwbp/#ReuseVocabularies). 

Fontes:
* [Documentação da API do CKAN](https://docs.ckan.org/en/latest/api/index.html)
* [CSV Lint](https://csvlint.io/about)
* [JSON Lint](https://jsonlint.com/)
* [Referência padrão mundial para contratos](https://standard.open-contracting.org/latest/en/schema/)
* [Portal da Transparência](http://www.transparencia.dadosabertos.mg.gov.br/dataset)
* Armazém do SIAFI
* Expertise das equipes dos órgãos centrais que utilizam os temros que designam

Caso exista duplicação de dados para publicação dos mesmos no CKAN, o serviço de extração e carga deve:

* Garantir a consistência entre os dados quando existirem alterações na base de dados origem;
* Utilizar um usuário específico para carga no CKAN;
* Configurável para efetuar cargas em instâncias CKAN não hospedadas na PRODEMGE;
* Possuir mecanismo de monitoramento das cargas realizadas (eg. email com log de atualização)
  

# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

O Planejamento Estratégico da Diretoria de Transparência Ativa prevê a publicação de todos os conjuntos de dados disponíveis na interface de consulta do Portal da Transparência, com a mesma periodicidade que este utiliza para carga/atualização. Em paralelo, a hospedagem do CKAN, que hoje abriga a seção de dados abertos, vai migrar para servidores sob governabilidade da CGE, o que permite a autonomia e aumenta a responsabilidade sobre a gestão do mesmo.

Tais medidas deverão estar articuladas com a implementação das especificações deste documento, no que tange ao fluxo de ETL, para que todos os agentes envolvidos desempenhem seu papel de forma a atender as práticas recomendadas na literatura sobre o assunto, gerando previsibildiade, confiança e eficiência na consecução do objetivo de publicar os dados abertos com periodicidade definida. 

# Especificação
<a href="#top">(inicio)</a>

## Etapas e responsabilidades dos setores no fluxo ETL

1) Extração: o NUCC deverá salvar os arquivos de cada dataset, na periodicidade e layout indicados pela DTA, em ftp ou local a ser consensuado com a DTI. 

No caso dos arquivos dos datasets que existem sem a correspondente interface de consulta no Portal, a DTA fará a carga do arquivo no local indicado (ou o próprio órgão de origem dos dados?)

* Anual = 
* Semestral = 
* Trimestral = extrato de termos de parceria
* Bimestral = planejamento e monitoramento SIGPLAN
* Mensal = remuneração, voos do governador
* Semanal = 
* Diária = despesa, receita, compras
* por evento de publicação =  extrato de doações de bens e serviços e comodatos

Cada evento de carga pelo NUCC deverá gerar um aviso automático por email, por dataset, de que foi realizado, como um log de operação.

2) Transformação: a DTA deverá definir parâmetros assegurando a premissa de menor internvenção humana possível, a não ser na criação ou exclusão de datasets. Todas as atualizações de metadados, por exemplo, deverão ser efetuadas via script no ambiente operado pela DTI na máquina do CKAN, sem necessidade de logar no ambiente de produção do novo CKAN

3) Carga: a partir dos dados extraídos, a carga se dará por meio de script elaborado e operado na DTI, que buscará o dado no ftp utilizado pelo NUCC e fará a carga, com periodicidade definida pela DTA, no ftp criado na máquina do CKAN

Cada evento de carga pela DTI deverá gerar um aviso automático por email, por dataset, de que foi realizado, como um log de operação.

## Aspectos genéricos dos diretórios e dos arquivos

* Nomes dos diretórios sem espaços, hifens (‘-‘) como separadores;

* Tabelas-dimensões com valores restritos aos que estiverem constando em cada tabela-fato de cada dataset;

* CSV: delimitadores de colunas são ponto e vírgula; delimitadores de valores são vírgulas; utilização de  quote (aspas simples) ao início de cada célula que contenha string (ESCAPING);

* ENCODING UTF-8 para o arquivo e para os caracteres, com a a inserção da assinatura unicode BOM (_Byte Order Mark_) em todos os arquivos gerados


### Exemplos



# Dúvidas

## Técnicas

* É possível que o CKAN faça uma requisição ao banco de dados do Portal da Transparência? Essa ação faz sentido do ponto de vista de performance?

* O CKAN permite alguma solução de negociação de conteúdo para oferta de múltiplos formatos de arquivos?

* Caso seja implementado uma nova consulta, ou exista alterações nas consultas pré-existentes, no Portal da Transparência, como isso será refletido no CKAN? Como garantir que as mudanças sejam implementadas por máquina, seja nos arquivos ou nos seus metadados (quais funções em quais linhas do scropt)?

* o que o script de carga faz de fato?

* Processo de atualização de metadados: prescinde de conferência pela DTI? onde estaria o git consumido e como mudar?

* É realmente necessário um arquivo json para descrever cada arquivo, como foi solicitado pela DTI durante os testes, em vez de um único por conjunto de dados?

## Negócio

* Qual a real necessidade de replicar periodicidade de atualização das consultas do Portal da Transparência no CKAN?

* Qual o grau de agregação/desagregação das informações que serão disponibilizadas no CKAN? A depender de cada caso como foram os testes-piloto dos datasets de dívida?

* Em qual formato de arquivo (eg. csv, json) os conjuntos de dados deverão ser disponibilizados no CKAN?

* Qual a responsabilidade da DTA nos arquivos de datasets que não têm consultas correspondentes na interface do Portal, ou que não estão visíveis no banco do Portal pelo NUCC? (Eg, doações, termos de parceria, relatórios de pedidos de acesso às informações)

## [Issues a partir dos testes no novo domínio criado](http://10.183.67.16/transparencia/issues/)
