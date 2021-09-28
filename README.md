# **`Software Architecture Notes`**

## **What is a Software Architect**

### Differences between Developer and Architect:
* Developer knows what CAN be done.
* Architect knows what SHOULD be done.

There are several architect roles in the technology industry, some examples
are:
- Infrastructure architect
  Designs infrastructure like:
  VMs, Servers, Networks, etc. She/he is the infrastructure expert.
- Software architect
- Enterprise Architect
  Works with top level management like CEO, CIO, etc. Streamlines the IT to
  support the business. No development-oriented work. Career normally paths
  are Senior Software Architect/ Experienced Project Manager.
  
### Responsibilities of the architect

>"A good architect knows that technology patterns and all the other buzzword are
>just means to the end result.
>
>The technology should serve the requirements and not the other way around." 
> -- <cite>Memi Lavi, Senior Software Architect & Consultant</cite>

So to summarize a software architect is someone who designs the system to 
be first secure reliable and easy to maintain and select the optimal 
technology platforms and patterns to achieve these goals.

### The architect in the organization

Architect **is not and should not be** in managerial position.

She/he does not manage vacation requests and definitely not conducting performance 
reviews or compensation negotiations.

When the architects are in a junior position normally it's contribution it's quite 
limited to the organization and only focused to the project, although, he/she sees
the big picture, but only for the project.

In senior positions architects add a tremendous value to the organization and 
normally reports directly to the CIO, they will make sure the project's architects
adhere to the organizational guidance.

### Should the architects code?

A good architect MUST know how to code, and there are some reasons for that:
* Architecture Trustworthiness
  
  You have to be able to test new technologies and platforms for yourself
  and know what it's implementable and what it's unimplementable.
* Support the Developers

  The architect must be able to help developers when they get stuck well 
  while implementing the architecture, and the minds of developers work to 
  detect deviations from the intended implementation.
* Respect

  One of the key factors to succeed as an architect is to gain the respect
  of the developers.
  
### Academic degrees and Career Path

There is no dedicated degree to architecture in software, so don't really need
a specific one, however, a Computer Science degree won't hurt. Additionally,
there are some courses and certifications like TOGAF but are more geared towards
Enterprise Architecture rather than Software Architecture.

Since there is no formal degree, or a course that qualifies you as an architect.
The main factor is experience preferably in the technological field.

## **The Architect's mindset**

### Understand the business

Learn the insides of the business, it's important to be familiar with:

* Weaknesses
* Strength
* Competition
* Growth Strategy

### See for the goals

After we have understood the business and learned all what there is to 
learn about it instead look at the specific system we're going to walk on.

**Goals** are not requirements, requirements are "What the system should do", 
goals describe the effect on the organization, remember, you need to think 
in the big picture, the goals are normally **described by the client**. 

### Identify your client's client

It means that with every decision you make you must ask yourself what 
will be the effect of this decision on your client's client.

Now you might say that working with the client is a system analyst's job 
is not the architect's job. This is usually correct but sometimes a project is carried out without 
the system analyst on board.

### Watch your language

Always keeping in mind what is the thing that really matters to the person 
you are talking to.

If you can't adapt to language to the best interests of the person we are 
talking to you will be able to achieve much more by the way this rule is right.

## **The Architecture Process**

### Understand the system requirements

Usually defined by the system analyst the system requirements describes 
what should the system do.

### Understand the non-functional requirements

You need to define technical and service level attributes. 

>ie. Users, Loads, Volumes, Performance, etc.

Much more important than the regular requirements.

### Map the components

Understand the system functionality, represent the tasks of the system
and communicate your understandings to your client in order to clarify.

### Select a technology stacks

You're going to decide to together with the development team what would
be the platform on which the system will be based.

Usually there will be more than one technology to be used in most systems.

You will have to select the backend platform, the front end platform, 
and the data storage platform.

**A wrong technology stack can lead to the failure of the whole system.**

### Design the architecture

This is the heart of your work, the qualities of a well-designed system 
such as loose coupling, stateless, scaling, caching, messaging and 
lots more inside-house qualities are used as the building blocks of 
the architecture.

### Write architecture document

