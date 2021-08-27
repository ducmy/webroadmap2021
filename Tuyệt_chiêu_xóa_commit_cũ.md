# Xóa commit cũ trước khi push lên host
### Orphan branch

```git
git checkout --orphan new-master master
git add .
git commit -m "Initial commit for new root"

=> Xóa toàn bộ commit cũ và thay bằng commit mới
```

### Sử dụng git rebase (có thể chỉnh sữa những commit cũ nhất định)

```git
git rebase -i HEAD~3 (sửa cái commit từ vị trí thứ 3)

```


Nguồn 
https://www.clock.co.uk/insight/deleting-a-git-commit
