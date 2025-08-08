# Projeto ELT de Dados de Infrações de Trânsito

Este notebook Python demonstra um pipeline ELT (Extract, Load, Transform) para processar dados de infrações de trânsito. O projeto envolve a leitura de arquivos CSV, a carga dos dados em um banco de dados Supabase e a transformação dos dados para análise.

## Estrutura do Notebook

O notebook está organizado nas seguintes seções:

### 1. Instalação das bibliotecas necessárias
Esta seção instala as bibliotecas Python essenciais para o projeto, incluindo `sqlalchemy`, `psycopg2-binary` e `pandas`.

### 2. Extração dos dados (Extract)
Aqui, os dados de infrações de trânsito dos anos de 2023, 2024 e 2025 são lidos a partir de arquivos CSV e carregados em dataframes do Pandas. A leitura inclui tratamento básico para arquivos não encontrados e outros erros.

### 3. Carga dos dados no Banco (Load)
Nesta etapa, os dataframes do Pandas são carregados em uma tabela no banco de dados PostgreSQL. A conexão com o banco é estabelecida utilizando `sqlalchemy` e as credenciais são gerenciadas de forma segura. Os dados de cada ano são adicionados sequencialmente à tabela.

### 4. Verificação da Carga no Banco de Dados
Após a carga, uma consulta é executada no banco de dados para verificar se os dados foram inseridos corretamente, exibindo uma amostra das primeiras linhas da tabela.

### 5. Transformação dos Dados (Transform)
Esta seção realiza diversas transformações nos dados carregados no banco de dados para limpá-los, padronizá-los e prepará-los para análise:

- **Tratamento da Coluna datainfracao:** Converte a coluna para o tipo DATE e a renomeia para `data_infracao`.
- **Tratamento da coluna horainfracao:** Converte a coluna para o tipo TIME e a renomeia para `hora_infracao`.
- **Tratamento da coluna dataimplantacao:** Converte a coluna para o tipo DATE e a renomeia para `data_implantacao`.
- **Renomeando a coluna agenteequipamento:** Renomeia a coluna para `agente_equipamento`.
- **Realocamento da coluna infracao:** Move a coluna `infracao` para a ordem original da tabela.
- **Renomeando a coluna descricaoinfracao:** Renomeia a coluna para `descricao_infracao`.
- **Tratamento da coluna amparolegal:** Divide a coluna em `artigo` e `subdivisao_artigo` para melhor granularidade.
- **Renomeando a coluna localcometimento:** Renomeia a coluna para `local_cometimento`.

### 6. Verificação Final dos Dados Transformados
Uma consulta final é executada para exibir uma amostra dos dados após todas as transformações, garantindo que as modificações foram aplicadas corretamente e que os dados estão prontos para análise.

## Como Executar

1. Certifique-se de ter os arquivos CSV (`infracoes_2023.csv`, `infracoes_2024.csv`, `infracoes_2025.csv`) disponíveis no ambiente de execução do notebook.
2. Configure as credenciais do Supabase no gerenciador de segredos do Colab, utilizando a chave `db_password`.
3. Execute as células do notebook sequencialmente.

Este pipeline ELT fornece uma base sólida para a análise dos dados de infrações de trânsito, permitindo insights sobre padrões, tendências e outras informações relevantes.
