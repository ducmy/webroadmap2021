## Basic flow
```powershell

# Pull project
$git clone <url>

# Show all branches
$git branch -v -a

# Create a new self branch (Trong trường hợp bạn không phải là người merge code,
# người merge có trách nhiệm reivew và chỉnh sửa)
# Cái này dành cho tụi code chay không phải leader thì làm khỏe, ko phải check
$git checkout -b <new_branch>

# Push your branch to server 
$git push -u origin HEAD
# or
$git push -u origin <new_branch>

# Or if you want to merge with new code with develop branch
$git fetch origin master
#or 
$git pull master

```

### Delete branch

#### Delete remote branch
git push origin --delete <name_of_branch>

#### Delete local branch (search)



## Add tag


## Create all local branches

#### Pipleline

```shell
for i in `git branch -a | grep remote | grep -v HEAD | grep -v master`; do git branch --track ${i#remotes/origin/} $i; done
```
