# code smells
The more common code smells are,

1.  **Comments**: It is good to have annotations, but if comments are overused (_subjective_) to compensate for the lack of clarity in code, it is a problem
2.  **Large Class**: If a class is very large (_subjective_), consider using decomposition
3.  **Data Class**: If a class is too small (_subjective_); opposite of a large class
4.  **Data Clump**: If a group of codes frequently appear together, consider using encapsulation
5.  **Duplicated Code**: If the same code, with little variations, is found in multiple parts of the codebase, consider using generalization
6.  **Long Method**: If a method is large (_subjective_), this indicates a poor separation of concerns, consider using decomposition
7.  **Long Parameter List**: If a method has a long list of parameters (_subjective_), consider passing parameter objects that encapsulate common parameters
8.  **Shotgun Surgery**: If a change in one place leads to changes in multiple other parts, this indicates tight coupling
***
![[bad code.png]]
***

#code #smells #code-smells