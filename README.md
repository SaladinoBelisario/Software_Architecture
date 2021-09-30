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

In this document, the architect describes the architecture that was designed as well as various 
requirements; functional and nonfunctional, the technology stack and more.

The architecture document is a cornerstone of the application development, and **no development
should begin before an architectural document is created** and the developer fully grasped
its contents.

This document is the center of the architectural work, although not the only thing you will do.
It's extremely important.

This document will include all the insights produced while working on the architecture.
This will help you in the future for justifying decisions that we made earlier in the process.

### Goals 

First and foremost, the architectural document is a foundation of the development effort of 
the system. It describes what should be developed and how, as a rule of thumb, no lines of code 
should be created before the development team read through the architectural document and make 
sure they fully understand what should be done and how.

The document outlines the technology stack into various components and services that comprise 
the system and how do they communicate with each other, without this knowledge, the development 
team have no idea what should be developed when following the document. The team should be 
able to develop a well thought of, fully documented, first secure, reliable and easy to 
maintain system. This cannot be accomplished when such a document is not present.

### Audience

Its real audience is almost everyone involved in the system, including the project manager, 
the CTO, if there is any, the QA leader and of course, the developers.

### Document's structure

#### Background and Overview

This is a short section, **one page of max** and its target audience is also the **team and
management members.**

You should describe briefly the system you are walking on from a business point of view, the 
section to describe at minimum the main role of the system. If it replaces an old system 
describe why the old ones should be replaced and what is expected business impact.

The section is incredibly important and for a few reasons. First, it displays your point of 
view of the system. If someone has some comments to make on it or if an error was found, 
it's better to have an opportunity to correct it as soon as possible.

The section should not have any technical details or architectural terms. No technical services, 
no programming languages, no clouds, nothing. **Just a simple text describing what the 
system should do from the end user point of view.**

#### Requirements

This is also a short section, usually **no more than one page** usually lists in its target 
audience is also the **team and management members**.

In this section, we are going to describe the various requirements from the system.

There are two important reasons for including the requirements in the architecture document.
First, similar to the background section, this section is included in the document to allow 
the readers to comment on the requirements and to make sure everyone is well aware of
what the system should do and under what conditions it's supposed to work.

This is a great opportunity for you to **validate your understanding of the system and make
sure that whatever you design solves an actual problem for the customer.**

Second, remember that the architecture is designed against a well-defined requirement.
A lot of the architectural characteristics such as redundancy, messaging, data storage and
more are designed in light of a specific requirement.

#### Executive Summary

Its length is usually a few pages, usually **no more than three**, and its audience, as you can
guess, is mainly **management, meaning the CEO, CTO and project manager**.

**The goal of the executive summary is to provide a very high level view of the architecture
using simple words and not too many technical terms, thus boosting the management confidence 
in working with you.**

Tips:

* Use charts and diagrams
* Write it AFTER the rest of the document
* Use well-known technical terms - sparsely!
* Do NOT repeat yourself

#### Architecture overview

This section is usually a long one and can reach to **up to 10 pages**. **Its audience is a 
development team and the QA Lead**.

The architectural overview section provides a high level view of the system's architecture.
Its goal is to present the architecture to the team and to explain its structure and logic.
This section does not deep dive into the specifics of any component of the architecture.

This section has usually three parts. The first part of this section gives a general 
description of the design architecture. This part lays the foundation of the architecture 
by describing its type and the reasoning behind it and the major non-functional requirements.

The second part is a high level diagram of the architecture. This diagram describes the 
general concept of the architecture using the various services, data stores and interactions 
so that the reader will comprehend what the various components of the architecture are and what
is the responsibility of each one.

The third and last part of the overview section is the walkthrough of the diagram. In this 
part you will describe the values part of the diagram in the role verbally. This part walks
through the diagram and explains each and every component in it. It describes in simple 
words what is the exact role of the component, what is its functionality and what interactions 
it has with each and every other component. In addition, it describes the data that is stored 
in the component data store, if there is one. This part is extremely important since the 
diagram cannot convey all the intricacies of the architecture. It's important to include any
logic details that you think will be relevant, such as the component users, expected load,
future extensions and more.

#### Components' Drill-Down

This section **describes the components that take part in the whole architecture as described 
in the Architecture or Overview section.** 

**There is no actual limit to the length of this section. Its audience is development team 
and QA Lead.**

Well, this section goes through the various components depicted in the architectural overview 
and describes them in length.

For each component there should be four subsections in the document:

* First, the role of the component in the architecture.
This is basically a short recap of the description founding architectural overview section.

