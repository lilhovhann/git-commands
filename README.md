# Git cheet sheet

Here you can find the common git commands and use cases.

## Check git version

```bash
git --version
```

## Connect local repository to remote one.

```bash
git remote add new
```
or
```bash
git remote add origin
```

##  Reset the commit branch back before the last n commits, then squash them into a single commit
```bash
git reset --hard HEAD~n
```
or
```bash
git merge –squash HEAD@{1}
```
As it is a hard reset, it will also overwrite every change in the working tree as well.git merge –squash HEAD@{1} HEAD@{1} is where the branch was just before the previous command. This command sets the state of the index to be as it would just after a merge from that commit. This whole operation could be a way to take 5 commits from a branch in which you started a new feature and squash them to a single commit, a meaningful one.

Commit changes of x branch to y branch
```bash
git checkout y
```
```bash
git merge x
```
