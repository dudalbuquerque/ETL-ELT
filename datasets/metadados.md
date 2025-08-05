## Metadados
> são dados sobre os dados

| Coluna            | Tipo        | Restrições           | Descrição                        |
|-------------------|------------ |----------------------|----------------------------------|
| data_infracao     | INT         | PRIMARY KEY, NOT NULL| Data que a infração foi cometida |
| hora_infracao     | VARCHAR(50) | NOT NULL             | Hora que a infração foi cometida |
| data_implantacao  | VARCHAR(100)| NOT NULL             | Data que a infração foi registrada no sistema |
| agente_equipamento| VARCHAR(20) | NOT NULL             | O meio ou equipamento utilizado pelo agente de trânsito para registrar a infração|
| cod_infracao      | VARCHAR(20) | UNIQUE, NOT NULL     | Código que indentifica unicamente a infração |
| descricao_infracao| VARCHAR(200)| NOT NULL             | Descrição sobre a infração                   |
| local_cometimento | VARCHAR(20) | NOT NULL             | Local onde ocorreu a infração                |
| artigo            | VARCHAR(20) | NOT NULL             | O número do artigo do CTB que foi infringido |
| subdivisao_artigo | VARCHAR(20) | NOT NULL             | Inciso ou parágrafo dentro de um artigo do Código de Trânsito Brasileiro |
