#  fsk
### What is `git fsk`?

##### We can use the command `git fsck` to recover the files after a hard reset.


`git fsck` stands for file system check. It checks for all the "dangling blobs" in the `.git` directory that are not part of any changes. For example, there could be some changes that were staged but not added anywhere.
<hr>
Once we are able to identify the "dangling blobs", we can view the details using `git show`.
***
#fsk
#git 