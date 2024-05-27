## O que é o DBT e para que serve?

Em um _pipeline_ ELT, os dados brutos são extraídos (_extract_) de uma fonte e carregados (_load_) em uma _data warehouse_ (no nosso caso: o _BigQuery Storage_). Em seguida, os dados brutos são transformados em tabelas utilizáveis, usando consultas **SQL** executadas sobre os dados estocados nessa _data warehouse_.

O **dbt** (_Data Build Tool_) é uma ferramenta de linha de comando que oferece uma maneira fácil para que analistas e engenheiros de dados criem, transformem e validem os dados em um _data warehouse_ de maneira mais eficiente. O **dbt** faz o T nos processos ELT (Extrair, Carregar, Transformar) ilustrados na figura abaixo.

![Fluxo de Dados com DBT](../static/img/tutoriais/dbt/fluxo_dbt.png)

No **dbt**, trabalhamos com modelos, que nada mais é que um arquivo **SQL** com uma instrução `select`. Esses modelos podem depender de outros modelos, ter testes definidos neles e podem ser criados como tabelas ou visualizações.

Fazendo um paralelo com o processo de ELT do Escritório de Dados: utilizamos _pipelines_ como `dump_db` ou `dump_url` para extrair os dados de uma base **SQL** ou uma planilha Google e subir esses dados no _Google Cloud Storage_. Após esse passo, os dados já estão disponíveis para consulta, visualização, construção de dashboards e todas as funções e facilitadores do _BigQuery_ podem ser aplicadas nos dados. Porém, na grande maioria das vezes, os dados brutos, diretos da fonte de dados original, precisam ser tratados antes de serem efetivamente utilizados.

Alguns exemplos de tratamento comumente feitos são:

- Tipagem de colunas (`FLOAT64`, `STRING`, `GEOMETRY`, `INT64`, etc.).
- (Re)nomeação de colunas.
- Mapeamento de _seed values_ (troca de `id_bairro` por `nome_bairro` ou vice-versa).
- Criação de novas colunas a partir dos próprios dados brutos.
- Complementação de dados a partir de outras bases que estão no mesmo _data warehouse_ (_Google Cloud Storage_).