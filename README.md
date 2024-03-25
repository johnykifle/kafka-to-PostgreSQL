# Kafka-to-PostgreSQL

Start kafka with 

``` docker-compose up -d ```

The above command starts Kafka container. If all is ok you can open in browser http://localhost:3040

### Produce message to Kafka

``` kafkactl produce my-topic --key=my-key --value="{name:value, age: 523}" ```


### Consume message from kafka

#### via Web UI
  -  Just open http://localhost:3040 -> Topics -> chose your topic name

#### via terminal
 - start on one shell ``` kafkactl consume my-topic```
 - on other shell start to product messages on `my-topic` by 
   ``` kafkactl produce my-topic --key=my-key --value="{name:value, age: 523}" ```

#### Via dotnet
  - Run the app with `dotnet run` and the application is ready to consume messages.
 
