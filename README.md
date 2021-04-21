# **`Software Architecture Notes`**

## **What is a Software Architect**

### Diferences between Developer and Architect:
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
a specific one, however, a Computer Science degree won't hurt. Additionally
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
## **Meet the -illities**
## **Component's architecture**
## **Design patterns**
## **System Architecture**
## **External considerations**
## **Architecture Document**
## **Case study**
## **Advanced topics**
## **Soft skills**
