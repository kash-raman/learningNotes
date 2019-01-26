Spring BOOT

Goal: 

* Provide a radically faster and widely accessible getting-started experience for all Spring development.
* Be opinionated out of the box but get out of the way quickly as requirements start to diverge from the defaults.
* Provide a range of non-functional features that are common to large classes of projects (such as embedded servers, security, metrics, health checks, and externalized configuration).
* Absolutely no code generation and no requirement for XML configuration.

Server : Tomcat, Jetty , Undertow 

 @EnableAutoConfiguration(exclude={}) - is non-invasive. Spring Boot auto-configuration attempts to automatically configure your Spring application based on the jar dependencies that you have added.
 you can also control the list of auto-configuration classes to exclude by using the spring.autoconfigure.exclude property. You can define exclusions both at the annotation level and by using the property.

A single@SpringBootApplication annotation can be used to enable those three features, that is:
* @EnableAutoConfiguration: enable Spring Boot’s auto-configuration mechanism
* @ComponentScan: enable @Component scan on the package where the application is located (see the best practices)
* @Configuration: allow to register extra beans in the context or import additional configuration classes



 @Configuration, @Import, @ComponentScan - one of these can be used when you have multiple configuration java files.

@ImportResources -if you have spring XML files.

Debug logs: 
using property file 
using —debug arg in jvm 

Application events are sent in the following order, as your application runs:
1. An ApplicationStartingEvent is sent at the start of a run but before any processing, except for the registration of listeners and initializers.
2. An ApplicationEnvironmentPreparedEvent is sent when the Environment to be used in the context is known but before the context is created.
3. An ApplicationPreparedEvent is sent just before the refresh is started but after bean definitions have been loaded.
4. An ApplicationStartedEvent is sent after the context has been refreshed but before any application and command-line runners have been called.
5. An ApplicationReadyEvent is sent after any application and command-line runners have been called. It indicates that the application is ready to service requests.
6. An ApplicationFailedEvent is sent if there is an exception on startup.


@SpringBootTEst
NONE,RANDOM,PORT,MOCK

