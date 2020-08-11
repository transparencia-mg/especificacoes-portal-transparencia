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

Partes diretamente envolvidas: Diretoria de Transparência Ativa (DTA); Diretoria de Tecnologia da Informação (DTI); Núcleo de Combate à Corrupção (NUCC); órgão ou setor custodiante de dados, externo à CGE.

## Premissas

* É necessário (mandatário para o funcionamento esperado do fluxo, tal qual descrito):
	
	a. automatizar da maior parte possível das atividades necessárias do fluxo ETL - é recomendado, portanto, que haja o menor número possível de intervenções humanas manuais nas etapas do fluxo;

	b. que os datasets sejam descritos pelos dados sem fricção (Frictionless Data), sendo o ´datapackage.json´ o conjunto de dados mínimo, com a garantia da DTA na elaboração desse arquivo, em qualquer nível de conhecimento do órgão/setor custodiate de dados sobre o formato json;

* É recomendado (adoção de práticas para garantir controle e reprodutibilidade):

 	c. o aproveitamento da maior parte das regras de boas práticas de dados já consolidadas e vocabulários preexistentes (tanto dos nomes de datasets, de recursos, de variáveis, de metadados) - corresponde à [Boa Prática 15 recomendada pela W3C](https://www.w3.org/TR/dwbp/#ReuseVocabularies);

 	d. que o órgão ou setor custodiante de dados use repositório Github para gerenciar datasets. Trata-se de melhor prática para controlar versões das publicações/atualizações de dados abertos - caso o órgão ou setor custodiante não adira, a DTA vai versionar automaticamente os dados no Github

* É desejável (para promover melhorias além das anteriores):

	e. a atualização de dados com a mesma periodicidade das consultas originárias do Portal da Transparência;
  
# Especificação
<a href="#top">(inicio)</a>

## Metadados

* É necessário:

	- o uso de um arquivo datapackage.json para descrever os metadados de cada dataset;
	- que o nome e extensão do arquivo sejam `datapackage.json`, invariavelmente, para qualquer dataset que descrevam;
	- que o `datapackage.json` contenha um schema para cada recurso deste dataset, segundo o [exemplo]();
	- que o `datapackage.json` esteja de acordo com as especificações da Frictionless Data; 
	- que o arquivo datapackage.json contenha, minimamente, valores válidos para todas as propriedades enumeradas no gerador da [Frictionless Data](https://create.frictionlessdata.io/) e as propriedades do arquivo csv a que se refere o datapackage; 
	- que as propriedades do arquivo csv sejam descritas pelo [CSV Dialect](https://specs.frictionlessdata.io/csv-dialect/);
	- que a codificação do arquivo `datapackage.json` seja UTF-8 (sem BOM)

## Recursos

É necessário:

- que a codificação do arquivo csv seja UTF-8 (com BOM); 

## Versionamento

* É necessário:

	- que cada dataset tenha um repositório com mesmo nome na organização https://github.com/dados-mg;
	- que o nome de cada dataset e de cada um dos seus recursos sigam as [convenções de nomenclatura](https://pandoc.org/MANUAL.html#extension-auto_identifiers); 
	- que os nomes das URLs dos repositórios sigam as [convenções](https://slugify.online/);
	- que cada repositório use a estrutura de pastas e arquivos seguinte:

	- que o ftp eventualmente utilizado para espelhar o repositório reproduze a mesma estrutura de pastas e arquivos acima;

* É desejável:

	_ que haja um FTP de "entrada" e um de "publicação". No FTP de "entrada" os vários orgãos (eg. SES) podem receber usuários específicos com permissão de leitura (read);

	- que as estrturas de pastas e arquivos a serem utilizadas se balizem pelo padrão https://drivendata.github.io/cookiecutter-data-science/; 

	- que no processo de atualização, o id do recurso seja a propriedade do datapackage.json que indicará a necessidade de nova carga das alterações realizadas

## Cenários e situações

1. Arquivo csv pronto para publicação

2. Arquivo tem que passar por processamento para ser publicado

3. Arquivo primário tem que ser processado mas arquivo primário não pode ser divulgado (ex.: unidade administrativa)

* Cada evento de carga pela DTI deverá gerar um aviso automático por email, por dataset, de que foi realizado, como um log de operação.


Caso exista duplicação de dados para publicação dos mesmos no CKAN, o serviço de extração e carga deve:

* Garantir a consistência entre os dados quando existirem alterações na base de dados origem;
* Utilizar um usuário específico para carga no CKAN;
* Configurável para efetuar cargas em instâncias CKAN não hospedadas na PRODEMGE;
* Possuir mecanismo de monitoramento das cargas realizadas (eg. email com log de atualização)

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