Describes the Process and Architecture, and MUST be relevant for all 
participants including the business perspective, the project management, 
etc.

### Support the team

The architecture will change a lot during the development of the system so
remember to support the team unless you want your work to become only a 
paperweight.

## **System Requirements**

### Two types of requirements

When talking about system requirements we usually think along the lines of 
"what the system should do" for functional requirements.
* Business Flows
* Business Services
* User Interfaces

And "what should the system deal with" for non-functional requirements.
* Performance
* Load
* Data Volume
* Concurrent Users
* SLA

Non-functional requirements are the most important requirements and that the architecture
should not under any circumstances designs a system without knowing what is non-functional 
requirements.

But it is equally important to be aware of the functional requirements. Many architects feel 
they only need to scheme all the functional requirements and concentrate on the non-functional ones.
That's a mistake to remember.

> Remember that a good architect must improve the business bottom line.

That won't be possible if you are not sure what the system should do.

### Non-Functional Requirements

You as an architect are going to work directly with the non-functional requirements.
Some of these are:

* Performance
  
  Define what it's "fast" for your client, **always talk in numbers**.
  * Latency

  "How much time does to accomplish a given single task"
  * Throughput
  
  "How many tasks can be performed in a given time unit"
  
* Load
  
  Defines the **quantity of work** before system crashing.

  **Always plan for extreme cases!**
  
* Data Volume

  How much data the system will accumulate over time.

  Helps with:
  * Deciding Database Type.
  * Designing Queries
  * Store Planning
  
* Concurrent Users
  
  Remember that load it's different from concurrent users since any given user
  can perform a wide range of tasks within the application.
  
  The rule of thumb for calculate concurrent users is:
  > Concurrent = Load x 10

* SLA (Service Level Agreement)

  Describes what is required uptime for the system in percentage.
  > For example:
  > 
  > A system with 99.99% SLA
  > 
  > 24x365 = 8760 hours/year
  > 
  > 8760 x (100-SLA) / 100 = 0.88 hours/year Downtime 


## **Type of applications**

Decided after the requirements are set.

This is an important decision since each type has its own pros and cons. Moreover, 
once a decision is made it's usually not easy to switch to other types.

The most common application types are web apps, web API, mobile, console, service and desktop.

### Web Apps

* Best suited for systems that require:
  * User interface
  * User Initiated Actions
  * Large Scale
  * Short, Focused Actions
* Request-Response based

### Web API

* Usually REST based
* Return Data, not HTML
* Very Accessible (Easy to integrate with many languages)
* Best suited for systems that require:
  * Data Retrieval ann Store
  * Client-Initiated Actions
  * Large Scale
  * Short, Focused Actions
* Request-Response based

### Mobile App

* Usually works with Web API
* Best suited for systems that require:
  * User Interaction
  * Front End for Web API
  * Location (GPS)

### Console application

* No fancy UI
* Requires technical skills
* Limited interaction
* Long-or-Short running process
* Best suited for systems that require:
  * Long-running process
  * Short actions by trained power-users
  
### Services

* No User Interface
* Best suited for systems that require:
  * Long-running processes in processes that no requires
  intervention
    
### Desktop applications

* Has all the resource in the PC
* Might connect to the web 
* Best suited for systems that require:
  * User-centric actions (Word processing)
  * Heavy gaming

## **Selecting technology stack**

One of the most important and loaded  tasks of the architect, and that is selecting the 
technology stack of the system.

The selected technology stock will determine what language is.

Platforms and tools will be used during system development and what are the skills required 
for the development team.

This decision is important for two reasons.

* One, it's irreversible.

  Once you've decided to use specific platform and work has begun on this platform, you can't 
reverse it. It's not possible to decide three months into development that actually we prefer another 
platform. Such a decision will result in a complete rewrite of the system and a substantial delay 
in schedule.

* Two, some decisions are emotional:

  You will encounter situations where the development team would like to a specific platform
because it's new, sexy and the team across the corridor already uses it.

So this decision has to be made with a **clear mind**, must be **heavily documented** and to
be a **group effort** and not only was the architect.

### Considerations

When selecting the technology stack, there are some considerations that must be taken into
account in order to ensure the best platform will be used in the systems.

