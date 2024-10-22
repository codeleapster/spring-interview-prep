## Container, Dependency Injection and IoC

### What is dependency injection and what are the advantages?

Dependency Injection is a technique where objects don't create their own dependencies. Instead, they declare what they need, and the framework supplies these dependencies to the objects.

**Types of Dependency Injection:**
- Constructor Injection
- Setter Injection
- Interface Injection

**Advantages of using Dependency Injection**
- Increases code reusability
- Increases code readibility
- Increases code maintainability
- Increases code testability
- Reduces coupling
- Increases cohesion

> [!NOTE]  
> Dependency Injection is a design pattern that solves the problem of flexing dependencies creation

> [!IMPORTANT]
> It is recommended to use interface for creating Spring beans as it allows for 
> - use of JDK Dynamic proxy
> - hides the implementation details
> - easily switch the beans

### What is meant by Application Context?

Application Context is a central part of Spring application. It holds bean definitions and contains registry of application components. It allows you to retrieve assembled and configured beans.

**Application Context:**
- Initiates Beans
- Configures Beans
- Assemblies Beans
- Manages Beans Lifecycle
- Is a Bean Factory
- Is a Resource Loader
- Has ability to push events to registered even listeners
- Exposes Environment which allows to resolve properties

**Common Application Context types:**
- AnnotationConfigApplicationContext
- AnnotationConfigWebApplicationContext
- ClassPathXmlApplicationContext
- FileSystemXmlApplicationContext
- XmlWebApplicationContext

### What is the concept of a "Container" and what is its lifecycle?

Container is an execution environment which provides additional technical services for your code to use. Usually containers use IoC technique, that allows you to focus on
creating business aspect of the code, while technical aspects like communication details (HTTP, REST, SOAP) are provided by execution environment.

Spring provides a container for beans. It manages lifecycle of the beans and also provides additional services through usage of Application Context.

**Spring Container Lifecycle:**
1. Application is started.
1. Spring container is created.
1. Containers reads configuration.
1. Beans definitions are created from configuration.
1. BeanFactoryPostProcessors are processing bean definitions.
1. Instances of Spring Beans are created.
1. Spring Beans are configured and assembled - resolve property values and inject dependencies
1. BeanPostProcessors are called.
1. Application Runs.
1. Application gets shutdown.
1. Spring Context is closed.
1. Destruction callbacks are invoked.

### How are you going to create a new instance of an ApplicationContext?

**Non Web Applications Way:**
- AnnotationConfigApplicationContext
- ClassPathXmlApplicationContext
- FileSystemXmlApplicationContext
 
**Web Applications Way:**
- Servlet 2 - web.xml, ContextLoaderListener, DispatcherServlet
- Servlet 3 - XmlWebApplicationContext
- Servlet 3 - AnnotationConfigWebApplicationContext

**Spring Boot Way:**
- SpringBootConsoleApplication CommandLineRunner
- SpringBootWebApplication Embedded Tomcat

### Can you describe the lifecycle of a Spring Bean in an ApplicationContext?

1. Context is Created:
   1. Beans Definitions are created based on Spring Bean Configuration.
   2. BeanFactoryPostProcessors are invoked.

1. Bean is Created:
   1. Instance of Bean is Created.
   2. Properties and Dependencies are set.
   3. BeanPostProcessor::postProcessBeforeInitialization gets called.
   4. @PostConstruct method gets called.
   5. InitializingBean::afterPropertiesSet method gets called.
   6. @Bean(initMethod) method gets called
   7. BeanPostProcessor::postProcessAfterInitialization gets called.

1. Bean is Ready to use.

1. Bean is Destroyed:
   1. @PreDestroy method gets called.
   2. DisposableBean::destroy method gets called.
   3. @Bean(destroyMethod) method gets
   
### How are you going to create an ApplicationContext in an integration test?

1. Make sure that you have spring test dependency added:

```xml
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-test</artifactId>
    <scope>test</scope>
</dependency>
```
2. Add Spring Runner to your test
```java
@RunWith(SpringRunner.class)
```
3. Add Context Configuration to your test
```java
@ContextConfiguration(classes = ApplicationConfiguration.class)
```

### What is the preferred way to close an application context? Does Spring Boot do this for you?

- Standalone Non Web Applications
  - Register Shutdown hook by calling ConfigurableApplicationContext#registerShutdownHook - Recommended way
  - Call ConfigurableApplicationContext#close
- Web Application
  - ContextLoaderListener will automatically close context when web container will stop web application
- Spring Boot
  - Application Context will be automatically closed
  - Shutdown hook will be automatically registered
  - ContextLoaderListener applies to Spring Boot Web Applications as well
  
### Can you describe: Dependency Injection using Java Configuration

When using Dependency Injection using Java Configuration you need to explicitly define all your beans and you need to use @ Autowire on @Bean method level to inject dependencies.

```java
@Configuration
public class ApplicationConfiguration {
    @Bean
    @Autowired
    public SpringBean1 springBean1(SpringBean2 springBean2, SpringBean3 springBean3) {
        return new SpringBean1(springBean2, springBean3);
    }

    @Bean
    public SpringBean2 springBean2() {
        return new SpringBean2();
    }

    @Bean
    public SpringBean3 springBean3() {
        return new SpringBean3();
    }
}
```

### Can you describe: Dependency Injection using annotations (@Component, @Autowired)

- Create classes annotated with @Component annotations
```java
@Component
public class SpringBean1
```
```java
@Component
public class SpringBean2
```
```java
@Component
public class SpringBean3
```
- Define dependencies when required
```java
@Autowired
private SpringBean2 springBean2;

@Autowired
private SpringBean3 springBean3;
```
- Create Configuration with Component Scanning Enabled
```java
@ComponentScan
public class ApplicationConfiguration {
}
```

