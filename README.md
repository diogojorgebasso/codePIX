# CodePIX - transação instantânea de capital

![image](https://user-images.githubusercontent.com/65865529/106500126-37e17700-64a0-11eb-866b-b80fa1223d9c.png)


##Principais desafios:
- comunicação rápida e eficiente
- criação e consulta instantânea das chaves (Síncrona)
- garantia de que nenhuma transação seja perdida

## Stacks:
- gRPC: framework muito ultilizado para microserviços, utlilizando protocol buffers e HTTP 2.0 
- Apache Kafka: processamento poderoso de dados

### Como o software interage com o as stacks:
- será capaz de atuar como um servidor gRPC
- consumir e publicar mensagens no apache kafka
- Ambas operações devem ser realizadas de forma simultânia ao executar o serviço
- Trabalhar com DDD (Domain Driven Domain)

A aplicação é flexível para a implementação de outros formatos: REST, graphQL

### Desing de software

Arquitetura Hexagonal / Ports and Adapters

### Estrutura e camadas do 
![image](https://user-images.githubusercontent.com/65865529/106503595-a0caee00-64a4-11eb-9b76-217ce3b8c385.png)

### Serviços utilizados ao executar o docker-compose
Aplicação principal
Postgres
PgAdmin
Apache Kafka
Criador dos tópicos a serem utilizados pelo Kafka
Confluent control center
ZooKeeper
