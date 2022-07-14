# 3 rules of good  git commits
### Focus On The Why

**This is the most important rule.** And it's also the most common mistake. Commit messages should explain _why_ the code was added, not _what_ was added. To see the _what_ I can just read the code. But to understand the _why_ I can only guess.

Even if I'm the author of the code, I will eventually forget the _why_.

### Use Imperative Mood In The Subject Line

_Imperative mood_ means "_used to demand or require that an action be performed_". This is the mood Git uses by default, and so should you.

For example, the `git revert` command will create a so-called "revert commit" for you. This commit will have a subject line with an imperative mood - "Revert 'Add field to schema'".

You can think about it that you are telling the system/app/etc. how to behave. This might be awkward at first but you'll get used to it.

> Note: You can write in whatever mood you prefer for commit bodies.

### Restrict Subject Line Length to 50 Characters

Have you ever seen a commit message on GitHub that ends with `...`? That's because GitHub truncates the subject line if it goes above 72 characters. The rest of the subject line moves to the commit body.

50 characters is the recommendation by GitHub. The limit exists to make the commit more readable. And you're forced to explain your code changes in a concise and comprehensible way.

If you're having problems explaining your code changes with 50 characters you might be committing too many changes at once. If this is the case, you should split the commit into multiple commits.

***
#commits #git #rules 