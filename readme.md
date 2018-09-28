## Como executar o servidor

    java -jar pll-connector-server-1.0.0.jar --spring.datasource.url=jdbc:mysql://<host>:<port>/<database> --spring.datasource.username=<user> --spring.datasource.password=<password>

O servidor sobe na porta 9000. É possível customizar passando mais um parâmetro adicional:

    --server.port=<port>

No arquivo schema.sql está a estrutura de banco que eu utilizei.

## Banco de testes na cloud

|Propriedade   |Valor                           |
|--------------|--------------------------------|
|Hostname      |us-cdbr-iron-east-01.cleardb.net|
|Porta         |3306                            |
|Banco de dados|ad_f4e16b10f49e489              |
|Username      |bd59731e9e9cb9                  |
|Password      |ef11f232                        |

Para rodar o servidor apontando para o banco de testes da cloud:

    java -jar pll-connector-server-1.0.0.jar --spring.datasource.url=jdbc:mysql://us-cdbr-iron-east-01.cleardb.net:3306/ad_f4e16b10f49e489 --spring.datasource.username=bd59731e9e9cb9 --spring.datasource.password=ef11f232
