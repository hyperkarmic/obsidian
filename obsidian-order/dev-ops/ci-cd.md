# CI/CD

_CI/C__D:_ **CI/CD** _is a method to frequently deliver apps to customers by_ **introducing automation into the stages of app development**_. The main concepts attributed to_ **CI/CD** _are_ **continuous integration**_,_ **continuous delivery**_, and_ **continuous deployment**_._ **CI/CD** _is a solution to the problems integrating new code can cause for development and operations teams_

**Continuous Intergaration (CI):****[Continuous Integration](https://semaphoreci.com/continuous-integration)** **(CI) is a software development methodology where developers — following the trunk-based model — merge their changes to the main branch many times per day.**

CI is supported by automated tests and a build server that runs them on every change. As a result, failures are made visible as soon as they are introduced and can be fixed within minutes.

**Continuous integration** is a practice that occurs when a developer commits code changes to GitHub or another code repository. As a result of this event, specific actions are triggered that check the code to ensure that it integrates easily with the existing codebase. This could happen frequently or at predetermined periods. The primary goal is to uncover integration issues and enforce quality checks to establish greater cohesiveness and development collaboration.

***
**[Continuous delivery](https://semaphoreci.com/blog/2017/07/27/what-is-the-difference-between-continuous-integration-continuous-deployment-and-continuous-delivery.html)****: is an extension of CI. Its goal is to automate every step required to package and release a piece of software. The output of a continuous delivery pipeline takes the form of a deployable binary, package, or container.**
***

**Continuous deployment:** is an optional step-up from continuous delivery. 

***
# Why CI/CD?

How does CI/CD improve the software development cycle now that we've seen it? What are the advantages over other methods? So, let's look at the power that CI/CD possesses.

1.  **Quick Delivery**: Making changes, reverting changes, and deploying hotfixes are all accomplished with a single click, triggered by a developer action.
2.  **Reliability**: At the heart of automation is the elimination of human inefficiencies. With CI/CD, testers can detect bugs early in the development process and fix them rapidly.
3.  **High-quality code**: CI/CD allows developers to contribute code to a centralized repository where they can collaborate on detecting and correcting the most severe bugs.
4.  **Customer Satisfaction**: Because things are moving so quickly, clients are happy, and happy clients consume more and help you build a brand.
5.  **Increased workforce productivity**: Automated tests, deployments, and collaboration foster a positive work environment and flexible development that keeps the needle moving.

Everyone is happy and productive when CI/CD is implemented.
***
An end-user creates a software specification. A CI algorithm is developed to identify all the required software components. The software components are tested to ensure they meet the requirements, the software components are deployed. The software is integrated and tested to ensure that they are working correctly.
***
Continuous integration (CI) and continuous delivery (CD), also known as CI/CD, embodies a culture, operating principles, and a set of practices that application development teams use to deliver code changes more frequently and reliably.

CI/CD is [a best practice for devops teams](https://www.infoworld.com/article/3268053/devops-best-practices-the-5-methods-you-should-adopt.html). It is also a best practice in [agile methodology](https://www.infoworld.com/article/3237508/what-is-agile-methodology-modern-software-development-explained.html). By automating integration and delivery, CI/CD lets software development teams focus on meeting business requirements while ensuring code quality and software security.
***
## CI/CD defined

[Continuous integration](https://www.infoworld.com/article/3295900/what-is-continuous-integration-ci-faster-better-software-development.html) is a coding philosophy and set of practices that drive development teams to frequently implement small code changes and check them in to a version control repository. Most modern applications require developing code using a variety of platforms and tools, so teams need a consistent mechanism to integrate and validate changes. Continuous integration establishes an automated way to build, package, and test their applications. Having a consistent integration process encourages developers to commit code changes more frequently, which leads to better collaboration and code quality.

_Continuous delivery_ picks up where continuous integration ends, and automates application delivery to selected environments, including production, development, and testing environments. Continuous delivery is an automated way to push code changes to these environments.
***
**Continuous Integration/CD**

Continuous Integration

is the practice of integrating changes from different developers in the team into a mainline as early as possible, in best cases several times a day This makes sure the code individual developers work on doesn’t divert too much. When you combine the process with automated testing, continuous integration can enable your code to be dependable.

Continuous Deployment

is closely related to Continuous Integration and refers to keeping your application deployable at any point or even automatically releasing to a test or production environment if the latest version passes all automated tests.
***
![[ci-cd.png]]
***
![[ci-cd2.png]]
***

![[ci-cd3.png]]


#CI #CD 