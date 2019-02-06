# Git

## Push local repository to remote

```bash
git remote add origin <REPOSITORY URL>
git push -u origin master
```

## Delete local tracking branches of deleted remote branches

This is typically useful when a branch (or multiple branches) has been merged (and deleted) on remote (such as GitHub or GitLab) and you want to delete the local tracking branch.

```bash
git remote prune origin
```

## Delete local branch

If a local branch has been merged successfully, you can delete it using the `-d` flag. This will cause an error in case the specified branch has not been fully merged yet.

```bash
git branch -d <BRANCH NAME>
```

If the branch has not been merged yet, but you want to delete it anyways, use the `-D` flag instead.

This also works perfectly well for merged branches, but you would typically use the `-d` flag for that to avoid accidentally deleting an unmerged branch.

The `-D` flag forces the delete regardless of whether the branch has been merged or not.

```bash
git branch -D <BRANCH NAME>
```
