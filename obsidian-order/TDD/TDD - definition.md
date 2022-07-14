# TDD - definition
TDD:[Test-Driven Development](https://semaphoreci.com/blog/test-driven-development) (TDD) is a software design practice in which a developer writes tests before code. By inverting the usual order in which software is written, a developer can think of a problem in terms of inputs and outputs and write more testable (and thus more modular) code.

The TDD cycle consists of three steps:

1.  **Red**: write a test that fails.
    
2.  **Green**: write the minimal code that passes the test.
    
3.  **Refactor**: improve the code, and make it more abstract, readable, and optimized.
<hr>
TDD is a process in which software requirements are converted into test cases BEFORE the software is fully developed.
***
Tests are a good documentation of what a piece of code is supposed to do.
***
Test-Driven Development (TDD) is the practice of designing applications and systems that are resilient to defects and new problems.
***
Testing is simply analyzing and sampling a software to find and remove issues from software. Testing is normally done for the following reasons:

-   If it meets the requirements that guided its design and development
-   If it responds correctly to all kinds of inputs
-   Checking the security of the system.
-   To check if it performs its functions within an acceptable time
-   To check if it is sufficiently usable
-   To check if it can be installed and run in its intended environments

There are different types of testing commonly used which include: black box and white box testing, visual testing, Automated testing, grey box testing and many more.

During testing there are also levels that are followed: Unit Testing, Integration Testing, System Testing, Acceptance Testing which I will be discussing more in the coming blog in part 2 of this blog post.

Check this out:

[https://en.wikipedia.org/wiki/Software_testing](https://en.wikipedia.org/wiki/Software_testing)

**Test Driven Development and Unit Testing**

Unit testing is where parts of are tested its main aim is to improve the design and finding problems in the code.

Test driven development is where a code design technique where the programmer writes a test before any production code, and then writes the code that will make that test pass. Its normally done by adding a test then run all tests and see if the new one fails, Writing some code, Running tests, Refactoring code and always Repeating the procedure.

[https://en.wikipedia.org/wiki/Test-driven_development](https://en.wikipedia.org/wiki/Test-driven_development)

[https://en.wikipedia.org/wiki/Unit_testing](https://en.wikipedia.org/wiki/Unit_testing)

**Debugging**

Is the process of identifying and removing errors from code

[https://en.wikipedia.org/wiki/Debugging](https://en.wikipedia.org/wiki/Debugging)

**Maintaining Code**

Its mainly done by writing clean code.

[https://simpleprogrammer.com/maintaining-code/](https://simpleprogrammer.com/maintaining-code/)

**Version/Source Control**

Source control basically involves tracking and managing any change in your code, software documents, programs e.t.c. Currently there are many systems that helps in source control. To master this you have to be familiar with these terms Baseline, Branch, list Checkout, Clone, Commit, Conflict, Delta compression, Dynamic stream Export, Fetch, Forward integration, Head, Import, Initialize, Interleaved ,deltas, Label and many more others.

**Benefits of using version/source control**

-   It helps you to manage the source code of your project.
-   It improves visibility.
-   Helps teams collaborate around the world.
-   Accelerates product delivery.

[https://en.wikipedia.org/wiki/Version_control](https://en.wikipedia.org/wiki/Version_control)

There are several types of version control systems that teams use t. Here are a few of the most commonly used ones.

-   Git
-   Gitlab
-   CVS Version Control
-   Bitbucket
-   Apache subversion
-   Mercurial

**Continuous Integration/CD**

Continuous Integration

is the practice of integrating changes from different developers in the team into a mainline as early as possible, in best cases several times a day This makes sure the code individual developers work on doesn’t divert too much. When you combine the process with automated testing, continuous integration can enable your code to be dependable.

Continuous Deployment

is closely related to Continuous Integration and refers to keeping your application deployable at any point or even automatically releasing to a test or production environment if the latest version passes all automated tests.

Commonly used Softwares:Jenkins,Hudson,Travis CI, Buddy,TeamCity,Jenkins,Travis CI,Bamboo,GitLab CI,CircleCI.

[https://en.wikipedia.org/wiki/Continuous_integration](https://en.wikipedia.org/wiki/Continuous_integration)

[https://codeship.com/continuous-integration-essentials](https://codeship.com/continuous-integration-essentials)
***
Testing is simply analyzing and sampling a software to find and remove issues from software. Testing is normally done for the following reasons:

-   If it meets the requirements that guided its design and development
-   If it responds correctly to all kinds of inputs
-   Checking the security of the system.
-   To check if it performs its functions within an acceptable time
-   To check if it is sufficiently usable
-   To check if it can be installed and run in its intended environments

There are different types of testing commonly used which include: black box and white box testing, visual testing, Automated testing, grey box testing and many more.
***
![[tdd-cycle.png]]
***
![[tdd-pyramid.png]]
***
![[TDD/img/test life cycle.png]]
![[test.png]]
***


# Why it’s important?

-   Having tests coverage will help you to refactor your code. Because you have tests to figure out if your refactoring broke nothing, you can do it as you want. You can take the risk to refactor, without risk, because it’s tested !
-   Writing test before writting production code will make you wrote only the part of code you need, no dead code. If you limit the amount of code, you make obviously it clearer, so cleaner.
-   In TDD, your tests are “Intent-based”. That means your tests will describe what is the attended comportement of your code, awareless of the details implementations. This has two advantages, first, refactor will not break all your tests each times (because tests are awareless of implementation). Second, your tests will serve as a living code documentation.

***



![[tdd-cycle-2.png]]
***

#tests #defintion #TDD #tdd
