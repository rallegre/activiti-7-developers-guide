# Query Service

The Query Service enable client applications to get Process & Task data without going straight to the Runtime Bundles.
The Query Service was designed to enable efficient querying mechanisms for data generated by one or more Runtime Bundles.
In contrast with the Audit Service, the Query Service picks up the event and apply some transformations to store state.

![](/assets/QueryService.png)

## Endpoints
The query component provides two different endpoints
- REST HAL APIs
- GRAPHQL Endpoint

## Event Listeners
The query service listen to events generated by runtime bundles and transform them to store state about the current process instances and tasks executions. This state is stored in a schema that is optimized for querying and based on the specification of this component different implementations using different technologies can be implemented.

Our reference implementation uses JPA entities to store this state and we defined a simple schema to store 3 entities:
- [ProcessInstance](https://github.com/Activiti/Activiti/blob/master/activiti-services/activiti-services-query/activiti-services-query-model/src/main/java/org/activiti/services/query/model/ProcessInstance.java)
- [Task](https://github.com/Activiti/Activiti/blob/master/activiti-services/activiti-services-query/activiti-services-query-model/src/main/java/org/activiti/services/query/model/Task.java)
- [Variable](https://github.com/Activiti/Activiti/blob/master/activiti-services/activiti-services-query/activiti-services-query-model/src/main/java/org/activiti/services/query/model/Variable.java)



## Implementations
- JPA using Spring Data JPA
- ElasticSearch using Spring Data Elastic (PR in review)

## Source Code & Docker Image

- [Query Service JPA -> Source Code](http://)
- [Query Service JPA-> Docker Image](http://)
- [Query Service ElasticSearch -> Source Code](http://)
- [Query Service ElasticSearch-> Docker Image](http://)
