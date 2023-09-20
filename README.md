## Clean Coder (uncle BoB)


---

**Table of contents:**

- [What is this?](#what-is-this)
- [Clean Code](#1clean-code)
- [Names](#2names)
- [Function](#3function)
- [Function Structure](#4function-structure)
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


## 1.Clean Code


## 2.Names
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



## 3.Function
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

## 4.Function Structure

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
     - what if plugins have plugin of their own
     - in most well write application the line between application and plugin blurs
   - the goal of all this partitioning is to create a system that is composed of independent deployable module
   - lots of systems are not independently deployable most of the time we gather all the modules in a single file
   - and ship it as a single unit, but that doesn't mean wee don't wane independently deployable 
   - a system that is independently deployable is also independently developed 
   - when we have a plugin structure, then a development team working on those plugable modules works independently 
   - because the plugin structure makes it less likely to team inter fear with each other, on the other hand, a switch 
   - that ruins this plugin struggle also runes the independent dependability
5. a long chine of if else statements has the same problem that switch statements do  


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

### Paradigms

1. object-oriented programing
2. structured programming
3. functional programming
   - what is functional programming? 
     - you can't change the state of variables
     - there are no side effects 
   - functional programming seems radical at first if never look into it,
   - I think you might be surprised;
   - you may even wonder writing a program like this is even possible
   - functional program tells us writing program without any assignments
     - instead of setting a bunch of variables, you pass those variables as argument
     - instead of looping over a set of variables, you recurse throw a set of function arguments
   - you call a function that always returns the same value back when you give the same input
   - the value of function only depends on its input arguments and not any other state of a system
   - so every time you call that function with the same input, you get the exact same output 
   - there is no side effect

### side effects
when a function changes a variable that out live a function call, for example,
when it changes an n instance of variable, then that function has a side effect ,
and that side effect may change the behavior of that function
or some other function the next time that called 
this kind of scary actions ,make program difficult to understand, and it is persistence source of errors

1. often side effects come in pairs
   - set get open close new delete
   - the function should be called in order to open before close, new before delete 
   - we call this temporal coupling
   - when you depend on one thing happens before the other
   - most of the time temporal compelling are hidden in the background
     - you look at two functions that should be called in certain order, and you can't explain why
   - can you eliminate temporal couplings 
     - for example in open close
     - you resolve the temporal coupling by passing a block
     - you hide the second function inside the first 
     - and then pass command into the first
     - and first will do the open, execute a block and then close 
     - this leaves the system in the same state it was before
     - and eliminate the temporal coupling 
     - this is a technics **passing a block**
     - this guarantees that every thing stays consistent that functions are executed in the right order 
     - and a limited side effect 
     - 
     - we can't get rid of every side effect, and we don't want to 
     - we need to be able to change a file, we need to be able to update a databases
     - we need to be able to generate oyt put
     - all these things are side effects, and they are desirable side effects
     - our goal is not to eliminate the side effects
     - **our goal is to impose discipline upon where and how those side effects happen**
```
public voide open(file F, fileCommand)
   f.open()
   c.process(F)
   f.close()

```
### Command Query Separation
one very successful managing side effects is creating a strong separation between command and queries.
in this contex a command changes the state of a system it hase aside effect, a query does not.
a query returns a value of computation or state of a system,
a command changes the state of the system and returns Nothing

1. Functions that change State should not return Values
2. Functions that return Values should not change State
- advantages
   - it's easy to recognize a function are or aren't having a side effect's

let's look at this the other way around:
```
User u = authorizer.login(username, password)
```
looking at this call, clearly it changes the state of system 
the authorizer created a new logged-in user, 
but the authorized get back to you what are supposed to do 
are you supposed to manage it, are you in the middle of big coupling
you are the one who is supposed to call logout at some point, 
don't you think the authorizer should keep control of user
```
User u = authorizer.getUser(userName)
```
why did the login function return to user
maybe the loging return to user, so it can return a null if login fails.
we are often tempted to return error code
like this from our command if they fail to change state.
but it's better to
throw an exception maintaining a convention that commands returns a void.
```
old_blah=set_blah(new_blah)
...
set_blah(old_blah)
```
multiple threads complicate things ,
image we got a function that changes the state of system but also returns a previous state
so that we can save it and restore it later
, we don't want to separate this in two call the same way command query separation ask us
because we don't want a separate thread to sneak in between those two calls 
but notice how similar it is to open and close problem, you can resolve it the same way by passing a block
```
with_blah(new_blah, some_blah_command)
```
so don't confuse your readers' command that return values should not change state
and functions that change state can change state, but they should not return a value

### Tell Don't Ask
an extreme form of command query separation tells us to avoid queries altogether
```
if user.is_loged_in():
    user.exec_command()
else:
    annuciator.promt_login()
```
wouldn't this be better if we use exception like this?
```
try:
    user.exec(command)
exec User.NotLoggedIn as e:
    annunciator.promt_login()
```
and wouldn't that actually better if we let user object deal with a problem entirely?
```
user.exec(command, annunciator)
```
after all, it's a user object that knows whether it's logged-in or not
that state belongs to a user object why we take that ste and make decisions 
for the user here, we should let the user deal with the problem 
 - you should be told the object's to do not just ask them
 - query functions can get out of control really quickly


```
o.get_x()
    o.get_y()
        o.get_z()
            .do_some_thing()
```
I am sure you have seen a long chaine of function like this,
we call this train wrecks because it looks like boxed cars together  
they are a clear violation of tell don't ask 
because we ask to then ask before we tell anything
```
o.do_some_thing()
```
wouldn't this be better like this 
now we get rid of problem we told O to do something and O's got to figure out how to get to the z
o probably doesn't know where is z either, but o knows it s somebody that they can tell to figur it out
so call do something will propagate out word to eventually get to z 

train wracks the long chain of query break the law called the "law of demeter"
this law tells us that it is a bad idea that single functions to know the entire navigation structure of system
consider how much knowledge this line of code has, it knows that x has y and y has z and that z can do something
 that determines the amount of knowledge for oneline of code to have, and it couples the function that contains it
to too much of hole system
we don't want our functions to know about hole system
individual functions should have a very limited amount of knowledge,
we don't wane a function to be able to walk the whole configuration database
we don't wanna a function to be able when its way to the entire object map of entire system
what we want to do it to tell our neighboring objects what we need to have done 
and depend on them to propagate the massage to outward