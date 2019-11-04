---
titulo:
pull_request:
---

# Visão geral da demanda

O objetivo dessa demanda é ofertar, de maneira tempestiva, os dados do Portal da Transparência como dados abertos no CKAN de maneira automatizada. A divulgação de maneira tempestiva consiste na publicação de dados no CKAN na mesma periodicidade de atualização das consultas originárias do Portal da Transparência. 

As tabelas e visões do Portal da Transparência devem ser mapeadas para os recursos do CKAN, possivelmente em múltiplos formatos (eg. csv e json), determinando o leiaute da divulgação.

Caso exista duplicação de dados para publicação dos mesmos no CKAN, o serviço de extração e carga deve:

* Garantir a consistência entre os dados quando existirem alterações na base de dados origem;
* Utilizar um usuário específico para carga no CKAN;
* Configurável para efetuar cargas em instâncias CKAN não hospedadas na PRODEMGE;
* Possuir mecanismo de monitoramento das cargas realizadas (eg. email com _log_ de atualização)

# Motivação / contexto da demanda

Porque a demanda é necessária? Qual problema ela visa solucionar?

# Especificação


# Dependências / Integrações

Para implementação da demanda é necessário ações de atores externos à equipe da PRODEMGE do Portal ou da DTA?

# Exemplos

Existe algum exemplo similar ao proposta na demanda que serviu de inspiração?

# Dúvidas

## Técnicas

* É possível que o CKAN faça uma requisição ao banco de dados do Portal da Transparência? Essa ação faz sentido do ponto de vista de performance?

* O CKAN permite alguma solução de negociação de conteúdo para oferta de múltiplos formatos de arquivos?

* Caso seja implementado uma nova consulta, ou exista alterações nas consultas pré-existentes, no Portal da Transparência, como isso será refletido no CKAN?

## Negócio

* Qual a real necessidade de replicar periodicidade de atualização das consultas do Portal da Transparência no CKAN?

* Qual o grau de agregação/desagregação das informações que serão disponibilizadas no CKAN?

* Em qual formato de arquivo (eg. csv, json) os conjuntos de dados deverão ser disponibilizados no CKAN?