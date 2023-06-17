# refactor
## How to refactor a project?

"
__Always be refactoring. If you touch the code, and you can improve it, improve it, but never optimise early__.”

" - a Precis od Fowlers work on the subject....

Here are some tips:

-   Split the project into multiple modules and refactor only one part at a time.
-   Define a code specification and strictly follow it to avoid refactored code becoming shitcode again.
-   Ensure the consistency of interfaces and functions before and after refactoring.
-   Reasonable arrangement of time to ensure that it does not affect the development of business requirements.
-   Ensure unit tests cover most of the code.

***
![[refactor.png]]
***
Refactoring is a technique in which we change the internal structure of the code, without any effect on the interface. We create a better internal structure and remove code smells.
***
_Smells are certain structures in the code that suggest (sometimes they scream for) the possibility of refactoring. —_ [_Martin P. Fowler_](https://medium.com/u/8cc65672c5d?source=post_page-----3af63cea6782--------------------------------)
***

#refactor #coding 