Let's look at these considerations.

* One: Can perform the required tasks (it must fill the requirements for the system).

* Second: Community, you always want to make sure there is a large active community 
which discusses the platform and can provide support.

* Third: popularity, although seems a bit superficial, the popularity factor is quite 
important and popular platforms will usually lead to a small community which will lead
to a lack of support.

### Backend and Service technology

Our discussion here is about Web apps, Web API, console and services. Let's call all of them
back backend for the sake of simplicity.

### Frontend technology

Here we are talking about mainly HTML, CSS and some Javascript framework for the Web, 
also we have Native, Hybrid and Cross-platform technologies for the Mobile apps.

### Data store technology

Selecting the datastore technology is one of the more important decisions you will make 
in the product design. After all, this is where your precious data is going to be stored
for the use of the application.

## **Meet the -illities**

The _"-illities"_ are a group of quality attributes that defines the applications capabilities, 
almost all those quality attributes of a name that ends with _illity_.

Quality attribute is an attribute of the system that describes a specific capability that is
not related to a specific functional requirement. If that sounds similar to no functional 
requirements, it's not a coincidence. Quality attributes are closely tied to non-functional
requirements, and they describe what technical capability should be used in order to fulfill 
the non-functional requirement.

### Scalability

Scalability is the ability of the application to support **adding computing resources in order 
to support additional load without any interruption** to the applications' activity.

### Manageability

Manageability, the ability to manage the application. 

What does it mean? Simply put, it's **the ability to know what's going on with the application**
at any given time and to take actions that will improve its walk.

For example, a manageable application will constantly report its status to monitoring agents 
and let them know when errors occur, when there is an exceptionally high load, when the room is
becoming dangerously high and so on.

### Modularity

Modularity is one of the more important quality attributes out there, making your application
modules will really help you along the road. It will minimize the effort needed to maintain the
application and make it much more flexible for changes.

So what exactly is the modular system? Simply speaking, a model, a system is a system that is
built from small, **well-defined building blocks** that can be changed or replaced without affecting
the whole system.

### Extensibility

Extensibility, insisting that implementing extensibility or an extensible system is a system 
that in its **functionality can be extended without modifying its existing code**.

### Testability

Testability is the attribute that defines **how easy it is to test the application**.

## **Component's architecture**

When talking about software architecture, we actually talk about two levels of architecture.

The first is the **components' architecture**. This is the architecture of the individual 
components and this is a topic of this section. The components' architecture deals with the
various inner components of the code, the way they interact with each other and how to make 
it fast and easy to maintain.

The second level is the **architecture of the whole system**, this kind of architecture deals
with the bigger picture and make sure the system is scalable, reliable, fast and easy to maintain.

In this section we'll discuss components' architecture.

### Layers

A good software component will always have layers.

The layers in software component represent a horizontal functionality of the code in the layers.

Now what does it mean? Traditionally, social components perform three basic actions:

* One, expose the sort of functionality through some kind of interface. This is usually done via
API or user interface, depending on the type of the application.

* Two, execute logic or the data that is received from the user. Again, they are API or user 
interface. This logic often includes validation, processing, additional calculation's
enrichment and more.

* And three, save the data into the data store and retrieve data from the data store.

Now these reactions are usually represented as layers when every label has its own name 
in software components architecture. These labels are called **user interface or UI** if the 
component has a user interface or **service interface (SI)**, if the component exposes API,
**business logic or BL** and **data access layer or DAL**.

#### Purpose or Layers

* Forces well-formed and focused code.
* Ensures modular design

In order to develop a good layered architecture there are some concepts that must be followed.

* One, Code Flow, which means a layer can call only a layer that is directly benefit in the 
code. What this means is that, for example, the code in the SI layer can call only a code in
the BL layer never occurred in the DAL layer. In addition, a code can never call a code in
layer above it. For example, the DAL code will never call a code in the BL.

* Second, Loose Coupling. A loosely coupled system is one:

  1. In which components are weakly associated (have breakable relationship) with each other,
  and so, changes in one component least affect existence or performance of another component.
  2. In which each of its components has, or makes use of, little or no knowledge of the 
  definitions of other separate components. Subareas include the coupling of classes,
  interfaces, data, and services.

