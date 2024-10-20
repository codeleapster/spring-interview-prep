## Spring Core - The Fundamentals
### Direct Questions
1. What is Spring Framework? 🟢
1. Give a brief overview of versions of Spring framework 🟢
1. What are the features of Spring Framework? 🟢
1. What are the advantages of using Spring Framework? 🟢
1. What is Dependency Injection in Spring, and how does it improve code quality? 🟢
1. What is dependency injection (DI)? What are the types of DI? 🟢
1. Explain the concept of Dependency Injection (DI) in Spring. 🟢
1. Explain Dependency Injection(DI) and its types? 🟢
1. Explain Inversion of Control(IoC) and types of IoC containers. 🟡
1. Explain the role of the Spring IoC container and how it manages beans. 🟡
1. What is the Inversion of Control (IoC) principle, and how does the Spring IoC container implement it? 🟡
1. How does the Spring IoC container initialize the application context?
1. What is a Spring Bean Factory? What are some of the implementations available?
1. What is a Spring Application Context? What are some example usages of one?
1. What are the different types of IoC containers provided by Spring? 🟡
1. How do we configure our Spring Application? 🟢
1. Types of Metadata in Spring Framework? 🟢
1. What are the different ways to configure a class as Spring Bean? 🟡
1. In the context of Spring, what is a “stereotype”? What are the existing stereotypes and what is the difference between them? 🟡
1. How do you load and inject properties into a Spring Bean? 🟡
1. How do you manage external properties and environment variables in a Spring application to ensure portability across environments? 🔴
1. What are the differences between constructor injection and setter injection in Spring? Provide examples of when you would use each. 🟡
1. Why is field injection generally not recommended in Spring? Are there any scenarios where it might be appropriate? 🟡
1. How does the @Autowired annotation work in Spring? What are the different ways you can use it?
1. Explain the use of @Qualifier in Spring. How does it resolve issues with multiple bean candidates?
1. Describe the use of the @Primary annotation in Spring. When would you use it?
1. Explain Spring Beans and their scopes. 🟢
1. Describe the Spring bean lifecycle. 🟢
1. What bean scopes are supported by Spring and what do they mean? Which is used by default? 🟢
1. What methods can be used for bean initialization in Spring? 🟡
1. Describe the lifecycle of a Spring Bean. What are the key lifecycle events and callback methods?
1. What is the InitializingBean interface, and how is it used in Spring? 🟡
1. What is the DisposableBean interface, and how does it work in Spring? 🟡
1. How do you define custom initialization and destruction methods in Spring? 🟡
1. Explain the use of @PostConstruct and @PreDestroy annotations in Spring bean lifecycle management. 🟡
1. What is the SmartLifecycle interface, and how is it used in managing bean lifecycles?
1. What is a BeanPostProcessor, and how is it used to modify beans during their lifecycle? 🟡
1. What is a BeanFactoryPostProcessor, and how does it differ from BeanPostProcessor? 🟡
1. Explain how you manage complex bean lifecycles in a large Spring application.
1. How do you ensure that beans are properly initialized and destroyed in a Spring application that uses async processing?
1. Describe how you handle bean lifecycle events in a distributed Spring application.
1. Explain how you would optimize bean creation and destruction to improve application performance.
1. How do you test bean lifecycle methods in a Spring application?
1. Explain the different bean scopes in Spring and provide examples of when to use each scope.
1. How do you define a bean scope in Spring? Can you list and explain the different scopes available?
1. How does the scope of a bean (e.g., singleton, prototype) affect dependency injection?
1. How do you configure beans in Spring using XML, annotations, and Java-based configurations?
1. What is Spring Expression Language (SpEL)? Provide an example of its use.
1. How do you inject properties into beans using the Spring IoC container?
1. How do you configure properties in a Spring application using @Value?
1. How do you inject values from a properties file into a Spring bean using the @Value annotation?
1. Explain the usage of SpEL in Spring applications. Can you give an example?
1. How do you use Spring Profiles in conjunction with dependency injection to manage environment-specific beans?
1. How do you use Spring Profiles to manage different configurations for different environments?
1. Explain Autowiring and its types

### Scenario Based Questions

1. Describe a situation where you encountered circular dependencies in Spring. How did you resolve it? 🔴
1. How do you handle circular dependencies in Spring?
1. Describe a situation where you encountered circular dependencies in Spring. How did you resolve it? 🔴
1. Explain how you would manage dependency injection in a multi-threaded Spring application to ensure thread safety. 🔴 
1. Describe how you manage dependency injection in a Spring application with asynchronous tasks. 🔴
1. Explain how you use factory methods for dependency injection in Spring. Provide an example where this approach was beneficial. 🔴
1. How do you manage dependency injection in a microservices architecture, ensuring each service has the necessary dependencies while maintaining loose coupling? 🔴
1. You have multiple implementations of an interface. How do you configure Spring to inject the correct implementation based on runtime conditions? 🔴
1. How does dependency injection affect the performance of a Spring application? Describe a scenario where DI introduced performance bottlenecks and how you resolved them. 🔴
1. You need to refactor a legacy codebase to implement dependency injection with Spring. What steps do you take, and what challenges do you anticipate? 🔴
1. Explain how you manage complex configuration properties in a Spring application deployed across multiple environments. 🔴
1. Describe how you would use Spring Core concepts to develop a microservices architecture. How do you handle inter-service communication and configuration management? 🔴
1. Explain how you would configure a custom scope for a bean in Spring. Provide a real-world use case. 🔴
1. How do you dynamically register beans in the Spring IoC container at runtime? 🔴
1. How would you dynamically inject beans at runtime based on user input or other dynamic factors? 🔴
1. You have a requirement for a custom bean scope that isn't provided by default in Spring. How do you create and manage this custom scope? 🔴
1. Explain how you would conditionally inject a bean based on a specific property or environment variable. 🔴
1. Describe the lifecycle phases of a Spring bean from instantiation to destruction. 🔴
1. What is the SmartLifecycle interface, and how is it used in managing bean lifecycles? 🔴
1. How do you listen for and handle lifecycle events in Spring? 🔴
1. You need to create a custom annotation that combines multiple Spring annotations. How do you design and implement this? 🔴
1. How do you manage external properties and environment variables in a Spring application to ensure portability across environments?
1. Explain how you would configure a custom scope for a bean in Spring. Provide a real-world use case.
1. You need to ensure certain beans are lazily initialized in your application. How do you configure this in Spring, and what are the potential pitfalls?
1. Imagine you need to migrate a large, monolithic Spring application to a microservices architecture. How do you handle the configuration management?
1. Explain how you manage complex configuration properties in a Spring application deployed across multiple environments.
1. How do you manage external properties and environment variables in a Spring application to ensure portability across environments?
