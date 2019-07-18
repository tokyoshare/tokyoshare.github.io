---
layout: blog
title: Git Tips-Xoá toàn bộ những branch cũ
category: dev
tags: [NodeJS, CSV, JSON]
summary: Cách để chuyển chữ cái đầu tiên của string thành dạng chữ thường
image: /images/blog/git-logo.png
---
**Đặt vấn đề**

Vốn dĩ là cty mình đang sử dụng git, rất nhiều developer cùng làm việc nên số lượng branch rất lớn. Bài toán đặt ra là mỗi lần merge các branch vào master xong, vì mọi người đều tiếc và để xem lỡ có vấn đề gì xảy ra không thì làm tiếp ở các branch đó, nên không ai xoá những branch đã merge vào master cả. Hậu quả là sau 1 năm, số branch cũ (rác) lên tới hàng trăm cái, việc tìm kiếm các branch trở nên rất khó khăn và vất vả. Vì vậy, mình quyết định đưa ra hành động táo bạo, là sẽ xoá hết tất cả những branch đã cũ. 

**Nhưng tiêu chí "branch cũ" là gì?** 

Trước tiên, mình xin phép được mô tả qua về cấu trúc git của bên mình chút. Cấu trúc của nó như thế này:

-stg

-master

-develop

-features/xxx

Trong đó features/xxx là nhánh mọi người sẽ làm việc, sau khi xong sẽ pull request vào develop để test, ok thì sẽ merge từ develop vào master để chờ đưa lên stg test lại trước khi release.

Lúc đầu mình định xoá theo thời gian commit cuối cùng, nhưng rồi nghĩ như vậy không ổn, có những task đã xong nhưng bị ngâm cả mấy tháng trời không thể release hoặc có những task điều tra kĩ thuật từ lâu rồi, vẫn cần để lại để tham khảo tránh mất công điều tra lại. Như vậy chọn tiêu chí theo thời gian commit cuối cùng có vẻ không hợp lý. Sau một hồi suy nghĩ, mình quyết định là "branch cũ" là những branch mà đã được merge vào master. Nghĩa là dù có xoá đi, thì vì trong master đã có source rồi nên bạn vẫn có thể dễ dàng tách branch từ master để làm việc tiếp.

**Thực hiện**

Ok,  chúng ta đã lựa chọn được tiêu chí để xoá branch rồi, vậy thì tiến hành thôi.  Đây là câu lệnh mình dùng để xoá các nhánh đã merge vào trong master từ remote:

```
git branch -r --merged master | grep "origin/feature" | cut -d "/" -f 2- | xargs -n 20 git push --delete origin
```

Chúng ta sẽ tìm hiểu qua từng cụm lệnh. ```|``` là cú pháp để truyền kết quả của câu lệnh trước vào làm tham số của câu lệnh tiếp theo.

```git branch -r --merged master``` : lấy tất cả các branch remotes mà đã được merge vào master

​	```-r``` hoặc ```-remote```  để lấy các branch remote.

​	``--merged master`` để lấy các brach đã được merge vào master.

```grep "origin/feature"``` : chỉ lấy những branch origin/feature/*

```cut -d "/" -f 2-``` : cut bỏ đi 2 dấu ```/``` trong branch name. Ví dụ tên branch là ```origin/feature/this-is-branch-name```, thì nó sẽ vứt bỏ đi phần ```origin/feature/```, và kết quả chỉ còn lại ```this-is-branch-name``` thôi.

```xargs -n 20 git push --delete origin```: xoá bỏ 20 branch từ origin cùng một lúc, với tham số đầu vào là branch name chúng ta thu được ở trên.

​	```xargs``` là lệnh giúp lấy kết quả của lệnh trước truyền vào như một mảng tham số

​	```-n 20 ``` là xoá 20 phần tử trong mảng tham số một lúc. Chúng ta có thể thay 20 bằng một số bất kì, số này càng lớn thì tốc độ xoá càng nhanh. Nếu set số này là 1 thì nó sẽ xoá lần lượt từng branch một, vì vậy tốc độ là chậm nhất.

**Kết quả**

Kết quả chạy câu lệnh trên là mình mình chạy xoá gần 200 branch trong feature chỉ mất tầm 30s. Trong khi nếu xoá bằng tay từng branch một thì chắc mất cả ngày không xong. :D

