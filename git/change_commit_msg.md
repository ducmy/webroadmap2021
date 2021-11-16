### Remove Author in Git

```shell
// Remember that switch to Git code
// Retrive the commit message of second (3-1)

git rebase -i HEAD~3  

Choose the edit moode from Commit list

git commit --amend --reset-author

// You can change commit message in this step

git rebase --continue

git commit --amend --reset-author

git rebase --continue

git commit --amend --reset-author

git rebase --continue

```
