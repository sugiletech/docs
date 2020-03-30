# Top 5 Software Architecture Patterns

## Layered (N-tier) Architecture

- Most common built around the database
- ata flows from top layer through middle layers to reach bottom layer
- Separation of concerns
- Eg: MVC
- Technologies/Frameworks: Java EE, Drupal, Express

![](https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/assets/sapr_0104.png)

### Challenges

- 'Sinkholde anti-pattern'
- Need to be careful about tight coupling and logical mess full of complex inter-dependencies
- Results into `Monolithic` applicaiton

### Best Suitable For

- New application that need to be built quickly
- Application need to mirrow traditional IT departments and processes
- Team of in-experienced developers
- Strict maintainability and testability standard required

## Event Driven Architecture

- Central unit accepts all data and then delegates it, via events, to the separate modules that handle the particular action type
- Data flows through only modules which needs to process it
- Similar to browser where browser orchestrates all input and make sure that only intended code sees particular event
- Easily adaptable to complex, often chaotic environment
- Scale easily vertically as well as horizontally
- Extensible when new event types appear

![](https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/assets/sapr_0203.png)
### Challenges

- Integration test can be complex if the modules can affect each other
- Error handling can be difficult to structuer, especially when several modules must handle same events
- Central unit must have a plan if a module fails
- Messaging overhead can slow down processing speed
- Maintaining a transaction-based mechanism for consistency is difficult because themodules are so decoupled and independent

### Best Suitable For

- Asynchronous systems with asynchronous data flow
- Applications where the individual data blocks interact with only a few of the many modules
- User interfaces

## Microkernel / Plug-in Architecture

- Has a core set of operations performed by a system at core
- Extra features are layered on top of the core system
- Eg: Eclipse, VS Code

![](https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/assets/sapr_0302.png)

### Challenges

- Deciding what belongs to the microkernel is often an art
- Plug-in must include fair amount of handshaking code so the microkernel is aware that plug-in is installed and ready to work
- Modifying the microkernel can be difficult once a number of plug-ins depend on it
- Choosing right granularity for the kernel functions is difficult to do in advance but almost impossible to change later

### Best Suitable For

- Tools used by wide variety of people
- Applications with a fixed set of core routines and a dynamic set of rules that must be upated frequently

## Microservice Architecture

- Goal is to create ta number of different tiny programs and then create a new little program every time someone wants to add a ew feature
- Used mainly when the different tasks are easily separated
- Microservices can be scaled up and down independently
- Eg: Netflix, Linked, Amazon

![](https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/assets/sapr_0402.png)

### Challenges

- Services must be largely independent or else interaction can cause the cloud to become imbalanced
- Not all applications have tasks that can't be easily split into independent units
- Performance can suffer when tasks are spread out between different microservices. Communication costs can be significant
- Too many microservices can confuse the users as parts of the users as parts of the web page appear much later than others

### Best Suitable For

- Website with small and independent components
- Corporate data centers with well-defined boundaries
- Rapidly developing new business and web application
- Development teams that are spread out, often across the globe

## Space-based / Cloud Architecture

- "space-based" refers to the "tuple space" of the users, which is cut up to partition the work between nodes
- Designed to avoid functional collapse under high load by splitting up both the processing and the storage between multiple servers
- Data is spread out across the nodes just like the responsibility for servicing calls
- Computations spread out across the entire data set must be split up into subjobs, spread out across all of the nodes, and then aggregated when it's done

![](https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/assets/sapr_0501.png)

### Challenges

- Transactional support is more difficult with RAM databases
- Generating enough load to test the system can be challenging, but the individual nodes can be tested independently
- Developing the experties to cache the data for speed without corrupting multiple copies is difficult

### Best Suitable For

- High-volume data like click streams and user logs
- Low-value data that can be lost occasioally without big consequences
- Social networks

> References:

- <https://techbeacon.com/app-dev-testing/top-5-software-architecture-patterns-how-make-right-choice>
