## Clean Coder (uncle BoB)


---

**Table of contents:**

- [What is this?](#what-is-this)
- [Clean Code](#1clean-code)
- [Names](#2names)
- [Function](#3function)
- [Function Structure](#4function-structure)
  * [Arguments](#arguments)
  * [Switch Statements](#switch-statements)
  * [Paradigms](#paradigms)
  * [Side Effects](#side-effects)
  * [Command and Query Separation](#command-query-separation)
  * [Tell Don't Ask](#tell-dont-ask)
  * [Early Returns](#early-returns)
  * [Error Handling](#error-handling)
- [Form](#5form)

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
6. choose your name so that code can be read like a well-written pros
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
   - passing a null to a function it is almost as bas as passing a boolean into the function
     - it's worse cuz it's not obvious that it's two possible states 
     - write two functions one that take null the other that don't
     - don't use null as a sudo boolean
   - i don't like defensive programming i don't like to littering my code with null check and error check 
   - I hate to think my teammates carelessly allowing null to slip throw to my functions 
   - defensive coding means that you don't trust your team or your team unit test 
   - if you are constantly checking your input arguments for nulls, that means:
     - that your unit test is not preventing you from passing those nulls
   - in public api code defensive; but core written in my system by my team good offence by sweet test
   - 
6. the step-down rule
    - public methods up — private methods down 
      - hand the public part to users
    -  importance up - detail down
      - all the functions point down, not backward pointing

### Switch Statements
Switch statements are a missed opportunity to use polymorphism.

There is no rule, but generally we don't use it.

They are not OO.

the big benefit of OO is the ability to manage dependencies
A -> B if there is module A has a function that calls the module B
that s dependency from module A to module B
that dependency it has two components (its runtime dependency)
the source code of module A is dependent on module B (like Import or using a method)
what we want to deploy module aA and B sepratly.For example, a module B is a plugin to module A
if module A is dependent on module B, they cannot be deployed separately, they can not be compiled separately
OO allow us to revert that source code dependency.A (dependent)-> I(interface) <- B(drive)
the source code dependency point's again's the flow of control, it opposes the flow of control
module B can be plugged in module B
each case in switch statements it's like to have a dependency outward on an external module
when we face a switch statements, we can do two things
  invert a dependency with polymorphism 
  the other option is to move switch statements to somewhere that cannot make any harm
  to replace a switch with polymorphism 
    take the argument of switch which is some type code and replace it with abstract base class 
    that has a method that corresponds to the operation that been performed by the switch
    then each of the switch cases became a driven class implement the method that case did 
    where to implement this ??in Factory
in every application you write, you should draw a line through a module diagram that separates core application
library from low-level detail 
the application part where most application code lives 
but on the main side, we have low-level stuf like factories, configuration data (the main program)
application is usually subdivided in different submodules
but the main part should be small and limited in subdivision
the dependency between these two partitions should point in one direction and one direction only
they should cross the line towards the application 
the main partition should depend on application the application should not have no dependency backward towards main
maine is plug in to the application

Dependency injection

the tricks to dependency injection carefully define and maintain your partitioning
go ahead and use the framework but only inject a few entrypoint from main in to the rest of the application 
and let min do the rest of work with factory and strategies
if your application is composed in independently deployable plugins 
then all of those plugins should know about core application and central core shouldn't know anything about plugins at all
all the source code dependencies should point inward from the plugins towards the core 
no software dependency should point outward way from the core towards plugins
  what if plugins have plugin of their own
  in most well write application the line between application and plugin blurs
the goal of all this partitioning is to create a system that is composed of independent deployable module
lots of systems are not independently deployable most of the time we gather all the modules in a single file
and ship it as a single unit, but that doesn't mean wee don't wane independently deployable 
a system that is independently deployable is also independently developed 
when we have a plugin structure, then a development team working on those plugable modules works independently 
because the plugin structure makes it less likely to team inter fear with each other, on the other hand, a switch 
that ruins this plugin struggle also runes the independent dependability 

a long chine of if else statements has the same problem that switch statements do  


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
   - functional program tells us writing program without any assignments
     - instead of setting a bunch of variables, you pass those variables as argument
     - instead of looping over a set of variables, you recurse throw a set of function arguments
   - function always returns the same value back when you give the same input
   - the value of function only depends on its input arguments and not any other state of a system

### side effects
when a function changes a variable that out live a function call, for example,
when it changes an instance of variable, then that function has a side effect ,
and that side effect may change the behavior of that function or some other function the next time that called 
this kind of scary actions ,make program difficult to understand, and it is persistence source of errors

1. temporal coupling 
   - often side effects come in pairs
   - set-get, open-close, new-delete
   - the function should be called in order to open before close, new before delete 
   - when you depend on one thing happens before the other
   - most of the time temporal compelling are hidden in the background
     - you look at two functions that should be called in certain order, and you can't explain why
   - you can eliminate temporal couplings 
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
in this contex a command changes the state of a system it has a side effect, a query does not.
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
```
User u = authorizer.getUser(userName)
```
looking at this call, clearly it changes the state of system 
the authorizer created a new logged-in user, 
but the authorized get back to you what are supposed to do 
are you supposed to manage it, are you in the middle of big coupling
you are the one who is supposed to call logout at some point.
don't you think the authorizer should keep control of user?
why did the login function return to user?
maybe the loging return to user, so it can return a null if login fails.
we are often tempted to return error code
like this from our command if they fail to change state.
but it's better to
throw an exception maintaining a convention that commands return a void.
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
that state belongs to a user object why we take that state and make decisions 
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
and depend on them to propagate the massage too outward to the appropriate destination


#### Law of Demeter

formalizes "tell don't ask" by this rule

*you may call methods of objects that are:*
1. Passed as arguments
2. Created locally
3. Instance variable
4. Globals

*you may **not** call methods on objects that are:*
1. returned from a previous method call `o.get_x().get_y().get_z().do_some_thing()`

following this rule is hard; in fact, it's even been called suggestion of demeter.
but the benefits are obvious, any functions that follow this rule, any function that tells instead of ask 
is decoupled from its surroundings

biological systems are extream example of tell don't ask 
cells they do not ask each other questions they tell each other what to do

### Structured Programming
SOP sees that all the algorithms should be composed out of three basic operations
```
      ┌─────────┐
      │  Block  │
      ├─────────┤    Sequence
      │  Block  │
      └─────────┘

┌───┬───────┬───┐
│   │   ?   │   │
│   └───┬───┘   │
│ T     │     F │    Selection
├───────┼───────┤
│ Block │  Block│
└───────┴───────┘

    ┌───────────┐
    │ ?         │
    │   ┌───────┤    Iteration
    │   │ Block │
    └───┴───────┘
```
**Sequence**
is simply arranged of two sequences at a time.
The exit of first bloch feed the entry of second.
**Selection** 
is just a boolean expression that splits the flow in two pass ways.
Each of those pass ways contains a block.
One of those two blocks gets executed
and then pass ways rejoin, and there is a single exit.
**Iteration**
is simply the repeated execution of a block 
unit on boolean expression get satisfied

****single input at the top, single output at the bottom****

### Early Returns
Does a single entry single exit rule mean that you can't have multiple returns from function?
No, not at all, early returns and garb returns,
simply take you to the end of function where the exit is.
There is no violation of structure.

on the other hand,also there is a small problem with returning from the middle of the loop
1. mid-loop returns add unexpressed and indirect exit condition
    - while this doesn't violent structure is does make loop more complicated
2. what about breaks and continents in the middle of the loop
    - Continue is no problem at all
        - because continue just no updown to button of the loop and loop does the next iteration
    - break on the other hand is a bit more problematic 
        - a label break is more problem cuz it exits from more than one loop at a time

****it is more important to make your code understandable that your code to work****

### Error Handling

***error handling is important, but if it obscures the logic, it is wrong***

1. Errors Firs
   - it's always best if you write your error handling code then write the rest of code
   - that way you don't paint your self into an implementation that can't handle error
2. Prefer Exceptions
3. Exceptions are for callers
    - I don't like reusing can exceptions from a language library
    - when I threw an exception, I wanted to be scoped to the class that throw it
    - and I wanted to be named as specific as possible
4. Use Unchecked Exceptions
   - in java drive your exception from runtime exception
   - in python drives your exception from Base Exception
5. How much massage should it have?
    - not much
    - I think the best case for exception is to not have a massage at all
    - I like my error to be so persisted, so no massages are needed
    - the best comments is the comment you don't have to write
    - this is doesn't mean don't put massages im my exceptions
      - sometimes there is a till little bit of information that is useful to pass along
      - but I always want a name and scope of the exception to do the most of the work
6. Spacial Cases
    - it's possible someone might just construct a stack with zero sizes
    - it's not error it's definition for zer size stack
7. Null is not an error
    - Top return a top value but what should it return if the stack is empty
    - nobody expects to receive a null
    - and unwanted null has a tendency to slip and slide throw the system
    - until eventually, they cuz a null pointer exception
    - so it thinks it's better to trow entirely new exception a stack empty exception
8. Null is a value
    - find is a method that searches the stack from top to bottom
    - and return the first index that matches the input argument that is integer 
    - what should it do if it doesn't find the argument?!
    - we could throw an exception
    - but that would be strainge
    - because we expect a find to fail from time to time
    - and we usually reserve an exception for things that are not expected
    - what we need is vale that we can return in a find that means not found
      - java convention is to return -1 but -1 is still an integer 
      - it might get used at a computation 
      - I think it's better to return null 
      - null is a value that means nothing 
      - -1 is not nothing
9. trying is a one thing
    - if "try" appears in a function, it must be a very first word world of function after any variable declaration
    - body of try block must contain a single line a function call
    - and the close and finally line the last thing the function nothing follows them
    - a function supposed to do one thing and error handling is one thing
    - a function should either do something or hande errors
    - but it shouldn't do both 

```
import pytest


class Stack:
    def __init__(self, capacity: int):
        self.size = 0
        if capacity >= 0:
            self.capacity = capacity
        else:
            raise Stack.IllegalCapacity()
        self.elements = [None for _ in range(self.capacity)]

    def is_empty(self):
        return self.size == 0

    def get_size(self):
        return self.size

    def top(self):
        if self.is_empty():
            raise Stack.Empty()
        return self.elements[self.size - 1]

    def push(self, element):
        if self.size == self.capacity:
            raise Stack.Overflow()
        self.elements[self.size] = element
        self.size += 1

    def pop(self):
        if self.is_empty():
            raise Stack.Underflow()
        self.size -= 1
        return self.elements[self.size]

    def find(self, element):
        for i, e in enumerate(self.elements[::-1]):
            if element == e:
                return i
        return None

    class Overflow(Exception):
        ...

    class Underflow(Exception):
        ...

    class IllegalCapacity(Exception):
        ...

    class Empty(Exception):
        ...


@pytest.fixture(scope="function")
def stack():
    stack: Stack = Stack(2)
    yield stack


class TestStack:

    def test_if_newly_created_stack_is_empty(self, stack):
        assert stack.is_empty() is True
        assert stack.get_size() == 0

    def test_after_one_push_stack_size_should_be_one(self, stack):
        stack.push(1)
        assert stack.get_size() == 1
        assert stack.is_empty() is False

    def test_after_one_push_and_one_pop_stack_should_be_empty(self, stack):
        stack.push(1)
        stack.pop()
        assert stack.get_size() == 0

    def test_when_pushed_past_limit_stack_over_flow(self, stack):
        stack.push(1)
        stack.push(1)
        try:
            stack.push(1)
        except Stack.Overflow:
            ...
        else:
            assert 1 == 0

    def test_when_empty_stack_is_popped_show_throw_under_flow(self, stack):
        try:
            stack.pop()
        except Stack.Underflow:
            ...
        else:
            assert 1 == 0

    def test_when_one_is_pushed_one_is_popped(self, stack):
        stack.push(1)
        assert stack.pop() == 1

    def test_when_one_two_is_pushed_two_one_is_popped(self, stack):
        stack.push(1)
        stack.push(2)
        assert stack.pop() == 2
        assert stack.pop() == 1

    def test_when_create_a_stack_with_negative_size_throw_illegal_capacity(self):
        try:
            stack: Stack = Stack(-1)
        except Stack.IllegalCapacity:
            ...
        else:
            assert 1 == 0

    def test_when_one_is_pushed_one_is_top(self, stack):
        stack.push(1)
        assert stack.top() == 1

    def test_when_stack_is_empty_top_throws_empty(self, stack):
        try:
            stack.top()
        except stack.Empty:
            ...
        else:
            assert 1 == 0

    def test_give_stack_with_one_two_pushed_find_one_two(self, stack):
        stack.push(1)
        stack.push(2)
        assert stack.find(1) == 1
        assert stack.find(2) == 0

    def test_give_stack_with_no_two_find_two_should_null(self, stack):
        stack.push(1)
        assert stack.find(2) is None

```

## 5.Form

### comments
### coding standards
1. every team should have a coding standard
2. coding standard shouldn't be written in a separated document
3. it should be clearly visible inside a code itself
4. when we comment on every thing, it cuz us to ignore them
5. comments should be **rare**
6. comments should be reserved for spacial cases when programmers' attention is really needed
7. and every programmer that reads them should be grateful and releave
8. [The Elements of Programming Style](*https://www.amazon.com/Elements-Programming-Style-2nd/dp/0070342075)
  - **documentation chapter 8**
  - the best document for a program is a clean structure
  - it also helps if the code is well formatted, with good mnemonic identifiers and labels (if any are needed)
  - and smattering of enlightening comments. Flow charts and program descriptions are secondary importance;
  - the only reliable documentation of a computer program is the code itself
  - the reason is simple whenever there are multiple presentations of a program 
  - the change for discrepancy exists
  - if the code is in error, artistic flow charts and detailed comments are to no avail
  - only by reading the code can the programmer know for sure what the program does
### comments are failure 
1. it should be the goal of every programmer to
2. write code that expresses its intense so well that it doesn't need comments
3. modern languages are remarkably expressive
4. we have a bunch of interesting syntax elements that we can use
   - classes, nested classes, namespace, enums, limitless names
5. every comment you write is failure to express your self well in code
### Comments are liar
1. it's very difficult for comment to remind trustfully for a length of time
2. over time comments degrade into disinformation 
3. comments don't rat because of lazy programmers
4. comments rat because they tent to be none local
### Good comments
1. not all comments are bas sometimes comments can be useful sometime they become required
2. legal comments
3. informative comments
   - for example, comments that explain some horrible regular expiration
4. clarifications ande explanation of intent
   - when you must write a comment to explain your intent, you failed 
     - of course, in those situation best is to not leave a code unexplained 
5. warnings of a consequence 
6. TODO comments
   - LOL XD
7. public api documentation 
   - best api documentation is the documentation that you don't have to write
### Bad comments
1. Mumbling
   - don't talk to your self in the comment of code
     - don't write about the lyrics of the song you are listening to ot your life situation
     - or they write a system bad way
2. Redundant explanation
   - make sure when write comment add something new
   - DRY don't repeat your self
3. Mandated Redundancy
   - if you see a comment that is wrong or miss leading, either fix it or remove it
4. jornal comments
   - you have source code control then use it
5. Big banner comments
   - position markers and big banner comments 
   - it is a great way to make sure that the world inside it never read
   - nothing shout ignore me more than a big banner comment
6. closing brace comments
7. Attribution comments
8. HTML in Comments
9. None Local Information
   - comments that talk about part of code that are far away wit rat a rat quickly
10. Commented Code (immediately remove it)
### Explanatory Structure
1. rater than use comments to describe what code dose learns how to use explanatory variables and names
### Formatting
1. White-space discipline is importance
2. white-space care's information
3. we should use it with the same level of care as any other structure in our source code 
4. when someone first looks at our code, we want them to be impressed by the attention to detail
5. stricken by how order is it convinced by professional at work
6. the very first think they see at our code is formatting
7. formatting is about communication, and communication is the first order of business for every other programmer
8. **getting your code to communicate is even more important to getting your code to work
### File Size
1. project size and file size are not related to each other
2. file length and project size are not related
3. perhaps file size is correlated to project size
4. we all have seen large files that become dumping ground for stuf that we haven't taken in the time to organize properly
5. as every think in software smaller is better
6. **keep your file sizes small**
### Vertical Formatting
1. use blink lines to separate things that should be separated like methods 
2. be disciplined in your use of blank spaces
3. decide how many lines should be used to separate method from each other and stick to that decision
4. personally i sue 1 one between methods
5. 1 line to separate methods from variables 
6. if there is more than one kind of variables like public const and private, I use blank line between them too
7. inside a function I will use a blank line to separate variable decoration from the rest of executable code 
8. I put blank line between statements and while loops separating them from code follows 
9. of course, if you keep your functions small, you don't need them as much
10. variables that have infinity for each other should be grouped together
11. if the variables are used together, group them together without blank line
12. things that are related to each other should be vertically closed to each other
13. the distance between then shows how closely related to each either they are 
14. things were not related to each other should be vertically apart
### Horizontal Formatting
how long should the line of code be?
1. you are never to scroll write to see
2. we don't like lines that are longer than 80 character
3. lines should be less than 100-120 lines
### Indentation
the code that came out-of-team should look like team wrote it,
I should be able to tell who wrote the code 
### Classes
what is a class ?!
you write class by writing a private variables
then you manipulate those variables by public functions
so from outside looking in class looks to have no variables at all, 
just a bag of functions
so from outside looking in class has no variables
since an object is an instance of a variable ,it's also true that the object appears to have no variables
to say this difficulty, from outside looking in an object have no observable state.
object to this observation ,by pointing out most classes have getters and setters
or in some languages mutable properties, 
so let me respond to this objection
if you take private variables of your class and expose them throw getters and setters , then you got a bad design
after all why you should make your variables private and then just expose them throw a setters and getters
remember the discipline of tell dont ask 
if a object has no observable state, also its easy to the object to do something 
it doesn't make lots of sense to ask any thing 
object that follows tell dont ask doesnt have much of getters 
and if doesn't have many getters there is not much point in have any setter either 
method of class manipulate variable of class 
the more variables that a class method manipulate the more cohesive that method is
a maximally cohesive method manipuldate every variable in the class 
a maximally cohesive class is composed of nothing, both maximally cohesive method 
getters and setters are not very cohesive because they only manipulate single variable each 
the more getters and setter a class has the less cohesive a class is,
so that doesn't mean the class shouldn't have getters and setters?
dog matter rules like this sell them apply in engineering discipline
I personally write setters and getters from time to time,  
but I try to minimize them because I try to maximize cohesion
in those instances that is chose to have getter I don't simply expose a variable

I try to abstract the information been retrieved 
let me show you what is mean 
```
class Car:
    galone_of_gas: int
```
what should we call getter?
```
class Car:
    galone_of_gas: int
    def get_gallon_of_gas:
        return self.galone_of_gas
```
that expose an awful amount of information of implementation in our class 
user from class can inform that there is a variable that holds the gallon of gas
there is a number of problems for being specefic
```
class Diesele(Car):
    def get_gallon_of_gas
    
```
let's say we wanted to derivative a car diesel car
of course it will inherent method get gallon of gas 
but that is not quit write a disease car don't run on gasolin
```
class ElectricCar(Car):
    def get_gallon_of_gas
```
we have method get gallon of gas in a base that derivative of electric car just dosn't fit 
when derivative doesn't fit with a base, something is wrong with a base
often because base exposes some implementation that shouldn't have,
for example, instead of creating a gallon of gas,  
we could use method get percent fueling
```
class Car:
    def get_percent_fuling():
        ...
```
this method will work just as fine as an electric car or diesel car 
can you smell polymorphism coming 
that's advantage of hiding your implementation, 
the less implementation you expose, the more uppercutting you have to make polymorphism 
that class with get gasoline method could not be polymorphism to an electric car and nuclear car
- poly
