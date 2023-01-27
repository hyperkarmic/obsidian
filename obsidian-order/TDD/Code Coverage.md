
Code coverage is a metric used to measure the amount of code that is executed during unit testing. It is an important tool in ensuring that all parts of a program are thoroughly tested and that any bugs or issues are identified early on. In this article, we will explore how code coverage works in unit testing with JavaScript, including the different types of coverage, how to measure it, and how to use it to improve your testing process.
***

Code coverage is typically calculated by using a tool to instrument the code, which adds additional lines of code that track which parts of the program are executed during a test run. These tools typically report the percentage of lines of code that were executed, as well as the number of lines that were not executed.

There are two main types of code coverage: statement coverage and branch coverage.

-   Statement/Statement coverage, measures the percentage of statements in the code that were executed during the test run.
-   Branch coverage, measures the percentage of branches in the code (e.g. if-else statements) that were taken during the test run.

To calculate the code coverage percentage, you need to divide the number of lines of code or branches that were executed by the total number of lines of code or branches in the program. The result will be a decimal between 0 and 1, which can be multiplied by 100 to express the coverage percentage.

For example, if a program has 100 lines of code and 80 lines were executed during a test run, the statement coverage would be 80/100=0.8 or 80%.
***

#TDD #code-coverage