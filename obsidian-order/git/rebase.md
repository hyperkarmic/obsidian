# rebase

### **Rebasing** is the process of _moving or combining a sequence of commits to a new base commit_. The primary reason you would like to use `rebase` in your project is to _maintain a linear project history_, making it much easier to view the logs.

<hr>
Thus `rebase` allows you to work off the _latest changes on any branch, even though you started working before the changes were introduced_. It also helps you in the case of **Fast Forward Merge** discussed in the **Merge Strategies** section.
<hr>
Generally, the rebasing action aims to assign a new commit to the current branch’s HEAD (latest commit). The most common usage of that functionality is to rebase a subbranch to the master’s current HEAD.
git rebase <source branch>

#git #rebase