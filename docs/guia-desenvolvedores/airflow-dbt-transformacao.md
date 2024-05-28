# Utilizando DBT + AIRFLOW para orquestração de transformação local

A integração de DBT (Data Build Tool) e Airflow representa uma poderosa abordagem para a orquestração de transformações de dados em um ambiente local. DBT é uma ferramenta que facilita a transformação de dados dentro de um data warehouse, permitindo que analistas e engenheiros de dados criem, testem e documentem seus pipelines de dados de maneira eficaz. Já o Apache Airflow é uma plataforma de código aberto que possibilita a programação, monitoramento e gestão de workflows de dados.

1. Configuração do Ambiente:

Instalar ou fazer upgrade do Astro CLI:

- **Observação: se der erro ao acessar a página de login do airflow, para corrigir só atualizar o Astro CLI para voltar ao normal**

```bash
curl -sSL install.astronomer.io | sudo bash -s
```

Acessar o a pasta do projeto via terminal, dentro da pasta podemos rodar o commando logo abaixo, para iniciar o a construção da imagem e container docker.

```bash
astro dev start
```


Após iniciar o airflow, acessar o Airflow utilizando o login e senha padrão.

Antes de rodar a dag será necessário configura a conexão do postgres no Airflow.

Na parte superior acessar 'ADMIN' no menu acessar connections