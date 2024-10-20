## Spring Boot

### Direction questions
1. Difference between Spring and Spring Boot?
1. Advantages of using Spring Boot?
1. What is an embedded container in Spring Boot, and why is it important?
1. How does Spring Boot handle database connections?
1. What is Spring Security, and how does it work?
1. How does Spring Boot handle error handling and exception handling?
1. What is Spring Data, and how does it work with Spring Boot?
1. What are the different types of Bean scopes in Spring Boot?
1. What is the difference between Spring Boot and Spring MVC?
1. What is the purpose of the @Autowired annotation?
1. What is the difference between the @Component, @Service, and @Repository annotations in Spring Boot?
1. What is the use of profiles in Spring Boot?
1. How can you externalize the configuration properties in Spring Boot?
1. What are the different types of databases that are supported by Spring Boot?
1. Explain Spring Boot and its advantages
1. Differentiate between Spring and Spring Boot
1. Explain some of the most used Spring Boot annotations
1. Explain the internal working of @SpringBootApplication
1. Explain types of configuration in Spring Boot
1. Explain the role of the Tomcat server in the Spring Boot Application
1. What are Profiles in Spring Boot
1. What is an Actuator and its usage in Spring Boot
1. What are the features of Spring Boot?
1. Differentiate between Spring and Spring Boot.
1. Explain the advantages of using Spring Boot for application development.
1. What do you understand by the term ‘Spring Boot’?
1. What does @SpringBootApplication annotation do internally?
1. What are the uses of @RequestMapping and @RestController annotations in Spring Boot?
1. Can the default web server in the Spring Boot application be disabled?
1. How to disable specific auto-configuration class?
1. Can you tell how to exclude any package without using the basePackages filter?
1. Can we change the default port of the embedded Tomcat server in Spring boot?
1. What are the possible sources of external configuration?
1. What is Spring Boot dependency management system?
1. What are the effects of running a Spring Boot Application as a “Java Application”?

### Scenario based questions
1. You've been tasked to break down a monolithic application into microservices using Spring Boot. How would you go about designing and implementing this? What are some common pitfalls and how would you avoid them?
1. After breaking down the monolithic application, how would you ensure communication between microservices? What protocols or tools would you use?
 
### Spring Boot Auto-configuration
1. How would you customize the auto-configuration in Spring Boot for a specific requirement that isn't covered out-of-the-box? Can you give an example?
1. Custom Auto-Configuration: How do you create a custom auto-configuration class in Spring Boot? Provide an example of a scenario where you had to override the default auto-configuration.
1. Customized Bean Definitions: How would you go about customizing a specific bean’s configuration that is otherwise auto-configured by Spring Boot? Can you give a detailed example?
1. Conditionally Loading Beans: Explain how to create and use a custom condition to conditionally load beans in Spring Boot. When would this be particularly useful?
1. Conditional Beans: Explain how you would use @Conditional annotations to control bean creation based on specific conditions. Can you provide an example of a complex condition you handled?
1. Excluding Auto-configurations: Describe a situation where you had to exclude certain auto-configurations in your project. How did you handle it, and what was the outcome?
1. SpringFactoriesLoader: How does the SpringFactoriesLoader work in the context of Spring Boot auto-configuration? Can you provide an example of creating a custom auto-configuration?
1. Meta-annotations: Can you explain the role of meta-annotations in Spring Boot and how they can be used to create custom annotations for specific auto-configuration needs?
1. Profile-based Configuration: How would you handle auto-configuration that needs to change based on the active profile? Give a real-world example.
1. Profile-specific Beans: How do you define beans that should only be loaded for specific profiles in Spring Boot? Provide an example where this was crucial for your application.
1. Auto-configuration Classes: Explain the process of writing a custom auto-configuration class in Spring Boot. What are the best practices for doing so?
1. Integration with Non-standard Databases: Describe how you would approach integrating a non-standard database with Spring Boot, requiring a custom auto-configuration.
1. Third-party Library Integration: How do you handle the auto-configuration of a third-party library that is not natively supported by Spring Boot?
1. Testing Auto-configurations: What strategies do you use to test custom auto-configurations? Describe a challenging scenario you faced and how you resolved it.
1. Testing Customizations: How do you test customizations in Spring Boot applications, such as custom auto-configuration or conditional beans? Share a particularly challenging test case.
1. Custom Starters: Describe a situation where you needed to create a custom Spring Boot starter. What were the components and dependencies, and how did you package it?
1. Customizing Spring Boot Starters: Imagine you need to create a custom Spring Boot starter that integrates with a proprietary library. How would you approach building and maintaining this starter?
1. Multiple Data Sources: Describe how you would configure a Spring Boot application to connect to multiple data sources, each with different properties. Explain a scenario where this was necessary and how you managed the complexity.
1. Externalized Configuration: Explain how you manage externalized configuration properties in Spring Boot using the @ConfigurationProperties annotation. Describe a scenario where you had to deal with complex configuration requirements.
1. Custom Property Source: Describe how you would create and register a custom property source in Spring Boot. What was the use case, and how did it enhance your configuration management?
1. SpringApplicationBuilder: Explain how you would use SpringApplicationBuilder to customize the startup process of a Spring Boot application. Provide a real-world example of its application.
1. Advanced Configuration: Describe a situation where you had to fine-tune Spring Boot’s advanced configuration settings (e.g., DataSource properties, Server properties) to meet specific requirements.
1. Auto-configuration Conflicts: Suppose you encounter a situation where multiple auto-configuration classes are conflicting, leading to unexpected behavior. How would you debug and resolve this issue?
1. Zero-downtime Deployment: How would you implement a zero-downtime deployment strategy for a Spring Boot application running in a cloud environment? What tools and practices would you use to achieve this?
1. Dynamic Configuration Changes: How do you handle dynamic configuration changes in a running Spring Boot application without requiring a restart? Provide an example where you implemented such a solution.
 
### Custom Annotations
1. Have you ever created custom annotations in Spring? Describe the scenario and the benefits it brought to the project.
1. How do you maintain and document custom annotations to ensure other team members understand their purpose and usage?

### Exception Handling
1. Describe a situation where you had to design a robust exception handling mechanism for a Spring application. What challenges did you face, and how did you overcome them?
1. How do you ensure that exception handling doesn't degrade the user experience? Do you use any particular design patterns or best practices?

### Legacy Code Integration
1. You need to integrate Spring with a legacy system that doesn’t follow modern design patterns. How would you approach this?
1. Integrating with Legacy Systems: You need to integrate a modern Spring Boot application with a legacy system that has limited documentation. How would you approach this integration, ensuring minimal disruption to the legacy system?
1. When integrating with a legacy system, how do you manage differences in data models or formats?