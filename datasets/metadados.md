## Metadados


| Coluna            | Tipo        | Restrições           | Descrição                        |
|-------------------|------------ |----------------------|----------------------------------|
| data_infracao     | DATE        | NOT NULL             | Data que a infração foi cometida |
| hora_infracao     | TIME        | NOT NULL             | Hora que a infração foi cometida |
| data_implantacao  | DATE        | NOT NULL             | Data que a infração foi registrada no sistema |
| agente_equipamento| VARCHAR(20) | NOT NULL             | O meio ou equipamento utilizado pelo agente de trânsito para registrar a infração|
| cod_infracao      | INT64(10)   | NOT NULL             | Código que indentifica qual infração foi cometida |
| descricao_infracao| VARCHAR(200)| NOT NULL             | Descrição sobre a infração                   |
| local_cometimento | VARCHAR(20) | NOT NULL             | Local onde ocorreu a infração                |
| artigo            | INT64(10)   | NOT NULL             | O número do artigo do CTB que foi infringido |
| subdivisao_artigo | VARCHAR(20) | NOT NULL             | Inciso ou parágrafo dentro de um artigo do Código de Trânsito Brasileiro |




