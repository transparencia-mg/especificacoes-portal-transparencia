|Título| Homologação da descrição do empenho
| -|:-
|__Contrato manutenção__ | nº 15210010062019 (INF. 3951)
|__Proposta Comercial__ | nº 626584/19
|__Mantis__ |nº 0146901
|__Versão html__ |[link]()

# Homologação do campo Descrição Histórico do Empenho

<div class="alert alert-info">

Considerando o relatado pelo Analista da PRODEMGE (Luiz), o erro detectado nesse documento refere-se a empenho do mês de junho. Nesse sentido, encontra-se concluída a homologação.
Aguardamos a disponibilização em produção para uma conferência mais extensa.

"*A geração do arquivo foi realizada em Março/2020. A divergência apresentada trata-se de um empenho **gerado em Junho**, ou seja, no arquivo disponibilizado para essa avaliação preliminar não continha tais dados.*

*Estamos no aguardo da reunião para decidir a frequência de geração do referido arquivo, a ser realizada no dia 15/07. Com base nesse retorno, o analista da Prodemge que atende a SEF não atualizou o arquivo de teste, conforme eu havia cogitado no e-mail, sendo assim, os testes estão temporariamente limitados dentro do escopo de empenhos gerados em 2020 até o mês de Março (sem garantias que todos os empenhos gerados em Março estão inclusos e que possíveis divergências entre as descrições podem ocorrer.)*"

  </div>

A homologação foi realizada por **amostragem** e apenas com base nos **empenhos de 2020**. Quando os dados forem disponibilizados em produção será possível verificar uma amostra maior.

* Informações do analista da PRODEMGE que realizou a intervenção no Portal:

>_A liberação preliminar se faz necessário não somente pelas informações desatualizadas, mas devido a identificação de alguns pontos identificados nos arquivos gerados e relatados a seguir:_
>
>_Todos os empenhos possuem um “histórico padrão”, geralmente uma linha apenas que descreve brevemente do que se trata o Empenho (por exemplo, APROPRIACAO EMPENHO - PESSOAL E ENCARGOS SOCIAIS);_
>
> * _Caso o “histórico padrão” seja removido, poderá ocasionar empenhos com histórico vazio._
> * _Boa parte dos empenhos, além do “histórico padrão”, possuem o “complemento de empenho”, sendo esse um texto livre inserido pelo usuário;_
>
> * _Para o processamento da carga foi considerado a junção do histórico padrão com o complemento de empenho, sendo segregados por uma quebra de linha;_
>* _O complemento de empenho, por se tratar de texto livre, possui algumas anomalias na formatação do texto. Limitações no mainframe e provavelmente a forma que o usuário insere as informações no mesmo, provocam quebras indesejadas de palavras ou não inserção de espaço entre palavras. Para resolver o problema foi aplicada uma técnica que identifica quando uma quebra de linha ocorre entre uma palavra (realizando a união) ou entre duas palavras (inserindo o espaço quando necessário).A técnica se baseia na validação da palavra por meio da lista de palavras existentes na língua portuguesa, sendo assim, não é perfeita, podendo, ocasionalmente, apresentar informações separadas por espaço quando as mesmas deveriam estar unidas._
>
>_O volume de dados cobre 100.417 dos 163.214 empenhos de despesa do ano de 2020. Caso o arquivo seja gerado ao longo do dia 09/07, esse será atualizado em homologação e irei comunicar sobre esse evento._


## Consulta Despesa:

<div class="alert alert-success">

__CONFERE__

PORTAL
--

![](static/empenho19-cge-2020.png)

SIAFI
--
![](static/siafi_empenho19_cge-2020.png)  
</div>

<div class="alert alert-success">

__CONFERE__

PORTAL
--

![](static/empenho306-cbmmg-2020.png)

SIAFI
![](static/siafi_empenho306_cbmmg-2020.png)
</div>

<div class="alert alert-success">

**Desconsiderar pois o empenho refere-se a junho/2020**

<s>DIVERGÊNCIA NA DESCRIÇÃO DO HISTÓRICO DO EMPENHO

PORTAL

![](static/empenho1579-fundacao-ezequiel-2020.png)

SIAFI

![](static/siafi_empenho1579_funed-2020.png)

![](static/siafi_empenho1579_funed-2020-telaanterior.png)
</s>
</div>

## Consulta Diárias

<div class="alert alert-success">

__CONFERE__

PORTAL
--
![](static/empenho33-age-2020-diarias.png)

SIAFI
--
![](static/siafi_empenho33_age-2020.png)

</div>

<div class="alert alert-success">

__CONFERE__

PORTAL
--
![](static/empenho78-detran-2020-diarias.png)

SIAFI
--
![](static/siafi_empenho78_detran-2020.png)

</div>