### Interfaces

Basically, an interface is a contract that declares the signatures of an implementation. The
interface states that given a piece of code that should do a specific task, its methods will
look in a specific way.

There is a saying in the software architecture field that goes like this:

**New is glue**, what it means is that whenever you see a new keyboard, you know there is a
close to a strong coupling between those two classes. **And this is something you want to avoid**.

### DI

Dependency injection is defined in Wikipedia as a technique whereby one object supplies the 
dependencies of another object.

### SOLID

The SOLID, this acronym coined by Bob Martin in the year 2000, represents five code design
principles that, when implemented, make the code easy to understand, Flexible and maintainable.

SOLID stands for: 

* Single responsibility principle. Each class, module or even method should have one and only
one responsibility, or in other words, a single, well-defined functionality in this 
functionality should be fully encapsulated within this class or module.

* Open-closed Principle. States that a software entity should be open for extension, but 
closed for modification, what this means is that in order to change behavior of a software
entity, for example, class, we would need to modify its code and then recompile and redeployed, 
but we will have means to extend its functionality without touching the code.

* Liskov substitution principle. States that if _S_ is a subtype of _T_, objects of type 
_T_ may be replaced with objects of type _S_ without altering any of the desired properties 
of the program.

* Interface segregation principle. This principle states that many client-specific
interfaces are better than one general-purpose interface. 

* Dependency inversion principle. Is also known as dependency injection, you can see the 
definition in the previous section.

### Naming conventions

Naming conventions are a set of rules that define how do we name various code elements, such
as classes, methods, variables, constant and more, the role of naming conventions is to make
our code more readable and easy to understand.

Note that naming conventions are not enforced by compilers and the code will work perfectly 
without using any convention. But a code without conventions will be messy and hard to
work with.

### Exception handling

One of the most important aspects of a well written component is its exception handling.

Best practices:

* Only catch exception if you have something to do with it. (Logging does not count).
  Examples:
  * Rolling back a transaction.
  * Retry.
  * Wrap the exception.
* Catch only specific exceptions. Example:
  * SQLException instead of Exception
* Use try-catch on the smallest code fragment possible.
  * Locate the code fragments that may rise exceptions and use try-catch on them.

### Logging

No matter how simple the code is or how urgent is the system, never ignore the logging.

A good system uses logging for two purposes:

* One, to track errors. If there are any exceptions during the system's activity, the system
will write to those exceptions to the log, complete with all the relevant details; 
full error messages, StackTraces, inner exceptions, user details and so on.

* The second purpose is to gather data logs should not be used only for exceptions, but to 
collect and store operational data on the system. For example, using logging, you can find out 
which model is the most visited by users and which one is less popular. You can store
performance data and find out which method performed poorly and which ones are
blazingly fast.

## **Design patterns**

The basic definition is that design patterns are a collection of general reusable solutions
to common problems in software design when writing software. There are a lot of small problems
that you will find yourself dealing with frequently, questions like how to communicate between 
classes or how to initialize interface implementations or how to access data stores and lots 
more questions. Almost every software developer has to answer somewhere along the lines. Design
patterns are a set of solutions or patterns that strive to answer those questions and provide a
well-defined pattern or template for those problems.

Using design patterns, you will gain the following benefits:

* The pattern is already tested and used by a lot of developers. There is no need to reinvent 
the wheel, and you can reuse solutions that were already formulated and implemented by the 
brightest minds in the industry.

* Design patterns will often make your code easier to read and modify, thus making the
application more flexible.

## **System Architecture**

**Most of the work of a software architect is designing the system architecture**, and you will 
find yourself using the concept we will discuss in this section, in almost all the systems 
you will walk on.

We already saw about components, architecture, we talked about layers, logging, dependency,
injection and more with system architecture we take a higher point of view, and we look at 
the big picture and in the big picture, we usually ask ourselves these questions.

* How will the system work under heavy load?

* What will happen is the system will crash at this exact moment in the business flow?

* How complicated can be the update process and more?

The system architecture includes the following aspects:

