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
## <a name="ocp">3.4 OCP - Open-Closed Principle (goal of OO architecture)</a>
## <a name="lsp">3.5 LSP - Liskov Substitution Principle</a>
## <a name="isp">3.6 ISP - Interface Segregation Principle</a>
## <a name="dip">3.7 DIP - Dependency Inversion Principle (primary mechanism of OO architecture)</a>

## <a name="concepts">Concepts :bulb:</a>

**<a name="mid-level">💡 Mid-level</a>**  
Principles are applied by programmers working at the module level. Applied just above the level of the code and help to define the kinds of software structures used within modules and components. 



## <a name="links">Links</a>
1. [Clean Architecture: A Craftsman's Guide to Software Structure and Design by Robert C. Martin](https://g.co/kgs/554Z2i)
2. [Design Principles and Design Patterns by Robert C. Martin (2000)](https://web.archive.org/web/20150906155800/http://www.objectmentor.com/resources/articles/Principles_and_Patterns.pdf)
3. [Wikipedia about Cohesion](https://en.wikipedia.org/wiki/Cohesion_(computer_science))
4. [Wikipedia about Coupling](https://en.wikipedia.org/wiki/Coupling_(computer_programming))
5. [Wikipedia about Conway's Law](https://en.wikipedia.org/wiki/Conway%27s_law)
6. [Conway's Law by Martin Fowler](https://martinfowler.com/bliki/ConwaysLaw.html)
