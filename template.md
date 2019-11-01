---
titulo: feat/"Especificação Layout Remuneração"
pull_request:https://github.com/transparencia-mg/especificacoes-portal-transparencia/tree/feat/especificacao-layout-remuneracao/pull-5
---

# Visão geral da intervenção

Objetivo: rever a especificação do leiaute da consulta de remuneração elaborada em 2015 e que está em produção atualmente, com o objetivo de ajustar campos do cabeçalho e da tabela/planilha. Seja para suprimir campos que não são necessários e adicionar outros necessários, além da adequação da forma de apresentação e dos espaços que alguns campos ocupam.

# Motivação / contexto da intervenção

A especificação da consulta de remuneração foi elaborada em 2012 quando da publicação do decreto 45.969/12 que obriga a publicação da remuneração e revista em 2015, quando da atualização e reformulação do Portal da Transparência. A revisão em 2015 visou dar mais transparência com relação à vida funcional dos servidores e à composição dos proventos, seguindo as boas práticas identificadas e as diversas demandas recebidas por meio de fale conosco e da Lei de Acesso a Informação.

Na primeira onda de reformulação optou-se por atualizar a interface web da consulta de remuneração já colocando os novos campos, mas não foi feita a adequação no banco de dados, o que seria feito logo em seguida. Posteriormente, foram priorizadas as novas consultas do Portal e, por fim, não houve recursos suficientes para realizar a adequação no banco.

Desde então existem campos disponibilizados na interface web da consulta que não possuem dados preenchidos.

# Especificação

Na consulta Página Principal > Pessoal > Remuneração dos Servidores > Faixa Salarial > Órgao > Cargo > Servidor, adotar:

* Para o cabeçalho:

Inclusões (valores de todos os campos que constam como '0' ou '-'). Atualmente, são eles: 
- Data de Nomeação/Contratação	
-	Data de Desligamento	
- Número Admissão		
- Regime Jurídico Descrição		
- Vínculo Descrição	
- Código Gratificação Cargo Efetivo	
- Descrição Gratificação Cargo Efetivo	
- Código Cargo Comissão		
- Código Gratificação Temporária
- Descrição Gratificação Temporária	
- Código Função Gratificada
- Descrição Função Gratificada	
- Código Instituição Lotação
-	Descrição Instituição Lotação	
- Código Instituição Exercício	
- Quinquênio
- Adicional de Desempenho	0
- Código Afastamento Licença
- Descrição Afastamento Licença	
- Decisão Judicial para não Publicar Remuneração	
 *Esta é a principal alteração trazida por esta especificação*
- Nível na carreira no mês filtrado para a pesquisa
- Grau na carreira no mês filtrado para a pesquisa

Exclusões:  

* Para a tabela:

Detalhamento da composição remuneratória (vantagens da carreira, ADE, cargos, funções gratificadas, gratificações temporárias estratégicas)

Discriminação dos auxílios (alimentação, transporte e outros) e outros que estão agregados como 'Demais eventuais'

Evidenciação de desconto decorrente de faltas nos dias trabalhados

Agregação de vantagens e deduções em subtotais ou em mesclas dos títulos dos cabeçalhos

# Dependências / Integrações

Será necessário agendamento de reuniões de validação com os órgãos envolvidos (CBMMG, PMMG), para que os mesmos possam preencher a planilha de remuneração tal qual definido nesta especificação.

# Exemplos



# Dúvidas
DIFERENÇA ENTRE '0' E '-' NO RESULTADO DA ATUAL CONSULTA

