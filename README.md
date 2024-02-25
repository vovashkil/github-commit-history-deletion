# How to delete github commit history
[Origin](https://stackoverflow.com/questions/13716658/how-to-delete-all-commit-history-in-github)

## Checkout/create orphan branch (this branch won't show in git branch command):
```
git checkout --orphan latest_branch
```
## Add all the files to the newly created branch:
```
git add -A
```
## Commit the changes:
```
git commit -am "commit message"
```
## Delete main (default) branch (this step is permanent):
### NB: instead of the default branch **main** you may want to use **master**
```
git branch -D main
```
## Rename the current branch to main:
```
git branch -m main
```
## Finally, all changes are completed on your local repository, and force update your remote repository:
```
git push -f origin main
```
