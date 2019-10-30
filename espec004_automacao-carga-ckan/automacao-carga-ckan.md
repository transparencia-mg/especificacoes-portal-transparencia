---
titulo:
pull_request:
---

# Visão geral da intervenção

Desenvolvimento de serviço que faça extração dos dados do Portal da Transparência e carga dos mesmos no CKAN de forma automatizada de acordo com formato e periodicidade pré-definidos.

O objetivo é que os dados do Portal da Transparência também sejam ofertados como dados abertos no CKAN sem necessidade de intervenção manual para cada atualização.

# Motivação / contexto da intervenção

Porque a intervenção é necessária? Qual problema ela visa solucionar?

# Especificação

* Deve ser garantido que caso exista alteração ou exclusão nos registros do Portal da Transparência, os mesmos devem ser refletidos nos conjuntos de dados equivalentes do CKAN

* O serviço deve ser capaz de efetuar carga em instâncias distintas do CKAN, ainda que não hospedadas na PRODEMGE

* O serviço deve utilizar um usuário específico do CKAN para carga de dados no CKAN

* Deve ser enviado por email _log_ de atualização das cargas no CKAN

# Dependências / Integrações

Para implementação da intervenção é necessário ações de atores externos à equipe da PRODEMGE do Portal ou da DTA?

# Exemplos

Existe algum exemplo similar ao proposta na intervenção que serviu de inspiração?

# Dúvidas

* Qual a real necessidade de replicar periodicidade de atualização das consultas do Portal da Transparência no CKAN?

* É possível que o CKAN faça uma requisição ao banco de dados do Portal da Transparência? Essa ação faz sentido do ponto de vista de performance?

* Qual o grau de agregação/desagregação das informações que serão disponibilizadas no CKAN?

* Em qual formato de arquivo (eg. csv, json) os conjuntos de dados deverão ser disponibilizados no CKAN?

* Caso seja implementado uma nova consulta, ou exista alterações nas consultas pré-existentes, no Portal da Transparência, como isso será inserido no CKAN?