* Second, the technology stack, this subsection should describe in detail what technologies 
will be used in developing the component. This is subsection should first lay out the various
parts in the component that the technology should be selected, for example, datastore, backend 
and front end. And then for each one of them, the selected technology should be described.

  > We already discussed the problems you should expect when trying to decide on the stack that 
  will be used in the system. For this reason, it is extremely important that the technology
  stack subsection will be extremely detailed and even more important include the rationale 
  behind the selection.

* Third is a components' architecture. This section describes the architecture of the 
component. It complements architecture overview that describes the bigger picture by going 
into each and every component and detailing what exactly it should do and how.

* The last subsection is development instructions. This is usually a small subsection no more
than half page containing bulleted list of concrete development instructions. These instructions
should point out specific guidelines that are not part of the architecture, but still relevant
for the developers.

## **Case study**

This is not a toy system specifically designed to make your life easier, but a real world
application used by real customer solving real data and cost millions to design, develop and
deploy.

>The system we are talking about is for a young, fictitious startup called IOT. Our startup 
develops a dashboard system that brought in almost three times the status of the IoT devices
its clients are using and managing. For example, smartphones, which are becoming more and 
more ubiquitous, has a lot of IoT devices. Think about the thermostats, light bulbs, routers,
cameras, electric switches, refrigerators and lots more. Each one of them has its own app 
and can be managed from a smartphone, but wouldn't be easier to get a unified view of all
those devices on a single screen? 

**This is what IoT is doing with this application!** It collects status information from
registered IoT devices and formats the data to visually pleasing dashboard, allowing you, 
the customer to know exactly what is going on with your devices. In addition, the customer 
can execute some predefined queries to access more information about the devices.

It's important to note that for phase one of the system, the customer is not adding or 
updating any data, the status info is received directly from the devices in the field.
The data is just presented to the customer. Another important aspect is that the lunch
customers will be entered into the system manually by the salespeople following an intensive
verification process to prevent data leaks. Because of that, the system does not have to
have a registration process, and you can assume the devices are already registered.

**You are the architect of the system, and it's your job to design the architecture so that 
your two application will boost the company's business, leading it eventually to a successful 
IPO.**

### Defining the requirements

The first thing you should do as an architect is to define the requirements, these requirements
are very important for your work, and they dictate what architecture will look like.

You probably remember there are two types of requirements, functional requirements and 
non-functional requirements.

Now the functional requirements are well-defined. In this case, it looks like the system 
analyst did a good job, and it's quite clear what the system should do. Let's summarize
the functional requirements in a short bullet:

* Receive status from IoT devices.
* Store the updates for future use.
* Query the updates.

Now let's go to the more interesting part, the non-functional requirements.

**What we know:**

* Messages are received from IoT devices
  * Probably **a lot** of messages
  * Affects the load
  * Affects the data volume

These factors are translated into two questions we need to ask.

> First, how many concurrent messages should the system expect in peak time?

> And second, what is the total number of expected messages per month?

In addition to make our calculations more accurate

> We should also ask what is the average size of a message?

* **Messages in peak time: 500**
* **Messages per month: 15.000.000**
* **Average size of a message: 300 bytes**

Now, 15 million messages per month with average size of 300 bytes per message.

Give us roughly **4500 megabytes per month**. Let's multiply this by 12 to get the yearly number.

And we are looking at **54 gigabytes per year**.

This is good. 54 gigabytes in today's storage is not a lot, and almost every database 
can handle it easily. And by that we're calculating the data volume non-functional 
requirements, which is **_54 GIGABYTES ANUALLY_**.

The load, however, is a completely different story with five hundred concurrent messages.
This is a quite busy system.

Next thing we need to know is how tolerant is the system for message loss?

Sure, we cannot lose any message, but let's think about it. This system receives its status 
updates. Each device sends updates every few seconds. What really happens when a message is lost?
Not much, actually. A few seconds later, another message will arrive with new update, which
will anyway make the previous message obsolete.

So the message lost non-functional requirement can be defined as 99 percent. Note that in this
kind of non-functional requirement, there is a huge difference between 100 percent and 99 percent.

OK, next, the next question we need to ask is:

> How many users will the system have?

> How many concurrent users should we expect?

The client expects the system to have a total of **2 million users** three years from now with 
no more than **40 concurrent users**.

Now it's important to understand what concurrent users mean. It does not mean how many users 
are currently using the system, but rather how many users are actively accessing the service.
This distinction is important.

When a user looks at the dashboard, he uses the system but does not access the server.
The dashboard is already on the user's screen, so the server does nothing when calculating load.
We are interested only in the actual work the server is doing. So we define concurrent users
as a number of users that actually access the server on the same time.

