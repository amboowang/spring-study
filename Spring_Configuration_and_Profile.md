# Spring Externalized Configuration
* https://docs.spring.io/spring-boot/docs/current/reference/html/boot-features-external-config.html
* https://docs.spring.io/spring-boot/docs/current/reference/html/common-application-properties.html

**Spring Profile:**
* https://docs.spring.io/spring-boot/docs/current/reference/html/boot-features-profiles.html

 ## Spring Expression Language (SpEL)
 * https://docs.spring.io/spring/docs/current/spring-framework-reference/html/expressions.html
 
 example:
 @Value("#{'${xxx.xxx}'=='sandbox' ? '${xxx.sandbox}' : '${xxx.production}'}")
 //With #{} it is an expression, with ${} it is a placeholder for a value
 
 
 @ConditionalOnExpression("'${server.host}'=='localhost'")  // can't apply to field
 
 ## How to do conditional auto-wiring in Spring?
* https://stackoverflow.com/questions/19225115/how-to-do-conditional-auto-wiring-in-spring
 
 
 
