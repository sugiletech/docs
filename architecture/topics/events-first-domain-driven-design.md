# Events-First Domain-Driven Design (EF DDD)

#domain-driven-design

- Focus on "What Happens": The Events


## Terminologies

### Events

- Represents facts about the domain and should be part of Ubiquitous Language of the domain

## Ubiquitous Language

- Practice of building up a common, rigorous language between developers and users.
- Should be based on domain model used in the software

### Domain Events

- Captures the memory of something interesting which affects the domain

### Bounded Contexts

- Prevents unnecessary complexity from leaking outside the contextual boundary, while allowing you to use a single and coherent domain model and domain lanuage within

### Commands

- Represent an `intent` to perform some sort of action
- Are often side-effecting ie. causing effect on receiving side

### Event Logging

- A centralized approach to model causality of facts.

### Event Storming

- A design process in which all of the stakeholders, domain expers and developers come to single room and brainstorm trying to find the domain language for the events and commands, exploring how they are casually related and the reactions they cause.

### Aggregates - Units of Consistency

- Consistency boundary - defines not only unit of consistency, but a unit of failure
- Consists of one or many entities with one of them serving as the `aggregate root`
- Only way to `reference aggregate is through aggregate` root which maintains integrity and consistency of aggregate as whole
- Always reference other aggregates by identity, using primary key, never through direct reference to the instance itself minimizing eager loading