With this information we can calculate the load:

* **Load: 540 concurrent requests**

The last question we need to ask is:

> What is the maximum downtime allowed?

Whe discuss three different levels of SLA: Silver, Gold and Platinum. Platinum level, which is
what most of the clients choose, dictates that the system should be fully stateless, easily
scaled out and utilized extensive logging and monitoring. There is no point in discussing 
specific uptime numbers such as 97 percent versus 99 percent.

### Mapping the components

The next task of mapping the requirement is mapping the components in this task, we decide 
what are the components that take part in our application, right. Remembering that the 
component is an autonomous piece of code that runs in its own process and has its own compute
resources.

Now, there is an important distinction here. We are looking at two completely different tasks, 
receiving messages and responding to client requests. These two tasks perform separate actions,
have different non-functional requirements and walk against separate entities because of the 
natural choice here is to separate these two tasks to two separate components, one that is 
responsible for receiving the messages, let's call it receiver and one that waits for user
requests, which will be called in for provider or simply info since info provider is a little
too long.

There is a very important aspect that is hiding here. We know the receiver is going to work 
under heavy load, 500 concurrent requests. That means that one of the important aspect of
the receiver is that it needs to release the message update requests as fast as possible, 
because for every millisecond it works on a specific message, there are more messages waiting
to be processed. And we don't want to reach a thread starvation situation, meaning the service
will not have enough resources to handle the waiting requests, and it will start throwing 
exceptions.

We will need to go to the client and ask what is the exact format of the messages and what 
processing is required on them.

Two days later, she comes back with the following answer:

> There are four types of IoT devices. Each one of them has its own message format.
Three of them use JSON format and one, which is an old one, uses a fixed format string.
In addition, most of the messages must be validated because the device software be might be
buggy, and we cannot trust it blindly.

So we now know the receiver has the following tasks. 

* One, receives the message, obviously. 
* Two, validate the message. 
* Three, parts of the message and convert it to a unified format
* Four, save it to the data store.

Let's talk a little on the third task.

This task is super important as it makes our data independent of each source, meaning when we
will create the data, it will always look the same and be of the same format regardless of
its source. No matter from which device the status update was received, the data is fully 
accessible to the client and there is no need to formatted while querying.

This concept is extremely important in systems that receive data from different sources, each
with its own format, the data must be stored in a unified format, regardless of its origin, to
allow fast and efficient querying.

For our system we're going to need another component, a Handler component to validate, parse and 
store the data. Additionally, we're going to use a centralized logging system.

### Choosing messaging methods

Let's begin with the receiver, the receiver, as its name implies, receives the messages from
the IoT devices. In this case, the messaging method is actually dictated by the way the 
various devices send their messages.

To find out how they do we will go back to the client.

After a few phone calls, she comes back to us with the answer.

The devices communicate via HTTP using the POST verb to send the update. Well, that's great.
It means our receiver just became a standard run-of-the-mill Web API application with rest
API as its interface.

Let's move on to the handler. Now here things begin to get a little complicated. As you probably
remember, the handler's role is to validate and pass the messages received by the receiver.
It's only reason for existence is to offload the tasks from the receiver, which should focus 
on receiving the messages and releasing the requests. After the handler handles the message, it
should store it in the data store for later use. It looks like the best mechanism here is QUEUE.

Last but not least, the logging service. Remember, we need the logs produced by other services 
to be sent to the logging service for aggregation. Logs tend to be quite massive, and we can 
expect the various services to produce a huge number of log records every hour. In order to be
friendly with cloud services, and achieve the performance needed we are going to use a QUEUE.

### Designing the logging service

Well, the reason we are starting with this service is twofold.

* First, we want to emphasize that logging is important. Many developers and sadly, architects
treat logging as an afterthought. But this is the wrong way to handle it. Logging is one of the
cornerstones of every application and therefore should be treated as any other service.

* Second, we want to build all our services in a way that already includes logging and not
adding it later. For that, we will need the logging service ready so the services can
communicate.

Here are the steps we need to take for the components drill-down:

* First, decide on the kind of application, is it Web app, service, desktop? 
* Second, decide on the technology stack of the component
* Third, design the architecture.

The logging service does not wait for any request. It is always on and once in a while 
pulls data from the queue.

So let's see how this stacks up against the application types we know.

So first, Web apps and Web API, they are both off the table since, as we just said, the 
logging service is not based on the only request response model, but is always online and
initiating its own activities.

It's definitely not mobile application. It runs on the server and not on the client.

What about console? Well, it looks like a good fit. Console applications are best suited for
long-running processes while offering limited user interface. This is exactly what we need
from our logging service. So this is a great candidate.

