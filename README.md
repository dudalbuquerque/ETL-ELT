# Projeto de Integração de dados
 Esse projeto é produto da disciplina Banco de dados ministrada pela professora Valeria Cesario e consiste na tranformação de dados usando a abordagem ETL e ELT em csvs de diferentes anos com o objetivo de construir uma bae de dados padronizada.
 O nosso projeot foi focado  nos registros de Infrações de Trânsito na cidade do Recife durante os anos de 2023, 2024 e 2025.Para lidar com arquivos grandes é preciso adotar as medidas abaixo
## Gerenciamento de Dados Grandes (Git LFS)

Este projeto utiliza arquivos de dados grandes que excedem o limite do GitHub. Para lidar com isso, estamos utilizando o **Git Large File Storage (Git LFS)**.

**É necessário ter o Git LFS instalado para conseguir trabalhar com os arquivos da base de dados deste repositório.**

### Como Configurar e Usar o Git LFS:

**Se você não tiver o Git LFS, baixe o instalador no site oficial:** [**https://git-lfs.com/**](https://git-lfs.com/)


1.  **Instale o Git LFS:**
    Verifique se o Git LFS está instalado executando `git lfs install` no seu terminal.
    ```bash
    git lfs install
    ```
    
2.  **Clone o repositório (se ainda não o fez):**
    ```bash
    git clone [https://github.com/dudalbuquerque/Projeto-de-integra-o-de-dados.git)
    ```
   
3.  **Entre no diretório do projeto:**
    ```bash
    cd Projeto-de-integra-o-de-dados
    ```

4.  **Baixe os arquivos grandes:**
    Após clonar ou puxar atualizações, os arquivos grandes podem aparecer como "ponteiros". Para baixar o conteúdo real dos dados, execute:
    ```bash
    git lfs pull
    ```
    Este comando garantirá que todos os arquivos de dados gerenciados pelo LFS estejam disponíveis em sua máquina.
