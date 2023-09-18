## Clean Coder (uncle BoB)


---

**Table of contents:**

- [What is this?](#what-is-this)
- [Clean Code](#clean-code)
- [Names](#names)
- [Function](#function)
- [Function Structure](#function-structure)
  * [Arguments](#arguments)


---

## What is this?

Hello 👋

this repository is a summary of the collection of robert c martin books
and python examples to make it more understandably 
(clean code, clean coder , clean architect, clean agile)

**Few important notes about it:**

1. It's derived from many years of experience & many Fastapi projects, both big & small.
2. It's pragmatic. All things mentioned here are things tested in production.

**SomeThing important that I forgot**


## Clean Code


## Names
1. chose your name thoughtfully
2. communicate your INTENT
3. avoid disinformation
4. pronounceable names
5. avoid encoding (like adding s,i,b,l, etc. to sow that variable is list string or anytype)
6. choose your name so that code can be read like a well-written latter
7. class and variables name should be named, functions should be verse, and boolean should be (is_user_admin)
8. follow the scope rule
    - variables in big scope should have a descriptive big name, in small scope should have a short name
    - functions in long scope should have a short name, in small scopes should have a large descriptive name



## Function
1. do 1 thing
2. do it well
3. do it only
4. it should be small even smaller than that
5. 4-6 line
6. small descriptive name
7. extract till you drp
**Before**
```python

```
**After**
```python

```

## Function Structure

### Arguments
1. **3** arguments **MAX**
    - if 3 or more arguments are so needed to pass together, why aren't they an object
2. same as constructor in class
    - better to use nicely named setter functions over a constructor with a hole bunch of arguments
3. no boolean arguments ever
    - if a function does two things, it's two functions
4. innes not outies
   - never use output as an argument, arguments should go into the function not coming out

5. the null defence
   - passing a null to a function or writing a function that expects a null to be passed in
   - it is almost as bas as passing a boolean into the function
   - actually, it's worse cuz it's not abuse that it's two possible states 
   - write two functions one that take null the other that don't
   - don't use null as a sudo boolean
   - i don't like defensive programming i don't like to littering my code with null check and error check 
   - I hate to think my teammates carelessly allowing null to slip throw to my functions 
   - defensive coding means that you don't trust your team or your team unit test 
   - if you are constantly checking your input arguments for nulls, that means that 
   - your unit test is not preventing you from passing those nulls
   - in public api code defensive but core written in my system by my team good offence by sweet test
   - 
6. the step-down rule
    - public methods up — private methods down 
    -  importance up - detail down
    - then you can take listing and then cut that listing between the public and private
    - and handing the public part to users
    - it's better to follow a suboptimal convention that confuses every body
    - all the functions point down, not backward pointing

### Switch Statements
1. switch statements are a missed opportunity to use polymorphism
2.  there is no rule, but generally we don't use it
3. they are not OO
   - the big benefit of OO is the ability to manage dependencies
   - A -> B if there is module A has a function that calls the module B
   - that s dependency from module A to module B
   - that dependency it has two component (it's runtime dependency)
   - the source code of module A is dependent on module B (like Import or using a method)
   - what we want to deploy module aA and B sepratly. For example, a module B is a plugin to module A
   - if module A is dependent on module B, they cannot be deployed separately, they can not be compiled separately
   - OO allow us to revert that source code dependency. A (dependent)-> I(interface) <- B(drive)
   - the source code dependency point's again's the flow of control, it opposes the flow of control
   - module B can be plugged in module B
   - each case in switch statements it's like to have a dependency outward on an external module
   - when we face a switch statements, we can do two things
     - invert a dependency with polymorphism 
     - the other option is to move switch statements to somewhere that cannot make any harm
     - to replace a switch with polymorphism 
       - take the argument of switch which is some type code and replace it with abstract base class 
       - that has a method that corresponds to the operation that been performed by the switch
       - then each of the switch cases became a driven class implement the method that case did 
       - where to implement this ?? in Factory
   - in every application you write, you should draw a line through a module diagram that separates core application
   - library from low-level detail 
   - the application part where most application code lives 
   - but on the main side, we have low-level stuf like factories, configuration data (the main program)
   - application is usually subdivided in different submodules
   - but the main part should be small and limited in subdivision
   - the dependency between these two partitions should point in one direction and one direction only
   - they should cross the line towards the application 
   - the main partition should depend on application the application should not have no dependency backward towards main
   - maine is plug in to the application
4. Dependency injection
   - the tricks to dependency injection carefully define and maintain your partitioning
   - go ahead and use the framework but only inject a few entrypoint from main in to the rest of the application 
   - and let min do the rest of work with factory and strategies
   - if your application is composed in independently deployable plugins 
   - then all of those plugins should know about core application and central core shouldn't know anything about plugins at all
   - all the source code dependencies should point inward from the plugins towards the core 
   - no software dependency should point outward way from the core towards plugins
     - waht if plugins have plugin of their own
     - in most well write application the line between application and plugin blurs 

```
         ┌───┐                    ┌───┐
         │app│                    │app│
         └─┬─┘                    └─┬─┘
           │                        │
     ┌─────▼─────┐            ┌─────▼──────┐
     │   Switch  │            │ Base Class │
     └─────┬─────┘            └─────▲──────┘
           │                        │
  ┌─────┬──┴──┬─────┐       ┌─────┬─┴───┬─────┐
  │     │     │     │       │     │     │     │
┌─▼─┐ ┌─▼─┐ ┌─▼─┐ ┌─▼─┐   ┌─┴─┐ ┌─┴─┐ ┌─┴─┐ ┌─┴─┐
│   │ │   │ │   │ │   │   │   │ │   │ │   │ │   │
└───┘ └───┘ └───┘ └───┘   └───┘ └───┘ └───┘ └───┘
    other modules               Drivetive
```       

```
                                              ────┐
                 ┌┬────────────────────┬┐         │      ┌┬──────────────┬┐
                 ││applicatio partition││         │      ││main partition││
                 └┴────────────────────┴┘         │      └┴──────────────┴┘
                                                  │
                                                  │
                                                  │
              ┌───────┐                           │   ┌───────┐
              │       │            ┌─────────┐    │   │factory│
┌──────┐ ┌────►       ├───────────►│ factory │◄───┼───┤  imp  │◄───┐
│      ├─┤    └──▲────┘            └─────────┘    │   └───────┘    │  ┌──────┐
│      │ │       │                                │                ├──┤ main │
└──────┘ │       │                                │                │  └──┬───┘
         │  ┌────┴──┐                             │   ┌───────┐    │     │
         └─►│       │              ┌─────────┐    │   │factory│    │     │
            │       ├─────────────►│ factory │◄───┼───┤ imp   │◄───┘     │
            └─┬───┬─┘              └─────────┘    │   └───────┘          │
              │   │                               │                      │
 ┌──────┐◄────┘   └────────────────────┐          │                      │
 │      │                              │          │                      │
 │      ├───►┌──────┐              ┌───▼──────┐   │                      │
 └──────┘    │      ├─────────────►│          │◄──┼──────────────────────┘
             │      │              └──────────┘   │
             └──────┘                             │
                                                  │
                                                  │
                                                  │
                                                  └─────
```
