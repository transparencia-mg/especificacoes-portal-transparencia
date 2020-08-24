## ETL requisitos

* de negócio e indicadores-chave (KPIs)

* compliance, normas e tempo de arquivamento

* qualidade dos dados

* segurança e dados extrasensitivos

* integração dos dados e priorização das dimensões para integração

* latência de dados

* arquivo: We recommend staging the data (writing it to disk) after each major activity of the ETL pipeline: after it’s been extracted, cleaned and conformed, and delivered; It’s almost always less problematic to read the data from permanent media than it is to reprocess the data through the ETL system at a later time; each staged/archived data set should have accompanying
metadata describing the origins and processing steps that produced the data. You should list the data sources and intermediate data steps that will be archived, together with retention policies, and compliance, security, and privacy
constraints.

* interfaces BI

* habilidades da equipe

* licenças legadas

## 34 subsistemas 

* extração

* transformação

* carga: 9 a 21

* gestão: 22 a 34

## Managing the ETL envoronment

22. Job Scheduler: 

Controle das relações e dependências entre jobs do ETL. (Jobs entendido como tarefas ou atividades específicas dentro do workflow)

Necessita reconhecer quando um arquivo está pronto para ser processado. Se a organização processa em tempo real, o scheduler deve suportar a arquitetura de tempo real. 

O controle de processos de jobs também deve capturar metadados e estatísticas sobre o processo, durante sua execução. 

Por fim, o scheduler deve apoiar um processo totalmente automatizado, incluindo notificar eventos ou situações que requeiram solução. 

O serviço de controle dos jobs compreende: 

- definição de séries ou passos dos jobs e relações e dependências entre eles; 

- a habilidade de monitorar flags nas bases de dados, checar a existência de arquivos e comparar datas de criação; 

- a captura de metadados do processo que estiver sendo executado no momento, como qual dataset está sendo carregado, o horário de início deste processo e sua duração;

- coleta e registro de informação sobre o que ocorreu durante todo o processo de ETL (logging), não somente no momento;

- após todo o processo de ETL ter sido desenvolvido e utilizado, ele deve funcionar sem qualquer intervenção humana. If a problem does occur, the control system needs to interface to the problem escalation system (subsystem 30).


23. Backup system: 

Seu objetivo é permitir o data warehouse voltar a funcionar normalmente após uma falha (física, como queda de energia ou dano físico a alguma máquina). Inclui o backup de estágios intermediários do processo de carga, para terminá-lo. 

Questão de custo-benefício de arquivamento e recuperação de dados dos jobs intermediários do processo de carga: hospedagem e desempenho X compliance. Solução é manter os dados em algum local da forma menos custosa possível, mas que ainda possa ser acessado.


24. Recovery and restart system: 

Proteção do sistema de ETL contra falhas no network, na base, no HD, na memória, na qualidade dos dados e contra novas versões de sistemas usados. 

Recomenda-se a implementação modular de ETL para mitigar custos de recuperação em etapas mal-sucedidas

25. Version Control System: 

Deve controlar check-ins e check-outs de todos os módulos e jobs do fluxo ETL. Deve permitir a comparação de diferenças entre versões e restaurar o contexto completo de uma versão, sendo necessário também evidenciar a versão do dataset/arquivo em que se estiver trabalhando durante todo o processo de ETL

- You have a master version number for each part of the ETL system as well as one for the system as a whole, don’t you? And you can restore yesterday’s complete ETL metadata context if it turns out there is a big mistake in the current release?

26. Version Migration System: espelhamento entre os ambientes de homologação e produção

27. Workflow Monitor: 

É o ponto de início de análise dos problemas de performance dos fluxos de jobs de ETL. Deve medir performance dos componentes da infraestrutura (uso de CPU, de memória, de HD, debuffer pool, de servidor, database performance), sendo considerado parte da estratégia global de coleta de metadados do processo de ETL. 

Principais gargalos:

■ Poorly indexed queries against a source system or intermediate table

■ SQL syntax causing wrong optimizer choice

■ Insuffi cient random access memory (RAM) causing thrashing

■ Sorting in the RDBMS

■ Slow transformation steps

■ Excessive I/O

■ Unnecessary writes followed by reads

■ Dropping and rebuilding aggregates from scratch rather than incrementally

■ Filtering (change data capture) applied too late in the pipeline

■ Untapped opportunities for parallelizing and pipelining

■ Unnecessary transaction logging especially if doing updates

■ Network traffic and file transfer overhead 

28. Sorting System

29. Lineage and Dependency Analyzer

30. Problem Escalation System

31. Parallelizing/Pipelining System

32. Security System

33. Compliance Manager

34. Metadata Repository Manager