Next is a service. Remember that services are quite similar to consult with two important
distinctions. They offer no UI at all and are managed by some kind of service manager. 
So it looks like the logging service can also be a service.

Last is desktop application, which of course is not relevant for the logging service since 
it runs on the server.

So we are left with console up and service.

Which one is better? Well, actually there is no definite answer it, and it depends mainly on
personal taste.

OK, so we have the application type, next, the technology stack, as you probably remember,
when deciding on the tech stack, we first need to define what are the elements in the 
component that need to be selected in all service. There are two such elements, the 
components code and the data store.

Let's begin with the code. Since the logging service is going to be a service, we do not have 
a lot of requirements for the technology stack, we need the code to be able to access the 
Queue API and store data in a data storage. In addition, there are no special requirements 
about the performance. Of course, we want it to be fast, but there is no specific 
requirement that limits us here. This stack can be .Net, .Net Core, Java and MySQL, Python and
MySQL, etc.

OK, great. So we have the technology stack. Now let's design architecture.

Remember our section about layered architecture, how we say that in most cases this is 
the go-to architecture of every component? Let's see if it fits here. As you probably remember 
later, the architecture has these three layer user interface or service interface, business
logic and data access that right to the data store.

As our applications doesn't have a UI what we are going to do is tweak the classic layered
pattern and modify the top layer to be a polling layer. This layer is responsible for
accessing the queue and retrieving the local code to be handled by the business layer.

The polling layer runs a timer, which polls the queue every few seconds. If new records are 
returned from the queue, the polling will send them to the business logic. This layer
validates them and make sure no garbage has been sent. If everything is OK, it sends them 
to the data access level, which sends them to the database. And that basically is the 
architecture of the logging service.

### Designing the receiver

So first, what kind of application is your service? Well, this is an easy one. We said the
devices send the messages via HTTP using the REST protocol. So the evident conclusion is 
that the service is a Web API which exposes wrist endpoints.

We already decided the logging service is going to be based in the .NET, and we will need a 
perfect reason to divert from this decision. Using multiple technologies in a single 
application can create a lot of headaches if done for the wrong reasons. So let's see if
there is any good reason NOT to continue with.

So does .NET Core good support for Web API applications? The answer is a resounding yes.

OK, so it looks like there is no reason not to use .NET Core and this is what we will do.

Remember what our service is supposed to do with the messages? It's going to put them
in the queue. That's right. There is no data for this service.

Well, you can argue that queue is some kind of data, but in reality, we don't treat it 
that way, but as a method for passing messages from one point to another. So while our service
definitely needs service interface, which is what the devices will talk to and the business 
logic which will validate the messages we need to substitute the data access layer with
another layer. In this case, we will create a new layer called queue handling layer, 
which will take care of the various tasks of working with the queue, mainly adding 
the message to the queue.

The logging would be a cross-cutting concern, so it would be a vertical implementation.

### Designing Handler service

One of the major factors that will influence the handler design is the fact that the message
has to be handled are waiting in the queue after being placed there by the receiver.

As far as our handler service is similar to our logging service he service is going to be a
Windows service.

By now we already have two services for which we determined the technology stack, the logging 
service and the receiver in both we went for .NET Core. Since it looks like there is no real
reason to select other technology for we can be quite comfortable in using .NET Core to.

And now to the architecture. We are going to use a traditional layered architectural
pattern here, same as in other services. Let's examine what layers are relevant here.

First service interface. Well, we don't have one. This service does not expose any API.
It is always active and initiates the call to the queue, it's not waiting for requests for
multiple services. So this layer, instead of exposing API, will orchestrate the work 
against the queue. Specifically, this layer is responsible for timing the polling of 
the queue and executing the actual polling. Let's call this layer polling, same as in the
logging service.

Next layer is the business logic layer. And yes, the service definitely needs such a layer.
This is responsible for validating and passing the messages, which are typical jobs for
business logic. Now note that in the real world app, we would have discussed a plugin mechanism
to allow dynamic loading of validators in parcels for specific messages types.

And last but not least, the data access layer. This is an extremely important player in the 
service, and it's responsible for setting the handle messages into the data store.

And of course, let's add the logging engine, which is similar to the one we used in the 
receiver is vertical and accessible by all the layers.

### Designing info service

The last service system is info service. So first, let's decide on the application type here.
Well, that's actually an easy one. We have a service that should be accessed by our client 
in order to perform some queries. That's a textbook for Web API service.

Now, the technology stack, here to the decision is quite easy. We already decided to use .NET Core 
for the receiver service, which is also a Web API, and there is no real reason to pick other 
technology for the info service.

