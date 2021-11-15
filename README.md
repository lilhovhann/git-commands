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

## Commit changes of x branch to y branch
```bash
git checkout y
```
```bash
git merge x
```

## Add new and updated files that are staged
```bash
git add -A
```

## List all remote repositories and their URLs
```bash
git remote -v
```


## Cherry pick the commit as the new HEAD of the commit history
```bash
git checkout feature-user-location
```
```bash
git cherry-pick kj2342134sdf090093f0sdgasdf99sdfo992mmmf9921231
```
Commits aren’t copied when cherry picking, they are cherry picked. The changes introduced by the commit are applied and a new commit is then created. This allow us to get specific changes as if they were patches. As a new commit is created upon feature-user-location, HEAD also changes to match it. You can see this in cat .git/HEAD and cat .git/refs/heads/feature-user-location for this case. See man git-cherry-pick for details.


## Set HEAD to the previous commit and leave changes from the undone commit in the stage/index.
```bash
git reset –-soft HEAD
```
