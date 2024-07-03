### Architecture Styles
- Distributed system architecture are bundled up with components and connectors.
- Components can be individual nodes or a modular unit with well defined inter-flow which can be replaceable or reusable.
- Connectors are those communication lies between modules or components, which cooperate among components.
- Main concept behind distributed architecture is to establish communication among the components over a communication network in order to achieve specific objective.

#### Four architecture style
1. Layered architecture style
2. Object-oriented architecture style 
3. Event based architecture style
4. Data-centered architecture style
5. Hybrid architecture style

##### 1. Layred Architecture Style
- Separate layers of components from each other giving it much modular approach
- OSI reference model layred architecture where each component interact with each other
- Each inter-action is sequential where a layer contact the adjacent layer and this process continues until the request is been completed.
- But in certain cases the implementation can be made so that some layer will be skipped, called cross-layer coordination.
- Cross coordination can provide better result to increase performance.
- The layer on bottom provide service to the layer on top request flow from top to bottom.
- Benefits of using this approach is that, the calls flow the predefined pass and modified without affecting entire architecture.

	 ![[Pasted image 20240630092549.png]]

##### 2. Object based Architecture Style
- Based on loosely occupied arrangement of objects.
- No specific architecture like layers and does not have sequential of step that need to carried out for given call.
- Each components are reflected as objects where each object can interact with other objects through given connector or interface.
- The different components can interact directly with other components through a direct method call.
- In the given figure communication between object happen as method invocation. These are generally called remote procedure call.

		![[Pasted image 20240630094253.png]]

##### 3. Data Centered  Architecture
- Based on data, where the primary communication happen via central data repository. Repository can be active or passive.
- This is more like procedure consumer problem. Procedure produces item to common data store and consumer can request data from it. This common repository could be a simple.
- Main idea behind this architecture is between object happen through common storage.
- This suppose different object by providing common storage.

		![[Pasted image 20240630095205.png]]

##### 4. Event Based Architecture
- Entire communication happens through the events.
- When an event is generated it will send to a bus system, Everyone else will be notified telling event has occurred. So, if anyone is interested, that node can full the event from bus and use it.
- Sometime the events could be data or users to resources. So, the receiver can access whatever the information is given in the event and process accordingly.
- Since components are loosely coupled, it is easy to remove, add and modify the components.
	eg: Publisher-Subscriber System
		Enterprise Service Bus
- The heterogeneous components can contact the bus through any communication protocol.
- This architecture styles is based on the publisher-subscriber architecture there is no direct communication or coordination between each node.

	![[Pasted image 20240701091635.png]]

### Middleware Organization
- In distributed system there is lack of uniformity and consistency.
- Various heterogeneous devices are taken over the world where OS cater these devices in common way.
- One way to achieve uniformity is through common layer known as middleware.
- It provide service beyond what it already provided by OS to enable various features.
- It enhances the functionality of components of distributed system.
- Middleware provides certain data structured and operations that allow process and user on for flung machine to inter operate and work together in consistent way.

	![[Pasted image 20240701093158.png]]

- There are two types of design patterns that are applied the organization of middleware.
	a. Wrappers
	b. Interceptors
- They target different problem but address same goal.

#### a. Wrappers
- While designing distributed system out of  existing components we immediately bump into the fundamental problem the interfaces offered by the legacy component are most likely not suitable for all applications.
- Wrapper is a special component that offer an interface acceptable to client application of which the function are transformed into those available component.
- It solves the problem of incompatible interfaces.
- Wrappers are much more than simple interface transformers.
- For eg:
	An object adapter is a component that allow application to invoke remote object, although that object may have been implemented as a communication of library function operating on the tables or relatable database.
	Consider Amazon S3 storage services, Two types of interfaces available:
	1. RESTful Architecture (Representational Static Transfer )
	2. Traditional approach 
	
	- RESTful architecture use HTTP request to perform CRUD (Read, Create, Delete, Update) operation on resources
	- RESTful architecture is based on set of principle constraints that allows for scalable, stateless communication between client and server.
- Wrappers has always played an important role in extending existing components.
- If application A managed data that was needed by application B one approach is to develop a wrapper specific for B so that it could access A's data.
- Facilitating a reduction of numbers of wrappers typically done through middle ware.
- One way of doing this is implementing a show called broker which is logically a synchronized component that handles all the access between different applications.
- In case of message broker application simply send the request to the broker containing information on what they need.
- The broker having knowledge of all relevant application contacts the appropriate application possibly combined and transform the response and return the result to initiate application.
- Broker offers single interface to each application.

![[Pasted image 20240702092238.png]]

#### b. Interceptors 
- Software construct that will beat the usual flow of control and allow other code to execute.
- It is primary means of adapting middleware to specific need of application.
- Plays important role in making middleware open.
- To make interceptor generic it need substainted implementation effort.
- Improves management of the software and distributed system as a whole.
- Consider microphone as supported in many object based distributed system.
- Let object A call a method that belong to object B. The remote object oriented invocation a carried out in these steps:-
- Step 1: A offer can local interface that is exactly same as interface offered by is A call the method available in that interface.
- Step 2: The call by A is transformed into generic object invocation which is made possible through generic object invocation. It offers the middleware at a machine where A resides.
- Step 3: Finally the generic object invocation is transformed into massage that sent through the transport level network interface as offered by A's local OS.

Assignment 2
System Architecture
1. Centralized organization (Intro, Application, Advantages, Disadvantages)
2. Client Server Architecture (Intro, Application, Advantages, Disadvantages) (optional)
3. Peer to peer Architecture (Intro, Application, Advantages, Disadvantages) (optional)
4. Decentralized organization (Intro, Application, Advantages, Disadvantages)