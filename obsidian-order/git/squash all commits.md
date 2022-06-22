# squash all commits into one

```bash
git checkout my-new-branch
git reset $(git merge-base master my-new-branch)
git add -A
git commit -m "OMG done in just one commit!"
git push --force
```

#git #commit #squash
