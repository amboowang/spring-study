## Cloud Foundary
Push the app and then create the user provided service by:
```
cf cups eureka -p "{\"url\": \"http://eureka-test.local.pcfdev.io/eureka/\"}"
```

Then in your client app yml file, the defaultZone would be:
```
eureka:
  client:
    serviceUrl:
      defaultZone: ${vcap.services.eureka.credentials.url}
```
**Note**: pay attentation to the credentials parameter name is correct in the yml file. Such as `url` 
