# microservice-eurekaserver-cloud

## Criar a imagem:
````
mvn spring-boot:build-image ou mvn spring-boot:build-image -DskipTest
````

## @EnableEurekaServer
> Esta anotação fará o projeto spring boot ou microserviço agir como um agente de descoberta de serviço.

> *** Atenção *** : ribbon não é mais necessário em versões mais modernas.

> Alguns detalhes para o funcionamento e acionamento do projeto:
> 
> 1 - Lembrar que como o profile está git no config-server(verificar o application.properties dele),
> tem que ver se o link para o eurekaserver.properties também está lá.
> 
> 2 - Aciona primeiro o config-server-bank e depois o eureka-server.
> 
> 3 - Depois de acionados, verificar os serviços descobertos pelo eureka em: localhost:8070