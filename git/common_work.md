### Cách để review lại code của những commit trước và cách khôi phục files

```bash
##xem và dò thông tin đoạn commit trước và tìm những hàm đã hoàn thiện

$git log

commit_id1
commit_id2

$git tag current_tag

#Chuyển qua commit đã làm

#git checkout -b commit_i1

#tạo tag cho commit trước đó
$git tag previous_tag


#So sánh giưa 2 tag (commit cũ và mới)

$git diff current_tag previous_tag > file.diff

Review điểm khác nhau.

## khôi phục lại những file cũ đã mất

#git checkout previous_tag path_file1 path_file2

```