Now to the architecture. We need a service interface, obviously, we definitely need a 
business logic to validate the requests. And of course, we need a data accessible to 
access the database and retrieve the data. And let's not forget the logging. 

So is that all? Well, not exactly.

One of the important steps in the architecture phase is to define the exact methods of the API.
Now, we didn't do it in the receiver service since the methods were dictated by the devices.
But here we are in a different situation, and we can decide what actions we want to expose 
as part of the API.

So after discussing it with the client, it looks like what really interested the end users
are two types of information, current status of devices and past event. Also, end users want 
to see the status of a specific device, as well as a high level view of all the devices in a
specific smartphone.

So that means our app should have the following functionality:

* Get all the updates for specific devices for a given time range
* Get the updates for a specific device, for a given time range
* Get the current status of all the devices in a specific house
* Get the current status of a specific device.

When designing API what really matters are usually two main factors:

* The API path
* The return code and contents

## **Advanced topics**

### Microservices

Microservices are all the rage right now. You can't have an architectural discussion 
without this term coming up sooner or later, usually sooner. 

But what is actually microservices? Well, put simply, a microservices based architecture is an
architecture in which the values functionalities are implemented as separate, loosely coupled
services that interact with each other using standard lightweight protocol.

To understand the motivation for microservices let's go back to the primer microservices days.
In these ancient times, application were built as a monolith, meaning all the functionalities
will run in a single process, usually built using the three layers architecture.

But there are some inherent problems with microservices systems, one, because the application
is executed in a single process. Then, if there is an exception in a single component, the 
whole process comes crashing down every bug, every case can render the application unusable.

Two, Every time we need to update the application, we need to update the whole code.
We cannot replace just a single component because again, we run in a single process with
a single executable.

Three, we are limited to one development platform. We cannot combine, say, Java and PHP in 
the same process.

And last compute resources are not optimized, if our application performs some heavy-duty 
calculations that require a lot of resources, but also to fulfill some lightweight queering, 
we cannot assign computing resources to the specific code that requires it.

The microservices, architecture claims to solve all of these issues. Remember, with 
microservices, the application is actually a collection of small, lightweight and loosely 
coupled services.

### Event Sourcing

Management in traditional applications, entities are stored in the database, usually as a
collection of attributes, with the application needed to update a specific attribute.
It simply accesses this attribute and modify its value, with Event Sourcing we handle it 
differently. When implementing events we do not modify attributes of the entity, rather we 
track events related to the entity.

### CQRS

So what exactly is CQRS?

Well, CQRS stands for Command Query Responsibility Segregation. What it actually means is 
this: while in traditional systems, the same database is used for retrieving and updating data
in CQRS based system these are separated to two different databases, meaning we have one
database for storing data in one database for retrieving the data into some kind of service
to think between them.

## **Soft skills**

In order to be a great architect it's not enough to be well versed in technology stacks, 
architectural patterns and coding best practices. **A great architect must have great soft skills.
These soft skills are essential when communicating with a project team from the developer 
to the project manager and even the CTO and CEO.**

Software architect is in a very unique position in the organizational tree. She has a very
deep knowledge about the application and its architecture, and she's expected to get
the development team about the actual implementation. But in reality, she has no authority
over them. She can't command the team what to do. She can only recommend now if the architect
is an arrogant, righteous person that makes everybody else feel inferior no one will want 
to work with him and as a result, no one would want to implement the architecture.

**The architect must be able to make the team do what he wants without the actual authority 
over them. This is called influence without authority.**

Some skills that you would need to consider as an architect are:

* Listening. One of the key factors in a successful teamwork is the ability to listen and to
assume you are not the smartest person in the room.

* Criticism. Your walk is going to be criticized probably heavily, you will be questioned on 
almost any design element in your architecture and will be asked to explain the logic behind it.

* Be smart, not right. Being smart means doing the thing that will help you achieve your goal
instead of doing the thing that will make you feel right.

* Organizational politics. Many times, in order to be a real successful architect and in
order to leave a mark, you will have to be well aware of the organizational politics.

* Public speaking. Architects specifically must be able to speak in front of a large audience.
Remember, architects usually have no formal authority over developers, system analysers or project
managers. If an architect wants to influence, she should utilize his speaking skills. In 
addition, architects are going to take part in many meetings. Some of them are critical to
the project's success and if their input is crucial. So as an architect, you have to be able 
to stand in front of an audience and deliver a convincing, effective speech.

* Learning. Always keep learning. We live in a dynamic world. In the soft/tech world is even 
more so things are changing in a blink of an eye forever that we are all the rage just
three years ago are now completely forgotten.