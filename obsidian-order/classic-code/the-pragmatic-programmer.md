## [The Pragmatic Programmer](https://www.amazon.com/Pragmatic-Programmer-journey-mastery-Anniversary/dp/0135957052)

by David Thomas & Andrew Hunt

The Pragmatic Programmer has become a classic, helping a generation of programmers understand the very essence of software development, in the language, framework, or methodology used.

Read this book, and you’ll learn how to:

-   Fight software rot
-   Avoid the trap of duplicating knowledge
-   Write flexible, dynamic, and adaptable code
-   Harness the power of basic tools
-   Avoid programming by coincidence
-   Learn real requirements
-   Solve the underlying problems of concurrent code
-   Guard against security vulnerabilities
-   Test ruthlessly and effectively, including property-based testing

### Patrick Klein Notes
-   Tip 1: Care about your craft and think about your work
    
-   Never run on auto-pilot
    
-   Kaizen - continuously make small improvements
    
-   Be aware of the bigger picture, think beyond the immediate problem
    
-   Pragmatic - dealing with things sensibly and realistically in a way that is based on practical rather than theoretical considerations
    
-   Take responsibility for everything you do
    
-   Learning is a continuous and ongoing process
    
-   The greatest of all weaknesses is the fear of appearing weak
    
-   Take responsibility for yourself and your actions in terms of your career advancement, your project, and your day-to-day work
    
-   Don't be afraid to admit ignorance or error
    
-   Be proud of your abilities, but honest about your shortcomings
    
-   Tip 3: Provide options, don't make excuses
    
-   Don't be afraid to ask or admit that you need help
    
-   Tip 4: Don't live with broken windows
    
-   People find it easier to join an ongoing success
    
-   It's easier to ask for forgiveness than it is to get permission
    
-   Tip 5: Be a catalyst for change
    
-   Tip 6: Remember the big picture
    
-   Constantly review what's happening around you, not just what you are personally doing
    
-   Tip 7: Make quality a requirements issue
    
-   Great software today is often preferable to perfect software tomorrow
    
-   Don't spoil a perfectly good program by overembellishment and over-refinement
    
-   Your code will never be perfect
    
-   An investment in knowledge always pays the best interest
    
-   Your knowledge and experience are your most important professional assets, but they are expiring assets
    
-   Knowledge portfolio: invest regularly, diversify, balance between conservative and high-risk, high reward investments, buy low and sell high for maximum returns, review and rebalance periodically
    
-   Tip 8: Invest regularly in your knowledge portfolio
    
-   Tip 9: Critically analyze what you read and hear
    
-   Write an outline on what you want to say before you say it and ask yourself, 'Does this get across whatever I am trying to say?'
    
-   Understand the needs, interests, and capabilities of your audience so you can communicate information effectively
    
-   What do you want them to learn? What is their interest in what you have to say? How sophisticated are they? How much detail do they want? Whom do you want to own the information? How can you motivate them to listen to you?
    
-   Listen to your audience
    
-   Tip 10: It's both what you say and the way you say it
    
-   DRY - Don't Repeat Yourself
    
-   Every piece of knowledge must have a single unambiguous, authoritative representation within a system
    
-   For object-orientation: use accessor functions to read and write the attributes of an object
    
-   Shortcuts make for long days
    
-   Tip 12: Make it easy to reuse
    
-   If it isn't easy, people won't do it
    
-   Nonorthogonal systems are inherently more complex to change and control
    
-   Two or more things are orthogonal if changes in one do not affect any of the others
    
-   Tip 13: Eliminate effects between unrelated things
    
-   Design components that are self-contained: independent, and with a single, well-defined purpose
    
-   Orthogonal systems increase productivity and reduce risk
    
-   Build unit tests for each module as part of the regular build process
    
-   Nothing is more dangerous than an idea if it's the only one you have
    
-   Tip 14: There are no final decisions
    
-   You can simply hide a third-party product behind a well-defined, abstract interface
    
-   Tip 15: Use tracer bullets to find the target
    
-   A project is never finished, there will always be changes required and functions to add
    
-   Prototypes are thrown away
    
-   Tip 16: Prototype to learn
    
-   The limits of language are the limits of one's world
    
-   Tip 17: Program close to the problem domain
    
-   Tip 18: Estimate to avoid suprises
    
-   Before estimating, ask someone who's already done it
    
-   Think about scope and understand the problem before starting to guess
    
-   Development steps: check requirements, analyze risk, design, implement, integrate, validate with users
    
-   Tip 19: Iterate the schedule with the code
    
-   When asked for an estimate, say 'I'll get back to you'
    
-   Keep track of your estimates and see how accurate you are and how you improve at them
    
-   Tools amplify your talent
    
-   Tip 20: Keep knowledge in plain text
    
-   Tip 21: Use the power of command shells
    
-   Gain familiarity with the command line to increase productivity
    
-   Tip 22: Use a single editor well
    
-   Progress, far from consisting in change, depends on retentiveness. Those who cannot remember the past are condemned to repeat it
    
-   Tip 23: Always use source control
    
-   Tip 24: Fix the problem not the blame
    
-   Tip 25: Don't panic
    
-   The first rule of debugging: think about what may be causing the bug
    
-   Rubber ducking or verbalizing assumptions and explaining, step by step, what the code is supposed to do often brings new insights and solutions
    
-   Tip 27: Don't assume it, prove it
    
-   Tip 28: Learn a text manipulation language
    
