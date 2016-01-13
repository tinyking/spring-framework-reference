# Summary

* [简介](README.md)
* [Spring框架概述](Part I. Overview of Spring Framework/README.md)
   * [入门](Part I. Overview of Spring Framework/1. Getting Started With Spring.md)
   * [介绍](Part I. Overview of Spring Framework/2. Introduction to Spring Framework.md)
       * [依赖注入 DI、反转控制 IOC](Part I. Overview of Spring Framework/2.1 Dependency Injection and Inversion of Control.md)
       * [模块](Part I. Overview of Spring Framework/2.2 Modules.md)
           * [核心容器](Part I. Overview of Spring Framework/Core Container.md)
           * [AOP、仪表](Part I. Overview of Spring Framework/AOP and Instrumentation.md)
           * [消息](Part I. Overview of Spring Framework/Messaging.md)
           * [数据接入及集成](Part I. Overview of Spring Framework/Data Access Integration.md)
           * [Web](Part I. Overview of Spring Framework/Web.md)
           * [Test](Part I. Overview of Spring Framework/Test.md)
       * [使用情景](Part I. Overview of Spring Framework/2.3 Usage scenarios.md)
           * [依赖管理及命名公约](Part I. Overview of Spring Framework/Dependency Management and Naming Conventions.md)
           * [Spring依赖、依赖Spring](Part I. Overview of Spring Framework/Spring Dependencies and Depending on Spring.md)
           * [Maven依赖管理](Part I. Overview of Spring Framework/Maven Dependency Management.md)
           * [Maven依赖清单](Part I. Overview of Spring Framework/Maven "Bill Of Materials" Dependency.md)
           * [Gradle依赖管理](Part I. Overview of Spring Framework/Gradle Dependency Management.md)
           * [Ivy依赖管理](Part I. Overview of Spring Framework/Ivy Dependency Management.md)
           * [分布式Zip文件](Part I. Overview of Spring Framework/Distribution Zip Files.md)
       * [Logging](Part I. Overview of Spring Framework/Logging.md)
           * [不使用Commons Logging](Part I. Overview of Spring Framework/Not Using Commons Logging.md)
           * [使用SLF4J](Part I. Overview of Spring Framework/Using SLF4J.md)
           * [使用Log4J](Part I. Overview of Spring Framework/Using Log4J.md)
               * [运行时容器与本地JCL](Part I. Overview of Spring Framework/Runtime Containers with Native JCL.md)
