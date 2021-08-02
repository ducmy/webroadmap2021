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

## Add tag