### Can you describe: Component scanning

Process in which Spring is scanning Classpath in search for classes annotated with stereotypes annotations (@Component, @Repository, @Service, @Controller, …) and based on those creates beans definitions.

- Simple component scanning within Configuration package and all subpackages
```java
@ComponentScan
public class ApplicationConfiguration {
}
```

- Advanced Component Scanning Rules
```java
@ComponentScan(
	basePackages = "com.spring.professional.exam.tutorial.module01.question10.annotations.beans",
	//basePackageClasses = SpringBean1.class,
	includeFilters = @ComponentScan.Filter(type = FilterType.REGEX, pattern = ".*Bean.*"),
	excludeFilters = @ComponentScan.Filter(type = FilterType.REGEX, pattern = ".*Bean1.*")
)
public class ApplicationConfigurationAdvanced {
}
```
### Can you describe: Sterotypes

Stereotypes are annotations applied to classes to describe role which will be performed by this class. Spring discovered classes annotated by stereotypes and creates bean definitions based on those types.

**Types of stereotypes:**
- Component - generic component in the system, root stereotype, candidate for autoscanning
- Service - class will contain business logic
- Repository - class is a data repository (used for data access objects, persistence)
- Controller - class is a controller, usually a web controller (used with @ RequestMapping

### Can you describe: Meta-Annotations

Meta-annotations are annotations that can be used to create new annotations.

**Example of Meta-Annotation:**
@RestController annotation is using @Controller and ResponseBody to define its behavior
```java
@Target({ElementType.TYPE})
@Retention(RetentionPolicy.RUNTIME)
@Documented
@Controller
@ResponseBody
public @interface RestController {
    @AliasFor(
        annotation = Controller.class
    )
    String value() default "";
}
```

### Can you describe: Scopes for Spring beans. What is the default scope?

|Scope|Description|
|--------|-------|
|Singleton|Single Bean per Spring Container - Default|
|Prototype| New Instance each time Bean is Requested|
|Request| New Instance per each HTTP Request|
|Session|New Instance per each HTTP Session|
|Application|One Instance per each ServletContext|
|Websocket|One Instance per each WebSocket|

### Are beans lazily or eagerly instantiated by default? How do you alter this behavior?

**Lazy and Eager Instance Creation vs Scope Type:**
- Singleton Beans are eagerly instantiated by default
- Prototype Beans are lazily instantiated by default (instance is created when bean is requested)
  - …however, if Singleton Bean has dependency on Prototype Bean, then Prototype Bean Instance will be created eagerly to satisfy dependencies for Singleton Bean

**Altering Behavior:**
- You can change default behavior for all beans by @ComponentScan annotation
  ```java
  @ComponentScan(lazyInit = true)
  ```
  - Setting lazyInit to true, will make all beans lazy, even Singleton Beans
  - Setting lazyInit to false (default), will create Singleton Beans Eagerly and Prototype Beans Lazily
- You can also change default behavior by using @Lazy annotation:
  - @Lazy annotation takes one parameter - Whether lazy initialization should occur
  - By default @Lazy is used to mark bean as lazily instantiated
  - You can use @Lazy(false) to force Eager Instantiation - use case for @ComponentScan(lazyInit = true ) when some beans always needs to be instantiated eagerly
- @Lazy can be applied to
  - Classed annotated with @Component makes bean Lazy or as specified by @Lazy parameter
  - Classes annotated with @Configuration annotation make all beans provided by configuration lazy or as specified by @Lazy parameter
  - Method annotated with @Bean annotation makes bean created by method Lazy or as specified by @Lazy parameter

### What is a property source? How would you use @PropertySource?

PropertySource is Spring Abstraction on Environment Key-Value pairs, which can come from:
- JVM Properties
- System Environmental Variables
- JNDI Properties
- Servlet Parameters
- Properties File Located on Filesystem
- Properties File Located on Classpath

You read properties with usage of @PropertySource or @PropertySources annotation:
```java
@PropertySources({
        @PropertySource("file:${app-home}/app-db.properties"),
        @PropertySource("classpath:/app-defaults.properties")
})
```

You access properties with the usage of @Value annotation:
```java
@Value("${db.host}")
private String dbHost;
```

### What is a BeanFactoryPostProcessor and what is it used for? When is it invoked? Why would you define a static @Bean method? What is a ProperySourcesPlaceholderConfigurer used for?

BeanFactoryPostProcessor is an interface that contains single method postProcessBeanFactory, implementing it allows you to create logic that will modify Spring Bean Metadata before any Bean is created. BeanFactoryPostProcessor does not create any beans, however it can access and alter Metadata that is used later to create Beans.

BeanFactoryPostProcessor is invoked after Spring will read or discover Bean Definitions, but before any Spring Bean is created. 

Because BeanFactoryPostProcessor is also a Spring Bean, but a special kind of Bean that should be invoked before other types of beans get created, Spring needs to have ability to create it before any other beans. This is why BeanFactoryPostProcessors needs to be registered from static method level.

```java
@Bean
public static CustomBeanFactoryPostProcessor customerBeanFactoryPostProcessor() {
	return new CustomBeanFactoryPostProcessor();
}
```

PropertySourcesPlaceholderConfigurer is a BeanFactoryPostProcessor that is used to resolve properties placeholder in Spring Beans on fields annotated with @Value("${ property_name}").

```java
@Value("${app.env}")
private String appEnv;

@Value("${app.envid}")
private String appEnvId;
```

### 