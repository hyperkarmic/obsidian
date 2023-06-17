### 1) Understand the problem

The goal of any algorithm is to solve a problem.  When solving an algorithm problem, it is important to understand the problem and the steps involved in solving it. This understanding will allow you to correctly follow the instructions and complete the task. Answer the common questions to be sure that you really understand the problem. Questions like what it does and what kind of input I’m expecting. what kind of output I should receive? Are there some exceptions I should be aware of? etc…

The goal of this challenge is to [write a function](https://nerdleveltech.com/javascript-functions-why-theyre-essential-to-understand-easy-guide/) that takes in a string and returns the index of the first letter in the string that does not repeat. For example, if the string is “nerd”, [the function](https://nerdleveltech.com/javascript-functions-why-theyre-essential-to-understand-easy-guide-part2/) should return 0, because the first letter “n” is the first non-repeating letter in the string. If the string is “abcdefg”, the function should return 0, because the first letter “a” is the first non-repeating letter in the string.

If the string does not contain any non-repeating letters, the function should return -1. For example, if the input string is “abcabc”, the function should return -1, because no letter in the string is unique or non-repeating.

### 2) Break the problem down

When solving **[algorithms problems](https://nerdleveltech.com/how-to-be-better-at-algorithms-examples-for-beginners/)**, breaking them down into smaller parts is usually the best way to go. Once you understand how each part works and interacts with the others, you can solve the problem more quickly.

**To solve this challenge, we need to do the following:**

1.  Iterate over the letters in the input string, and for each letter, keep track of how many times it appears in the string. We can do this using an object, dictionary, or map, where the keys are the letters in the string, and the values are the counts for each letter.
2.  Once we have counted the occurrences of each letter in the string, we need to find the index of the first letter that has a count of 1 (i.e. the first non-repeating letter). To do this, we can iterate over the letters in the string again, and for each letter, check if its count in the object/dictionary is 1. If it is, we return the index of the letter.
3.  If we reach the end of the loop without finding any value that has only 1 or non-repeating letters, we return -1 to indicate that no non-repeating letters were found.

### 3) Find your solution

We found one solution and the key steps in this solution are to keep track of the counts of each letter in the input string, and then to search for the first letter with a count of 1.  If the count of this letter is 1 meaning that this letter only shows one time in the string. These steps can be implemented in a variety of ways, depending on the language and tools you are using to solve the challenge.

### 4) Check your solution

Checking your solution again answers some questions like can I write a better code? by better I mean is the code I provided covering all cases of inputs? is it efficient? and by efficient, I mean using fewer computer resources when possible. If you’re comfortable with your answers then check if there is another solution out there for the same problem you solved, if any are found. go through them I learned a lot by doing that. Also get some feedback on your code, that way you’ll learn many ways of approaching a problem to solve it.

As we mentioned above we asked ourselves these questions but the algorithm we wrote couldn’t go through all the different cases successfully: for example, The code can’t handle the case wh![[algo-solving.jpg]]en we handled two cases of the same character “L” and “l” in the word “Level”
***
![[problem-solving.jpg]]
***
![[prob-info.png]]

***
![[personal-prob-.png]]

#algorithms #problem-solving 