* [Spring Framework 4.x新特性](Part II. What’s New in Spring Framework 4.x/README.md)
   * [Spring框架4.0增强及新特性](Part II. What’s New in Spring Framework 4.x/3. New Features and Enhancements in Spring Framework 4.0.md)
       * [改善入门体验](Part II. What’s New in Spring Framework 4.x/3.1 Improved Getting Started Experience.md)
       * [移除弃用的包和方法](Part II. What’s New in Spring Framework 4.x/3.2 Removed Deprecated Packages and Methods.md)
       * [Java 8 (Java 6、7)](Part II. What’s New in Spring Framework 4.x/3.3 Java 8 (as well as 6 and 7)
       * [Java EE 6、7](Part II. What’s New in Spring Framework 4.x/3.4 Java EE 6 and 7.md)
       * [Groovy Bean定义DSL](Part II. What’s New in Spring Framework 4.x/3.5 Groovy Bean Definition DSL.md)
       * [核心容器改进](Part II. What’s New in Spring Framework 4.x/3.6 Core Container Improvements.md)
       * [通用Web改进](Part II. What’s New in Spring Framework 4.x/3.7 General WEeb Improvements.md)
       * WebSocket、SockJS、STOMP Messaging
       * 测试改进
   * [Spring框架4.1增强及新特性](Part II. What’s New in Spring Framework 4.x/4. New Features and Enhancements in Spring Framework 4.1.md)
       * JMS改进
       * Caching改进
       * Web改进
       * WebSocket STOMP Messaging改进
       * 测试改进
* [核心技术]
   * IoC容器
       * Spring Ioc容器及beans介绍
       * 容器概览
           * 配置元数据
           * 容器实例化
               * 基于XML的配置
           * 容器使用
       * Bean概览
           * 命名beans
               * Bean别名
           * Beans实例化
               * 构造函数实例化
               * 静态工厂方法实例化
               * 静态工厂实例方法实例化
       * 依赖
           * 反转依赖
               * 构造函数反转依赖
               * Setter反转依赖
               * Dependency resolution process
               * [DI实例]Examples of dependency injection
           * Dependencies and configuration in detail
               * Straight values (primitives, Strings, and so on)
               * References to other beans (collaborators)
               * Inner beans
               * Collections
               * Null and empty string values
               * XML shortcut with the p-namespace
               * XML shortcut with the c-namespace
               * Compound property names
           * Using depends-on
           * Lazy-initialized beans
           * Autowiring collaborators
               * Limitations and disadvantages of autowiring
               * Excluding a bean from autowiring
           * Method injection
               * Lookup method injection
               * Arbitrary method replacement
       * Bean scopes
           * The singleton scope
           * The prototype scope
           * Singleton beans with prototype-bean dependencies
           * Request, session, and global session scopes
               * Initial web configuration
               * Request scope
               * Session scope
               * Global session scope
               * Application scope
               * Scoped beans as dependencies
           * Custom scopes
               * Creating a custom scope
               * Using a custom scope
       * Customizing the nature of a bean
           * Lifecycle callbacks
               * Initialization callbacks
               * Destruction callbacks
               * Default initialization and destroy methods
               * Combining lifecycle mechanisms
               * Startup and shutdown callbacks
               * Shutting down the Spring IoC container gracefully in non-web applications
           * ApplicationContextAware and BeanNameAware
           * Other Aware interfaces
       * Bean definition inheritance
       * Container Extension Points
           * Customizing beans using a BeanPostProcessor
               * Example: Hello World, BeanPostProcessor-style
               * Example: The RequiredAnnotationBeanPostProcessor
           * Customizing configuration metadata with a BeanFactoryPostProcessor
               * Example: the Class name substitution PropertyPlaceholderConfigurer
               * Example: the PropertyOverrideConfigurer
           * Customizing instantiation logic with a FactoryBean
       * Annotation-based container configuration
           * `@Required`
           * `@Autowired`
           * Fine-tuning annotation-based autowiring with qualifiers
           * Using generics as autowiring qualifiers
           * CustomAutowireConfigurer
           * @Resource
           * @PostConstruct and @PreDestroy
       * Classpath scanning and managed components
           * @Component and further stereotype annotations
           * Meta-annotations
           * Automatically detecting classes and registering bean definitions
           * Using filters to customize scanning
           * Defining bean metadata within components
           * Naming autodetected components
           * Providing a scope for autodetected components
           * Providing qualifier metadata with annotations
       * Using JSR 330 Standard Annotations
           * Dependency Injection with @Inject and @Named
           * @Named: a standard equivalent to the @Component annotation
           * Limitations of the standard approach
       * Java-based container configuration
           * Basic concepts: @Bean and @Configuration
           * Instantiating the Spring container using AnnotationConfigApplicationContext
               * Simple construction
               * Building the container programmatically using register(Class<?>…)
               * Enabling component scanning with scan(String…)
               * Support for web applications with AnnotationConfigWebApplicationContext
           * Using the @Bean annotation
               * Declaring a bean
               * Receiving lifecycle callbacks
               * Specifying bean scope
               * Customizing bean naming
               * Bean aliasing
               * Bean description
           * Using the @Configuration annotation
               * Injecting inter-bean dependencies
               * Lookup method injection
               * Further information about how Java-based configuration works internally
           * Composing Java-based configurations
               * Using the @Import annotation
               * Conditionally including @Configuration classes or @Beans
               * Combining Java and XML configuration
       * Environment abstraction
           * Bean definition profiles
               * @Profile
           * XML Bean definition profiles
               * Enabling a profile
               * Default profile
           * PropertySource Abstraction
           * @PropertySource
           * Placeholder resolution in statements
       * Registering a LoadTimeWeaver
       * Additional Capabilities of the ApplicationContext
           * Internationalization using MessageSource
           * Standard and Custom Events
           * Convenient access to low-level resources
           * Convenient ApplicationContext instantiation for web applications
           * Deploying a Spring ApplicationContext as a Java EE RAR file
       * The BeanFactory
           * BeanFactory or ApplicationContext?
           * Glue code and the evil singleton
   * Resources
       * Introduction
       * The Resource interface
       * Built-in Resource implementations
           * UrlResource
           * ClassPathResource
           * FileSystemResource
           * ServletContextResource
           * InputStreamResource
           * ByteArrayResource
       * The ResourceLoader
       * The ResourceLoaderAware interface
       * Resources as dependencies
       * Application contexts and Resource paths
           * Constructing application contexts
               * Constructing ClassPathXmlApplicationContext instances - shortcuts
           * Wildcards in application context constructor resource paths
               * Ant-style Patterns
               * The Classpath*: portability classpath*: prefix
               * Other notes relating to wildcards
           * FileSystemResource caveats
   * Validation, Data Binding, and Type Conversion
       * Introduction
       * Validation using Spring’s Validator interface
       * Resolving codes to error messages
       * Bean manipulation and the BeanWrapper
           * Setting and getting basic and nested properties
           * Built-in PropertyEditor implementations
               * Registering additional custom PropertyEditors
       * Spring Type Conversion
           * Converter SPI
           * ConverterFactory
           * GenericConverter
               * ConditionalGenericConverter
           * ConversionService API
           * Configuring a ConversionService
           * Using a ConversionService programmatically
       * Spring Field Formatting
           * Formatter SPI
           * Annotation-driven Formatting
               * Format Annotation API
           * FormatterRegistry SPI
           * FormatterRegistrar SPI
           * Configuring Formatting in Spring MVC
       * Configuring a global date & time format
       * Spring Validation
           * Overview of the JSR-303 Bean Validation API
           * Configuring a Bean Validation Provider
               * Injecting a Validator
               * Configuring Custom Constraints
               * Spring-driven Method Validation
               * Additional Configuration Options
           * Configuring a DataBinder
           * Spring MVC 3 Validation
               * Triggering @Controller Input Validation
               * Configuring a Validator for use by Spring MVC
               * Configuring a JSR-303/JSR-349 Validator for use by Spring MVC
   * Spring Expression Language (SpEL)
       * Introduction
       * Feature Overview
       * Expression Evaluation using Spring’s Expression Interface
           * The EvaluationContext interface
               * Type Conversion
           * Parser configuration
           * SpEL compilation
               * Compiler configuration
               * Compiler limitations
       * Expression support for defining bean definitions
           * XML based configuration
           * Annotation-based configuration
       * Language Reference
           * Literal expressions
           * Properties, Arrays, Lists, Maps, Indexers
           * Inline lists
           * Inline Maps
           * Array construction
           * Methods
           * Operators
               * Relational operators
               * Logical operators
               * Mathematical operators
           * Assignment
           * Types
           * Constructors
           * Variables
               * The #this and #root variables
           * Functions
           * Bean references
           * Ternary Operator (If-Then-Else)
           * The Elvis Operator
           * Safe Navigation operator
           * Collection Selection
           * Collection Projection
           * Expression templating
       * Classes used in the examples
   * Aspect Oriented Programming with Spring
       * Introduction
           * AOP concepts
           * Spring AOP capabilities and goals
           * AOP Proxies
       * `@AspectJ` support
           * Enabling `@AspectJ` Support
               * Enabling `@AspectJ` Support with Java configuration
               * Enabling `@AspectJ` Support with XML configuration
           * Declaring an aspect
           * Declaring a pointcut
               * Supported Pointcut Designators
               * Combining pointcut expressions
               * Sharing common pointcut definitions
               * Examples
               * Writing good pointcuts
           * Declaring advice
               * Before advice
               * After returning advice
               * After throwing advice
               * After (finally) advice
               * Around advice
               * Advice parameters
               * Advice ordering
           * Introductions
           * Aspect instantiation models
           * Example
       * Schema-based AOP support
           * Declaring an aspect
           * Declaring a pointcut
           * Declaring advice
               * Before advice
               * After returning advice
               * After throwing advice
               * After (finally) advice
               * Around advice
               * Advice parameters
               * Advice ordering
           * Introductions
           * Aspect instantiation models
           * Advisors
           * Example
       * Choosing which AOP declaration style to use
           * Spring AOP or full AspectJ?
           * `@AspectJ` or XML for Spring AOP?
       * Mixing aspect types
       * Proxying mechanisms
           * Understanding AOP proxies
       * Programmatic creation of `@AspectJ` Proxies
       * Using AspectJ with Spring applications
           * Using AspectJ to dependency inject domain objects with Spring
               * Unit testing `@Configurable` objects
               * Working with multiple application contexts
           * Other Spring aspects for AspectJ
           * Configuring AspectJ aspects using Spring IoC
           * Load-time weaving with AspectJ in the Spring Framework
               * A first example
               * Aspects
               * META-INF/aop.xml
               * Required libraries (JARS)
               * Spring configuration
               * Environment-specific configuration
           * Further Resources
       * Spring AOP APIs
           * Introduction
           * Pointcut API in Spring
               * Concepts
               * Operations on pointcuts
               * AspectJ expression pointcuts
               * Convenience pointcut implementations
                   * Static pointcuts
                   * Dynamic pointcuts
               * Pointcut superclasses
               * Custom pointcuts
           * Advice API in Spring
               * Advice lifecycles
               * Advice types in Spring
                   * Interception around advice
                   * Before advice
                   * Throws advice
                   * After Returning advice
                   * Introduction advice
               * Advisor API in Spring
               * Using the ProxyFactoryBean to create AOP proxies
                   * Basics
                   * JavaBean properties
                   * JDK- and CGLIB-based proxies
                   * Proxying interfaces
                   * Proxying classes
                   * Using global advisors
               * Concise proxy definitions
               * Creating AOP proxies programmatically with the ProxyFactory
               * Manipulating advised objects
               * Using the "auto-proxy" facility
                   * Autoproxy bean definitions
                       * BeanNameAutoProxyCreator
                       * DefaultAdvisorAutoProxyCreator
                       * AbstractAdvisorAutoProxyCreator
                   * Using metadata-driven auto-proxying
               * Using TargetSources
                   * Hot swappable target sources
                   * Pooling target sources
                   * Prototype target sources
                   * ThreadLocal target sources
               * Defining new Advice types
               * Further resources
           * Testing
               * Introduction to Spring Testing
               * Unit Testing
                   * Mock Objects
                       * Environment
                       * JNDI
                       * Servlet API
                       * Portlet API
                   * Unit Testing support Classes
                       * General utilities
                       * Spring MVC
               * Integration Testing
                   * Overview
                   * Goals of Integration Testing
                       * Context management and caching
                       * Dependency Injection of test fixtures
                       * Transaction management
                       * Support classes for integration testing
                   * JDBC Testing Support
                   * Annotations
                       * Spring Testing Annotations
                       * Standard Annotation Support
                       * Spring JUnit Testing Annotations
                       * Meta-Annotation Support for Testing
                   * Spring TestContext Framework
                       * Key abstractions
                       * TestExecutionListener configuration
                       * Context management
                       * Dependency injection of test fixtures
                       * Testing request and session scoped beans
                       * Transaction management
                       * Executing SQL scripts
                       * TestContext Framework support classes
                   * Spring MVC Test Framework
                       * Server-Side Tests
                       * Client-Side REST Tests
                   * PetClinic Example
               * Further Resources
* [数据接入](Part IV. Data Access/README.md)
   * Transaction Management
       * Introduction to Spring Framework transaction management
       * Advantages of the Spring Framework’s transaction support model
           * Global transactions
           * Local transactions
           * Spring Framework’s consistent programming model
       * Understanding the Spring Framework transaction abstraction
       * Synchronizing resources with transactions
           * High-level synchronization approach
           * Low-level synchronization approach
           * TransactionAwareDataSourceProxy
       * Declarative transaction management
           * Understanding the Spring Framework’s declarative transaction implementation
           * Example of declarative transaction implementation
           * Rolling back a declarative transaction
           * Configuring different transactional semantics for different beans
           * <tx:advice/> settings
           * Using `@Transactional`
               * `@Transactional` settings
               * Multiple Transaction Managers with `@Transactional`
               * Custom shortcut annotations
           * Transaction propagation
               * Required
               * RequiresNew
               * Nested
           * Advising transactional operations
           * Using `@Transactional` with AspectJ
       * Programmatic transaction management
           * Using the TransactionTemplate
               * Specifying transaction settings
           * Using the PlatformTransactionManager
       * Choosing between programmatic and declarative transaction management
       * Application server-specific integration
           * IBM WebSphere
           * Oracle WebLogic Server
       * Solutions to common problems
           * Use of the wrong transaction manager for a specific DataSource
       * Further Resources
   * DAO support
       * Introduction
       * Consistent exception hierarchy
       * Annotations used for configuring DAO or Repository classes
   * Data access with JDBC
       * Introduction to Spring Framework JDBC
           * Choosing an approach for JDBC database access
           * Package hierarchy
       * Using the JDBC core classes to control basic JDBC processing and error handling
           * JdbcTemplate
               * Examples of JdbcTemplate class usage
               * JdbcTemplate best practices
           * NamedParameterJdbcTemplate
           * SQLExceptionTranslator
           * Executing statements
           * Running queries
           * Updating the database
           * Retrieving auto-generated keys
       * Controlling database connections
           * DataSource
           * DataSourceUtils
           * SmartDataSource
           * AbstractDataSource
           * SingleConnectionDataSource
           * DriverManagerDataSource
           * TransactionAwareDataSourceProxy
           * DataSourceTransactionManager
           * NativeJdbcExtractor
       * JDBC batch operations
           * Basic batch operations with the JdbcTemplate
           * Batch operations with a List of objects
           * Batch operations with multiple batches
       * Simplifying JDBC operations with the SimpleJdbc classes
           * Inserting data using SimpleJdbcInsert
           * Retrieving auto-generated keys using SimpleJdbcInsert
           * Specifying columns for a SimpleJdbcInsert
           * Using SqlParameterSource to provide parameter values
           * Calling a stored procedure with SimpleJdbcCall
           * Explicitly declaring parameters to use for a SimpleJdbcCall
           * How to define SqlParameters
           * Calling a stored function using SimpleJdbcCall
           * Returning ResultSet/REF Cursor from a SimpleJdbcCall
       * Modeling JDBC operations as Java objects
           * SqlQuery
           * MappingSqlQuery
           * SqlUpdate
           * StoredProcedure
       * Common problems with parameter and data value handling
           * Providing SQL type information for parameters
           * Handling BLOB and CLOB objects
           * Passing in lists of values for IN clause
           * Handling complex types for stored procedure calls
       * Embedded database support
           * Why use an embedded database?
           * Creating an embedded database instance using Spring XML
           * Creating an embedded database instance programmatically
           * Extending the embedded database support
           * Using HSQL
           * Using H2
           * Using Derby
           * Testing data access logic with an embedded database
       * Initializing a DataSource
           * Initializing a database instance using Spring XML
               * Initialization of Other Components that Depend on the Database
   * Object Relational Mapping (ORM) Data Access
       * Introduction to ORM with Spring
       * General ORM integration considerations
           * Resource and transaction management
           * Exception translation
   * Hibernate
       * SessionFactory setup in a Spring container
       * Implementing DAOs based on plain Hibernate 3 API
       * Declarative transaction demarcation
       * Programmatic transaction demarcation
       * Transaction management strategies
       * Comparing container-managed and locally defined resources
       * Spurious application server warnings with Hibernate
   * JDO
       * PersistenceManagerFactory setup
       * Implementing DAOs based on the plain JDO API
       * Transaction management
       * JdoDialect
   * JPA
       * Three options for JPA setup in a Spring environment
           * LocalEntityManagerFactoryBean
           * Obtaining an EntityManagerFactory from JNDI
           * LocalContainerEntityManagerFactoryBean
           * Dealing with multiple persistence units
       * Implementing DAOs based on plain JPA
       * Transaction Management
       * JpaDialect
   * Marshalling XML using O/X Mappers
       * Introduction
           * Ease of configuration
           * Consistent Interfaces
           * Consistent Exception Hierarchy
       * Marshaller and Unmarshaller
           * Marshaller
           * Unmarshaller
           * XmlMappingException
       * 16.3. Using Marshaller and Unmarshaller
       * 16.4. XML Schema-based Configuration
       * 16.5. JAXB
           * 16.5.1. Jaxb2Marshaller
               * XML Schema-based Configuration
       * 16.6. Castor
           * 16.6.1. CastorMarshaller
           * 16.6.2. Mapping
               * XML Schema-based Configuration
       * 16.7. XMLBeans
           * 16.7.1. XmlBeansMarshaller
               * XML Schema-based Configuration
       * 16.8. JiBX
           * 16.8.1. JibxMarshaller
               * XML Schema-based Configuration
       * 16.9. XStream
           * 16.9.1. XStreamMarshaller
* [Web](Part V. The Web/README.md)
   * [Web MVC框架](Part V. The Web/17. Web MVC framework.md)
       * [Spring Web MVC框架介绍](Part V. The Web/17.1. Introduction to Spring Web MVC framework)
           * [Spring Web MVC特性]17.1.1. Features of Spring Web MVC
           * 17.1.2. Pluggability of other MVC implementations
       * 17.2. The DispatcherServlet
           * 17.2.1. Special Bean Types In the WebApplicationContext
           * 17.2.2. Default DispatcherServlet Configuration
           * 17.2.3. DispatcherServlet Processing Sequence
       * [Web安全](Part V. The Web/17.12. Web Security.md)
       * []17.13 Convention over configuration support
* [集成](Part VI. Integration/README.md)
   * [Remoting 和 web services](Part VI. Integration/22. Remoting and web services using Spring.md)
       * [介绍](Part VI. Integration/22.1 Introduction.md)
   * [使用RMI暴露Services](Part VI. Integration/22.2 Exposing services using RMI.md)
       * [使用RmiServiceExporter导出Services](Part VI. Integration/Exporting the service using the RmiServiceExporter.md)
   * [Email](Part VI. Integration/27. Email.md)
       * [介绍](Part VI. Integration/27.1 Introduction.md)
       * [使用方法](Part VI. Integration/27.2 Usage.md)
       * [使用JavaMail MimeMessageHelper](Part VI. Integration/27.3 Using the JavaMail MimeMessageHelper.md)
   * [缓存抽象](Part VI. Integration/30. Cache Abstraction.md)
       * [介绍](Part VI. Integration/30.1 Introduction.md)
       * [理解缓存抽象](Part VI. Integration/30.2 Understanding the cache abstraction.md)
       * [声明基于注解的缓存](Part VI. Integration/30.3 Declarative annotation-based caching.md)
* [附加](Part VII. Appendices/README.md)

