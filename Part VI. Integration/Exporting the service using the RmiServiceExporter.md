# 使用RmiServiceExporter导出Services

 Using the RmiServiceExporter, we can expose the interface of our AccountService object as RMI
object. The interface can be accessed by using RmiProxyFactoryBean, or via plain RMI in case of
a traditional RMI service. The RmiServiceExporter explicitly supports the exposing of any non-RMI
services via RMI invokers.

Of course, we first have to set up our service in the Spring container:

```xml
<bean id="accountService" class="example.AccountServiceImpl">
    <!-- any additional properties, maybe a DAO? -->
</bean>
```


使用`RmiServiceExporter`暴露Services:

```xml
<bean class="org.springframework.remoting.rmi.RmiServiceExporter">
    <!-- does not necessarily have to be the same name as the bean to be exported -->
    <property name="serviceName" value="AccountService"/>
    <property name="service" ref="accountService"/>
    <property name="serviceInterface" value="example.AccountService"/>
    <!-- defaults to 1099 -->
    <property name="registryPort" value="1199"/>
</bean>
```