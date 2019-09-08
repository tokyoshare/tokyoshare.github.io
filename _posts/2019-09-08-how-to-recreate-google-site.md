---
layout: blog
title: Tôi đã viết lại website của Google trong 2 giờ như thế nào?
category: dev
tags: [ReactJS, Material Icons, Material UI]
summary: Viết lại trang Material Icons của Google trong 2 giờ
image: /images/blog/material-icon/1.png
---

<iframe width="300" height="400" src="https://www.youtube.com/embed/O8zhXPDUOtw" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
Nếu như bạn nào đã từng làm web chắc hẳn các bạn biết đến chuẩn Material Design của Google. Đây là chuẩn chung mà Google xây dựng lên để dùng cho việc thiết kế giao diện web, mobile app theo các nguyên lý thiết kế cơ bản dựa trên các khối màu. Hiện nay Google áp dụng chuẩn thiết kế này cho hầu hết các dịch vụ của mình. Bạn có thể truy cập vào trang http://material.io để biết thêm thông tin. Trang web này là một hệ thống các chỉ dẫn, components và tool cho phép người dùng tạo các thiết kế giao diện phù hợp theo chuẩn Material Design. 

![/images/blog/material-icon/1.png]()

Một trong những tool mà mình hay sử dụng nhất trên trang của google là http://material.io/icons, dùng để tìm kiếm các icon theo chuẩn Material Design. Tuy nhiên, điểm mình ghét nhất của trang này là nó rất khó để tra cứu. Hơn nữa, hiện nay mình làm ReactJS đang dùng  Material-UI framework (đây là thư viện các components cho ReactJS viết theo chuẩn Material Design của Google.). Trong Material-UI framework có một phần liên quan đến icons, tuy nhiên, mỗi lần muốn khai báo một icon để sử dụng trong code, mình lại phải mướt mồ hôi đi tìm trong website của Google, rồi sau đó lại phải convert tên icon ra theo chuẩn của Material-UI. Điều này vô hình chung làm tốn rất nhiều thời gian.

Do đó, mình quyết định làm lại website của Material Icons, thêm vào đó là cách tra cứu cách khai báo của các icon trên các framework khác nhau như trên website, Material-UI, AngularJS...  

Tuy nhiên, câu hỏi đầu tiên đặt ra là: "Material Icons có nhiều icons vậy, không lẽ mình phải tự đi ngồi tổng hợp dữ liệu hay sao? Mình đâu có rảnh, một giờ rửa bát của mình cũng 10$ rồi =))". Ngồi mày mò một lúc, check các dữ liệu mà Google trả về, mình phát hiện hoá ra Google nó trả về cho client cả một file `icons.json`, trong đó lưu trữ tất cả thông tin về các icons của trang material icons. "Thôi rồi, Lượm ơi". Hoá ra Google cũng không bảo mật lắm nhỉ :D.

![/images/blog/material-icon/3.png]()

Ok, vậy là khỏi lo về dữ liệu rồi, giờ là lúc nghĩ về thiết kế giao diện nhỉ. 

Vì trang Material Icons của Google dùng thiết kế dạng dropdown list để chọn category của icons, đây là một trong những điểm khiến mình khó chịu nhất, vì mình không hình dung được có bao nhiêu category lúc vào trang (không lẽ lần nào vào cũng phải nhớ). Vì vậy, mình phải chọn một thiết kế giao diện mà vừa thoả mãn được 2 tiêu chí: thứ nhất là tại một thời điểm người dùng chỉ được chọn 1 category giống như dropdown list, thứ 2, nó phải show ra hết được tất cả các category để người dùng dễ hình dung họ có thể chọn bao nhiêu loại icons và họ nên chọn loại icon nào. Kết hợp 2 tiêu chí đó, mình quyết định chọn thiết kế giao diện theo dạng tab, với mỗi tab sẽ là một icon category và sẽ có thêm một tab chuyên cho mục Search, khi người dùng tìm kiếm thì sẽ hiển thị thêm tab Search này.

"Hàng" Google

![/images/blog/material-icon/5.png]()

"Hàng" made by me:

![/images/blog/material-icon/4.png]()

Điểm bất cập thứ 2 của trang của Google là vùng hiển thị các icons ít quá, user phải kéo mỏi tay lên mới bắt đầu xem được tổng thể các icon, vì ngay đầu trang mấy bố đã chiếm gần hết trang vì mấy cái thông tin về các resource khác liên quan rồi (what the hell, tôi vào đây để tìm icons mà, những thông tin khác bỏ vào một chỗ nào đấy được ko???)

"Hàng" Google:

![/images/blog/material-icon/7.png]()

"Hàng" made by me:

![/images/blog/material-icon/8.png]()

Khi chọn 1 icon, trang của Google cũng không bật ngay ra cửa sổ thông tin của icon đó, mà bắt người dùng phải thêm một bước nữa click vào button mới hiển thị panel thông tin của icon. Đây cũng là một trải nghiệm người dùng tệ nữa của Google đối với mình. Vì vậy, mình thiết kế hẳn một panel bên tay phải chỉ chuyên hiển thị thông tin về icon vừa được chọn để người dùng nhìn thấy được luôn sau chỉ 1 click chuột.

"Hàng" Google:

![/images/blog/material-icon/5.png]()

"Hàng" made by me:

![/images/blog/material-icon/6.png]()

Vậy là xong phần về thiết kế giao diện, bây giờ chúng ta tiến hành vào phần code nhỉ. Vì chương trình này khá đơn giản, không cần backend (vì dữ liệu chỉ là 1 file `icons.json` của Google), không có image asset(vì tất cả mọi thứ mình đều sử dụng icon của Material Icons). Do đó mình quyết định viết bằng ReactJS, xử dụng thêm một số hàm của React Hooks như useState, useEffect chứ không dùng tới mấy cấu trúc quản lý store, state phức tạp như Redux. Cả chương trình này mình cũng chỉ viết tầm chưa đến 1000 dòng code. Source code của chương trình này mình up lên ở đây (Code hơi thối vì code theo dòng suy nghĩ, ko có comment, mong mọi người thông cảm =))).:

https://github.com/tokyoshare/icons

![/images/blog/material-icon/9.png]()

Xong phần code, rồi, vì trang web chỉ là một website tĩnh, vì vậy mình quyết định up lên github và sử dụng tính năng github page để deploy nó lên trên trang của mình. 

![/images/blog/material-icon/10.png]()

![/images/blog/material-icon/11.png]()

Như vậy là đã xong trang web trong vòng 2 tiếng . Mọi người có thể xem trang của mình ở đây:

https://toolhub.dev/icons/





