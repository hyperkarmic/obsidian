##cherry pick


`_git cherry-pick_` _is like copying something from a folder and pasting it in another folder. So, it will not delete the commit from where you cherry picked and in destination branch commit id will also be different._
<hr>
### Need a feature introduced in a **commit** in another branch, but the branch is not ready to be **merged** yet? No, you don't have to take the _500-year long nap_ till the branch is merged!

You can just **Cherry Pick** the commits you require
<hr>
```

git cherry-pick <commit-id>


git cherry-pick -x <commit hash>


git cherry-pick  <commit hash>
```

***
What cherry-pick does is, it enables arbitrary Git commits to be picked by reference and appended to the current working HEAD. Therefore, Cherry picking is the act of picking a commit from a branch and applying it to another.
***

Chill, It's just a meme. Cherry-picking is much easier. All you need is -

-   A freshly created branch from the branch you finally want to merge your changes to.
-   Your original commit hash, which looks something like _3cf741bbdbcdeed65e5371912742e854a035e665_. (Don't worry, you only need the first 8 characters of the whole hash i.e. _3cf741bb_)

Now switch to your newly created branch and run the following command. (click!!!!)

```git cherry-pick <commitSHA>  ---> i.e. git cherry-pick 3cf741bb

```

#git 