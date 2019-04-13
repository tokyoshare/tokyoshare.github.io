---
layout: blog
title: Cách để tạo CLI trong 15 phút (Phần I)
category: dev
tags: [NodeJS, CLI, Todo]
summary: Cách để tạo CLI trong một nốt nhạc
image: /images/blog/todo.jpg
---

Thực ra thì mình là một người rất thích viết code, nhưng lại rất lười viết hướng dẫn sử dụng cho người khác. Không biết đây có phải là căn bệnh chung của những dev nhiều kinh nghiệm ở VN không =)). Tuy nhiên, hôm trước tự nhiên thằng cu em cùng cty (thực ra là cùng cty khách hàng mình) nó đăng một bài viết hướng dẫn cách viết một cli bằng python lên blog của nó. Đọc cũng thấy hay, nên mình quyết định sẽ bắt chước nó viết một cái cli =)). Mình sẽ để link bài viết của hắn ở cuối bài để bạn nào muốn tham khảo thì có thể đọc.

Bây giờ, quay về chủ đề chính. Vậy CLI là gì và nó có tác dụng như thế nào? Tra wiki xem nào:
```
*A command-line interface or command language interpreter (CLI), also known as command-line user interface, 
console user interface and character user interface (CUI), is a means of interacting with a computer program 
where the user (or client) issues commands to the program in the form of successive lines of text.*
```

Ok, vậy là rõ rồi nhé. 

```
*CLI là viết tắt của command-line interface hoặc command language interpreter, hay còn được gọi 
là giao diện người dùng bằng dòng lệnh, nghĩa là người dùng có thể tương tác với máy tính bằng 
cách gõ các lệnh lên màn hình console thay vì giao diện trực quan (có lẽ cũng vì thế nó được gọi
là CÙI-character user interface)*
```

Vậy CLI dùng để làm gì? 

Nó có thể dùng làm rất nhiều việc, ví dụ như dọn vệ sinh, rửa bát, quét nhà (mình đùa đấy, thực ra đấy là việc chính của mình ở nhà :((). Thường thì bạn sẽ dùng các lệnh cli để làm những việc lặp đi lặp lại, các tác vụ đơn giản mà bạn không muốn dùng(hoặc ko có để dùng) các tools quá phức tạp.

Bạn sẽ thấy có rất nhiều loại cli đi kèm với các thương hiệu nổi tiếng như node-cli, aws-cli, v.v.. Nhưng những chương trình ấy nó viết để cho cả thế giới dùng, trong khi công việc của bạn thì nhiều lúc có những việc nó lặp đi lặp lại một cách nhàm chán mà cả thế giới ko ai quan tâm để viết cho bạn một cái chương trình để giải quyết nó, đó là lúc bạn nên nghĩ đến việc viết cho riêng mình một cái cli.

Tại sao phải là cli?

1. vì công việc của bạn lặp đi lặp lại.
2. vì nó gọn nhẹ, dễ viết, dễ sửa đổi.
3. vì bạn có thể bật nó lên để nghịch trong giờ làm việc mà các sếp vẫn nghĩ bạn là nhân viên chăm chỉ :D

OK, vậy chúng ta bắt đầu nào. Hôm nay mình sẽ hướng dẫn cho các bạn viết một cái cli Todo, để quản lý các task của bản thân.

## I. Khởi tạo project

Đầu tiên chúng ta sẽ tạo một folder và đặt tên nó là Todo.