# Clean Code
## [Clean Code](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)

by Robert Martin

Every year, countless hours and significant resources are lost because of poorly written code. But it doesn’t have to be that way.

Clean Code is divided into three parts. The first describes the principles, patterns, and practices of writing clean code. The second part consists of several case studies of increasing complexity. Each case study is an exercise in cleaning up code―of transforming a code base that has some problems into one that is sound and efficient. The third part is the payoff: a single chapter containing a list of heuristics and “smells” gathered while creating the case studies. The result is a knowledge base that describes the way we think when we write, read, and clean code.

Read this book, and you’ll learn how to:

-   How to tell the difference between good and bad code
-   How to write good code and how to transform bad code into good code
-   How to create good names, good functions, good objects, and good classes
-   How to format code for maximum readability
-   How to implement complete error handling without obscuring code logic
-   How to unit test and practice test-driven development
-   What “smells” and heuristics can help you identify bad code

This book is a must for any developer, software engineer, project manager, team lead, or systems analyst with an interest in producing better code.

// ==========================================>

# notes from Parker Klein
-   As an engineer, you have a depth of knowledge about your systems and projects that no managers can possibly have. With that knowledge comes the responsibility to act
    
-   You can’t take pride and honor in something that you can’t be held accountable for
    
-   When a professional makes a mistake, he cleans up the mess
    
-   It is unprofessional in the extreme to purposely send code that you know to be faulty to QA
    
-   Say. Mean. Do. The three parts to making a commitment. 1. You say you'll do it. 2. You mean it. 3. You actually do it
    
-   If you can't make your commitment, the most important thing is to raise a red flag as soon as possible to whoever you committed to
    
-   I will ... by ...
    
-   If you are tired or distracted, do not code. It creates waste. Find a way to eliminate the distractions and settle your mind
    
-   When you are stuck, when you are tired, disengage for awhile
    
-   Training of less experienced programmers is the responsibility of those who have more experience
    
-   It is the responsibility of professional developers (and stakeholders) to make sure that all ambiguity is removed from the requirements
    
-   Acceptance tests are tests written by a collaboration of the stakeholders and the programmers in order to define when a requirement is done
    
-   Remember, as a professional it is your job to help your team create the best software they can. That means that everybody needs to watch out for errors and slip-ups, and work together to correct them
    
-   Acceptance tests are formal requirements documents that specify how the system should behave from the business’ point of view
    
-   Every time someone commits a module, the continuous integration system should kick off a build, and then run all the tests in the system
    
-   Any argument that can’t be settled in five minutes can’t be settled by arguing
    
-   A commitment is something you must achieve. If you commit to getting something done by a certain date, then you simply have to get it done by that date
    
-   Professionals don’t make commitments unless they know they can achieve them
    
-   Other people are going to accept your commitments and make plans based upon them. The cost of missing those commitments, to them, and to your reputation, is enormous. Missing a commitment is an act of dishonesty only slightly less onerous than an overt lie
    
-   Professionals draw a clear distinction between estimates and commitments. They do not commit unless they know for certain they will succeed. They communicate the probability distribution of their estimates as clearly as possible, so that managers can make appropriate plans
    
-   Manage your stress. Sleepless nights won’t help you get done any faster. Sitting and fretting won’t help either. And the worst thing you could do is to rush! Resist that temptation at all costs. Rushing will only drive you deeper into the hole
    
-   Slow down. Think the problem through. Plot a course to the best possible outcome, and then drive towards that outcome at a reasonable and steady pace
    
-   It’s good to be passionate about what we do. But it’s also good to keep your eye on the goals of the people who pay you
    
-   The first responsibility of the professional programmer is to meet the needs of his or her employer

### _"If you want your code to be easy to write, make it easy to read. — Robert C. Martin, Clean Code"_
***
##### Sidorov Notes
# General rules

1.  Follow standard conventions.
2.  Keep it simple stupid. Simpler is always better. Reduce complexity as much as possible.
3.  Boy scout rule. Leave the campground cleaner than you found it.
4.  Always find root cause. Always look for the root cause of a problem.

# Design rules

1.  Keep configurable data at high levels.
2.  Prefer polymorphism to if/else or switch/case.
3.  Separate multi-threading code.
4.  Prevent over-configurability.
5.  Use dependency injection.
6.  Follow Law of Demeter. A class should know only its direct dependencies.

# Understandability tips

1.  Be consistent. If you do something a certain way, do all similar things in the same way.
2.  Use explanatory variables.
3.  Encapsulate boundary conditions. Boundary conditions are hard to keep track of. Put the processing for them in one place.
4.  Prefer dedicated value objects to a primitive type.
5.  Avoid logical dependency. Don’t write methods which works correctly depending on something else in the same class.
6.  Avoid negative conditionals.

# Names rules

1.  Choose descriptive and unambiguous names.
2.  Make the meaningful distinctions.
3.  Use pronounceable names.
4.  Use searchable names.
5.  Replace magic numbers with named constants.
6.  Avoid encodings. Don’t append prefixes or type information.

# Functions rules

1.  Small.
2.  Do one thing.
3.  Use descriptive names.
4.  Prefer fewer arguments.
5.  Have no side effects.
6.  Don’t use flag arguments. Split method into several independent methods that can be called from the client without the flag.

# Comments rules

1.  Always try to explain yourself in code.
2.  Don’t be redundant.
3.  Don’t add obvious noise.
4.  Don’t use closing brace comments.
5.  Don’t comment out code. Just remove.
6.  Use as an explanation of intent.
7.  Use as clarification of code.
8.  Use as a warning of consequences.

# Source code structure

1.  Separate concepts vertically.
2.  Related code should appear vertically dense.
3.  Declare variables close to their usage.
4.  Dependent functions should be close.
5.  Similar functions should be close.
6.  Place functions in the downward direction.
7.  Keep lines short.
8.  Don’t use horizontal alignment.
9.  Use white space to associate related things and disassociate weakly related.
10.  Don’t break indentation.

# Objects and data structures

1.  Hide internal structure.
2.  Prefer data structures.
3.  Avoid hybrids structures (half object and half data).
4.  Should be small.
5.  Do one thing.
6.  A small number of instance variables.
7.  Base class should know nothing about their derivatives.
8.  Better to have many functions than to pass some code into a function to select a behavior.
9.  Prefer non-static methods to static methods.

# Tests

1.  One assert per test.
2.  Readable.
3.  Fast.
4.  Independent.
5.  Repeatable.

# Code smells

1.  Rigidity. The software is difficult to change. A small change causes a cascade of subsequent changes.
2.  Fragility. The software breaks in many places due to a single change.
3.  Immobility. You cannot reuse parts of the code in other projects because of the involved risks and high effort.
4.  Needless Complexity.
5.  Needless Repetition.
6.  Opacity. The code is hard to understand.

#clean-code
#Martin
#book 

