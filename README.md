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
    * [Comments](#comments)
    * [Structure](#formatting)
    * [Classes](#classes)
    * [Data Structure](#data-structure)
    * [Boundaries](#boundaries)
- [TDD](#6test-driven-development-part-a)
    * [The Three Laws of TDD](#the-three-laws-of-tdd)
    * [Red, Green, Refactor](#red-green-refactor)
    * [Objections](#objections)
---

## What is this?

Hello 👋

this repository is a summary of the collection of robert c martin books
and python examples to make it more understandably 
(clean code, clean coder , clean architect, clean agile)

**Few important notes about it:**

1. It's derived from many years of experience & many projects, both big & small.
2. It's pragmatic. All things mentioned here are things tested in production.

**SomeThing important that I forgot**


## 1.Clean Code
for such ambition we need the right skill,and as developers we code,
so let's sharpen those skills and start coding a better world together

1.OH, NO!
2.Angry face
1.I MADE MASS OF THE CODE
TRASH
2.HOW WE CAN FIX THIS?!
CHOAS
ROBISH
ROBERT C MARTIN INTRO
TO IS ONE CLEAN CODING AND CLEAN ARCHITECTURE AND HWO CAN TEACH US BETTER THAN
mr clean code aka uncle bob the one and only robert c martin

founders of agile manifesto, software craftsman ship, solid, ...

hi I am bob (no iam not XD I am aref), and by the way, 
thanks to every body who brought me hear that awfully nice of you(tanks to an association team)

How many of you are programmers
I don't care if you are young or old or black or white or a man or woman,
I don't care if you are a programmer you are part of my trial

you and I share a passion for something,
and we can communicate about it in a way that most of the people can't

so lets talk about clean code
[clean code book picture]
today talk is clean code , (30min session) so we are able to cover a little bit of ground here
[the only measurement of clean code meme wtf per second]
how are gone make our code good enough to service a codereview 
such that our pears are not tearing out their hair figure out what our code does
why is this important

### Craftsmanship
[
    - acknowledgment
        . i can teach you a physics of bicycle
    - work
        . but learn to ride will take work
]
how many computers are in this room
100 good answer 
how many computers do you have on your body 
I can start count by me / I have my iphone, how many processors are in here
main-processor screen processor wifi processor and the gps processor, and bluetooth processor and...
i am holding in my hand in the mount of computing executing power that exed the computing power of hole world in 1980
which is very interesting and you know we all have one and what we do with it we play angry birds
which if you think about it is very cool
{
    that 's more processor with me i have airpods how many processor i in this, at least tree
    look around you how many computer are in the wall or ciling
    (look around and show stuff)
}
how often do you interact with software 
not you how often does your ground ma interact with software
in our society today it is impossible to go 60 seconds with out interacting with software system 
you cant talk on phone you cat watch tv you cant microwave , you can't wash the dishes or your close, 
{
    you cant drive, how many code in modern car, not a tesla just normal old modern car car : over 100 million
    when you press break do you blive a cable from pedal to the disk
    or do you realize there is a if statement
    and who wrote those if statement
    if statement that decide whether or not car stop when you push on the break
    how many people died for faille in that statement
    1000
    you and i are killing people
    most of us walk in into store and see foolish computer and type five line to print our name in a  loop
    and when we saw it we screamed [really scream] yeeee that's what i want to do for the rest of my life
    but now we are killing people
}
our society runs on software nothing happens in pour society with out software
you cannot by anything , you cannot sell anything , you cant get insurance , you cant get money out of bank
software runs everything
and our society does not realize, just how dependent it is

and who white that software ... We Do
we rule the world

other people think they rule the world, but they hand it to us, 
we write the rules that run in machine that govern every thing

the event that actually causes society to wake up is some poor programmers do one foolish thing and kill 10000 people in shop
whey they point at us and ask how you let this happen, and if that answer is "my boss told us it should be done by monday
then politicians will shame, and they will regulate us, they tell what language should use and what platform should we use, 
what course we have to take and what book we have to read, what process we have to follow , what signature we have to get 
and we become civil server

I would like to avoide this , so how do you avoide it 
you get there first by establishing the ethics of software development , 
what is our ethic do we have sated set of ethics , do we have set of standards that all programmers follow
do programmers oath to set of standards, we don't have that we don't have a profession because of that 
because to have a professional you must have something that you profess,
and we don't profess anything at the time , we have to come up with this, we have to learn to adopt a set of standards so when that politicians of 
world point at us, and they will , and ask how you let this happen we can respond by saying 
"look this was horrible accident, and we regret that, but it was not dude to happen, but it wasn't do to own negligence"
and when politicians of the world decide to regulate us they know how to do it because they will simply take the rules that we 
already invented , and bring them into law .
this is what happened to doctors, what happened to lawyers , architect ...


and so we start to think what our ethic is, what do we value.
and one of those better is the clean code, 
so let's talk about that ...


### Bad Code

[
A Fragile premise?

"Good code matters."
Kent Beck
]
does any of you heard about kent beck
do a little bit research on kent beck, he is one of the leaders in the field

he wrote a book a long time age "implementation patterns"
and in that book he said that the book was base on the fragile premise
and fragile premis was a good code matter
when i read that in his book i scrached and i tought why kent beck has said that was fragile premise
it seems to me a rook solide promise, yes code code matters and matter for a good bunch of powerfull  resons

so for exxample why are we so slow 
### why are proggramers so slow 
how hwo here has worked on green field project 
a project where is no code
how fast can you go , those few days. where there is no code
and someone come to you and say can you get that feature done
and you say 
[yessss , puusususu, you start witing code pewwwww , code pures out every pecific of your body ]
and you get thet feature working ,
and every body say wow you get that working fast . it only toke you few days
[yeee we are programmers]
can you do it againe 
[yes, pewwwwwwww]
come backe to yoiur team later 
can you get a fuature working for us
[oh tricker probbably gone take six month]
you use to do that in a copple of days
[ye but you don't know, how messy this system has become, if we even touch oneline of code oh hell could break loss]
why that happend

this is what happend to software teams theyt start fast ,
they start out with a beutifull design and they start out lovely
and fast and they write features and every things working great
but they make a mass, because they wanna go fast, and as they make a mass 
and as the mass builds the team get slower and slower until they bottom out at they 1% of theire original productivity
and what do you gone do about this , lets say you are manager right ,
you got this team and this team is working on a software for a two years now
and they cant get anything done, no feaure can't get done in less than few month and even than it's going to be late
and it wont work , you know the real world for a manegers what you gone do
 
you made promisses to people , you set planes out there there is people expecting featurs and team canot deliver those 
features , what you gone do as a manager. waht would youir option be,
you gotte go fast somehow , add more people , every one know yoiu go twice as fast if you double a crew
and you are laghing , why you are laghing cuse you know this is none sense 
you can't go faster bye doubling the staff. adding more people doesnot make you go faster 
what does it do the moment you deside to add new people to team what happen
it slows down, cuz the new people suck life out of old people 
for month , now you are hoppong those new people usually get smart after a while and the productivity will rise
but there is a onother refacts that kicks in who is training the new people 
the people who made the mass in the first place , and in factthat is not old people that are training
this is the old code that traine new people , the new people  trown at the fier and they have gotte make some sense out of 
the system they read old code they say to them selfe , oh i see how thong are done around here ,
they emulated ofcourse and just continio to make problem worse
and the code gets messier and messier no matther how many people you add to the team and
nothing you do can't make that productivity rise, 
thats why programers are slow...

slow because they make a mass, if they didin't make a mass they will be fast
if yoiu could keep the code clean , it wouln't be a mass
you could add new feature in reasonable amont of time 
just as long as you could continio keep the code odered and clean

### strategy
we are are going to talk about nummber of strategy
but i wanna to impress that point on you prety throuly 
we go slow because we make masses, why make masses
waht drive us to make mass the first place 
the desier to go fast
we make mass be cause we think i have to get done quickly , they ecpecting me get a lot of stuff
done i gotte get it done.. oh worked

    - how many of you done this?
it's hard to get code to work, and you try to make it work and try things setting with your debugger and 
steping into trial and error to make it work and then sundenly it works [don't any body breath]
move care fully and check it in , that s wrong thing to do
if fact that you got in working is that only hve to do job , once the codeworks 
that's when you have to clean it 
    
    - no one writes clean code first time nobody

just it's to hard to get the code work
so one the code works, it will be a mass 

how much do you invest in cleaning
roughlly the same time took you to write it

and thats the problem no body wants to put that efford in
cause they think they are done once the code works
you are done when its right 
(first make it work, then make it right, then better, faster, efficent,..)

and if you adobt that aditute , then the code will stay clean
and you never go throw slow down
[
    - the only way to go fast is to go well
]

### what is clean code
 who knows who this guy is?
[
    "
        i like my code to be
        elegant and efficent 
        ...
        clean code does one thing well
    "
    Bjarne stroustrup
]
 yarnes strustrip
c++ he made a language cpp  
and this one "thing", has been in software for 40 years or more people always writing about function should do one thing
is a very very old idea , but what does one thing mean, it's linda like subjective meature
what does it mean for a function to do one thing . i thing i know the answer to this and i will tell you little bit
later, i have completly objective way to meature one thing
and if you would hear to that objective way , transforms the structure of your code remarkably

[
    "
        Clean Code is simple and direct.
        clean codes read like a well written prose...
    "   
    Gready Booch
] 
 
the cheaf scientist at rational he wrote book in 1988 called objrdt orented software design
gready booch was also first person that i belived to have the title cheef scientist ,
i think he invented that. and ever since every body wanted to be cheef scintist

        clean codes read like a well written prose...

have you ever read code?
that read like well written prose
what is that mean well written prose
i think i can show you what that means

[
    "
        clean code always looklike it was written by someone who cares
    "
    Micheal Feaders
]
what a lovely statement
tahts a good aditute
when was the last time you read a module and your tought as you reading that module the authure cared about me
the authur cared about every body who read code
when was the last time you had that exprience
the authur of this code cared about me

and by the way bring the fastinating point 
what is your job?
you may think that your job is to get the code to work , that's not your job
thats only haf of your job and that least imortant part half your job
the more importante part of your job is that you must write code that other people can mentaine
and use and make work, if you hand me code that works perfectly but i can't undrestand it
then as soon as the requirments came that code is useless
on the other hand if you give me a code that does not work but i undrestand it , 
i can make it work
it is much more imprtante that your pears to be able to undrestand a code than the computer can undrestand a code
it is more importante to comminucate with your pears using a programming languegs that it is to comminucate the computer
because if you do that well. somebody will make that work

[
    "
        you know you are working on a clean code
        when each routine you read turn out
        to be pretty much what you expect
    "
    warn cunningham
]

when was the last time you read code and as you reding it , 
it was pretty much what you expected














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
    __galone_of_gas: int
```
what should we call getter?
```
class Car:
    __galone_of_gas: int
    def get_gallon_of_gas:
        return self.__galone_of_gas
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

 polymorphism is a key to independently deploy ability and plugin structure

polymorphism allows us to protect client code like a car driver from changes to implementation of server code

like car, it's pretty easy to write a car driver that can ride any derivative car without knowing or caring what that derivative is
from outside looking in class is nothing but a set of methods, those methods may operate on a data,
but you know nothing about how that data is implemented
these methods are not setters and getters they hide the data they don't expose it 
if they must expose some data they do in the most abstract way possible
```
                     ┌───────────────────────┐
┌────────────┐       │  Car                  │
│            │       ├───────────────────────┤
│ Car Driver ├─────► │ - galon_of_gas        │
│            │       ├───────────────────────┤
└────────────┘       │ + get_percent_fuel()  │
                     └───────────▲───────────┘
                                 ▲
                                 │
                  ┌──────────────┴────────────┐
                  │                           │
          ┌───────┴────────┐         ┌────────┴──────┐
          │                │         │               │
          │  Electric Car  │         │  Nuclier Car  │
          │                │         │               │
          └────────────────┘         └───────────────┘
```
maybe you are wondering about class employe
that clearly has methods like get name and get address that expose data within them
what do you think different between class and data structure

### Data Structure

data structure is an opposite of a class, data structure has a hole bunch of data variables that are public and vitually no functions

```
class DataStructure
    valiables: any
```
classes have a private method but public method 
data structure has a public method but no variables

data methods can have methods but typically are simple methods like getters or setters or little navigation aids
the method of data structure manipulate individual variables
they don't manipulate cohesive of groups of variables the way of methods of class do
the method of data structure expose implementation they don't hide it they don't abstract it

you can't tell data structure to do anything all you can do is to ask a question

the software that manipulates data structure is the anti scent of tell don't ask

dou can tell an object to do something generic like print itself on a screen,
and it will do it automatically do a thing appropriate to it type it will polymorphic dispatch to appropriate  method,
but you can't ask a data structure to do anything generic, 
the only thing that you can do to ask it very specific question 
if you want to print an on a data structure on screen then you have to ask for its type then this patch to approprite function your self
probably with a with statement
and so fata structure and switch statements are related in the same way that class to polymorphism related
datastructure and switch statements offer protection same way the objects do they area is different type op protection

***object protects you from new type***

switch state magnets expose us to changes in type
when a new type is ever added,all the switch statements have to be modified
and all the client code is impacted by breaking independent deploy ability
but objects are not immune to all type of changes , 
 what happened when you add a method to base class 
when you do that all the clients of the basement are effected and all the derivatives of base class are effected
the all have to be recompiled and redeployed
when you add a method to a baseclass you break in dependent deploy ability
```
def print_employe(e: Employe):
    if e.type == Hourly:
        print_hourly_employe(e)
    if e.type == Salaried:
        print_salary_employe(e)
```
data structure and switch statements on the other hand are immune to the new function 
when you add new function all you need is to add new switch 
```
def delete_employe(e: Employe):
    if e.type == Hourly:
        delete_hourly_employe(e)
    if e.type == Salaried:
        delete_salary_employe(e)
```

for example, I have a set of data structures that represent a set of shapes
(Circle, Square, Triangle, Rectangle)
and let's also say I have a set of functions that operate on those data structures by taking a list of them
so I got function draw all shapes that iterate throw a list of shapes and draw them all,  
we got a noting function call erase all shapes and rotate and ...
if you look inside all those functions, there is switch state statements selection among all of them
```
               ┌──────►
┌──────┐       │        ┌───────┐
│ draw ├────┬──┼───────►│Circle │
└──────┘    ├──┼───┼──► └───────┘
            │  │   │
┌────────┐  │  ├──►│    ┌───────┐
│ delete ├──┤  │   ├───►│Square │
└────────┘  ├──┼───┼──► └───────┘
            │  │   │
┌────────┐  │  ├───►    ┌─────────┐
│ rotate ├──┼──┤   ┌───►│Rectangle│
└────────┘  ├──┼───┼──► └─────────┘
            │  │   │
            │  │   │    ┌────────┐
            │  │   ├───►│Triangle│
            └──┼───┴──► └────────┘
               │
               └───────►
```
if we add a new function to rotate all shapes, of course, you expect to have a switch statements,
but it wouldn't have an effect on any existing adata structure
**So adding a new function to data structure in switch statements does not break independent deploy ability**

- classes protect us from a new type but expose us to new method
- data structures protect us against new method but expose us to a new type

### Boundaries
1. separate main from the rest of the application
2. split things is two partitions with main one side and the application on the other 
3. all the source code dependencies should cross that boundary in going in one direction away from main toward the application
4. this makes a main a plug to the rest of the application
5. app is a crisscross, other boundaries are views/models, database/domain object
6. for each boundary, one side is concreate, one side is abstract
7. for example, main is concreate the rest of the app is abstract from a main point of view 
8. source code dependency point from concrete to abstract C -> A , database -> Domain object
9. database depend on domain but domain does not depend on database
10. Application, Domain <- database interface layer (orm) -> Database
11. oo invert dependency not dataflow that means application can still call database layer, although it doesn't know database layer exist

### The Impedance Mismatch
1. data structure mappers are tool for taking datastructure from db and moving it to memory
2. when you get a bunch of business rules into a domain object, then you get classes that don't look every much like a database table or schema
3. specific application may desire different schema
4. on the application side of the boundary we can separate owr self from schema by actually designing objects we like to use
5. this would be a true object with exposed methods and hidden data
6. rather than manipulating table rows, we manipulate business objects
7. it's the responsibility of the database layer to convert back and ford between datastructure that lives in database and business object that the application wants to use
8. that means on the application side of boundaries we would like to set of interface that declare data access s method
9. we like to user business objects use those interfaces to access data they need
10. one other side of the boundary we like a set of classes that drives from those interfaces and impliment data access by integrating data structures that have been fetched from a database
11. we can use orm tool to fetch those datastructure out of a database

## 6.Test Driven Development Part A

### Fear and Code Rot 
1. every code gets rot after a while into chaos
2. we don't clean it because we scare to break it
3. because you know if you touch it, you break it, and if you break it will become yours

### Eliminating Fear

### Demonstration
Test eliminates the fear of cleaning a code

### The Real World
maybe you are thinking this is all in well and good for an open source where all the developers work for Free, 
but in a real world the sweet of test like this it just is too expensive and time-consuming to create
1. test saves a massive amount of time, and they have been here from day one
2. we can develop it faster and safer than any project
3. there are few defects we debug less, we code faster, we code better

### *****The Three Laws of TDD*****
test-driven development is a discipline, 
and as a discipline it has a set of rules abandoning those rules and write a test when ever you feel like it 
is not disiple and does not make you a test-driven discipline

1. ***write No production code except to pass a failing test***
2. ***write only Enough of a test to demonstrate a failure***
3. ***write only Enough production code to pass the test***

### Debugging time
imagen a group of developers following these three laws no matter who no matter when sometime in last mint or so
 everything they worked on is executed and pass 
- increase in productivity must lead to less debugging skill

### Design Documents
have you ever integrated third party package , somehow another gave you a nice zip file when you pack it 
you all the software you may also get a pdf, it would be a please manual written by tech rider 
at the end of that manuel there is a ugly section of appendixes where all the code examples are
where do you go first
you go to code example because you want to see the trues
you want to go to code ande see what really is going on 

those unit tests you are writing are a code example fore hole system.

you want to create an object there is a unit test that creates that object every why that can be created
you want to know how to call some api there are some unite tests that call all the unit every way that its possible
test are low level design documents they remain in language that you understand their author unambiguous
they are so formal that they execute, and they can't get out of sync without execute application

the cost of documentation is always high, and the reliability has been wolfy an adequate

### Decoupling
when you write your test code first, you have to design a production code to be accessible from the test

since you have not written that production code yet test has tremendous influence on the design of production code yet
and that influences make a production code test able

- writing test first makes production code testable

another word for testable is decoupled
shortly it will help to have better design

### courage to chane
the test stops the code from roting

why design and architecture considered to be so important 
it's because we want the structure of the system to be
1. flexable 
2. maintainable 
3. scalable

when we add new feature, we want to make sure that the structure of the system is flexable enough to allow
those changes without breaking every thing, but nothing makes a system more flexable than sweet of test
because that test eliminates the test
a perfectly designed system with no test you are afraid to clean it and improve it 

***if you wanna a flexable system, get a flexable system that you trust

### Trust
I want you
to think of testing a purchase that you want to use to jump out of airplane that how much you need to trust them

so how do you get a swit of test that you trust with your life?'
follow the three laws

if you write your test after a facts then you never trust that test you always worried that there is a hole in it
this is because testing after a facts is boring you already know that work because you test it manually
writing a test after facts is a residual milestone it's not a necessary part of your code to work,
so it feels like west and that means that you have gone take shortcut with your purchase
there are some portions of code that are difficult to write at for , you test them manually so know them work
therefore you don't feel it to write a unit test
and so your test sweet has hole

### Conclusion
those three laws of TDD may have sounded pretty foolish at first, but nothing has  more profound 
on the way software works since the invention of screen editor, 
those three laws change the way you work on mint by mint bases
and that change result in much less debugging ,reliable low level documentation decoupled design 
and the courage to change and clean code.
nothing I have found more reliably prevented and reversed code rot
than the three laws of test driven develop ment


## 6.Test Driven Development Part B

### Red, Green, Refactor
#### Bowling game
```
import pytest


class Game:
    def __init__(self):
        self.__rolls: list[int] = list()

    def roll(self, pins: int) -> None:
        self.__rolls.append(pins)

    def score(self) -> int:
        score: int = 0
        first_in_frame = 0
        for frame in range(10):
            if self.__is_strike(first_in_frame):
                score += 10 + self.__next_two_ball_for_strike(first_in_frame)
                first_in_frame += 1
            elif self.__is_spare(first_in_frame):  # spare
                score += 10 + self.__next_ball_for_spare(first_in_frame)
                first_in_frame += 2
            else:
                score += self.__two_ball_in_frame(first_in_frame)
                first_in_frame += 2
        return score

    def __two_ball_in_frame(self, first_in_frame):
        return self.__rolls[first_in_frame] + self.__rolls[first_in_frame + 1]

    def __next_ball_for_spare(self, first_in_frame):
        return self.__rolls[first_in_frame + 2]

    def __next_two_ball_for_strike(self, first_in_frame):
        return self.__rolls[first_in_frame + 1] + self.__rolls[first_in_frame + 2]

    def __is_spare(self, first_in_frame) -> bool:
        return self.__rolls[first_in_frame] + self.__rolls[first_in_frame + 1] == 10

    def __is_strike(self, first_in_frame) -> bool:
        return self.__rolls[first_in_frame] == 10


@pytest.fixture(scope="function")
def g() -> Game:
    g: Game = Game()
    yield g


class TestBowling:

    def roll_many(self, n: int, pins: int, game):
        for _ in range(n):
            game.roll(pins)

    def roll_spare(self, g):
        g.roll(5)
        g.roll(5)

    def roll_strike(self, g):
        g.roll(10)

    def test_gutter_game(self, g):
        self.roll_many(20, 0, g)
        assert g.score() == 0

    def test_all_ones(self, g):
        self.roll_many(20, 1, g)
        assert g.score() == 20

    def test_one_spare(self, g):
        self.roll_spare(g)
        g.roll(3)
        self.roll_many(17, 0, g)
        assert g.score() == 16

    def test_one_strike(self, g):
        self.roll_strike(g)
        g.roll(3)
        g.roll(4)
        self.roll_many(16, 0, g)
        assert g.score() == 24

    def test_perfect_game(self, g):
        self.roll_many(12, 10, g)
        assert g.score() == 300
```
- when you write a real code, you write the simplest real code

### Objections
1. test is code by following tdd you write much more code than normal, then it must slow you down?
    - tdd makes you drive fast, first of all you spend less lot time debugging
    - tdd allows you to clean your code so don't need constantly dealing with every body mass
2. there are managers who either throw ignorance or disagreements they never allow their programmers to practice tdd?
    - but why have your boss should to know
    - do you ask your boss to use semicolon or indent if statement 
    - when is the last time your asked your boss if you can go to the bathroom?
    - tdd is personal practice permission is not required
3. still they will object!!!
    - tell him you are doing it in order to go faster
    - if he objects tell him, you have to double all you estimate
    - if he objects more, tell him mining his own business
    - after all, you are a software developer
4. is that refactor rework isn't better to write code current the first time?
    - every created on a planet is iterative
    - programmers don't write prefect code first time either
5. who test the tests?
    - we have to stream of code the test and the production code 
    - and the test, tests the production code
    - but the production code tests the tests
6. a single change in production code can cause many hundreds of tests to break, perhaps maintaining all those tests is to expensive
    - if only they are poorly designed
    - design your test well and if you discover better design refactor your test
    - tests are as important as prediction code even they are more important
    - thread them the same way you thread your production don't allow them to be mass
    - if a single change in production causes a hole bunch of tests to break, your test is to couple to production
    - so find a way like abstraction or some other way to decouple your test
7.  test can prove the presence of a bug but cannot prove the absence of a bug 
    - our goal is to create purchase to eliminate the fear of change we will never achieve 100% certainty, but 99 is pretty damn good
8. to gain sweet of test, it is tested that matter not when we write them
    - if you write your test at the end, they are not going to be complete
    - humans consider things that come first to be more important
    - whe n you write those tests first you trust those tests
    - test is important than production because that makes production flexable
    - without the test production code rot
    - 
9. there is a vast amount of code, and it does not have test what we do about that
    - (working effectively with legacy code, michel feather) define legacy as a code without test
    - it is hard to get legacy code tested because it is not designed to be testable
    - in order to test, you have to make a series of small decoupling design changes
    - but without the test, you have no way to tell if your design breaks it every thing
    - in order to test, you must refactor but without test you cannot refactor
    
    - find some small par ot legacy code that you can test without making big changes
    - then use those tests to extend the design changes more safely
    - I don't trust big refactoring or test projects
    - instead, I waited till a new feature was needed in some part of legacy code 
    - and then will change a little bit of design and add a few tests in the effected area
    - month by month, year by year, slow and gradual prices will eventually spread test throughout the bulk of legacy code
    - there is some part of legacy that you never get tested, but an important part will get tested 
    - and also all new code you write test first
    - and in this situation that you have the option either to modify older code or write a new module write new module so can write it test fist
    - always prefer test first
10. how then do you test databases 
    - you don't, databases are black boxes that you usually do not test
    - what you usually test is that your schema and quires work as planned 
    - the first step is to separate the application from the database using the layering technique 
    - then you can test the database independently of the application
    - you can test generated query behave properly by loading database with a minimum number of rows and then execute those quires 
11. some programmers complain that testing is not part of those programming descriptions
    - they need to grow up
12. some programmers suggest that tdd is too hard
    - would they want cheese with their wine?

### Discipline and Professionalism
### Double Entry Book keeping 
software is a sensitive discipline bye that I mean that there are single bits with in a binary
of an application that if set a  wrong way will crash the system hart
 you can go to a bridge or over pass and start to remove bolts that bridge probably won't fall down write away, 
but I can reach into an application and flip one little bit and crash it

### QA Should find Nothing

### 100% code coverage
probably you could not realisticly cover 100% of you code but that doesnt mean you should exept a less tahn goal
the fact that you cant get obtaine it doesn't  mean you shouldn't push as harder to get possible through

### Conclution
1. code rots because we afride to clean it
2. to geep a system clean we must aliminate the fear of change
3. only a sweet of test that you trust with your life can eliminte that fear


## 7.Architecture
architecture is disciplin of laying down the fundation of an entier software system
it is composed of higher level decision , decision that must made first,
decision that must servive the life time of architecture,

architecure is not just a foundation, it's hole anglada ,
architechure include grand shape of system and tinyest low level design,
it include the most abstract of moudle interface ande most concreate of method implementation,

programers are all architectes in one form or other
architecure don't code are not architecture at all

waht architecure is and what architecture dose 
the taht system take in order to meet the use case and inorder to stay flexable and maintainable

mvc is low level user interface partitioning
but is not a particulaly good high level application partitioning is desn't split a system in a right way
jcobson parttioning boundry control entiti partitioning taht split the app;ication architeture more nicely
and can be used with mvc to make a very good sysytem structure

we studied the horor disis of freamwok bounding and we will find ways to tread and cure this frightfull courage

### What is Architecture
architecture is not about tools and building matterials , architecture is about usage 

### Architecture expose usage
the architecture of library o church screams at you that this is church or a library

a good architecture whether it is a architecture aof building or the architecture of software
it is all about how a system been usend , a good architecture scream the usecase
when you  look at the software system and all you can see is the mvc structure of a web system
then the architecture of that system is hiding it's use cases ans exposing the deliviry mechanism
we don't wanna see the delivery mechanism we wanna see the use cases 
1. we don't want the use cases coupled to the delivery.
2. we want the seperation be so strong tha they can be deployed independently from each other
3. we don't want the use case know anything about delivery mechanism 
4. we want decission about the UI DB Framework Tools the Service layer be compleatly independet from usecase

### Deferring Decisions
decision about ui databases framework and service layers can and should be deferred 
thats one of primary goal of good architecture .
a good architecture know how to keep options open for as long as possible.
a good architecture maximise the number of decision not made.

### separation of value
so what if the entier value of the system is actually in user interface.
all the bussines value ,is really in the way the system is delivered in and not the way system does.
simple crud system and reall business value is in how that crud is delivered

should the architecture of UI heavy system should be about it's usecases  or should it be about UI
that's a wrong question to ask
the real question is sens the UI is so critical should it be coupled to the rest of application
and the answer to that is clearly not
if the UI is critical we dont want its architecture poluted by the concern of rest of application
another way to look atthis is the separation of bussines value
consider for a moment just the use-cases and the UI 
let's say we seperated this two  in the in dependently deployable and independently developl component
such that ui is a plugin to the use-case     UI -> use-case
let's say the estimate for the use-cases is 50k$ but the estimate dot developing UI is 150k$

now the bussines can compare this two values and ask it self a very intresting question
why is the ui much more expensive and should that be the case 
maybe the ui shouln't be more expensive than use-cases
maybe there is lesss expnsive way to do ui
now it's possible that bussines would look at those numbers and decide ui is so critical that they don't mind at all
that it cost threee times what the use-case cost
and the other hand they may lookat horor those numbers and quickly get back to more appropriate size ui
the pointa is with out that seperation there is no way for thebussines to tell cost of ui or the cust of use cases
have the appropreate ratioa 
seperating usecae from ui alows the bussines to meture the cost of each ans hnd that cost to the coresponding bissines value
and this is not limmited just to ui hole system component can be  isolated this way the database the web the frameworks

### conlution

### use-case
if i showed the sofware architecture of an accountin system dilevered over the web 
what is the first thing that would you know about that system???

the fact that this is accounting system is a far more importent than the fact that this is a web system
most we systems do exacly opposit of this they scream web at you

is mvc the views in the controller are strongly we related the models are completly subservient to the controllers
ant the views in the controller are so titly coupled to the models ,
that they have termendes influence over the structure of those models.
many developers miss takely belive that models are object that represent bussinet rules
such athat system makes the web central orgonise system and regent bussiness rules to enoing details.
it is the web that is the detail

you should be able to easyli change the delivery mechanisem
without changing the architecture of the system

given the two version of sme system on delivered on web and one delivered over the consol app

we describe how user inter act whit the system without using web related worlds 
instesd we use word in concept that don't imply the delively mechanisem
json called this interactor descriptions Use Case
ivar jacobson idea was that the development of an application should be deriven by the delivery in dependent usecase
in other words is the use-cases that form the central orgonising prensiples
and the abstraction around which the system is build

when you look at at the architecture of use case driven system you see the use cases not the delivery mecahnisem
what use see is the intent if the system

### Use Cases
use case is  formal decription if how a user intereacts with a system in order to achive specefic goal

for example goal is to create a order with in a order proccessing system

CREATE ORDER
Data:
customer id
customer contact info
shipment destination
shipment mechanism
payment information

Primary Course: 
1. order clerk issues "Create Order" command with above data.
2. system validates all data
3. system creates order and determines order-id
4. system delivers order-id to clark

Exeption Course:
1. system deliver error massage to the system
USE CASE is essentially an algorithem for the interpration of input data and the genetation of output data
this means that we can create an object that implements that usecase
ofcurse there is a detaile that cause use cases more complex than this
for example in this use case what would happend if the validation fails on one or more entred fields

this senario is primary course use case because it shows you what happend if nothing goes wrong
but what if something goes wrong that handles bye extention course
 notis how this extatins are simple modification to the high level argorithem original use case
it would be pretty simple to integrate this extentions into the object that it implement those use cases


user story begins by the name of use case and they eventually evolved to use-case


now look agine at the algorithem of the primary cource of thisuse-case once again
it mentions others bussines objects like costomer and order , the algorithem define a use case , and clearly it has bussiness ruls on it
but thise bussines ruls don't belong to a customer or oder bussines objects 

so where those bussiness ruls belong to ...
what king of objects should we putt them in
and where that use case object fit in our system artichecture

```
                     ┌────────┐
                     │Customer│
                     └▲───────┘
┌────────────┐        │
│Create Order├────────┤
└────────────┘        │
                     ┌▼───────┐
                     │ Order  ◄──┐
                     └▲───────┘  │
┌────────────┐        │          │
│Add Item    ├────────┤          │
└────────────┘        │          │
                     ┌▼───────┐  │   ┌──────────┐
                     │ Item   │  ├───┤Ship Order│
                     └────────┘  │   └──────────┘
                                 │
                                 │
                                 │
                     ┌────────┐  │
                     │Shipment◄──┘
                     └────────┘
```

as we create more and more use cases we are going to discover more and more bussines objects and more and more use case algorithem

this leave us with a problem
how do we partiotion our system in such a way that this use cases became central organising perinciple


### Partitioning
the objects we are talking about is now are at higher level architectural level than model viw controller
architectures like this have three fundamental kinds of objects
bussines objects => Entities
user interface objects => Bounderies
use case objects => Iteractors - controlls

entites are repository of Application independent bussines rules
 the mothods on entities objects perform functions that are valid in any other applications that entite object can be used in

for example consider a priduct object such an object would be usefull for film seytem or a order entry systemS and inventry management system
or even an online catolog . in jacabson view methos of that product object should be used for to all those applications .
that product object would have no methods we specefic to any of those applications. any application specific method would go into one of 
intractor objects. 

use cases are application specific business ruls
user cases are also implemented by interactor therefore interactor object are also application specific. and that mean any application specirfic
busisness rule blong inside an interactor object

for example imagen the use cases for create order or order item these use case blong ordering entry sytem therfore
the interactor object that implemnets those usecses are specific  to roder entry sysytem

iteractor achive thire goles by application specific logic that cause the application ignostic logic with the entities
for example create order entite invoce both costracractor and get id method of order entitiy

clearly this two method are application agnostic ,it's interactor that know how call thos methods to achive the goal of usecase

```
┌────────────┐   ────►     ┌─────────┐
│Create Order│  create     │  Order  │
│ Interactor ├────────────►│  Entity │
└────────────┘  get-id     └─────────┘
                 ────►
                 o id
                  ◄───
```

one of the jobs of usecase is to accept input data from the user and deliver output data back to the users
this is the job of thierd kinf of objects the boundry object
boundry object isolate the usecase from the delivery mechanisem and provide a comminucation path between the two
if you got a mvc or a consoul or a client all of that are of the far side of boundry the usecases on the other side knows knothing about it

```
                                System Architecture
                     ┌────────────────────────────────────────────────┐
                     │┼──────────────────────────────────────────────┼│
┌───────────┐        ││                                              ││
│┼─────────┼│        ││  ┌───────I─┐       ┌──────┐      ┌─────────┐ ││
││         ││        ││  │         │◄──────┤      ├─────►│         │ ││
││         │┼────────┼┼──► Boundry │       │  UC  │      │  Entity │ ││
││         ││        ││  │         │  ┌────┤      ├───┐  │         │ ││
││         ││        ││  └─────────┘  │    └──────┘   │  └─────────┘ ││
││         ││        ││               │               │              ││
││         ││        ││               │               │              ││
││         ││        ││  ┌─────I───┐◄─┘    ┌──────┐   └─►┌─────────┐ ││
││ Delivery││        ││  │         │       │      │      │         │ ││
││ mech.   │┼────────┼┼─►│ Boundry ◄───────┤  UC  ├─────►│  Entity │ ││
││         ││        ││  │         │       │      │      │         │ ││
││         ││        ││  └─────────┘  ┌────┴──────┘  ▲──►└─────────┘ ││
││         ││        ││               │              │               ││
││         ││        ││               │              │               ││
││         ││        ││  ┌───────I─┐  │    ┌──────┐  │   ┌─────────┐ ││
││         ││        ││  │         │◄─┘    │      ├──┘   │         │ ││
││         │┼────────┼┼──► Boundry │       │  UC  │      │  Entity │ ││
││         ││        ││  │         │◄──────┤      ├─────►│         │ ││
│┼─────────┼│        ││  └─────────┘       └──────┘      └─────────┘ ││
└───────────┘        ││                                              ││
                     │┼──────────────────────────────────────────────┼│
                     └────────────────────────────────────────────────┘
```
the delivery mech gathers users data wraps it up into a nice need cononical form shipsit throw thw boundry to the inter actors
then interactor invoce theire application specific rulls they go on manupi;ate the entities objects and then application agnosticbusines ruls
finally they gather result togheter and wrapit up into anice neet cannonical form and ship it back to the boundry to the delivery mech.


```
               ┌───────────────┐◄──  ──── ───── ────┐
      ┌── ────►│ Request Model │                    │
      │        └─────────────┬─┴────── ────── ───┐  │
      │                      │                   │
┌─────┼─────┐        ┌┐      ▼                   │  │
│┼────┼────┼│        ││  ┌───────I─┐             │  │            ┌─────────┐
││    │    ││        ││  │         │                             │         │
││         │┼────────┼┼─►│ Boundry ◄────────┐    │  │   ┌───────►│  Entity │
││    │    ││        ││  │         │        │    │  │   │        │         │
││    │    ││        ││  └─────────┘        │           │   ── ─►└─────────┘
││    └─ ──┼┼─┐      ││                     │    │  │   │  ┼
││         ││ │      ││                     │    ▼  │   │
││         ││        ││                   ┌─┴───────┴───┴┐◄─     ┌─────────┐
││ Delivery││ │      ││                   │              │       │         │
││ mech.   ││ │      ││                   │  Interactor  ├──────►│  Entity │
││         ││        ││                   │              │       │         │
││         ││ │      ││                   └─┬────┬───┬──┬┴─◄─ ─► └─────────┘
││         ││ │      ││                     │    │   │  │ ▲
││     ┌─ ─┼┼─┘      ││                     │        │  │ │
││     │   ││        ││  ┌───────I─┐        │    │   │  │  ── ──►┌─────────┐
││   ──┼───┼┼────┐   ││  │         │        │    │      │        │         │
││  │  │   │┼────┼───┼┼──► Boundry │◄───────┘        │  └───────►│  Entity │
││  │  │   ││    │   ││  │         │             │   │           │         │
│┼──┼──┼───┼│    │   ││  └─────────┘             │               └─────────┘
└───┼──┼────┘        └┘     ▲                        │
    │  │         │          │                    │   │
    ▼  │       ┌─┴──────────┴───┐◄─ ─── ────── ──┘
  ┌────┴─┐     │ Response Model │                    │
  │ User │     └────────────────┴─── ────── ───── ───┘
  └──────┘
```

and so the bussines rules both the app;ication and specific and application agnostic are strongly decoupled
from the delivery mech in a case of web deliver system the hole web framework hangs of the side of application
and thats the way it should be wheter your application should be 

### Isolation
to keep the delivery mech apandis strongly isolated from the rest of architecture we need to stricly control those source code dependencies
so that they cross the boundri in just one direction

URL ROUTING HTML infact mv architecture lives on the other side of boundry 

now days it's navie that complex views can derive from simple business objects  
most views infact use hole colabration of business objects, in fact most views are significint portion of usecase

so now days a model from mvc framework draw it's data from colabration of entites and interactors that impliment the usecases 
thta model maybe single object but it's not a business object 
infact those models are sell more than simple data structurs that are passed back and forth acrose the boundry 

```
                   ┌┐                                          ┌─────────┐
┌───────────┐      ││                                          │         │
│           ├──────┼┼────┐                            ┌───────►│  Entity │
│ Presenter │      ││    │                            │        │         │
│           ├────┐ ││    │                            │        └─────────┘
└─┬─────────┘    │ ││    │                            │
  │              │ ││    │                            │
  ▼              │ ││  ┌─▼─────I─┐      ┌─────────────┴┐       ┌─────────┐
┌────────────┐   │ ││  │         │      │              │       │         │
│            │   │ ││  │ Boundry │◄─────┤  Interactor  ├──────►│  Entity │
│ View Model │   │ ││  │         │      │              │       │         │
│            │   │ ││  └────────┬┘      └────┬────────┬┘       └─────────┘
└────────────┘   │ ││           │            │        │
  ▲              │ ││           │            │        │
  │              │ ││           │            │        │        ┌─────────┐
┌─┴────────┐     │ ││           ▼            ▼        │        │         │
│          │     │ ││          ┌────────────────┐     └───────►│  Entity │
│   View   │     └─┼┼─────────►│ Response Model │              │         │
│          │       ││          └────────────────┘              └─────────┘
└──────────┘       └┘
```

in the wb version of mvc the web server srecive a http request it runs this request throw it's routing mechanisem 
inorder to select a controler the controller parses throw a http request extract the request data from it and puting it into a nice 
simple little datat structure 

that date structure is really simple it doesn't have any of dictionary or hash map that usually assosiated with web server and web frameworks
all the web ralated date tokens and data identifier and formats have been removed if you look at it a nd isolation 
you wouldn't be able to tell any part of it came from a web . it's just a pure and simple data structure 

that data structure is the model of reques and ships a cross the boundry to interactore 
the interactore orcasterate the magic of convertiong the model of the request into the model of the response 
it imp;ement the usecase it cordinates the dance between all the entite objects it gathers toghthter all the resault data and place it into a 
pure data structure the model of the response

the interactor then passes the response model back throw the boundry to a presenter object in the delivery framework 
that presenter object converts the data elements in the responce model to a format more suitable for the web 
the final presentation data structure then hand it to the view with renders it in to the html

```
                                  ┌───────────────┐
          ┌──────────────────────►│ Request Model │◄────┐
          │                       └───────────────┘     │
          │                            ▲                │
          │         ┌┐                 │                │
          │         ││                 │                │
┌─────────┴──┐      ││     ┌───────I─┐ │                │
│            │      ││     │         ├─┘                │
│ Controller ├──────┼┼────►│ Boundry │                  │
│            │      ││     │         ◄───────────┐      │
└────────────┘      ││     └─────────┘           │      │
                    ││                        ┌──┴──────┴────┐
                    ││                        │              │
                    ││                        │  Interactor  │
                    ││                        │              │
                    ││                        └───┬─────┬────┘
 ┌───────────┐      ││     ┌───────I─┐            │     │
 │           │      ││     │         │◄───────────┘     │
 │ Presenter ├──────┼┼─────► Boundry │                  │
 │           │      ││     │         ├─┐                │
 └────────┬──┘      ││     └─────────┘ │                │
          │         ││                 │                │
          │         ││                 │                │
          │         └┘                 ▼                │
          │                        ┌────────────────┐   │
          └───────────────────────►│ Response Model │◄──┘
                                   └────────────────┘
```

notice the structure of boundry it compose of two seperate sets of interfaces
the first set of interfaces is used by the controllers but implemented by the interactors it accespt the request model structures
the second set of interface is used by the interactors but implemented by the presenter it accepts the response data model structures

those interfaces are the boundry , they belong on the application side and they are part of appllication artichecture 
delivery mechanisem dependes uppon them even implements them and no dependency should cross that boundry pointing 
towards the delivery mechanisem

entity dont know anything about framework
and that means you can develop them and you can test them with out the web server running
you can runn all of your test with out the web server running and that's because entity and interactors are playing old object 
infact you could write a test all the interactor and entites long before you make a we desicion 
you can get the hole application working before you deside on a web server

### Database



## 19.Advance Test Driven Development Part1
by the first law we are not allowed to write any production code until we warit a first unit test
that unit test up to be pretty simple somthing really degenarate like 
an invalid input 
so lest see what our invertor dose when pass a null

### single assert rule
that assertion is a one logical assertion not single physical assert
lots of logical assertion are repesented by several call to assert
```
# n is even and greater than ten
assert n%2 == 0
assert n > 10
```
the foal of this rule is to kake sure when you write this test there is arange act and one logical assert
we want assert act aseert not arrange act assert act assert act assert act assert

Why?

whe want to every action be tesated seperatelly 
we don't want the input of one test id the aot put of previews test
why ?
test independent isolation

### AAA rule
Arrange
act
assert


## 19.Advance Test Driven Development Part2

***As the Test gets more specific, the Code gets mo Generic***

## 20.Clean Test
