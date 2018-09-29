## Como executar o servidor

    java -jar pll-connector-server\pll-connector-server.jar --spring.datasource.url=jdbc:mysql://<host>:<port>/<database> --spring.datasource.username=<user> --spring.datasource.password=<password>

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
|Password      |575e7dfae73659d                 |

Para rodar o servidor apontando para o banco de testes da cloud:

    java -jar pll-connector-server\pll-connector-server.jar --spring.datasource.url=jdbc:mysql://us-cdbr-iron-east-01.cleardb.net:3306/ad_f4e16b10f49e489 --spring.datasource.username=bd59731e9e9cb9 --spring.datasource.password=575e7dfae73659d

## Instalação

Para instalar deve-se copiar a pasta pll-connector-server para a máquina onde a aplicação vai ficar hospedada. É possível alterar os parâmetros de execução da aplicação editando o arquivo pll-connector-server.xml.

Usando um prompt de comando com permissão administrativa executar os seguintes comandos:
    cd pll-connector-server
    pll-connector-server.exe install
    net start pll-connector-server

Isto irá instalar o pll-connector-server como um serviço do windows e executá-lo. Depois disto é possível abrir o gerenciador de serviços do windows e configurar o serviço como desejar.

## Logs

Na pasta logs vão ser criados 3 arquivos de log.
- pll-connector-server.wrapper.log: loga a atividade do agente que executa a aplicação java.
- pll-connector-server.out.log: loga a atividade do servidor. Este log é importante para monitoração do andamento da aplicação.
- pll-connector-server.err.log: loga os erros da aplicação.
