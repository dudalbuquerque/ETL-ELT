# Integração dos dados - Abordagem ETL

Este notebook Python demonstra um pipeline ETL (Extract, Transform, Load) para processar os dados de infrações de trânsito. O projeto envolve a leitura de arquivos CSV, a transformação dos dados para análise,  e a carga dos dados em um banco de dados PostgreSQL.

Estrutura do Notebook
O notebook está organizado nas seguintes seções:
```
    └──  datasets
    |    └── concat.ipynb   
    └──  ETL
        └──  processos.ipynb
 ```

## 1. Instalação das bibliotecas necessárias

Esta seção instala as bibliotecas Python essenciais para o projeto, incluindo sqlalchemy, psycopg2-binary e pandas.Além disso também é necessário baixar a extensão do jupyter notebooks no vscode

  ```pip  install  pandas psycopg2-binary sqlalchemy```

## 2. Para rodar

Para rodar os comandos do arquivo "Processo_ETL.ipynb" é necessário executar o arquivo "concat.ipynb" localizado na pasta "datasets" que concatena os csv e torna possível executar os tratamentos nessa nova base que agrega os três anos que escolhemos como foco, 2023, 2024, 2025 respectivamente.Depois disso, vá executando célula por célula para ver a transformação acontecer     

## 3. Tomada de decisão e tratamentos

Antes de começar a tratar os três de maneira conjugada, precismaos padronizar o tipo de datas e e horas, colunas datainfracao e data_implementação.No ano de 2023 e 2025 elas estavam no mesmo formato, ambas como DATE -  2023-12-31, 2025-05-31   - mas já em 2024 estava com outro formato -  31/12/2024 00:00  - então padronizamos 2024 para qu se encaixasse no padrão dos outros anos.

Como os arquivos escolhidos tinham o mesmo número de colunas e tipos de dados o tratamento dos 3 já pode ser feito de maneira conjugada, como um único arquivo.

Em uma primeira análise percebemos que seria necessário o tratamentos dos dados para uniformizar os dados e facilitar o seu entendimento

### Tratamentos que realizamos:
- Renomear as colunas de forma a torná-las mais legíveis  EX 'datainfracao': 'data_infracao'
- Dividimos a coluna 'amparo_legal' em artigos e subdivisao_artigo
- Tiramos valores indesejados da coluna 'artigo' ex "SENTIDO OLINDA" ---> "Não informado"
- Padronização dos valores de 'subdivisao_artigo' EX 'inciso VIII': 'Inc. VIII', 'parágrafo único': '§ único'
- Tratamos de valores nulos nas colunas 'artigo', 'subdivisao_artigo', 'agente_equipamento' --> "Não informado"
- Padronizamos os tipos de dados das colunas

## Visualização

Para visualização da base de dados tratada execute as células entituladas " Carregamento para o PostgreSQL" e substitua com suas credenciais
