## Metadados


| Coluna            | Tipo        | Restrições           | Descrição                        |
|-------------------|------------ |----------------------|----------------------------------|
| data_infracao     | DATE        | NOT NULL             | Data que a infração foi cometida |
| hora_infracao     | TIME        | NOT NULL             | Hora que a infração foi cometida |
| data_implantacao  | DATE        | NOT NULL             | Data que a infração foi registrada no sistema |
| agente_equipamento| TEXT        | NOT NULL             | O meio ou equipamento utilizado pelo agente de trânsito para registrar a infração|
| cod_infracao      | BIGINT      | NOT NULL             | Código que indentifica qual infração foi cometida |
| descricao_infracao| TEXT        | NOT NULL             | Descrição sobre a infração                   |
| local_cometimento | TEXT        | NOT NULL             | Local onde ocorreu a infração                |
| artigo            | TEXT        | NOT NULL             | O número do artigo do CTB que foi infringido |
| subdivisao_artigo | TEXT        | NOT NULL             | Inciso ou parágrafo dentro de um artigo do Código de Trânsito Brasileiro |




