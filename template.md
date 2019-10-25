---
titulo: feat/"Especificação Layout Remuneração"
pull_request:https://github.com/transparencia-mg/especificacoes-portal-transparencia/tree/feat/especificacao-layout-remuneracao/pull-4
---

# Visão geral da intervenção

Objetivo: rever a especificação do leiaute da consulta de remuneração elaborada em 2015 e que está em produção atualmente.

# Motivação / contexto da intervenção

Validar necessidade de preenchimento dos campos da consulta de remuneração que estão vazios. Suprimir campos que não são necessárias, e adicionar campos necessários, seja em decorrência de alterações legislativas (LGPD, p.ex.) e decisões concensuadas entre os técnicos das áreas envolvidas.

# Especificação

Na consulta Página Principal > Pessoal > Remuneração dos Servidores > Faixa Salarial > Órgao > Cargo > Servidor, adotar:

Exclusões: campos NUMERO_ADMISSAO, CPF,  

Inclusões:

Valores de todos os campos que constam como '0' ou '-'

Número e grau do cargo efetivo

Detalhamento da composição remuneratória (discriminação dos vencimentos)

Discriminação dos auxílios (alimentação, transporte e outros) e outros que estão agregados como 'Demais eventuais'

Evidenciação de desconto decorrente de faltas nos dias trabalhados

Agregação de vantagens e deduções em subtotais

# Dependências / Integrações

SISAP

# Exemplos



# Dúvidas
DIFERENÇA ENTRE '0' E '-' NO RESULTADO DA ATUAL CONSULTA

