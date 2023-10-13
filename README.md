# Design principles: SOLID

Personal digest of [Clean Architecture: A Craftsman's Guide to Software Structure and Design by Robert C. Martin (2017)](https://g.co/kgs/554Z2i), [Design Principles and Design Patterns by Robert C. Martin (2000)](https://web.archive.org/web/20150906155800/http://www.objectmentor.com/resources/articles/Principles_and_Patterns.pdf) & [else around the internet](#links) about SOLID principles.

## Content
1. [1st: Symptoms of rotting design - poor architecture](#symptoms)
2. [2nd: Causes to rot](#causes)
3. [3rd: Solution - Principles of Object Oriented Class Design](#solution)  
3.1 [What is SOLID](#what_is_solid)  
3.2 [Goal of SOLID](#goal_of_solid)  
3.3 [SRP - Single Responsibility Principle](#srp)  
3.4 [OCP - Open-Closed Principle](#ocp)  
3.5 [LSP - Liskov Substitution Principle](#lsp)  
3.6 [ISP - Interface Segregation Principle](#isp)  
3.7 [DIP - Dependency Inversion Principle](#dip)  
4. [Concepts :bulb:](#concepts)
5. [Links](#links)



## <a name="symptoms">1st: Symptoms of rotting design - poor architecture</a>

:triangular_flag_on_post: ***Rigidity*** *(stiffness, fixed)*  
When easy change causes cascade of changes in dependent modules. If manager’s start to fear to fix problems or refuse to allow changes - design deficiency becomes an adverse management policy.  
:triangular_flag_on_post: ***Fragility***  
Breaks everytime changed. Impossible to maintain & probability of breakage increases with time.  
:triangular_flag_on_post: ***Immobility***  
Inability to reuse. Module has too much baggage it depends upon. Safer is to rewrite than reuse.  
:triangular_flag_on_post: ***Viscosity*** *(swamp)*  
Easy to do the wrong thing, hard to do the right thing. Viscosity of environment - long compiles, source code control system requires a long time to check-in - engineers' temptation to todo as few check-in’s as possible/make changes that don’t force large recompiles.

## <a name="causes">2nd: Causes to rot</a>

- Changing requirements - initial design left behind - design not resilient to changes.
- New unplanned dependencies between modules of software. Need of ependency management - creation of dependency firewalls.

## <a name="solution">3rd: Solution - Principles of Object Oriented Class Design</a>
## <a name="what_is_solid">3.1 What is SOLID</a>

The SOLID principles - principles, that tell us how to arrange our functions and data structures into classes, and how those classes should be interconnected.

## <a name="goal_of_solid">3.2 Goal of SOLID</a>

The goal of the principles is the creation of [mid-level💡](#mid-level) software structures that: 
1. Tolerate change
2. Are easy to understand
3. Make components to be reused in many software systems


## <a name="srp">3.3 SRP - Single Responsibility Principle</a>

> There should never be more than one reason for a class to change.

or

> Each software module should have one and only one reason to change.

or

> A module should be responsible to one, and only one, actor. 

### What SRP is NOT:  
“A function should do one, and only one, thing.” - it’s a refactoring principle, to refactor large functions into smaller functions; we use it at the lowest levels. But it’s NOT the SRP.

### What SRP IS:
- SRP is the reason we separate concerns.
- Gather together the things that change for the same reasons. Separate those things that change for different reasons.
- We want to increase the [cohesion💡](#cohesion) between things that change for the same reasons, and we want to decrease the [coupling💡](#coupling) between those things that change for different reasons.
- An active corollary to [Conway’s law💡](#conways-law): The best structure for a software system is heavily influenced by the social structure of the organization that uses it so that each software module has one, and only one, reason to change.

### What is the reason to change?
- When you write a software module, you want to make sure that when changes are requested, those ***changes can only originate from a single person***, or rather, a single tightly coupled group of people representing a single narrowly defined business function. You want to isolate your modules from the complexities of the organization as a whole, and design your systems such that each module is responsible (responds to) the needs of just that ***one business function***.

### Symptoms of SRP violation

1. Accidental duplication. These problems occur because we put code that different actors depend on into close proximity. The SRP says to separate the code that different actors depend on.

2. Merges. Multiple people changing the same source file for different reasons. To avoid this problem is to separate code that supports different actors. Solution - move the functions into different classes. 

SRP appears at two different levels:
- Level of components (relates to [Common Closure Principle :link:](https://ericbackhage.net/clean-code/the-common-closure-principle/))
- Architectural level (relates to [Axis of Change💡](#axis-of-change))

## <a name="ocp">3.4 OCP - Open-Closed Principle (goal of OO architecture)</a>
## <a name="lsp">3.5 LSP - Liskov Substitution Principle</a>
## <a name="isp">3.6 ISP - Interface Segregation Principle</a>
## <a name="dip">3.7 DIP - Dependency Inversion Principle (primary mechanism of OO architecture)</a>

## <a name="concepts">Concepts :bulb:</a>

**<a name="mid-level">💡 Mid-level</a>**  
Principles are applied by programmers working at the module level. Applied just above the level of the code and help to define the kinds of software structures used within modules and components. 

**<a name="conways-law">💡 Conway’s law</a>**  
An adage that states organizations design systems that mirror their own communication structure. It’s an observation that the architectures of software systems look remarkably similar to the organization of the development team that built it.

**<a name="cohesion">💡 Cohesion (bond)</a>**  
The degree to which the elements inside a module belong together. In one sense, it is a measure of the strength of relationship between the methods and data of a class and some unifying purpose or concept served by that class. The force that binds together the code responsible to a single actor. 

**<a name="coupling">💡 Coupling</a>**  
Degree of interdependence between software modules.

**<a name="axis-of-change">💡 Axis of Change</a>**  
An idea that changes in a system tend to occur around the axis of a class's responsibility. When a change is needed, it's likely to be in the area of a class's responsibility. By having each class focus on a single responsibility, it becomes easier to manage changes because they are likely to be localized to specific classes.

## <a name="links">Links</a>
1. [Clean Architecture: A Craftsman's Guide to Software Structure and Design by Robert C. Martin](https://g.co/kgs/554Z2i)
2. [Design Principles and Design Patterns by Robert C. Martin (2000)](https://web.archive.org/web/20150906155800/http://www.objectmentor.com/resources/articles/Principles_and_Patterns.pdf)
3. [Wikipedia about Cohesion](https://en.wikipedia.org/wiki/Cohesion_(computer_science))
4. [Wikipedia about Coupling](https://en.wikipedia.org/wiki/Coupling_(computer_programming))
5. [Wikipedia about Conway's Law](https://en.wikipedia.org/wiki/Conway%27s_law)
6. [Conway's Law by Martin Fowler](https://martinfowler.com/bliki/ConwaysLaw.html)
7. [Common Closure Principle](https://ericbackhage.net/clean-code/the-common-closure-principle/)

