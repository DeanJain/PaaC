---
marp: true
title: Design Principles and Patterns
description: Design Principles and Patterns PaaC
theme: gaia
size: 16:9
paginate: true
_paginate: false
header: ":copyright: OSS"
footer: "PaaC Rocks :heart:"
---
![](#012)

![bg opacity 100%](https://pbs.twimg.com/media/DP07zHPW4AIUkkk?format=jpg)

# <!--fit--> Design Principles & Patterns

<br /> <br />
###### If debugging is the process of removing software bugs, then programming must be the process of putting them in...  ~Edsger Dijkstra
<br/><br/>

### Dean.Jain - Staff Engineer @Amex

<!-- This is presenter note. You can write down notes through HTML comment. -->

---
![bg](#123)
![](#fff)

<!-- _class: lead -->
#### Agenda
- Intro : What
- History : When 
- Types : What All
- Details : How and Why
- Discussion Q/A ?

![bg right 90%](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTDqmvKIonQfgPF_7Rk--M4KDCl9xmto8bhWg&usqp=CAU)

<style scoped>a { color: #eee; }</style>
---
##### Software development is a learning process; working code is a side effect!

<!-- _class: lead -->
# Key Design Principles :key:

- (**KISS**) Keep It Simple Stupid :kiss: -> Do The **Simplest** Thing That Could Possibly Work
- **YAGNI** :do_not_litter: -> You Arent Gonna Need It 
- **DRY** :repeat: -> Dont Repeat Yourself (Single Source of Truth)
- **Code For The Maintainer** :green_book: -> Always code and comment in such a way that if someone a few notches junior checks up the code, they will take pleasure in reading and learning from it.
- **Avoid Premature Optimization** :sweat_drops: -> Make It Work Make It Right Make It Fast
- **Minimise Coupling** :couple: -> Coupling between modules/components is their degree of mutual interdependence; Lower coupling is better. In other words, coupling is the probability that code unit "B" will "break" after an unknown change to code unit "A".
- **Maximise Cohesion** :handshake: -> Cohesion of a single module/component is the degree to which its responsibilities form a meaningful unit; higher cohesion is better.

<style scoped> { font-size:24px;}</style>
---
![bg](#123)
![](#fff)
<!-- _class: lead -->
#### SOLID Principles: :rock:

* **SRP** states that a class should have exactly one responsibility
* **OCP** - class (or function) should be open for extension but closed for modification
* **LSP** states that if type S inherits from type T then both T and S should be interchangeable in functions that expect T.
* **ISP** says to avoid writing monstrous interfaces that burden classes with responsibilities they don't need or want. 
* **DIP** - Instead of writing code that refers to actual classes, you should instead write code that refers to interfaces or perhaps abstract classes

<style scoped> { font-size:23px;}</style>

![right bg 80%](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT4Wry5epHg-_WRnLzvxdZfWsmpy5AbAa6YXw&usqp=CAU)

##### Q: How to Apply Design Principles?? 
---
<!-- _class: lead -->
### What’s a design pattern?
- Design patterns are typical **solutions to commonly occurring problems** in software design. **They are like pre-made blueprints** that you can customize to solve a recurring design problem in your code.
- The pattern is not a specific piece of code, but **a general concept for solving a particular problem. You can follow the pattern details and implement a solution that suits the realities of your own program**.
- Design patterns are a **toolkit of tried and tested solutions to common problems** in software design.

---

![bg](#123)
![](#fff)

<!-- _class: lead -->
#### History:
- The concept of patterns was first described by Christopher Alexander in A Pattern Language: Towns, Buildings, Construction.
- Erich Gamma, John Vlissides, Ralph Johnson, and Richard Helm In 1994, they published Design Patterns: Elements of Reusable Object-Oriented Software, in which they applied the concept of design patterns to programming. 
- The book **featured 23 patterns** solving various problems of object-oriented design and became a best-seller very quickly. Due to its lengthy name, people started to call it **“the book by the gang of four”** which was soon shortened to simply **“the GoF book”**.
- Many patterns followed...

<style scoped> { font-size:32px;}</style>  
---
### Microservices Patterns

![width:1100px height:500px](https://microservices.io/i/PatternsRelatedToMicroservices.jpg)

---
![bg](#123)
![](#fff)
### Modern Design Patterns ++
1. Circuit Breaker
  Acts as a proxy for operations that might fail. The proxy should monitor the number of recent failures that have occurred, and use this information to decide whether to allow the operation to proceed, or simply return an exception immediately. Netflix’s Hystrix or Reselience4J or Envoy proxy can be used to implement it.

2. Sidecar
   Envoy Proxy is one of the most popular sidecar proxies, It helps you keep the core functionality of the application separate, using the sidecar to isolate common features like networking, observability, and security.

3. Backend-for-Frontend
   build/customize back-end services for the specific front end (Mobile vs desktop), gateway can be used to do redirection based on user agent
   
4. Strangler
   creating a facade on top of your legacy and a new application, providing an abstracted view to the consumers so that cloud migration/moderniazation is easier.

<style scoped> { font-size:24px;}</style> 
---
<!-- _class: lead -->
### Classic Design Patterns:
1. **Creational** patterns provide object creation mechanisms that increase flexibility and reuse of existing code.

2. **Structural** patterns explain how to assemble objects and classes into larger structures, while keeping the structures flexible and efficient.

3. **Behavioral** patterns take care of effective communication / assignment of responsibilities (algo) between objects.

---

![Marp bg 90%](https://foxlearn.com/images/creation-design-pattern-4c0dd968-cb74-4340.png?ezimgfmt=rs:689x384/rscb4/ng:webp/ngcb4)

---

![Marp bg 80%](https://foxlearn.com/images/structural-design-patterns-f4c5795f-4c2e-4b48.png?ezimgfmt=rs:769x434/rscb4/ng:webp/ngcb4)

---

![Marp bg 70%](https://foxlearn.com/images/behavioral-design-patterns-36362633-221d-494c.png?ezimgfmt=rs:769x549/rscb4/ng:webp/ngcb4)

---

![bg](#123)
![](#fff)

<!-- Scoped style -->
<style scoped>
h1 {
  color: yellow;
}
</style>

## Creational - Factory Method: 
Method, Provides an interface for creating objects in a superclass, but allows subclasses to alter the type of objects that will be created.

### Creational - Abstract Factory
Object, a super-factory which creates other factories, is also called as factory of factories. lets you produce families of related objects without specifying their concrete classes.

### Creational - Builder 
Construct complex objects step by step (step-by-step initialization of many fields and nested objects). The pattern allows to produce different types and representations of an object using the same construction code.

### Creational - Prototype 
lets you copy existing objects without making your code dependent on their classes. declares a common interface for all objects that support cloning. This interface lets you clone an object without coupling your code to the class of that object.

### Creational - Singleton 
lets you ensure that a class has only one instance, while providing a global access point to this instance.

<style scoped> { font-size:20px;}</style>
---

### Structural - Adapter 
allows objects with incompatible interfaces to collaborate (XML -> JSON Adaptor)

### Structural - Bridge 
lets you split a large class or a set of closely related classes into two separate hierarchies (abstraction and implementation) which can be developed independently of each other.

### Structural - Composite 
lets you compose objects into tree structures and then work with these structures as if they were individual objects. Composite class holds a collection of smaller/individual objects.

### Structural - Decorator 
lets you attach new behaviors to objects by placing these objects inside special wrapper objects that contain the old behaviors.

### Structural - Facade 
provides a simplified interface to a library, a framework, or any other complex set of classes. Having a facade is handy when you need to integrate your app with a sophisticated library that has dozens of features, but you just need a tiny bit of its functionality.

<style scoped> { font-size:20px;}</style>
---

### Structural - Flyweight 
lets you fit more objects into the available amount of RAM by sharing common parts (immutable) of state between multiple objects instead of keeping all of the data in each object.

### Structural - Proxy 
lets you provide a substitute or placeholder for another object. A proxy controls access to the original object, allowing you to perform something either before or after the request gets through to the original object.

---
![bg](#123)
![](#fff)

### Behavioral - Chain of Responsibility 
lets you pass requests along a chain of handlers. Upon receiving a request, each handler decides either to process the request or to pass it to the next handler in the chain.

### Behavioral - Command 
turns a request into a stand-alone object that contains all information about the request. This transformation lets you pass requests as a method arguments, delay or queue a request’s execution, and support undoable operations.

### Behavioral - Iterator 
lets you traverse elements of a collection without exposing its underlying representation (list, stack, tree, etc.), Iterators implement various traversal algorithms. 

### Behavioral - Mediator/Controller/Gateway 
lets you reduce chaotic dependencies between objects. The pattern restricts direct communications between the objects and forces them to collaborate only via a mediator/controller/gateway object.

### Behavioral - Memento/Snapshot 
lets you save and restore the previous state of an object without revealing the details of its implementation (history of state).

<style scoped> { font-size:20px;}</style>
---
![bg](#123)
![](#fff)

### Behavioral - Observer/Event-Subscriber/Listener
- lets you define a subscription mechanism to notify multiple objects about any events that happen to the object they’re observing.
- The Observer pattern suggests that you add a subscription mechanism to the publisher class so individual objects can subscribe to or unsubscribe from a stream of events coming from that publisher. 
- this mechanism consists of 1) an array field for storing a list of references to subscriber objects and 2) several public methods which allow adding subscribers to and removing them from that list.

### Behavioral - State 
lets an object alter its behavior when its internal state changes. It appears as if the object changed its class. extract all state-specific code into a set of distinct classes. As a result, you can add new states or change existing ones independently of each other, reducing the maintenance cost.

### Behavioral - Strategy 
lets you define a family of algorithms, put each of them into a separate class, and make their objects interchangeable. take a class that does something specific in a lot of different ways and extract all of these algorithms into separate classes called strategies.

### Behavioral - Template Method 
defines the skeleton of an algorithm in the superclass but lets subclasses override specific steps of the algorithm without changing its structure. break down an algorithm into a series of steps, turn these steps into methods, and put a series of calls to these methods inside a single template method. The steps may either be abstract, or have some default implementation. To use the algorithm, the client is supposed to provide its own subclass, implement all abstract steps, and override some of the optional ones if needed

### Behavioral - Visitor 
lets you separate algorithms from the objects on which they operate. The Visitor pattern suggests that you place the new behavior into a separate class called visitor, instead of trying to integrate it into existing classes. The original object that had to perform the behavior is now passed to one of the visitor’s methods as an argument, providing the method access to all necessary data contained within the object.

<style scoped> { font-size:15px;}</style>
---
![bg](#123)
![](#fff)

- ### What do you guys think :ok_hand::blush:
- ### Discussion :hand::unlock:
- ### Questions :question::bulb:
---

![bg 40% opacity blur](https://avatars.githubusercontent.com/deanjain)

##### Created by Dean Jain ([@dean.jain](https://github.com/deanjain)) 

<br />

##### References:
- https://refactoring.guru/design-patterns
- https://foxlearn.com/design-patterns/what-are-design-patterns-431.html
- https://en.wikipedia.org/wiki/Design_Patterns
- https://microservices.io/patterns/microservices.html
  

Powered by PaaC (Presentation as a Code) :heart::purple_heart::green_heart::blue_heart: