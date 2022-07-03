# Unit Tests
# Why Use Unit Testing ?

Unit testing is automated testing that focuses on a single ‘unit’ of your code, such as a function or a module. This makes the tests quick to write and to run, and therefore there can be many tests. Unit tests are specific to such a small piece of your code that it makes tracing errors easy and efficient.

The terms TDD (test-driven development) and BDD (behavior-driven development) refer to approaches to writing tests for a piece of software, and often TDD results in writing unit tests. In TDD, developers write a failing test for what they want their code to achieve first, and then write some code to pass the test. For example, if you want to write a method that gets the average of an array of integers, in TDD you would first write a unit test that fails. You would then adjust the method that is supposed to achieve this until it passes the test. In order to establish more boundaries for this method, more unit tests are written to fail, and then the method adjusted to pass them. This means that writing unit test is part of the process of test driven development.

Additionally, unit testing prevents code from becoming too fragile. Unit tests that verify a module’s functionality should still be applicable when that module has additions or changes. If a new method is added to a class and breaks existing functionality in the class, the existing unit tests will fail. This will indicate to the developer that either the new method has negative side effects, or that the scope of the change is larger than just that method and the existing unit tests need to change. Either way, the developer knows before deployment that their addition or modification breaks existing expected functionality.

Unit testing also provides a sort of make shift documentation for developers. By reading the unit tests for existing modules, a developer can establish what the functionality currently is and should be before making changes or tracking down a bug. This can help establish whether a bug is actually a bug or just missing functionality, and determine the complexity of potential updates to functionality.
***
![[4testing areas.png]]
***

#unit-tests #tests #TDD