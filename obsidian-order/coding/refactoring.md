# refactoring
Refactoring: A change made to the internal structure of software to make it easier to understand and cheaper to modify without changing its observable behavior (Martin Fowler)
***
# What is Refactoring?

According to Martin Fowler, refactoring is a technique to make changes from existing program code by changing algorithms without changing the behavior of business processes. Changes that occur are not felt by the user but are behind the scenes or back-end processes.

Refactoring poses risks, changes that occur in program code can cause new problems or bugs if not done properly and can take days, even months. Refactoring is riskier when it is run irregularly or systematically. Start digging for information on algorithms or program functions, and then find opportunities for refactoring_,_ and the deeper you try to dig up information, the more changes are made.
***
“I_f someone says their code was broken for a couple of days while they are refactoring, you can be pretty sure they were not refactoring”._ ~ _Martin Fowler, Refactoring: Improving the Design of Existing Code_

_“When you have to add a feature to a program but the code is not structured in a convenient way, first refactor the program to make it easy to add the feature, then add the feature. “ ~ Martin Fowler, Refactoring: Improving the Design of Existing Code_
***
### why?
**Improving Software Design**
**Makes Software Easier to Understand**
**Helps Software Engineers Find Bugs**
***
# Why is Refactoring done if the program code is working fine?

The main purpose of refactoring is to make program code easier to maintain in the future and to complement programs that are made in perfunctory (works mostly) or technical debt. In addition, the purpose of refactoring is not to add new functionality or remove existing programs, but to improve the design that was first created, rather difficult architecture, in the beginning, is completely perfect.
***
## time to refactor?
1.  Finding program logic that is made repeatedly or declaring the same code structure over and over again.
2.  Some software engineers have problems with a function or class in writing program features.
3.  Spending more time identifying bugs or errors than creating the program itself.
4.  It’s not always the system that was first created according to user needs or stable as users grow.


***
# **The smell of technical debt**

_Over time many of our projects start to develop a certain smell. For some of us we can’t smell our own code but we just know there’s something off and we can’t quite point it out. There are certain indicators that do make it a little more obvious._

1.  **Feature creep**: _current expectations excede the original assumptions._
2.  **Cognitive load**: _it’s too hard to trace the logic or data flow._
3.  **Difficulty skyrockets**: _simple changes take too long or seem impossible._
4.  **Performance conundrums**: _you just can’t figure out why it’s slow._
5.  **Best practices**: _they changed again and your code starts to look dated._
***
# Best practices for refactoring code

## 1. Set Clearly Defined Objectives

Before coding refactorings begin, be sure to clearly define the scope and targets. You should also consider what and what not to refactor before refactoring. Set deadlines and workable targets that align with the current workflow, such as the CI/CD process being used in the company. Plan and set clear and well-defined objectives that are not related to other tasks.

## 2. Identify problem areas

Identifying weaknesses in the code is the first step in improving it. This might be anything from disparate variable names to entire sections of code that are difficult to comprehend.

## 3. Make small changes

It is critical to make small, incremental changes when refactoring code. This will ensure that your code remains stable and that you can easily revert your modifications if necessary.

## 4. Test, test, and test — early and often

Although refactoring doesn’t alter the functionality of the software, it still requires test coverage to ensure none of its functions have been changed. After refactoring, you must verify that the code hasn’t introduced additional problems.

## 5. Use refactoring tools

There are numerous refactoring tools available. These tools can assist you in automating some of the refactoring procedures and making it easier to revert your modifications if necessary.

Here are some popular refactoring tools:
***


-   [Eclipse IDE](https://www.eclipse.org/eclipseide/)
-   [Visual studio intellicode](https://visualstudio.microsoft.com/de/services/intellicode/)
-   [Spring Tool Suite 4](https://spring.io/tools#main)
-   [Rider](https://www.jetbrains.com/dotnet/guide/products/rider/)
-   [IntelliJ IDEA](https://www.jetbrains.com/idea/download/?fromIDE=#section=mac)
-   [SonarQube](https://www.sonarqube.org/)
-   [Stepsize](http://stepsize.com/)

## 6. Document your changes

Be certain to document your changes once you’ve finished refactoring. This will help other developers understand why the code was changed and what the new structure is.

## 7. Use a Source Control System

It’s critical to use a source control system when refactoring code so that you can easily revert to a previous version if something goes wrong. This may save you a lot of time and frustration in the event that you make a mistake.

#refactor #refactoring #coding #fowler