

They are many different types of tests in any serious software project.

-   Unit tests verify the functionality of individual units or modules of code. In many projects, you will need 80% of your total tests written in unit tests.
-   Integration tests verify the interactions between different units or modules of code. Another 15% — 20% for integration tests.
-   End-to-end tests verify the functionality of the entire system or application. Because end-to-end tests are real — meaning they need a lot of resources and as they are hooking up the real components (database, network and the 3rd party services), they are expensive, fragile and should only be used for the most critical paths. You usually won’t have too many tests here (around up to 5%).

***
![[3-types-of-test.jpg]]
#TDD 