# Intro

<img src=assets/refactoring_2nd_edition.png align="right" width=150 height=200>  

The book “[Refactoring: Improving the Design of Existing Code, 2nd edition](https://martinfowler.com/books/refactoring.html)” by Martin Fowler, with Kent Beck, is one of the “must-read” for a developer.

This book explains the definition of refactoring, their principles, bad smells in the code, which indicate the need to refactor them, and describes how to build test into code. Then, the author begins with the catalog of refactorings, where he explains in detail each type of refactoring, its motivation, steps to apply it and an explanatory example.   
From my point of view, it is a very easy book to read, since each refactoring has a code example where you can see the refactoring process, the original code and step by step it explains each refactor that is applied until get the refactored code.

# Disclaimer

This is my summary of the concepts that I have highlighted from each chapter. I have written these notes as a quick reference guide.  
This summary is not intended to be a replacement for the book, in the book are explained concepts with examples and develops deeply more concepts, with extense examples, and much more.

So please, if you are interested, get the [original book](https://martinfowler.com/books/refactoring.html) for the full overview. I think it is a book that must have at home, underline and reread. 🤓

If the publisher thinks this guide should be private, please let me know (saralerma2@gmail.com) and I will make it private.

Feel free to send suggestions, I will be really grateful 🤍

# Contents

- [Preface](#preface)
- [Chapter 1. Refactoring: A Fist Example](#chapter-1-refactoring-a-first-example)
  - [1. Refactoring vs. Performance](#1-refactoring-vs-performance)
- [Chapter 2. Principles in Refactoring](#chapter-2-principles-in-refactoring)
- [Chapter 3. Bad Smells in Code](#chapter-3-bad-smells-in-code)
  - [1. Mysterious name](#1-mysterious-name)
  - [2. Duplicated code](#2-duplicated-code)
  - [3. Long function](#3-long-function)
  - [4. Long parameter list](#4-long-parameter-list)
  - [5. Global data](#5-global-data)
  - [6. Mutable data](#6-mutable-data)
  - [7. Divergent change](#7-divergent-change)
  - [8. Shotgun surgery](#8-shotgun-surgery)
  - [9. Feature envy](#9-feature-envy)
  - [10. Data clumps](#10-data-clumps)
  - [11. Primitive Obsession](#11-primittive-obsession)
  - [12. Repeated switches](#12-repeated-switches)
  - [13. Loops](#13-loops)
  - [14. Lazy element](#14-lazy-element)
  - [15. Speculative generality](#15-speculative-generality)
  - [16. Temporary field](#16-temporary-field)
  - [17. Message chains](#17-message-chains)
  - [18. Middle man](#18-middle-man)
  - [19. Insider trading](#19-insider-trading)
  - [20. Large class](#20-large-class)
  - [21. Alternative Classes with Different Interfaces](#21-alternative-classes-with-different-interfaces)
  - [22. Data class](#22-data-class)
  - [23. Refused Bequest](#23-refused-bequest)
  - [24. Comment](#24-comment)
- [Chapter 4. Building Tests](#chapter-4-building-tests)
- [Chapter 5. Introducing the Catalog](#chapter-5-introducing-the-catalog)
- [Chapter 6. A First Set of Refactorings](#6-most-common-set-of-refactoring)
  - [1. Extract Function (106)](#1-extract-function-106)
  - [2. Inline Function (115)](#2-inline-function-115)
  - [3. Extract Variable (119)](#3-extract-variable-119)
  - [4. Inline Variable (123)](#4-inline-variable-123)
  - [5. Change Function Declaration (124)](#5-change-function-declaration-124)
  - [6. Encapsulate Variable (132)](#6-encapsulate-variable-132)
  - [7. Rename Variable (137)](#7-rename-variable-137)
  - [8. Introduce Parameter Object (140)](#8-introduce-parameter-object-140)
  - [9. Combine Functions Into Class (144)](#9-combine-functions-into-class-144)
  - [10. Combine Functions Into Transform (149)](#10-combine-functions-into-transform-149)
  - [11. Split Phase (154)](#11-split-phase-154)
- [Chapter 7. Encapsulation](#7-encapsulation)
  - [1. Encapsulate Record (162)](#1-encapsulate-record-162)
  - [2. Encapsulate Collection (170)](#2-encapsulate-collection-170)
  - [3. Replace Primitive with Object (174)](#3-replace-primitive-with-object-174)
  - [4. Replace Temp with Query (178)](#4-replace-temp-with-query-178)
  - [5. Extract Class (182)](#5-extract-class-182)
  - [6. Inline Class (186)](#6-inline-class-186)
  - [7. Hide Delegate (189)](#7-hide-delegate-189)
  - [8. Remove Middle Man (192)](#8-remove-middle-man-192)
  - [9. Substitute Algorithm (195)](#9-substitute-algorithm-195)
- [Chapter 8. Moving Features](#8-moving-features)
  - [1. Move Function (198)](#1-move-function-198)
  - [2. Move Field (207)](#2-move-field-207)
  - [3. Move Statements into Function (213)](#3-move-statements-into-function-213)
  - [4. Move Statements To Callers (217)](#4-move-statements-to-callers-217)
  - [5. Replace Inline Code with Function Call (222)](#5-replace-inline-code-with-function-call-222)
  - [6. Slide Statements (223)](#6-slide-statements-223)
  - [7. Split Loop (227)](#7-split-loop-227)
  - [8. Replace Loop with Pipeline (231)](#8-replace-loop-with-pipeline-231)
  - [9. Remove Dead Code (237)](#9-remove-dead-code-237)
- [Chapter 9. Organizing Data](#9-organizing-data)
  - [1. Split Variable (240)](#1-split-variable-240)
  - [2. Rename Field (244)](#2-rename-field-244)
  - [3. Replace Derived Variable With Query (248)](#3-replace-derived-variable-with-query-248)
  - [4. Change Reference To Value (252)](#4-change-reference-to-value-252)
  - [5. Change Value To Reference (256)](#5-change-value-to-reference-256)
- [Chapter 10. Simplifying Conditional Logic](#10-simplifying-conditional-logic)
  - [1. Decompose Conditional (260)](#1-decompose-conditional-260)
  - [2. Consolidate Conditional Expression (263)](#2-consolidate-conditional-expression-263)
  - [3. Replace Nested Conditional with Guard Clauses (266)](#3-replace-nested-conditional-with-guard-clauses-266)
  - [4. Replace Conditional with Polymorphism (272)](#4-replace-conditional-with-polymorphism-272)
  - [5. Introduce Special Case (289)](#5-introduce-special-case-289)
  - [6. Introduce Assertion (302)](#6-introduce-assertion-302)
- [Chapter 11. Refactoring APIS](#11-refactoring-apis)
  - [1. Separate Query from Modifier (306)](#1-separate-query-from-modifier-306)
  - [2. Parameterize Function (310)](#2-parameterize-function-310)
  - [3. Remove Flag Argument (314)](#3-remove-flag-argument-314)
  - [4. Preserve Whole Object (319)](#4-preserve-whole-object-319)
  - [5. Replace Parameter with Query (324)](#5-replace-parameter-with-query-324)
  - [6. Replace Query with Parameter (327)](#6-replace-query-with-parameter-327)
  - [7. Remove Setting Method (331)](#7-remove-setting-method-331)
  - [8. Replace Constructor with Factory Function (334)](#8-replace-constructor-with-factory-function-334)
  - [9. Replace Function with Command (337)](#9-replace-function-with-command-337)
  - [10. Replace Command with Function (344)](#10-replace-command-with-function-344)
- [Chapter 12. Dealing with inheritance](#12-dealing-with-inheritance)
  - [1. Pull Up Method (350)](#1-pull-up-method-350)
  - [2. Pull Up Field (353)](#2-pull-up-field-353)
  - [3. Pull Up Constructor Body (355)](#3-pull-up-constructor-body-355)
  - [4. Push Down Method (359)](#4-push-down-method-359)
  - [5. Push Down Field (361)](#5-push-down-field-361)
  - [6. Replace Type Code with Subclasses (362)](#6-replace-type-code-with-subclasses-362)
  - [7. Remove Subclass (369)](#7-remove-subclass-369)
  - [8. Extract Superclass (375)](#8-extract-superclass-375)
  - [9. Collapse Hierarchy (380)](#9-collapse-hierarchy-380)
  - [10. Replace Subclass with Delegate (381)](#10-replace-subclass-with-delegate-381)
  - [11. Replace Superclass with Delegate (399)](#11-replace-superclass-with-delegate-399)


# Preface

The key to keeping code readable and modifiable is refactoring. However, refactoring is risky because it requires changes to working code that can introduce subtle bugs.  
This book explains the principles and best practices of refactoring and points out when and where you should start digging in your code to improve it.

## What is refactoring?
Refactoring is the process of changing a software system in a way that **does not alter the external behavior** of the code yet **improves its internal structure**.  
Minimizes the chances of introducing bugs. Improves the design of the code after it has been written.

# Chapter 1. Refactoring: A Fist Example
A poorly designed system is hard to change because it is difficult to figure out what to change and how these changes will interact with the existing code to get the behavior you want. And if it is hard to figure out what to change, there is a good chance that you will make mistakes and introduce bugs.   

When you have to add a feature to a program but the code is not structured in a convenient way, **first refactor** the program to make it easy to add the feature, and **then, add the feature**.  
Before you start refactoring, make sure you have a solid **suite of tests**. Use test for avoid opportunities for introducing bugs.

The key to effective refactoring is recognizing that you go faster when you take **tiny steps**, each step leaving the code in a working state that compiles and passes its tests.  
Steps: COMPILE - TEST - COMMIT (commit the change to your local version control system) 🔄 

## Refactoring vs. Performance
Most of the time you should ignore performance. If your refactoring introduces performance slow­downs, finish refactoring first and do performance tuning afterward.  
> 1st - refactor   
  2nd - try improve performance

# Chapter 2. Principles in Refactoring

Refactoring is a change made to the internal structure of software to make it easier to understand and modify **without changing its observable behavior** (code so the same - nothing should change that the user should care about).

If you are refactoring to develop software, divide your time between two distinct activities (two hats): 
- adding functionality (don't changing existing code) and 
- refactoring (restructuring the code, not adding new capabilities). 
> Be aware of which activity you are performing. 

### Why should you refactor?
1.	**Improves the Design of Software**: Without refactoring, the internal design (the architecture) of software tends to decay. As people change code to achieve short­term goals, often without a full comprehension of the architecture.  
By eliminating duplication, you ensure that the code says everything only once, which is the essence of good design.
2.	**Makes Software Easier to Understand**: Code readable and the code communicate its purpose - say clearly what you want.
3.	**Helps you find Bugs**: Help in understanding the code also means help in spotting bugs.
4.	**Helps you Program Faster**: Every new feature requires time to understand how to fit it into the existing code base, and once it’s added, bugs often crop up that take even longer to fix.  
The code base starts looking like a series of patches 🩹 covering bugs (or functionalities not thought from the beginning), and it takes an exercise to figure out how things work.  
Software with a good internal design allows you to easily find how and where you need to make changes to add a new feature. Good modularity allows you to only have to understand a small subset of the code base to make a change. If the code is clear, you are less likely to introduce a bug, and if you do, the debugging effort is smaller.  
The author refers to this effect as the [_Design Stamina Hypothesis_](https://martinfowler.com/bliki/DesignStaminaHypothesis.html): By putting you effort into a good internal design, you increase the stamina of the software effort, allowing you to go faster for longer.
### When should you refactor?

1.	**Preparatory Refactoring**:  
Making It Easier to Add a Feature.  
The best time to refactor is just **before** you need to add a new feature to the code base.
2.	**Comprehension Refactoring**:  
Making Code Easier to Understand.  
Before you can change some code, you need to understand what it does.
3.	**Litter-Pickup Refactoring**:  
A variation of comprehension refactoring is when you understand what the code is doing, but realize that it’s doing it badly. The logic is unnecessarily convoluted. 
If it’s easy to change, you will do it right away.  
If it’s a bit more effort to fix, you might make a note of it and fix it when you are done with your immediate task.  
    > As the old camping adage says, “always leave the camp site cleaner than when you found it”.
4.	**Planned and Opportunistic Refactoring**:  
It’s a common error to see refactoring as something people do to fix past mistakes or clean up ugly code. Certainly you have to refactor when you run into ugly code, but excellent code also needs plenty of refactoring.  
The tradeoffs you made correctly for yesterday’s feature, set may no longer be the right ones for the new features you are adding today. The advantage is that clean code is easier to refactor when you need to change those tradeoffs to reflect the new reality.  
Often, the fastest way to add a new feature is to change the code to make it easy to add. As new capabilities are needed, the software changes to reflect that. Those changes can often be greater in the existing code than in the new code.  
Sometimes, even with regular refactoring you will see a problem area grow to the point when it needs some concerted effort to fix. But such planned refactoring episodes should be rare. Most refactoring effort should be the unremarkable, opportunistic kind.  

    > One bit of advice - to separate refactoring work and new feature additions into different version ­control commits. The big advantage of this is that they can be reviewed and approved independently. However, often the refactorings are closely interwoven with adding new features, and it’s not worth the time to separate them out. This can also remove the context for the refactoring, making the refactoring commits hard to justify.
5.	**Long-Term Refactoring**:  
A useful strategy is to agree to gradually work on the problem over the course of the next few weeks. Whenever anyone goes near any code that is in the refactoring zone, they move it a little way in the direction they want to improve. This takes advantage of the fact that refactoring doesn’t break the code, because each small change leaves everything in a still working state.
6.	**Refactoring in a Code Review**:  
Code reviews help **spread knowledge** through a development team. 🧑‍🏫  
Reviews help more experienced developers pass knowledge to those less experienced. They help more people understand more aspects of a large software system. They are also very important in writing clear code. Your code may look clear to you but not to your team.  
It’s better to have the original author of the code present because the author can provide context on the code and fully appreciate the reviewers’ intentions for their changes.  
If it's needed, you can sitting 1:1 with the original author, going through the code and refactoring as you go. The logical conclusion of this style is pair programming: continuous code review embedded within the process of programming.

### What do you tell your manager?
Software developers job is to build effective software as rapidly as you can. If you need to add a new function, maybe you find it’s quicker to refactor first and then add the function.  
Manager wants do things the fastest way you can, how you do is your responsibility. You are being paid for your expertise in programming new capabilities fast, and the fastest way is by refactoring — therefore you refactor.  

When should you not refactor?
1. You don't need to modify it - If you run across code that is a mess, but you don’t need to modify it, then you don’t need to refactor it. Just refactor when you need to understand how it works.  
2. It's difficult to refactor - Sometimes it’s easier to rewrite it than to refactor it. You spend some time trying and thus get a sense of how difficult it is.  
3. You don't have good judgment and experience - The decision to refactor or rewrite requires good judgment and experience.

In simpler words, when you don't need to touch it, understand it or it's hard to refactor (in this case is easier to rewrite than refactor - for this you need good judgment and experience).

## Problems with refactoring  
Refactoring is a valuable technique but there are problems associated with it, and it’s important to understand how they manifest themselves and how you can react to them:
1.	**Slowing down new features**  
Many people see time spent refactoring as slowing down the development of new features.  
The whole purpose of refactoring is to make us faster, make your program faster - faster to add features, faster to fix bugs. It's better **little refactor and more often**.
2.	**Code ownership**  
Many refactorings involve making changes that affect to other parts of a system and maybe it’s owned by a different team and you don’t have access to their repository. **Allow team ownership of code** -> so that anyone in the same team can modify the team’s code, even if originally written by someone else. Encourage an open-source model where people from other teams can change the code.
3.	**Branches**  
Distinguish between **merging and integration**. 
    - If you **merge** mainline into your code, this is a **one-way** movement— your branch changes but the mainline doesn’t. 
    - If you **integrate** is a **two-­way** process that pulls changes from mainline into your branch and then pushes the result back into mainline, **changing both**. And the complexity of merges increases with big branches (for example: 4 weeks).   

    Solution: With **Continuous Integration (CI)** each team member integrates with mainline (master branch) at least once per day. This prevents any branches diverting too far from each other and thus greatly reduces the complexity of merges.
    CI doesn’t come for free: It means you  
    1. use practices to ensure the mainline is healthy,  
    2. learn to break large features into smaller chunks, and  
    3. use feature toggles (aka *feature flags*) to switch off any in-process features that can’t be broken down.  

    CI reduces the complexity of merges and is more compatible with refactoring.  
    Refactorings often involve making lots of little changes all over the code base. 
4.	**Testing**  
To catch an error quickly you must run a test suite on the code. Self-­testing code enables refactoring and it also makes it much safer to add new features, since you can quickly find and fix any bugs you introduce.
5.	**Legacy code**  
It’s important to **have tests before start to refactor legacy code**. [Book recommended: Working Effectively with Legacy Code]  
You should get the system under test by finding seams in the program where you can insert tests and refactor in relevant pieces, not all code at once.  
    > Write always self-testing code from start.
6.	**Databases**  
An approach of database design and database refactoring is to combine the structural changes to a database’s schema and access code with data migration scripts that can easily compose to handle large changes.  
One difference from regular refactorings is that database changes often are best separated over multiple releases to production. This makes it easy to reverse any change that causes a problem in production. This approach to database changes is an example of a general approach of parallel change.

## Refactoring, Arquitecture and YAGNI (You Aren’t Going to Need It)
The real impact of refactoring on architecture is in how it can be used to form a well-designed code base that can respond gracefully to changing needs.  
An strategy could be; instead of speculating on what flexibility you will need in the future and what mechanisms will best enable that -> you build software that solves only the currently understood needs, but you make this software excellently designed for those needs.  
As your understanding of the users’ needs changes, you should use refactoring to adapt the architecture to those new demands.  This approach to design goes under various names: simple design, incremental design, or yagni.  
Yagni makes it easier to do refactoring because it’s easier to change a simple system than one that has lots of speculative flexibility included.  
Evolutionary architecture where architects explore the patterns and practices that take advantage of your ability to iterate over architectural decisions.

### Refactoring and the wider software development process
Extreme Programming (XP) is a process which was notable for putting together a set of relatively unusual and interdependent practices, such as, continuous integration, self­-testing code, and refactoring.  
Self-­testing code there is a suite of automated tests that you can run and be confident that, if you made an error in your programming, some test will fail.  
With CI, each member’s refactoring efforts are quickly shared with their colleagues. And Continuous Delivery (CD) keeps your software in an always ­releasable state.

## Refactoring and Performance
A common concern with refactoring is the effect it has on the performance of a program. To make the software easier to understand, you can make changes that will cause the program to run slower.  
Three general approaches to writing fast software:
1. The most serious of these is **time budgeting**, often used in hard real­time systems. As you decompose the design, you give each component a budget for resources—time and footprint. That component must not exceed its budget (although a mechanism for exchanging budgeted resources is allowed). This technique is inappropriate for other kinds of systems, such as the corporate information systems. 
2. **Constant attention** approach.  
Every programmer make changes to improve performance, which is intuitively attractive but usually make the program harder to work with and this slows development.  
Even if you know exactly what is going on in your system, **measure performance, don’t speculate**. You’ll learn something, and 9/10 times, it won’t be that you were right!  
The interesting thing about performance is that **in most programs, most of their time is spent in a small fraction of the code.**
3. **Optimize small fraction of the code more used**.  
The third approach to performance improvement takes advantage of this 90­percent statistic. In this approach, you build your program in a well-­factored manner without paying attention to performance until you begin a deliberate performance optimization exercise. During this performance optimization, you follow a specific process to tune the program.  
You begin by running the program under a profiler that monitors the program and tells you where it is consuming time and space. In this way you can find and improve the performance of that small part of the program where the performance hot spots lie.  
You make the changes in small steps. After each step you compile, test, and rerun the profiler. If you haven’t improved performance, you back out the change.

## Where did refactoring from?
### Automated Refactoring
A technology that is currently gaining momentum is Language Servers, software that will form a syntax tree and present an API to text editors. Such language servers can support many text editors and provide commands to do sophisticated code analysis and refactoring operations.

# Chapter 3. Bad Smells in Code
### 1. Mysterious name
Name should clearly communicate what they do and how to use them. If you have a good name for a function, you mostly don’t need to look at its body.
### 2. Duplicated code
Same code structure in more than one place.

### 3. Long function
A longer a function is more **difficult to understand**.  
A block of code with a comment that tells you what it is doing can be replaced by a method whose name is based on the comment. Even a single line is worth extracting if it needs explanation.

### 4. Long parameter list
Long parameter lists are often **confusing**. They are hard to understand,  inconsistent, difficult to use and easily introduce bug.  
**Solution**: [Replace Parameter with Query (324)](#5-replace-parameter-with-query-324), [Preserve Whole Object (319)](#4-preserve-whole-object-319), [Introduce Parameter Object (140)](#8-introduce-parameter-object-140), [Remove Flag Argument (314)](#3-remove-flag-argument-314)

### 5. Global data
Global variable is **difficult to track and debug**.  
The problem with global data is that it can be modified from anywhere in the code base, and there’s no mechanism to discover which bit of code touched it. Global data is global variables and also class variables and singletons.  

**Solution**: *[Encapsulate Variable (132)](#6-encapsulate-variable-132)* - At least when you have it wrapped by a function, you can start seeing where it’s modified and start to control its access. Then, it’s good to limit its scope as much as possible by moving it within a class or module where only that module’s code can see it. Global data is especially nasty when it’s mutable.

### 6. Mutable data
Changes to data can often **lead to unexpected consequences and tricky bugs**.  
Data should never change and that updating a data structure should always return a new copy of the structure with the change, leaving the old data pristine.  
Mutable data isn’t a big problem when it’s a variable whose scope is just a couple of lines—but its risk increases as its scope grows.

### 7. Divergent change
Divergent change occurs when **one module is often changed in different ways for different reasons**. By moving such contexts into separate modules - when you have a change to one context, you only have to understand that one context and ignore the other.

### 8. Shotgun surgery
It’s the opposite of divergent change - when, every time you make a change, you have to make a lot of little edits in different classes.

### 9. Feature envy
A classic case of Feature Envy occurs **when a function in one module spends more time communicating with functions or data inside another module than it does within its own module.** For example, a function invoking a lot of getter methods on another object to calculate some value.  
When you modularize a program, you are trying to separate the code into zones to maximize the interaction inside a zone and minimize interaction between zones.  
**Solution**: move the function with the data *[Move Function (198)](#1-move-function-198)*.

### 10. Data clumps
Same three or four data items together in lots of places
**Data items tend to be together** - Bunches of data (fields, parameters, etc.) that hang around together.  
Often, data group are together in lots of places: as fields in a couple of classes, as parameters in many method signatures.  
**Solution**: turn the clumps into an object.

### 11. Primitive Obsession
Use primitive types instead of custom fundamental (small) types.  
Create their own fundamental types which are useful for their domain, such as money, coordinates, or ranges.  
**Solution**: You can move out of the primitive cave into the centrally heated world of meaningful types by using *[Replace Primitive with Object (174)](#3-replace-primitive-with-object-174)*.  
If the primitive is a type code controlling conditional behavior, use *[Replace Type Code with Subclasses (362)](#6-replace-type-code-with-subclasses-362)* followed by *[Replace Conditional with Polymorphism (272)](#4-replace-conditional-with-polymorphism-272)*.  
Groups of primitives that commonly appear together are data clumps and should be civilized with *[Extract Class (182)](#5-extract-class-182)* and *[Introduce Parameter Object (140)](#8-introduce-parameter-object-140)*.

### 12. Repeated switches
Replace repeated switches (conditional - tested `if`/`else`) with *[Replace Conditional with Polymorphism (272)](#4-replace-conditional-with-polymorphism-272)*.

### 13. Loops
*[Replace Loop with Pipeline (231)](#8-replace-loop-with-pipeline-231)* - pipeline operations, such as filter and map.

### 14. Lazy element
Remove a class, struct or function that isn't doing enough to pay for itself.

### 15. Speculative generality
All sorts of hooks (features) and special cases to handle things that aren't required.  
> YAGNI: Don't implement features for the future that are not required because maybe in the future you don't need the and later the code is harder to maintain.

### 16. Temporary field
An instance variable that is set only in certain circumstances. Difficult to understand why a filed is there if you don’t use other times.

### 17. Message chains
When a client asks one object for another object, which the client then asks for yet another object, and so on.  
Any change to the intermediate relationships causes the client to have to change.  
Often, a better alternative is to see what the resulting object is used for.   
> Check [Law of Demeter](https://betterprogramming.pub/demeters-law-don-t-talk-to-strangers-87bb4af11694).

### 18. Middle man
One of the prime features of objects is encapsulation, hiding internal details from the rest of the world. Encapsulation often comes with delegation. **When an object delegates much of its functionality.**  
**Solution**: Use *[Remove Middle Man (192)](#8-remove-middle-man-192)* and talk to the object that really knows what’s going on. 

### 19. Insider trading
Trading data increases coupling. To make things work, some trade has to occur, but you need to reduce it to a minimum and keep it all above board.  
**Solution**: *[Move Function (198)](#1-move-function-198)* and *[Move Field (207)](#2-move-field-207)* to reduce the need to chat.

### 20. Large class
A class is trying to do too much, it often shows up as too many fields, too many variables, too much code.  
**Solution**: The clients of such a class are often the best clue for splitting up the class.  
Look at whether clients use a subset of the features of the class. Each subset is a possible separate class.

### 21. Alternative Classes with Different Interfaces
Classes with methods that look to similar but classes can be unified because their interfaces are different.  
**Solution**: [Change Function Declaration (124)](#5-change-function-declaration-124) to make functions match and Move Functions to move behavior into classes until the protocols match.

### 22. Data class
Classes that have fields, getting and setting methods for the fields, and nothing else.  
**Solution**: Look for where these getting and setting methods are used by other classes. Try to use *[Move Function (198)](#1-move-function-198)* to move behavior into the data class. If you can’t move a whole function, use [Extract Function (106)](#1-extract-function-106) to create a function that can be moved.

### 23. Refused Bequest (legacy)
Subclasses don't make uses of parents' methods. Why? **Hierarchy is wrong**.  
**Solution**: Create new sibling class and use *[Push Down Method (359)](#4-push-down-method-359)* and *[Push Down Field (361)](#5-push-down-field-361)* to push all the unused code to the sibling. That way, the parent holds only what is common.
### 24. Comment
The comments are there because the code is bad.  
**Solution**: When you feel the need to write a comment, first try to refactor the code so that any comment becomes superfluous.

# Chapter 4. Building Tests

## The Value of Self-Testing Code
Programmers spend most time debugging. With testing you are more productive.  
Make sure all tests are fully automatic and that they check their own results. 
> *Don’t start to refactor without a test suite!*  

A suite of tests is a powerful bug detector that decapitates the time it takes to find bugs.  

**Test-­Driven Development (TDD)** approach to programming relies on short cycles of writing a (failing) test, writing the code to make that test work, and refactoring to ensure the result is as clean as possible.   
*Refactoring requires tests.*  
Always make sure a test will fail when it should.
## Run tests frequently 
Run those exercising the code you are working on at least every few minutes; run all tests at least daily.

## Probing the Boundaries
Think of the boundary conditions under which things might go wrong and concentrate your tests there.  
It is better to write and run incomplete tests than not to run complete tests.
Don’t let the fear that testing can’t catch all bugs stop you from writing tests that catch most bugs.  
Don’t try to test everything, concentrate where the risk is. 

Testing phases: 
1. Setup 
2. Exercise 
3. Verify 
4. Teardown (Remove fixtures between tests - grant with `beforeEach`)
### Difference between failure vs. error 
Many testing frameworks distinguish between this situation, which they call an error, and a regular failure.  
A **failure** indicates a verify step where the actual value is outside the bounds expected by the verify statement.  
But the **error** is an exception raised during an earlier phase (in this case, the setup).

## Measurement - how much testing is enough?
There’s no a good measurement of how much testing is enough, it’s subjective - **how confident are you?**  
Test coverage analysis is only good for identifying untested areas of the code, but for assessing the quality of a test suite.  
When you get a bug report, start by writing a unit test that exposes the bug.

# Chapter 5. Introducing the Catalog
To describe the refactorings the author uses a standard format, each refactoring has five parts, as follows:  
1. **Name** - The name is important to building a vocabulary of refactorings. Refactorings often go by different names now, so the author also list any aliases that seem to be common.
2. **Sketch** of the refactoring.
3. The **motivation** describes why the refactoring should be done and describes circumstances in which it shouldn’t be done.
4. The **mechanics** are a concise, step-­by-­step description of how to carry out the refactoring.
5. The **examples** show a very simple use of the refactoring to illustrate how it works.

But in this summary I am not going to follow this structure, I will write for each refactoring the name, brief explanation and example.

> 📝 NOTE: the names of the refactorings are accompanied by numbers in parentheses, these are the pages where these refactorings are explained in the book.

# Chapter 6. A First Set of Refactorings
Set of refactorings most useful to learn first.
## 1. Extract Function (106)

aliases *Extract Method*

inverse of *[Inline Function (115)](#2-inline-function-115)*

Extract fragment of code into its own function named after its purpose. You have a code fragment that can be grouped together.

Separate between intention and implementation - each function must have a purpose or intent, and sometimes it is necessary to extract a function into several so that each one expresses the purpose of the function body. The size of the function (lines of code) does not matter if the code is more readable since optimizing compliers often work better with shorter functions which can be cached more easily.

```javascript
function printOwing(invoice) {
  printBanner();
  let outstanding  = calculateOutstanding();

  //print details
  console.log(`name: ${invoice.customer}`);
  console.log(`amount: ${outstanding}`);  
}
```
⬇️
```javascript
function printOwing(invoice) {
  printBanner();
  let outstanding  = calculateOutstanding();
  printDetails(outstanding);

  function printDetails(outstanding) {
    console.log(`name: ${invoice.customer}`);
    console.log(`amount: ${outstanding}`);
  }
}
```
**Motivation**

* Increases the chances that other methods can use a method.
* Allows the higher-level methods to read more like a series of comments.

> TIP: Call the return value from a function `result` - that way you always know its role.

## 2. Inline Function (115)

aliases *Inline Method*

inverse of *[Extract Function (106)](#1-extract-function-106)*

Get rid of the function when the body of the code is just as clear as the name.

```javascript
function getRating(driver) {
  return moreThanFiveLateDeliveries(driver) ? 2 : 1;
}

function moreThanFiveLateDeliveries(driver) {
  return driver.numberOfLateDeliveries > 5;
}
```
⬇️
```javascript
function getRating(driver) {
  return (driver.numberOfLateDeliveries > 5) ? 2 : 1;
}
```
Don't do this refactor if you have complexities like recursion, multiple return points, inlining a method into another object when you don't have accessors, and so on.

## 3. Extract Variable (119)

aliases *Introduce Explaining Variable*

inverse of *[Inline Variable (123)](#4-inline-variable-123)* 

Add a name to an expression.

```javascript
//price is base price ­- quantity discount + shipping
return order.quantity * order.itemPrice -
  Math.max(0, order.quantity - 500) * order.itemPrice * 0.05 +
  Math.min(order.quantity * order.itemPrice * 0.1, 100)
```
⬇️
```javascript
const basePrice = order.quantity * order.itemPrice
const quantityDiscount = Math.max(0, order.quantity - 500) * order.itemPrice * 0.05
const shipping = Math.min(basePrice * 0.1, 100)
return basePrice - quantityDiscount + shipping
```

**Motivation**
- Break down and name a part of a more complex piece of logic.
- Easier for debugging.

## 4. Inline Variable (123)

aliases *Inline Temp*

inverse of *[Extract Variable (119)](#3-extract-variable-119)*

Remove variable which name doesn't really communicate more than the expression itself.

```javascript
let basePrice = anOrder.basePrice
return (basePrice > 1000)
```
⬇️
```javascript
return anOrder.basePrice > 1000
```

## 5. Change Function Declaration (124)

aliases *Rename Function*, *Rename Method*, *Add Parameter*, *Remove Parameter*, *Change Signature*

Rename a function.

```javascript
function circum(radius) {...}
```
⬇️
```javascript
function circumference(radius) {...}
```

Rename list of parameters.
The parameters of a function set the context in which you can use a function. 
```javascript
function format(personPhone) {...}
```
⬇️
```javascript
function format(phone) {...}
```
> TIP: A good way to improve a name is to write a comment to describe the function's purpose, the turn that comment into a name.

**Motivation**
- Easier to understand.
- Easier to reuse, sometime better encapsulation.

## 6. Encapsulate Variable (132)

aliases *Self-Encapsulate Field*, *Encapsulate Field*

Data is more awkward to manipulate than functions. Since using a function usually means calling it, you can easily rename or move a function while keeping the old function intact as a forwarding function (so your old code calls the old function, which calls the new function). 
```javascript
function oldFunction() { return newFunction() }
```
But ifyou move data around, you have to change all the references to the data in a single cycle to keep the code working, and with global data is such a pain.  
So if you want to move widely accessed data, first encapsulate it by routing all its access through functions (accessors - setter and getter).  
That way, you turn the difficult task of reorganizing data into the simpler task of reorganizing functions.
> TIP: Try to make all mutable data encapsulated and only accessed through functions.   
Encapsulate a reference to some data structure.

```javascript
let defaultOwner = {firstName: "Martin", lastName: "Fowler"}
```
⬇️
```javascript
// defaultOwner.js
let defaultOwnerData = {firstName: "Martin", lastName: "Fowler"}
export function defaultOwner() { return defaultOwnerData } //getter
export function setDefaultOwner(arg) { defaultOwnerData = arg } //setter
```
The basic refactoring encapsulates the reference to the data item. But you often will want to take the encapsulation deeper to control not just changes to the variable but also to its contents.  
prevent any changes to the value modifying the getting function to return a *copy of the data*. Then any clients using it can change it, but that change isn’t reflected in the shared data.  

**Motivation**
- Provide a clear point to monitor changes and use of the data, like validation.

## 7. Rename Variable (137)
Make shared variable's name can self-explain.

```javascript
let a = height * width
```
⬇️
```javascript
let area = height * width
```

## 8. Introduce Parameter Object (140)
Replace groups of data items that regularly travel together with a single data structure.

```javascript
function amountInvoiced(startDate, endDate) {...}
function amountReceived(startDate, endDate) {...}
function amountOverdue(startDate, endDate) {...}
```
⬇️
```javascript
function amountInvoiced(aDateRange) {...}
function amountReceived(aDateRange) {...}
function amountOverdue(aDateRange) {...}
```

**Motivation**
- Reduce the size of parameter list.
- Make explicit the relationship between the data items.
- Make code more consistent.
- Enable deeper changes to the code.

## 9. Combine Functions Into Class (144)
Classes bind together data and functions into a shared environment, exposing some of the data and function to other program elements for collaboration.   
So, form a class base on group of functions that operate closely on a common data.

```javascript
function base(aReading) {...}
function taxableCharge(aReading) {...}
function calculateBaseCharge(aReading) {...}
```
⬇️
```javascript
class Reading() {
  base() {...}
  taxableCharge() {...}
  calculateBaseCharge() {...}
}
```
> *Uniform Access Principle*: All services offered by a module should be available through a uniform notation, which does not betray whether they are implemented through storage or through computation. In other words, it states that there should be no syntactical difference between working with an attribute, pre-computed property, or method/query of an object.

**Motivation**
- Simplify function call by removing many arguments.
- Easier to pass object to other parts of the system.

## 10. Combine Functions Into Transform (149)

Software involves feeding data into programs that calculate various derived information from it. These derived values may be needed in several places, and those calculations are often repeated wherever the derived data is used. It's better to bring all of these derivations together, so you have a consistent place to find and update them and avoid any duplicate logic.

Takes the source data (`argReading`) as input (in data transform function - `enrichReading`) and calculates all the derivations(`base(aReading)` and `taxableCharge(aReading)`), putting each derived value as a field (`aReading.baseCharge` and `aReading.taxableCharge`) in the output data(`aReading`).

```javascript
function base(aReading) {...}
function taxableCharge(aReading) {...}
```
⬇️
```javascript
function enrichReading(argReading) { //source data as input
  const aReading = _.cloneDeep(argReading)
  aReading.baseCharge = base(aReading) //derived value as a field
  aReading.taxableCharge = taxableCharge(aReading) //derived value as a field
  return aReading //output data
}
```
Alternative: Use [Combine Functions Into Class (144)](#9-combine-functions-into-class-144) that moves the logic into functions on a class. The difference is that using a class is much better if the source data gets updated within the code. Using a transform stores derived data in the new record, so if the source data changes, you will run into inconsistencies.

**Motivation**
- Avoid duplication of logic.
- Find easily functions because they are kept close to the data structures they operate on.

## 11. Split Phase (154)
Separate code which do different things into separate modules.
The best clue is when different stages of the fragment use different sets of data and functions.

```javascript
const orderData = orderString.split(/\s+/) //1
const productPrice = priceList[orderData[0].split("-")[1]] //2
const orderPrice = parseInt(orderData[1]) * productPrice //3
```
⬇️
```javascript
const orderRecord = parseOrder(orderString)
const orderPrice = price(orderRecord, priceList)

function parseOrder(aString) {
  const values = aString.split(/\s+/) //1
  return {
    productID: values[0].split("-")[1], //2
    quantity: parseInt(values[1]) //3
  }
}
function price(order, priceList) {
  return order.quantity * priceList[order.productID]
}
```

**Motivation**
- Make the different explicit, revealing the different in the code
- Be able to deal with each module separately

# Chapter 7. Encapsulation

## 1. Encapsulate Record (162)

aliases *Replace Record with Data Class*

It's better use objects over records for **mutable** data.  
With objects, you can hide what is stored and provide methods for all three values. The user of the object doesn’t need to know or care which is stored and which is calculated.
> Remind: **Records are immutable, they can't be updated or changed.**

```javascript
organization = {name: "Acme gooseberries", country: "GB"} //Record(immutable)
```
⬇️

```javascript
class Organization { //Data Class
  constructor(data) {
    this._name = data.name
    this._country = data.country
  }

  get name() { return this._name }
  set name(arg) { this._name = arg }
  get country() { return this._country }
  set country(arg) { this._country = arg }
}
```

**Motivation**
- Hide what's stored and provide methods to get value.
- Easier to refactoring, for example: rename.

## 2. Encapsulate Collection (170)

A method returns a collection (`get courses()`). Make it return a read-only view and provide add/remove methods instead of a setter for the collection.

Access to a collection variable may be encapsulated, but if the getter returns the collection itself, then that collection’s membership can be altered without the enclosing class being able to intervene.

```javascript
class Person {
  get courses() { return this._courses }
  set courses(aList) { this._courses = aList }
}
```
⬇️
```javascript
class Person {
  get courses() { return this._courses.slice() } //slice() method does not change the original array
  addCourse(aCourse) {...}
  removeCourse(aCourse) {...}
}
```
> 📝 NOTE: The getter should not return the collection object itself, should return something that prevents manipulation of the collection and hides unnecessary details (example - using `slice()`).

**Motivation**
- Change to the collection should go through the owning class to prevent unexpected changes.
- Prevent modification of the underlying collection for example: return a copy or read-only proxy instead of collection value

## 3. Replace Primitive with Object (174)

aliases *Replace Data Value with Object*, *Replace Type Code with Class*

You have a data item (example - phone number represented as `String`) that needs additional data or behavior (for example - extract the area code). Create class for that data, in this way the class will wrap the primitive and the additional behavior.

```javascript
orders.filter(o => "high" === o.priority || "rush" === o.priority)
```
⬇️

```javascript
orders.filter(o => o.priority.higherThan(new Priority("normal"))) // create Priority class with higherThan new behavior
```

**Motivation**
- Encapsulate behavior with Class.

## 4. Replace Temp with Query (178)

When you are using a temporary variable to store the result of an expression -> extract the assignment of the variable into a query method. Any method in the class can get at the information.

```javascript
const basePrice = this._quantity * this._itemPrice //const basePrice temp var
if (basePrice > 1000) {
  return basePrice * 0.95
} else {
  return basePrice * 0.98
}
```
⬇️
```javascript
get basePrice() { return this._quantity * this._itemPrice } // query for basePrice
...
if (this.basePrice > 1000) {
  return this.basePrice * 0.95
} else {
  return this.basePrice * 0.98
}
```

**Motivation**
- Avoid duplicating the calculation logic in similar functions.

## 5. Extract Class (182)

inverse of *[Inline Class (186)](#6-inline-class-186)*

When a subset of the data and a subset of the methods seem to go together (for example - `areaCode` and `number` belongs to a `PhoneNumber`), or subsets of data that usually change together or are particularly dependent on each other, you must extract that data to a corresponding class (move from `Person` to `PhoneNumber`).  
Create a new class (`TelephoneNumber`) and move the relevant fields and methods from the old class (`Person`) into the new class (`TelephoneNumber`).

```javascript
class Person {
  get officeAreaCode() { return this._officeAreaCode }
  get officeNumber() { return this._officeNumber }
}
```
⬇️
```javascript
class Person {
  get officeAreaCode() { return this._telephoneNumber.areaCode }
  get officeNumber() { return this._telephoneNumber.number }
}
class TelephoneNumber {
  get areaCode() { return this._areaCode }
  get number() { return this._number }
}
```

**Motivation**
- Smaller class is easier to understand.
- Separate class's responsibility.

## 6. Inline Class (186)

inverse of *[Extract Class (182)](#5-extract-class-182)*

Merge class if class isn't doing very much. Move its feature to another class then delete it.

```javascript
class Person {
  get officeAreaCode() { return this._telephoneNumber.areaCode }
  get officeNumber() { return this._telephoneNumber.number }
}
class TelephoneNumber {
  get areaCode() { return this._areaCode }
  get number() { return this._number }
}
```
⬇️
```javascript
class Person {
  get officeAreaCode() { return this._officeAreaCode }
  get officeNumber() { return this._officeNumber }
}
```

**Motivation**
- Class is no longer pulling its weight and shouldn’t be around any more.
- When want to refactor pair of classes. First Inline Class -> Extract Class to make new separation.

## 7. Hide Delegate (189)

inverse of *[Remove Middle Man (192)](#8-remove-middle-man-192)*

Check [Law of Demeter](https://betterprogramming.pub/demeters-law-don-t-talk-to-strangers-87bb4af11694). One of the keys to good modular design is encapsulation.
Encapsulation means that modules need to know less about other parts of the system. Then, when things change, fewer modules need to be told about the change—which makes the change easier to make.

If a client calls a method defined on an object in a field of a server object, the client needs to know about this delegate object.  
Remove this dependency by creating a delegating method on the server that hides the delegate.  
Then any changes I make to the delegate propagate only to the server and not to the clients.  

<p align="center">
  <img src=assets/7.7.hideDelegate_example.png width=400 height=200>  
</p>


```javascript
manager = aPerson.department.manager
```
⬇️
```javascript
manager = aPerson.manager

class Person {
  get manager() {
    return this.department.manager
  }
}
```

**Motivation**
- Client doesn't need to know and response to delegation's change.
- Better encapsulation.

## 8. Remove Middle Man (192)

inverse of *[Hide Delegate (189)](#7-hide-delegate-189)*

When there are a lot of delegated methods in the server class (*[Middle man](#18-middle-man)*) or a class is doing too much, it's better that the client call the delegate directly.

```javascript
manager = aPerson.manager

class Person {
  get manager() { return this.department.manager }
}
```
⬇️
```javascript
manager = aPerson.department.manager
```

**Motivation**
- When there are too many delegating methods.

## 9. Substitute Algorithm (195)

Replace complicated algorithm with simpler algorithm.

```javascript
function foundPerson(people) {
  for (let i = 0; i < people.length; i++) {
    if (people[i] === "Don") {
      return "Don"
    }
    if (people[i] === "John") {
      return "John"
    }
    if (people[i] === "Kent") {
      return "Kent"
    }
  }
  return ""
}
```
⬇️
```javascript
function foundPerson(people) {
  const candidates = ["Don", "John", "Kent"]
  return people.find(p => candidates.includes(p)) || ''
}
```

**Motivation**
- Change to algorithm which make changes easier.
- The clearer algorithm is the better 😉.

# Chapter 8. Moving Features

Moving elements between contexts.

## 1. Move Function (198)

aliases *Move method*

When a function references elements in other contexts more than the one it currently resides in, move function between classes or variables.
To decide move a function look at:
- what functions call this one, 
- what functions are called by the moving function, and 
- what data that function uses.

```javascript
class Account {
  get overdraftCharge() {...}
```
⬇️
```javascript
class AccountType {
  get overdraftCharge() {...}
```

**Motivation**
- Improve encapsulation, less coupling.

## 2. Move Field (207)

Move field from once class to another.

```javascript
class Customer {
  get plan() { return this._plan }
  get discountRate() { return this._discountRate }
```
⬇️
```javascript
class Customer {
  get plan() { return this._plan }
  get discountRate() { return this.plan.discountRate }
```

**Motivation**
When move a field:
- Pieces of data that are always passed to functions together are usually best put in a single record in order to clarify their relationship.
- If a change in one record causes a field in another record to change too, that is a sign of a field in the wrong place.
- If you have to update the same field in multiple structures, that is a sign that it should move to another place where it only needs to be updated once.

## 3. Move Statements into Function (213)

inverse of *[Move Statements To Callers (217)](#4-move-statements-to-callers-217)*

When statement is a part of called functions (always go together), move it inside the function.

```javascript
result.push(`<p>title: ${person.photo.title}</p>`)
result.concat(photoData(person.photo))

function photoData(aPhoto) {
  return [
    `<p>location: ${aPhoto.location}</p>`,
    `<p>date: ${aPhoto.data.toDateString()}</p>`
  ]
}
```
⬇️
```javascript
result.concat(photoData(person.photo))

function photoData(aPhoto) {
  return [
    `<p>title: ${aPhoto.title}</p>`,
    `<p>location: ${aPhoto.location}</p>`,
    `<p>date: ${aPhoto.data.toDateString()}</p>`
  ]
}
```

**Motivation**
- Remove duplicated code.

## 4. Move Statements To Callers (217)

inverse of *[Move Statements into Function (213)](#3-move-statements-into-function-213)*

Functions are the basic building block of the abstractions.  
When common behavior used in several places needs to vary in some of its call - You need to move the varying behavior out of the function -> to its callers.

```javascript
emitPhotoData(outStream, person.photo)

function emitPhotoData(outStream, photo) {
  outStream.write(`<p>title: ${photo.title}</p>\n`)
  outStream.write(`<p>location: ${photo.location}</p>\n`)
}
```
⬇️
```javascript
emitPhotoData(outStream, person.photo)
outStream.write(`<p>location: ${photo.location}</p>\n`)

function emitPhotoData(outStream, photo) {
  outStream.write(`<p>title: ${photo.title}</p>\n`)
}
```

**Motivation**
- Avoid behavior's duplication.

## 5. Replace Inline Code with Function Call (222)

Replace the inline code with a call to the existing function (for example - `includes`).

```javascript
let appliesToMass = false
for (const s of states) {
  if (s === "MA") appliesToMass = true
}
```

```javascript
appliesToMass = states.includes("MA")
```

**Motivation**
- Meaningful function name is easier to understand.

## 6. Slide Statements (223)

aliases *Consolidate Duplicate Conditional Fragments*

Move related code to near each other. Declare the variable just before you first use it.

> **Command-Query Separation (CQS)** principle: Every method should either be a command that performs an action (command - update), or a query that returns data to the caller, but NOT both. So, any function that returns a value is free of side effects. In other words, asking a question should not change the answer. 

```javascript
const pricingPlan = retrievePricingPlan()
const order = retreiveOrder()
let charge
const chargePerUnit = pricingPlan.unit // related to pricingPlan
```
⬇️
```javascript
const pricingPlan = retrievePricingPlan()
const chargePerUnit = pricingPlan.unit
const order = retreiveOrder()
let charge
```

**Motivation**
- It makes code easier to understand and easier to [Extract Function (106)](#1-extract-function-106).

## 7. Split Loop (227)

Split the loop which does two different things at once just because they can do that with on pass through a loop. Splitting the loop, you ensure you only need to understand the behavior you nee to modify.

> 📝 NOTE: Many programmers are uncomfortable with this refactoring, as it forces you to execute the loop twice. But remind to separate refactoring from optimization (Refactoring and Performance (64)) - Once you have your code clear, you’ll optimize it. And if the loop traversal is a bottleneck, it’s easy to join the loops back together. But the actual iteration through even a large list is rarely a bottleneck, and splitting the loops often enables other, more powerful, optimizations.

```javascript
let averageAge = 0
let totalSalary = 0
for (const p of people) {
  averageAge += p.age
  totalSalary += p.salary
}
averageAge = averageAge / people.length
```
⬇️
```javascript
let totalSalary = 0
for (const p of people) {
  totalSalary += p.salary
}

let averageAge = 0
for (const p of people) {
  averageAge += p.age
}
averageAge = averageAge / people.length
```

**Motivation**
- Easier to use.
- Easier to understand because each loop will do only 1 thing.

## 8. Replace Loop with Pipeline (231)

Collection Pipelines allow you to describe your processing as a series of operations, each consuming and emitting a collection.
Replace loop with collection pipeline, like:
- `map`, which uses a function to transform each element of the input collection and
- `filter`, which uses a function to select a **subset** of the input collection for later steps in the pipeline.

```javascript
const names = []
for (const i of input) {
  if (i.job === "programmer") { // replace with filter
    names.push(i.name) // replace with map that returns the name
  }
}
```
⬇️
```javascript
const names = input
  .filter(i => i.job === "programmer")
  .map(i => i.name)
```

**Motivation**
- Easier to understand the flow of data.

## 9. Remove Dead Code (237)

When code isn't used any more, comment out dead code or remove it directly.

```javascript
if (false) {
  doSomethingThatUsedToMatter()
}
```
⬇️
```javascript
// nothing jejeje
```

**Motivation**
- Easier and quicker for developer to understand the codebase.

# Chapter 9. Organizing data

## 1. Split Variable (240)

Any variable with more than one responsibility should be replaced with multiple variables - **one variable for each responsibility**.

```javascript
let temp = 2 * (height + width) //1st responsibility
console.log(temp)
temp = height * width // 2nd responsibility
console.log(temp)
```
⬇️
```javascript
const perimeter = 2 * (height + width)
console.log(perimeter)
const area = height * width
console.log(area)
```

**Motivation**
- Easier to understand

## 2. Rename Field (244)

Names are important, and field names in record structures can be especially important
when those record structures are widely used across a program. Data structures are really important in understanding the code.

```javascript
class Organization {
  get name() {...}
}
```
⬇️
```javascript
class Organization {
  get title() {...}
}
```

## 3. Replace Derived Variable With Query (248)

Remove any variables which cloud be easily calculate.

```javascript
get discountedTotal() { return this._discountedTotal }
set discount(aNumber) {
  const old = this._discount
  this._discount = aNumber
  this._discountedTotal += old - aNumber
}
```
⬇️
```javascript
get discountedTotal() { return this._baseTotal - this._discount }
set discount(aNumber) { this._discount = aNumber }
```

**Motivation**
- Minimize scope of mutable data at much as possible.
- Often a calculate makes it clearer what the meaning of data is, and it's protected from being corrupted when you fail to update the variable as the source data changes.

## 4. Change Reference To Value (252)

inverse of *[Change Value To Reference (256)](#5-change-value-to-reference-256)*

Treat data as *value*. When update, replace entire inner object with a new one (a copy).
When you nest an object, or data structure, within another you can treat the inner object as a reference or as a value.  
The difference is in how you handle updates of the inner object’s properties. 
- If you treat it as a **reference** (memory link), you’ll update the inner object’s property keeping the same inner object.
- If you treat it as a **value**, you will replace the entire inner object with a new one(a copy) that has the desired property.

Value objects are immutable. You can replicate values around your program and not worry about maintaining memory links.  
Value objects are especially useful in distributed and concurrent systems.  
BUT if you want to share an object between several objects so that any change to the shared object is visible to all its collaborators, then you need the shared object to be a reference.

```javascript
class Product {
  applyDiscount(arg) { this._price.amount -= arg }
}
```
⬇️
```javascript
class Product {
  applyDiscount(arg) {
    this._price = new Money(this._price.amount - arg, this._price.currency)
  }
}
```
> Remind for test value-based equality: `==` same value and `===` same reference in memory.

**Motivation**
- Immutable data is easier to deal with

## 5. Change Value To Reference (256)

When you need to share an object in different places, or have duplicated objects and you want to update them.

A data structure may have several records linked to the same logical data structure.  
If you need to update the share data, with physical copies, you have to update all the copies and if you miss one, you will get a troubling inconsistency in your data.

```javascript
let customer = new Customer(customerData)
```
⬇️
```javascript
let customer = customerRepository.get(customerData.id)
```

**Motivation**
- Update one reference is easier and more consistent than update multiple copies.

# Chapter 10. Simplifying conditional logic
## 1. Decompose Conditional (260)

When the code do various things depending on various conditions (complicated conditional) - Decompose condition and replacing each chunk of code with a function call.

```javascript
if (!aDate.isBefore(plan.summerStart) && !aDate.isAfter(plan.summerEnd)) // replace with summer()
  charge = quantity * plan.summerRate // replace with summerCharge()
else
  charge = quantity * plan.regularRate + plan.regularServiceCharge // replace with regularCharge()
```
⬇️
```javascript
if (summer()) 
  charge = summerCharge()
else
  charge = regularCharge()
```

**Motivation**
- Clearer intention of what you are branching on.

## 2. Consolidate Conditional Expression (263)

When you have different conditions that return same resulting action. Consolidate different condition check which the result action is same to a single condition check with single result.  
Don't apply this refactor if you consider that the checks are independent.

```javascript
if (anEmployee.seniority < 2) return 0
if (anEmployee.monthsDisabled > 12) return 0;
if (anEmployee.isPartTime) return 0
```
⬇️
```javascript
if (isNotEligableForDisability()) return 0

function isNotEligableForDisability() {
   return ((anEmployee.seniority < 2)
          || (anEmployee.monthsDisabled > 12)
          || (anEmployee.isPartTime))
}
```

**Motivation**
- Often lead to [Extract Function (106)](#1-extract-function-106), which reveal instead of the code by function name
- If conditions are not related, don't consolidate them

## 3. Replace Nested Conditional with Guard Clauses (266)

If the condition is an **unusual** condition, check the condition (Guard Clause) and return if it’s true.  
But if both conditions are part of **normal** behavior, use a condition with an `if` and an `else` leg.  
Guard clause says: “This isn’t the core to this function, and if it happens, do something and get out.”

```javascript
function getPayAmount() {
  let result
  if (isDead)
    result = deadAmount()
  else {
    if (isSeparated) {
      result = separatedAmount()
    } else {
      if (isRetired)
        result = retiredAmount()
      else
        result = normalPayAmount()
    }
  }
  return result
}
```
⬇️
```javascript
function getPayAmount() {
  if (isDead) return deadAmount()
  if (isSeparated) return separatedAmount()
  if (isRetired) return retiredAmount()
  return normalPayAmount()
}
```

**Motivation**
- It shows conditional branch are normal or unusual.
- To clarify some pre-checks before the main processing.

## 4. Replace Conditional with Polymorphism (272)

When you have a conditional that chooses different behavior depending on the type of an object. Use object oriented class instead of complex conditional logic/switch.  
Move each leg of the conditional to an overriding method in a subclass. Make the original method abstract.

Common cases:
1. When you can form a set of types, each handling the conditional logic differently.  
**Solution**: remove the duplication of the common switch logic by creating classes for each case and use polymorphism to bring out the type­specific behavior.
2. When you can think of the logic as a base case with variants.  
**Solution**: Put the base case logic into a superclass and each variant case into a subclass.
3. When you see complex conditional logic.


```javascript
switch (bird.type) {
  case 'EuropeanSwallow':
    return 'average'
  case 'AfricanSwallow':
    return (bird.numberOfCoconuts) > 2 ? 'tired' : 'average'
  case 'NorwegianBlueParrot':
    return (bird.voltage > 100) ? 'scorched' : 'beautiful'
  default:
    return 'unknown'
}
```
⬇️
```javascript
class EuropeanSwallow {
  get plumage() {
    return 'average'
  }
}
class AfricanSwallow {
  get plumage() {
    return (this.numberOfCoconuts > 2) ? 'tired' : 'average'
  }
}
class NorwegianBlueParrot {
  get plumage() {
    return (this.voltage > 100) ? 'scorched' : 'beautiful'
  }
}
```

**Motivation**
- Using classes and polymorphism make the separation more explicit.

## 5. Introduce Special Case (289)

aliases *Introduce Null Object*

When uses conditionals for special cases, such as nulls - create a special object with methods for all the common behavior.  
When many users of a data structure check a specific value, and then most of them do the same thing - bring special check case to a single place.

```javascript
if (aCustomer === "unknown") customerName = "occupant"
```
⬇️
```javascript
class UnknownCustomer {
  get name() { return "occupant" }
}
```

**Motivation**
- Remove duplicate code.
- Easy to add additional behavior to special object.

## 6. Introduce Assertion (302)

> 📝 NOTE: An assertion is a conditional statement that is assumed to be always true. Failure of an assertion indicates a programmer error.

When you want to communicate and check a state of the program, make the assumption explicit by writing an assertion. 
When sections of code work only if certain conditions are true.

```javascript
if (this.discountRate) {
  base = base - (this.discountRate * base)
}
```
⬇️
```javascript
assert(this.discountRate >= 0)
if (this.discountRate) {
  base = base - (this.discountRate * base)
}
```

**Motivation**
- Reader can understand the assumptions that the code is making.
- Help in debugging because assertions can help catch bugs closer to their origin.

# Chapter 11. Refactoring APIs

APIs (*Application Programming Interfaces*) are the joints that you use to plug modules and their functions together.

## 1. Separate Query from Modifier (306)

When you have a method that returns a value but also changes the state of an object - separate function that returns a value (query only) and function with *observable* side effects like modify data. 

> 📝 NOTE: *observable* side effects! A common optimization is to cache the value of a query in a field so that repeated calls go quicker. Although this, changes the state of the object with the cache, *the change is not observable*. Any sequence of queries will always return the same results for each query. 

```javascript
function getTotalOutstandingAndSendBill() {
  const result = customer.invoices.reduce((total, each) => each.amount + total, 0)
  sendBill()
  return result
}
```
⬇️
```javascript
function totalOutstanding() {
  return customer.invoices.reduce((total, each) => each.amount + total, 0)  
}
function sendBill() {
  emailGateway.send(formatBill(customer))
}
```

**Motivation**
- Easy to test and reuse an immutable function (query only).
- Signaling methods with side effects and those without.

## 2. Parameterize Function (310)

aliases *Parameterize Method*

When functions carry out similar logic with different literal values - remove duplication using a single function with parameters for the different values.

```javascript
function tenPercentRaise(aPerson) {
  aPerson.salary = aPerson.salary.multiply(1.1)
}
function fivePercentRaise(aPerson) {
  aPerson.salary = aPerson.salary.multiply(1.05)
}
```
⬇️
```javascript
function raise(aPerson, factor) {
  aPerson.salary = aPerson.salary.multiply(1 + factor)
}
```

**Motivation**
- Increase usefulness/flexibility of the function.
- Remove duplicate code.

## 3. Remove Flag Argument (314)

aliases *Replace Parameter with Explicit Methods*

A *flag argument* is a function argument that the caller uses to indicate which logic the called function should execute.  
When parameters are a signal of an entirely different behavior (literal flag) - Remove *literal* flag argument by explicit function for the task you want to do.

> 📝 NOTE: Not all arguments are flag arguments. To be a flag argument, the callers must be setting the boolean value to a literal value, not data that is flowing through the program. Also, the implementation function must be using the argument to influence its control flow, not as data that it passes to further functions.

```javascript
function setDimension(name, value) {
  if (name === 'height') {
    this._height = value
    return
  }
  if (name === 'width') {
    this._width = value
    return
  }
}
```
⬇️
```javascript
function setHeight(value) { this._height = value }
function setWidth(value) { this._width = value }
```

**Motivation**
- Easy to read and understand code.
- Be careful if flag argument appears more than 1 time in the function, or is passed to further function.

## 4. Preserve Whole Object (319)

When several values from a record are passed as parameters in a function - replace those values with the whole record itself, letting the function body derive the values it needs.

> 📝 NOTE: If function and object are in different modules, the function will have a dependency on the whole object, so it will make tight coupling if you apply this refactor.

When an object calls another object with several of its own data values - replace those values with a self ­reference (`this` in JavaScript).

```javascript
const low = aRoom.daysTempRange.low
const high = aRoom.daysTempRange.high
if (aPlan.withinRange(low, high))
```
⬇️
```javascript
if (aPlan.withInRange(aRoom.daysTempRange))
```

**Motivation**
- Don't need to add additional parameter if function needs more data in the future.
- Reduce size of the parameter list.

## 5. Replace Parameter with Query (324)

aliases *Replace Parameter with Method*

inverse of *[Replace Query with Parameter (327)](#6-replace-query-with-parameter-327)*

When a call passes in a value that the function can just as easily determine for itself, that is a form of duplication — one that unnecessarily complicates the caller which has to determine the value of a parameter when it could be freed from that work. 

So, when the value of the parameter you want to remove is determined merely by querying another parameter in the list - remove unnecessary parameter and resolve it in the called function.


```javascript
availableVacation(anEmployee, anEmployee.grade)

function availableVacation(anEmployee, grade) {
  // calculate vacation...
}
```
⬇️
```javascript
availableVacation(anEmployee)

function availableVacation(anEmployee) {
  const grade = anEmployee.grade
  // calculate vacation...
}
```

**Motivation**
- Shorter list of parameters.
- Simpler work for the caller (because fewer parameters).
- Be careful because it can increase function's dependency.

## 6. Replace Query with Parameter (327)

inverse of *[Replace Parameter with Query (324)](#5-replace-parameter-with-query-324)*

When an internal reference should be passed as a parameter.  
When a reference to a global variable, or to an element in the same module that you intend to move away - replace the internal reference with a parameter, shifting the responsibility of resolving the reference to the caller of the function.

It’s easier to reason about a function that will always give the same result when called with same parameter values — this is called referential transparency. Check the NOTE.  
If a function accesses some element in its scope that isn’t referentially transparent, then the containing function also lacks referential transparency - you can fix that by moving that element to a parameter.

> 📝 NOTE: A common pattern is to have modules consisting of pure functions which are wrapped sby logic that handles the I/O and other variable elements of a program. Remind that **pure functions** are functions that, given the same input (args), always return the same output (values) and don't have side effects.

BUT, by moving a query to a parameter, you force your caller to figure out how to provide this value. And you need to try to design interfaces that make life easier for their consumers.

```javascript
targetTemperature(aPlan)

function targetTemperature(aPlan) {
  currentTemperature = thermostat.currentTemperature
  // rest of function...
```
⬇️
```javascript
targetTemperature(aPlan, thermostat.currentTemperature)

function targetTemperature(aPlan, currentTemperature) {
  // rest of function...
```

**Motivation**
- Reduce function's dependency.
- Create more pure functions.

## 7. Remove Setting Method (331)

A class is a common form of module, so try to make the objects as immutable as possible - make a field immutable by removing setting method. In this way, the field is set only in the constructor, making it clear that updates make no sense after construction.

```javascript
class Person {
  get name() {...}
  set name(aString) {...}
}
```
⬇️
```javascript
class Person {
  get name() {...}
}
```

## 8. Replace Constructor with Factory Function (334)

aliases *Replace Constructor with Factory Method*

When a caller asks for a new object and you need more flexibility than a simple constructor gives - replace the constructor with Factory function.

```javascript
leadEngineer = new Employee(document.leadEngineer, 'E')
```
⬇️
```javascript
leadEngineer = createEngineer(document.leadEngineer)
```

**Motivation**
- You want to do more than simple construction (can only return an instance of the object that is asked for) when you create an object.


## 9. Replace Function with Command (337)

aliases *Replace Method with Method Object*
inverse of *[Replace Constructor with Factory Function (334)](#8-replace-constructor-with-factory-function-334)*

When you need to break down a particularly complex function that passes a lot of data around - Encapsulate function/request into its own object (command object), which makes it easier to use [Extract Function (106)](#1-extract-function-106) on the function’s body.  
A **command object** is build around a single method, whose request and execution is the purpose of the object.
So, when you must handle complex computations - broken down into separate methods:
- sharing common state through the fields 
- they can be invoked via different methods for different effects
- they can have their data built up in stages

BUT, this refactor adds complexity, so you should use command object when you specifically need a facility that simpler approaches can't provide.


```javascript
function score(candidate, medicalExam, scoringGuide) {
  let result = 0
  let healthLevel = 0
  // long body code
}
```
⬇️
```javascript
class Scorer {
  constructor(candidate, medicalExam, scoringGuide) {
    this._candidate = candidate
    this._medicalExam = medicalExam
    this._scoringGuide = scoringGuide
  }

  execute() {
    this._result = 0
    this._healthLevel = 0
    // long body code
  }
}
```

**Motivation**
- Commands objects can have complimentary operations, such as undo.
- Can provide methods to build up their parameters to have richer lifecycle.
- Can build customization using inheritance and hooks.
- More flexibility - Easily break down a complex function into simpler methods, which can also be called directly while testing and debugging.

## 10. Replace Command with Function (344)

When you are not handling complex computations, when you simplify the function and no longer need it as a command object - turn it back into a function.

```javascript
class ChargeCalculator {
  constructor (customer, usage){
    this._customer = customer
    this._usage = usage
  }
  execute() {
    return this._customer.rate * this._usage
  }
}
```
⬇️
```javascript
function charge(customer, usage) {
  return customer.rate * usage
}
```

**Motivation**
- Function call is simpler than command object.

# Chapter 12. Dealing with 

Inheritance is a mechanism to express some objects whose behavior varies from category to category.
Downside from inheritance:
- You can only use for a single axis of variation. for example: if you want to vary behavior of people by their age category and by their income level, you can either have subclasses for young and senior, or for well-off and poor, you can't have both.
- Introduces coupling between classes. Any change in the parent can easily break children.

## 1. Pull Up Method (350)

inverse of *[Push Down Method (359)](#4-push-down-method-359)*

Move similar methods in subclasses to superclass.
When there are two methods that can be parameterized, through *[Parameterize Function (310)](#2-parameterize-function-310)*, in such a way that they end up as essentially the same method.

If you have two methods with a similar *overall flow*(steps in the same order), but differing in details, you should consider the [Form Template Method](https://www.refactoring.com/catalog/formTemplateMethod.html) -> get the steps into methods with the same signature, so that the original methods become the same. Then you can pull them up.  
Example: you have 2 subclasses `ResidentialSite` and `LifelineSite` which have same method, `getBillableAmount`, but with some differences in the body, specifically in the calculation of the Base amount and Tax amount.  
So, you separate the steps of get amount and taxes in different methods(for example: `getBaseAmount` and `getTaxAmount`), and push `getBillableAmount`, `getBaseAmount` and `getTaxAmount` to the superclass `Site`, and the subclasses implement specific details for `getBaseAmount` and `getTaxAmount`.


```java
class Employee {...}

class Salesman extends Employee {
  get name() {...}
}

class Engineer extends Employee {
  get name() {...}
}
```
⬇️
```java
class Employee {
  get name() {...}
}

class Salesman extends Employee {...}
class Engineer extends Employee {...}
```

**Motivation**
- Eliminate duplicate code in subclasses.
- If two methods has similar workflow, consider using Template Method Pattern

## 2. Pull Up Field (353)

inverse of *[Push Down Field (361)](#5-push-down-field-361)*

Pull up similar field to superclass to remove duplication.

```java
class Employee {...} //Java

class Salesman extends Employee {
  private String name;
}

class Engineer extends Employee {
  private String name;
}
```
⬇️
```java
class Employee {
  protected String name;
}

class Salesman extends Employee {...}
class Engineer extends Employee {...}
```

## 3. Pull Up Constructor Body (355)

When you have constructors on subclasses with mostly identical bodies. But, constructors have special rules about what can be done in what order, so you can't [Extract Function (106)](#1-extract-function-106) and [Pull Up Method (350)](#1-pull-up-method-350) directly.

Create a superclass constructor; call this from the subclass methods.

```javascript
class Party {...}

class Employee extends Party {
  constructor(name, id, monthlyCost) {
    super()
    this._id = id
    this._name = name
    this._monthlyCost = monthlyCost
  }
}
```
⬇️
```javascript
class Party {
  constructor(name){
    this._name = name
  }
}

class Employee extends Party {
  constructor(name, id, monthlyCost) {
    super(name)
    this._id = id
    this._monthlyCost = monthlyCost
  }
}
```

## 4. Push Down Method (359)

inverse of *[Pull Up Method (350)](#1-pull-up-method-350)*

If method is only relevant to one subclass (or a small portion of subclasses), moving it from superclass to subclass.

```javascript
class Employee {
  get quota {...}
}

class Engineer extends Employee {...}
class Salesman extends Employee {...}
```
⬇️
```javascript
class Employee {...}
class Engineer extends Employee {...}
class Salesman extends Employee {
  get quota {...}
}
```

## 5. Push Down Field (361)

inverse of *[Pull Up Field (353)](#2-pull-up-field-353)*

If field is only used in one subclass, move it to those subclasses.

```java
class Employee { //Java
  private String quota;
}

class Engineer extends Employee {...}
class Salesman extends Employee {...}
```
⬇️
```java
class Employee {...}
class Engineer extends Employee {...}

class Salesman extends Employee {
  protected String quota;
}
```

## 6. Replace Type Code with Subclasses (362)

aliases *Replace Type Code with State/Strategy, Extract Subclass*

inverse of *[Remove Subclass (369)](#7-remove-subclass-369)*

Subclasses support variations in data structure and polymorphic behavior.

When you have field to trigger different behavior based on its value (`new Employee(name, type)`) - replace it with subclasses (`Engineer`, `Salesman`, `Manager`).

When you have several functions that invoke different behavior depending on the value of the type code. Allow you to use polymorphism to handle conditional logic (several functions) - easily to apply Replace Conditional with Polymorphism later.

When you have fields or methods that are only valid for particular values of a type code. (for example: sales quote fields is just valid for "salesman" type code).

BUT, you can't use direct subclasses if the type is mutable.

```javascript
function createEmployee(name, type) {
  return new Employee(name, type) //type code
}
```
⬇️
```javascript
function createEmployee(name, type) {
  switch (type) { 
    case "engineer": return new Engineer(name)
    case "salesman": return new Salesman(name)
    case "manager":  return new Manager (name)
  }
}
```

**Motivation**
- Execute different code depending on the value of a type

## 7. Remove Subclass (369)

aliases *Replace Subclass with Fields*
inverse of *[Replace Type Code with Subclasses (362)](#6-replace-type-code-with-subclasses-362)*

You have subclasses do to little. Replace the subclass with a field in superclass.

```javascript
class Person {
  get genderCode() {return "X"}
}
class Male extends Person {
  get genderCode() {return "M"}
}
class Female extends Person {
  get genderCode() {return "F"}
}
```
⬇️
```javascript
class Person {
  get genderCode() {return this._genderCode}
}
```

## 8. Extract Superclass (375)

If two classes do similar things (same intent), create superclass and move these similarities to superclass.

```javascript
class Department {
  get totalAnnualCost() {...}
  get name() {...}
  get headCount() {...}
}

class Employee {
  get annualCost() {...}
  get name() {...}
  get id() {...}
}
```
⬇️
```javascript
class Party {
  get name() {...}
  get annualCost() {...}
}

class Department extends Party {
  get annualCost() {...} //because implementation is different
  get headCount() {...}
}

class Employee extends Party {
  get annualCost() {...} //because implementation is different
  get id() {...}
}
```

**Motivation**
- Remove duplication.
- Prepare for Replace Superclass with Delegate refactor.

## 9. Collapse Hierarchy (380)

Merge superclass and subclass when there are no longer different enough to keep them separate.

```javascript
class Employee {...}
class Salesman extends Employee {...}
```
⬇️
```javascript
class Employee {...}
```

## 10. Replace Subclass with Delegate (381)

Most of the time it's better to use Inheritance but if you can't use it because, for example you can only use inheritance once (for one type), you can transform it to Delegate.

Delegation handles both problems of inheritance (just a single axis of variation and coupling between classes) cause you can delegate to many different classes for different reasons and delegation is a regular relationship between objects(less coupling than subclassing).

"Favor object composition over class inheritance" (where composition is effectively the same as delegation) -> “Favor a judicious mixture of composition and
inheritance over either alone”

Sometimes, inheritance handles some situations well, whereas using delegation involves adding dispatch logic, two­way references, and thus extra complexity. The refactoring may still be worthwhile, since the advantage of a mutable field, or a need to use inheritance for other purposes, may outweigh the disadvantage of losing inheritance.

```javascript
class Order {
  get daysToShip() {
    return this._warehouse.daysToShip
  }
}

class PriorityOrder extends Order {
  get daysToShip() {
    return this._priorityPlan.daysToShip
  }
}
```
⬇️
```javascript
class Order {
  get daysToShip() {
    return (this._priorityDelegate)
      ? this._priorityDelegate.daysToShip
      : this._warehouse.daysToShip
  }
}

class PriorityOrderDelegate {
  get daysToShip() {
    return this._priorityPlan.daysToShip
  }
}
```

**Motivation**
- If there are more than 1 reason to vary something, inheritance is not enough.
- Inheritance introduce very close relationship.

## 11. Replace Superclass with Delegate (399)

aliases *Replace Inheritance with Delegation*

If functions of the superclass don’t make sense on the subclass, replace with with delegate.  
A classic examples of mis-­inheritance was making a stack be a subclass of list. The idea that led to this was reusing of list’s data storage and operations to manipulate it. While it’s good to reuse, this inheritance had a problem:  
All the operations of the list were present on the interface of the stack, although most of them were not applicable to a stack.  
A better approach is to make the list into a field of the stack and delegate the necessary operations to it.

With **Replace Superclass with Delegate**, you avoid the highly coupled relationship between sub­ and superclass, with the subclass easily broken by changes in the superclass.  
BUT, you need to write a forwarding function for any function that is the same in the host and in the delegate.

So, mostly use inheritance first, and apply **Replace Superclass with Delegate** when, and if, it becomes a problem.

```javascript
class List {...}
class Stack extends List {...}
```
⬇️
```javascript
class Stack {
  constructor() {
    this._storage = new List();
  }
}
class List {...}
```

**Motivation**
- Easier to maintain code.

---
I have learned many things from this book and I hope it helps you as much as it helped me! 🤗 🤍

---

Content from [Refactoring: Improving the Design of Existing Code, 2nd edition](https://refactoring.com/) by Martin Fowler, with Kent Beck.   
Visit https://martinfowler.com/books/refactoring.html.  
Copyright ©️ 2019 Pearson Education, Inc.