---
pull_request: '[espec001]()'
titulo: Fluxo ETL no CKAN da CGE
output:
  html_document:
    theme: united
    toc: yes
---

# Visão geral da demanda
<a href="#top">(inicio)</a>

Essa demanda visa especificar as ações necessárias e requisitos do processo de extração, transformação e carga (fluxo ETL) dos dados do [Portal de Dados Abertos](dados.mg.gov.br) a ser implementado pela CGE.

Partes diretamente envolvidas: administrador do Portal; administrador dos sistemas; órgão ou setor custodiante de dados, externo à CGE.


## Princípios Gerais

* Automatização da maior parte possível das atividades necessárias do fluxo ETL - menor número possível de intervenções humanas manuais nas etapas do fluxo;

* Aproveitamento da maior parte das regras de boas práticas de dados já consolidadas e vocabulários preexistentes (tanto dos nomes de datasets, de recursos, de variáveis, de metadados) - corresponde à [Boa Prática 15 recomendada pela W3C](https://www.w3.org/TR/dwbp/#ReuseVocabularies)

## Conceitos 

* É necessário: mandatário para o funcionamento esperado do fluxo, tal qual descrito
	
* É recomendado: adoção de práticas para garantir controle e reprodutibilidade

* É desejável: para promover melhorias além das anteriores

 
# Especificação
<a href="#top">(inicio)</a>

Cada conjunto de dados, denominado dataset, deve conter seus recursos (pondendo ser arquivos anexados ou não) e metadados. Abaixo seguem os requisitos de arquivo e de qualidade para tais elementos:

## Metadados

* É necessário:

	- o uso de um arquivo `datapackage.json` para descrever os metadados de cada dataset;

	- que o `datapackage.json` esteja de acordo com as [especificações da Frictionless Data](https://specs.frictionlessdata.io/data-package/#specification); 

	- que o nome e extensão do arquivo sejam `datapackage.json`, invariavelmente, para qualquer dataset que descrevam;

	- que o `datapackage.json` contenha um schema para cada recurso deste dataset, segundo o [exemplo](https://raw.githubusercontent.com/dados-mg/dataset-template/master/datapackage.json):

	````
      "schema": {
        "fields": [
          {
            "name": "id",
            "type": "integer",
            "format": "default",
            "title": "Incremental counter",
            "description": "An integer counter for the rows"
          },
          {
            "name": "letter",
            "type": "string",
            "format": "default",
            "title": "Alfhabet letter",
            "description": "A lower case alfabet letter"
          },
          {
            "name": "vowel",
            "type": "boolean",
            "format": "default",
            "title": "Grammer of letter",
            "description": "Is the letter a vowel?"
          }
        ]
      },
	```` 


	- que o arquivo `datapackage.json` contenha, minimamente, valores válidos para todas as propriedades enumeradas no gerador da [Frictionless Data](https://create.frictionlessdata.io/):

	````
	* dataset:
		profile, resources, keywords, name, title, description, homepage, version, contributors, licenses
	* recurso:
		id, name, path, profile, schema, fields
	* variáveis:
		name, type, format, title, description
	```` 
	- que as propriedades do arquivo csv sejam descritas pelo [CSV Dialect](https://specs.frictionlessdata.io/csv-dialect/);

	- que a codificação do arquivo `datapackage.json` seja UTF-8 (sem Byte Order Mask/BOM);

	- que o start da recarga de arquivo de metadados para administrador de banco seja a alteração na versão, indicada como propriedade no `datapackage.json`

## Recursos

É necessário:

- pelo menos a indicação da URL do local onde o recurso esteja hospedado, ou a inserção de seu arquivo - em qualquer das situações, a indicação do local onde o recurso existe  deverá constar no `datapackage.json`, na propriedade _path_;

- em sendo um recurso tabular, que tenha um schema válido no `datapackage.json`;
	
- em sendo um recurso em csv, que a codificação do arquivo csv seja UTF-8 (com BOM); 

É recomendado:
	- que o dado tabular seja em formato `.csv`;

OBS.: o upload de recurso não exige necessariamente um arquivo para ser anexado; se o arquivo estiver hospedado em URL de sítio do autor, a URL deverá ser indicada na propriedade '_path_' do `datapackage.json` do seu dataset. É possível que haja um dataset sem recurso, somente com o `datapackage.json ` descrevendo seus metadados; mas não é possível haver um dataset com recurso e sem o `datapackage.json` 

## Versionamento

* É necessário:

	- que cada dataset tenha um repositório com mesmo nome na organização [dados-mg](https://github.com/dados-mg);
	
	- que o nome de cada dataset, das URLs de seus respectivos repositórios e de cada um dos seus recursos sigam as convenções de nomenclatura (indicações: [pandoc](https://pandoc.org/MANUAL.html#extension-auto_identifiers) e [SLUG](https://slugify.online/));
	
	- que cada repositório use a estrutura de pastas e arquivos seguinte:

		dataset
		
			|--data
			
				|--recurso
				
				|--recurso
				
			|--datapackage.json

	- que o ftp eventualmente utilizado para espelhar o repositório reproduze a mesma estrutura de pastas e arquivos acima;
	
	-  e que os _commits_ referentes aos recursos e ao `datapakage.json` de cada dataset sejam validados automaticamente pelo serviço [Goodtables.io](http://goodtables.io/). Esse serviço faz o confronto dos dados do arquivo do recurso e do `datapakage.json` com as especificações do Frictionless data e do json schema;

É necessário que as operações seguintes sejam descritas em mudanças no `datapackage.json`:

	- adição/supressão de recurso,

	- adição/supressão de variável de recurso, 

	- alteração de propriedade de variável de recurso,

	- adição de dataset,

	- adição/supressão/alteração de propriedade de dataset 

* É desejável:

	_ que haja um FTP de "entrada" e um de "publicação". No FTP de "entrada" os vários orgãos (eg. SES) podem receber usuários específicos com permissão de leitura (read);

## Cenários e situações

#### Carga

0. Etapa prévia à publicação

O administrador do portal validará a versão final do arquivo junto ao custodiante do dado, cotejando aspectos de metadados, recursos e versionamento mencionados anteriormente. Validada a versão final do arquivo para publicação, ela deverá ser incluída (commitada) no repositório correspondente no Github, seguindo as regras e convenções de nomenclatura e estrutura de pastas e arquivos (incluindo o caminho relativo indicado na propriedade _path_: **data/arquivo.csv**).

É necessário que o repositório do GitHub obtenha a validação automática do Goodtables.io, a partir do último _commit_, para confirmar se estrutura e padrões de valores do arquivo do recurso (ou URL do recurso indicada no _path_) refletem o _schema_ definido no `datapackage.json`. O link contido no _badge_ de validação que existirá no repositório traz o hiperlink do resultado do _job_ no Goodtables.io. Este resultado indicará necessidades de ajustes no arquivo do recurso ou no `datapackage.json`. As inconsistências devem ser abordadas e resolvidas até o horário diário prederminado de atualização do CKAN pelo script de carga.


1. Arquivo pronto para publicação:

É necessário que o script de carga tenha uma função para perceber, diariamente, se alterações foram realizadas no `datapackage.json` e/ou no `arquivo.csv` de cada dataset.

As alterações devem ser refletidas no ambiente em produção, numa publicação automatizada. Para tal, a rotina deve realizar a importação dessa última versão commitada dos arquivos alterados no respectivo repositório para o ftp de publicação da máquina CKAN do administrador de sistemas. Na inviabilidade de importação dos arquivos pelo script de carga, o adminsitrador do Portal fará o upload manual dos mesmos para o ftp de publicação da máquina CKAN, utilizando a mesma estrutura de pastas e arquivos mencionada anteriormente. Em qualquer dos casos, a rotina fará o upload dos arquivos alterados e atualização dos campos de metadados (chaves/keys e respectivos valores) no CKAN, de modo que fiquem visíveis na interface gráfica, sem necessidade de inserção manual.

* Situações:

1.1. alteração somente de datapackage.json

1.2. adição ou supressão de recurso 

1.3. alteração de recurso:

	propriedades do recurso

	valores das variáveis

	propriedades das variáveis



2. Pós-publicação (carga/upload)

Ao realizar a publicação, é necessário que o script atualize o dicionário de dados automátizado da extensão DataStore, para que os metadados das variáveis (título, tipo, descrição representem as alterações realizadas com o upload do novo arquivo). Na inviabilidade dessa atualização automática, o relatório de notificação descrito a seguir deve ter incluída uma mensagem de aviso ou lembrete para a necessidade de atualização manual do Dicionário de Dados.

Ao fim do processo de publicação, é necessário que o script gere um relatório de notificação de erros resumidos para os emails previamente registrados dos agentes do adminsitrador do Portal. Tal relatório deve resumir e quantificar as operações realizadas na rotina, precisando sua data e horário de realização, e também deve permitir o acesso um relatório mais detalhado (log) que compare os resultados (outputs) das operações previstas com aquelas realizadas (modelo ?).

Caso exista duplicação de dados para publicação dos mesmos no CKAN, o serviço de extração e carga deve:

* Garantir a consistência entre os dados quando existirem alterações na base de dados origem;
* Utilizar um usuário específico para carga no CKAN;
* Configurável para efetuar cargas em instâncias CKAN não hospedadas na PRODEMGE;
* Possuir mecanismo de monitoramento das cargas realizadas (eg. email com log de atualização)

#### Processamento

 Arquivo tem que passar por processamento para ser publicado:


 Arquivo primário tem que ser processado mas não pode ser divulgado (ex.: unidade administrativa)



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

2) Transformação: a DTA deverá definir parâmetros assegurando a premissa de menor internvenção humana possível, a não ser na criação ou exclusão de datasets. Todas as atualizações de metadados, por exemplo, deverão ser efetuadas via script no ambiente operado pela DTI na máquina do CKAN, sem necessidade de logar no ambiente de produção do novo CKAN

3) Carga: a partir dos dados extraídos, a carga se dará por meio de script elaborado e operado na DTI, que buscará o dado no ftp utilizado pelo NUCC e fará a carga, com periodicidade definida pela DTA, no ftp criado na máquina do CKAN

### Exemplos

* Datapackage:

	com um único arquivo no schema: https://raw.githubusercontent.com/dados-mg/letters-datapackage/master/datapackage.json

	com múltiplos arquivos no schema

* Dataset sem recurso

* Dataset com único recurso

* Dataset com múltiplos recursos

# Dúvidas

## Técnicas

* É possível que o CKAN faça uma requisição ao banco de dados do Portal da Transparência? Essa ação faz sentido do ponto de vista de performance?

* Caso uma nova consulta seja implementada, ou existam alterações nas consultas pré-existentes, no Portal da Transparência, como isso será refletido no CKAN? Como garantir que as mudanças sejam implementadas por máquina, seja nos arquivos ou nos seus metadados (quais funções em quais linhas do script)?

* o que o script de carga faz de fato?

## Negócio

* Qual a real necessidade de replicar periodicidade de atualização das consultas do Portal da Transparência no CKAN?

	Verificar se bases legais detertminam a periodicidade de atualização; fazer benchmarking outros portais abertos, e.g. govenro federal

* Qual o grau de agregação/desagregação das informações que serão disponibilizadas no CKAN? A depender de cada caso como foram os testes-piloto dos datasets de dívida?

* Qual a responsabilidade da DTA nos arquivos de datasets que não têm consultas correspondentes na interface do Portal, ou que não estão visíveis no banco do Portal pelo NUCC? (Eg, doações, termos de parceria, relatórios de pedidos de acesso às informações)

## [Issues a partir dos testes no novo domínio criado](https://github.com/dados-mg/issues/issues)

# Fontes:

* [Repositório dados.mg no Github](https://github.com/dados-mg)

* [Documentação da API do CKAN](https://docs.ckan.org/en/latest/api/index.html)

* [Frictionless Data - datapackage creator](https://create.frictionlessdata.io/)

* [Goodtables](https://goodtables.io/)

* [CSV Dialect](https://specs.frictionlessdata.io/csv-dialect/)

* [JSON Lint](https://jsonlint.com/)

* Armazém do SIAFI

* Expertise das equipes dos órgãos centrais que utilizam os temros que designam