* One, defining the software components or services that together composes the system.
* Two defining the way these components communicate with each other.
* Three, designing the various capabilities of the system, namely scalability, redundancy, 
performance, manageability and more.

### Loose coupling

When talking about loose coupling in system architecture we talk about making sure the 
various components or services are not strongly tied to other components.

The reasoning for this is again quite similar to the loose coupling inside components. If 
services will be coupled to other services, then every time the service is changed in the model
system, this happens a lot, this change might affect other services that use it.

By loosely coupling the services, we ensure the independence of each of the services and make 
sure they can be modified with minimal impact on other services, if at all. This will make our
system much more flexible and of course, very easy to maintain.

In general, loose coupling in services means that the fact that a service is implemented in a
specific platform or exposes specific API will not force other services to use the same platform.

In addition, loose coupling also means that changes in the service API, such as if URL or
its parameters, will have minimal to no effect on the services.

### Stateless

The stateless architectural pattern is probably one of the most important patterns in software 
architecture.

>"...if I had to single out one pattern as the one you must implement, it probably will be the
> Stateless pattern."
> -- <cite>Memi Lavi, Senior Software Architect & Consultant</cite>

**The application state is stored in only two places, the data store and the user interface, 
if there is any. No state is stored in the application code.**

Always make you architecture stateless, there are almost no scenarios which justifies stateful
architecture, and you probably will never encounter them. This is the best way to support
scalability and redundancy in your system, and you should definitely use it.

### Caching

Using cashing, **we bring data closer to its consumer so that its retrieval will be faster**.

The cache is another layer that usually sits between the data storage and the business logic 
that stores data in a way that makes it very easy and fast to retrieve.

Cache engines usually stored data in memory, thus making the retrieval extremely fast.

Search engines such as Redis saves the data to disk periodically but still retrieving the 
data is done against a memory storage cache engines, often some trade-offs when compared to 
more traditional databases. Cache, trades reliability for performance, data stored in memory
is more volatile and will be lost in case of a server crash.

Now, as architects, we must be able to determine whether, when and how to use cash in our 
system and for that, let's just define the type of data that we would want to cache.
The rule of thumb goes like this: **Cache should hold data that is frequently accessed 
and readily modified**.

In general, we can say there are two types of cache:

* In-memory, In-process cache
* Distributed cache

### Messaging

The term messaging refers to the means of communication between the various services in the system.

Note that the messaging selection is not exclusive. We can often find systems with various
messaging methods, each used for different proposals.

Let's see the criteria:

* The first concern is, of course, performance. We will always prefer a faster method of messaging.

* Next is message size. Indeed, most systems do not require large messages between services, 
but sometimes it is useful.

* Next criterion is the execution model. Some messaging platform requires a quick response
model which has its limitations, and some enable long-running processes to execute.

* Another important criterion is the feedback and reliability, and by feedback I mean the ability to
determine whether the messaging has failed and if it is the ability to perform some corrective
action. Not all messaging methods reportes status and this is definitely an important 
consideration.

* The last criterion is the complexity of implementation. If a messaging platform requires 
a lot of development effort that is something we would like to know beforehand.

Most common messaging methods:

* REST API.
* HTTP push notifications.
* Queue
* File-based or Database-based

### Logging and Monitoring

In software there's a rule of thumb about system reliability, your system would fail, the
question is what's going to happen when it fails.

## **External considerations**

### Deadlines

Deadlines are a major factor when designing architecture, when deciding on the architectural 
patterns we are going to use, we must be an even vaguely how long will it take to implement 
them and how does it relate to the project's deadlines.

### Existing Dev team skills

When selecting the technology stack, which is one of the most important parts of designing
a system, always factor in the existing team knowledge and skills, deciding on a technology
stack that the team is not familiar with might cause two problems:

* Delay
* Low Quality

### IT support

One of the biggest temptations when designing the architecture is to recommend various tools 
for the architectural aspects, tools like Queue engines, business flow managers, NoSQL
databases and more are quite common recommendations for modern day architectural problems.
Those tools, however,  **need someone who is familiar with them and can maintain them.**

## **Architecture Document**
## **Case study**
## **Advanced topics**
## **Soft skills**
