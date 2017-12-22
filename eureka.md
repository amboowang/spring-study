## Cloud Foundary
Push the app and then create the user provided service by:

**Note**: Notice the `defaultZone` property in the eureka server. 
```
cf cups eureka -p "{\"url\": \"http://eureka-test.local.pcfdev.io/eureka/\"}"
```

Then in your client app yml file, the defaultZone would be:
```
# Spring properties
spring:
  application:
     name: accounts-service

# Discovery Server Access
eureka:
  instance:
    #instanceId: ${spring.application.name}:${spring.application.instance_id:${random.value}}
    instanceId:  ${vcap.application.name}:${vcap.application.application_id}:${CF_INSTANCE_INDEX:${random.value}}
    #instanceId:  ${vcap.application.name}:${random.value}
  client:
    serviceUrl:
      #defaultZone: ${vcap.services.eureka.credentials.url}
      #defaultZone: http://eureka-test.local.pcfdev.io/eureka
      defaultZone:  ${vcap.services.eureka.credentials.url:http://127.0.0.1:1111/eureka/}

# HTTP Server
server:
  port: ${PORT:2222}    # HTTP (Tomcat) port
```
**Note**: pay attentation to the credentials parameter name is correct in the yml file. Such as `url` 
