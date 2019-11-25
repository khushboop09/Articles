# Monolithic architecture

### Introduction
___

Monolithic application will have a single point of development. One application will have multiple modules segregated on the basis of features, business logic. It will have a single build system, single point of deployment.

![Monolithic architecture ](https://microservices.io/i/DecomposingApplications.011.jpg)
___
### Advantages

  - It's easier to develop and test.
  - Comparatively straightforward deployment
  - Horizontal scaling is easy

### Disadvantages
  - Application can become very big, which result in long duration deployments.
  - Big applications will slow down start up time. 
  - Difficulty in scaling when different modules have conflicting resource requirements. 
  - It has a single point of failure, thus a bug in one module may affect the entire process.  
 


# Microservices architecture
### Introduction
___
Microservices are a way to create applications, where applications are broken down into services (*microservices*). Each service should be sufficiently independent from each other. The development teams can choose the language tool that they are comfortable in. Each of this microservice is a small application of its own, with its own business logic. 

![Microservices architecture ](https://miro.medium.com/max/800/0*nQZhIgz34givPDhY.png)

---

### Advantages
- Decreases the complexity because it segments the application into smaller, less complex services
- It enables each service to be developed independently by a team that is focused on that service.
- Reduces dependency on one particular technology, as each service can have a different stack. 
- It allows each service to be scaled independently. 
- There is no single point of failure, hence if one service breaks it will not necessarily break the whole application.
 
### Disadvantages
- Implementing this architecture is going to introduce some complexity as its a  [distributed system](http://www.antonkharenko.com/2015/06/notes-on-distributed-vs-non-distributed.html). Its essential to implement an inter process communication mechanism. 
- [Testing of microservices](http://martinfowler.com/articles/microservice-testing/) can become extremely tricky. To test one service one might need to start all the other dependent services as well. 
- Its more difficult to introduce changes because it may span into multiple services. 
- Deployment in monolith applications is more straightforward as compared to microservices architecture.

___

### Conclusion
It's difficult to build complex applications. Monolith architechture better suits simple, lightweight applications . There are opinions that suggest beginning with the monolith first and others that suggest not starting with monolith when your target is an architecture of microservices. Nevertheless, understanding monolithic architecture is important because it is the foundation for microservices




