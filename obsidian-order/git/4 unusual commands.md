# 4 unusual git commands
-   `$ git clean`. Effective removal of the untracked files that are non-staged.
-   `$ git pull --rebase --autostash`. An efficient stash and pop of uncommitted changes.
-   `$ git branch --merged | egrep -v "" | xargs git branch`. Viable deletion of already merged branches excluding important ones.
-   `$ git reflog`. An effective return to the point before something was broken (the log is removed after 90 days by default).
***
![[git-commands.png]]
#git #unusual