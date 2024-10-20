## Spring Core - The Fundamentals
### Direct Questions
1. What is Spring Framework? 🟢
2. What are the features of Spring Framework? 🟢
3. What are the advantages of using Spring Framework? 🟢
4. Give a brief overview of versions of Spring framework 🟢
5. What is dependency injection (DI)?
6. How does dependency injection improve code quality? 🟢
7. What are the types of DI? 🟢
8. Explain the concept of Dependency Injection (DI) in Spring. 🟢
9.  What is the Inversion of Control (IoC) principle, and how does the Spring IoC container implement it? 🟡
10. What are the different types of IoC containers provided by Spring? 🟡
11. Explain Inversion of Control(IoC) and types of IoC containers. 🟡
12. Explain the role of the Spring IoC container and how it manages beans. 🟡
13. What is a Spring Bean Factory? What are some of the implementations available?
14. What is a Spring Application Context? What are some example usages of one?
15. How does the Spring IoC container initialize the application context?
16. How do we configure our Spring Application? 🟢
17. Types of Metadata in Spring Framework? 🟢
18. Explain Spring Beans and their scopes. 🟢
19. What bean scopes are supported by Spring and what do they mean? Which is used by default? 🟢
20. Explain the different bean scopes in Spring and provide examples of when to use each scope.
21. How do you define a bean scope in Spring? Can you list and explain the different scopes available?
22. How does the scope of a bean (e.g., singleton, prototype) affect dependency injection?
23. How do you configure beans in Spring using XML, annotations, and Java-based configurations?
24. What are the different ways to configure a class as Spring Bean? 🟡
25. In the context of Spring, what is a “stereotype”? What are the existing stereotypes and what is the difference between them? 🟡
26. How do you load and inject properties into a Spring Bean? 🟡
27. How do you inject properties into beans using the Spring IoC container?
28. How do you configure properties in a Spring application using @Value?
29. How do you inject values from a properties file into a Spring bean using the @Value annotation?
30. What are the differences between constructor injection and setter injection in Spring? Provide examples of when you would use each. 🟡
31. Why is field injection generally not recommended in Spring? Are there any scenarios where it might be appropriate? 🟡
32. Explain Autowiring and its types
33. How does the @Autowired annotation work in Spring? What are the different ways you can use it?🟢
34. Explain the use of @Qualifier in Spring. How does it resolve issues with multiple bean candidates? 🟢
35. Describe the use of the @Primary annotation in Spring. When would you use it? 🟢
36. How do you manage external properties and environment variables in a Spring application to ensure portability across environments? 🟡
37. Describe the Spring bean lifecycle. 🟢
38. Describe the lifecycle of a Spring Bean. What are the key lifecycle events and callback methods? 🟢
39. What methods can be used for bean initialization in Spring? 🟢
40. What is the InitializingBean interface, and how is it used in Spring? 🟢
41. What is the DisposableBean interface, and how does it work in Spring? 🟢
42. How do you define custom initialization and destruction methods in Spring? 🟢
43. Explain the use of @PostConstruct and @PreDestroy annotations in Spring bean lifecycle management. 🟢
44. What is the SmartLifecycle interface, and how is it used in managing bean lifecycles? 🟡
45. What is a BeanPostProcessor, and how is it used to modify beans during their lifecycle? 🟢
46. What is a BeanFactoryPostProcessor, and how does it differ from BeanPostProcessor? 🟢
47. Explain how you manage complex bean lifecycles in a large Spring application. 🟡
48. How do you ensure that beans are properly initialized and destroyed in a Spring application that uses async processing? 🟡
49. Describe how you handle bean lifecycle events in a distributed Spring application. 🟡
50. Explain how you would optimize bean creation and destruction to improve application performance. 🟡
51. How do you test bean lifecycle methods in a Spring application? 🟡
52. What is Spring Expression Language (SpEL)? Provide an example of its use.
53. Explain the usage of SpEL in Spring applications. Can you give an example?
54. How do you use Spring Profiles in conjunction with dependency injection to manage environment-specific beans?
55. How do you use Spring Profiles to manage different configurations for different environments?

### Scenario Based Questions

1. Describe a situation where you encountered circular dependencies in Spring. How did you resolve it? 🔴
2. How do you handle circular dependencies in Spring? 🔴
3. Explain how you would manage dependency injection in a multi-threaded Spring application to ensure thread safety. 🔴 
4. Describe how you manage dependency injection in a Spring application with asynchronous tasks. 🔴
5. Explain how you use factory methods for dependency injection in Spring. Provide an example where this approach was beneficial. 🔴
6. You have multiple implementations of an interface. How do you configure Spring to inject the correct implementation based on runtime conditions? 🔴
8. How does dependency injection affect the performance of a Spring application? Describe a scenario where DI introduced performance bottlenecks and how you resolved them. 🔴
9. You need to refactor a legacy codebase to implement dependency injection with Spring. What steps do you take, and what challenges do you anticipate? 🔴
10. Explain how you manage complex configuration properties in a Spring application deployed across multiple environments. 🔴
11. Explain how you would configure a custom scope for a bean in Spring. Provide a real-world use case. 🔴
12. You have a requirement for a custom bean scope that isn't provided by default in Spring. How do you create and manage this custom scope? 🔴
13. How do you dynamically register beans in the Spring IoC container at runtime? 🔴
14. How would you dynamically inject beans at runtime based on user input or other dynamic factors? 🔴
15. Explain how you would conditionally inject a bean based on a specific property or environment variable. 🔴
16. Describe the lifecycle phases of a Spring bean from instantiation to destruction. 🔴
17. What is the SmartLifecycle interface, and how is it used in managing bean lifecycles? 🔴
18. How do you listen for and handle lifecycle events in Spring? 🔴
19. You need to create a custom annotation that combines multiple Spring annotations. How do you design and implement this? 🔴
20. How do you manage external properties and environment variables in a Spring application to ensure portability across environments?
21. You need to ensure certain beans are lazily initialized in your application. How do you configure this in Spring, and what are the potential pitfalls?
22. Imagine you need to migrate a large, monolithic Spring application to a microservices architecture. How do you handle the configuration management?
