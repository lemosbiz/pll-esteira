## Como executar o servidor

    java -jar pll-connector-server-1.0.0.jar --spring.datasource.url=jdbc:mysql://<host>:<port>/<database> --spring.datasource.username=<user> --spring.datasource.password=<password>

O servidor sobe na porta 9000. É possível customizar passando mais um parâmetro adicional:

    --server.port=<port>

No arquivo schema.sql está a estrutura de banco que eu utilizei.

