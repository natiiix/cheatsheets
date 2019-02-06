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