-   Tip 29: Write code that writes code
    
-   Tip 30: You can't write perfect software
    
-   Code in defense against your own mistakes
    
-   Design by contract: preconditions (requirements to be called), postconditions (state of the program when it concludes), and class invariants (what must be true)
    
-   Liskov substitution principle: subclasses must be usable through the base class interface without the need for the user to know the difference
    
-   Loop invariant: state valid before the loop executes, on each iteration, and after the loop terminates
    
-   Tip 32: Crash early
    
-   Tip 33: If it can't happen, use assertions to ensure that it won't
    
-   If you ever say that that can never happen, add code to check it
    
-   Tip 34: Use exceptions for exceptional problems
    
-   Tip 35: Finish what you start
    
-   Organize code into modules and limit the interaction between them
    
-   Be careful about how many other modules you interact with
    
-   Law of demeter for functions: any method of an object should call only methods belonging to itself, any parameters that were passed into the method, any objects it created, any directly held component objects
    
-   Tip 36: Minimize coupling between modules
    
-   Tip 37: Configure, don't integrate
    
-   Make our systems and details highly configurable
    
-   Metadata is data about data. Use metadata for configurations
    
-   Program for the general case and put the specifics elsewhere
    
-   Tip 38: Put abstractions in code, details in metadata
    
-   Tip 39: Analyze workflow to improve concurrency
    
-   Tip 40: Design using services
    
-   Services are independent, concurrent objects behind well-defined, consistent interfaces
    
-   Tip 41: Always design for concurrency
    
-   Divide and conquer a program with modules that each has a single, well-defined responsibility
    
-   Pub/sub protocol: events are generated by a publisher and we register subscribers to listen, the publisher keeps track of the subscriber objects and notifies them when it generates an event of interest
    
-   The model is the data itself with common operations to manipulate it
    
-   The view displays the data in different ways
    
-   The controller controls the view and communicates with the data model
    
-   Tip 41: Separate views from models
    
-   MVC: model - abstract the data model representing the target object, view - a way to interpret the model, subscribes to changes in the model and logical events from the controller, controller - controls the view and provides new data to the model, pushes events to both the model and the view
    
-   Views subscribe to the models
    
-   Data arrival should trigger appropriate rules and events
    
-   Practice the basic principle of good modularization and hiding implementation behind small, well-documented interfaces
    
-   Tip 44: Don't program by coincidence
    
-   Be aware, don't code blind, know the technology, have a plan, document your assumptions, test your code and assumptions, prioritize effort
    
-   Refactor if the cost will be less than not making the change
    
-   Tip 46: Test your estimates
    
-   Insertion sort works well for small sets
    
-   Be wary of premature optimization
    
-   Refactoring: rewriting, reworking, or rearchitecting
    
-   When to refactor: duplication, nonorthogonal design, outdated knowledge, performance
    
-   Tip 47: Refactor early and often
    
-   Refactoring is redesign
    
-   Refactoring is an activity that needs to be undertaken slowly. deliberately, and carefully
    
-   Make sure you have good tests before you begin refactoring
    
-   Don't refactor and add functionality at the same time
    
-   Take short, deliberate sweeps
    
-   Manage the pain: if it hurts now, but is going to hurt even more later, you might as well get it over with
    
-   Unit testing: testing done on each module to verify its behavior
    
-   Regression testing: test results against previous runs of the same test
    
-   Test each subcomponent of a module first
    
-   Tip 48: Design to test
    
-   Tip 49: Test your software or your users will
    
-   Tip 50: Don't use wizard code you don't understand
    
-   Tip 51: Don't gather requirements, dig for them
    
-   Discover why users do certain things instead of the way they do it. Solve their business problem
    
-   Become a user
    
-   Tip 52: Work with a user to think like a user
    
-   Tip 53: Abstractions live longer than details
    
-   Tip 54: Use a project glossary
    
-   The key to solving puzzles is both to recognize the constraints and to recognize the degrees of freedom
    
-   Tip 55: Don't think outside the box, find the box
    
-   Tip 56: Listen to nagging doubts, start when you're ready
    
-   Tip 57: Somethings are better done than described
    
-   Tip 58: Don't be a slave to formal methods
    
-   Tip 59: Expensive tools do not produce better designs
    
-   Quality is a team issue, comes from individual contributions of all team members
    
-   Keep a librarian of the documentation
    
-   Tip 60: Organize around functionality, not job functions
    
-   If you don't interact with users or the context, you will not be able to make informed decisions
    
-   Tool builders automate the project's daily tasks
    
-   Tip 61: Use cron jobs to schedule automatic commands to be run
    
-   Tip 62: Test early, test often, test automatically
    
-   Tip 63: Coding ain't done until all the tests run
    
-   Integration testing: tests major subsystems
    
-   Does the software fit the user like an extension of the hand?
    
-   You need real world. boundary conditions, and certain statistical props to test with
    
-   Tip 64: Use saboteurs to test your testing
    
-   Tip 65: Test state coverage, not code coverage
    
-   Tip 66: Find bugs once
    
-   Tip 67: Treat English as just another programming language
    
-   Tip68: Build documentation in, don't bolt it on
    
-   Comment why something is done, its purpose, its goal
    
-   The success of a project is measured by how well it meets the expectations of its users
    
-   Tip 69: Greatly exceed your user's expectations
    
-   Tip 70: Sign your work
- 
#pragmatic
#book #Thomas #Hunt
