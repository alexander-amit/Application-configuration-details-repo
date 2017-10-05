## Application-configuration-details-repo
Multi-Module demo project for Spring-Cloud-Config

1. Client - Application whose configurations will be fetched from server at runtime even without restarting the application.
@value - used for injecting values into fields in Spring-managed beans 
@RefreshScope - used to refresh the configuration of spring-context bean

2. Server - is a spring boot application. Acts as a central configuration server for all Micro-services(App1, App2, ....) of Product.
@EnableConfigServer - enables the application to get the external config properties form Git.

Use case -
1. Client and Server are deployed.
2. Some configuration has beed changed by user for client(name - App1)
3. Changed Configuration can loaded in App1 without restarting the app by refreshing the Scope(@RefreshScope) of applicaiton. (refresh it through postman).
4. After refreshing chenges made in "App1.properties" will reflect in application. 
