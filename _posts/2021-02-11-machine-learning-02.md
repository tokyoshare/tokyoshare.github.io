---
layout: blog
title: Machine Learning Series-Bài 2.
category: dev
tags: [Machine Learning, AI, Deep Learning]
summary: Python và các thư viện ML
image: https://www.pythontutorial.net/wp-content/uploads/2022/08/what-is-numpy.png

---

##  Python và các thư viện ML

Python là một ngôn ngữ lập trình bậc cao cho các mục đích lập trình đa năng, do Guido van Rossum tạo ra và lần đầu ra mắt vào năm 1991. Python được thiết kế với ưu điểm mạnh là dễ đọc, dễ học và dễ nhớ. Python là ngôn ngữ có hình thức rất sáng sủa, cấu trúc rõ ràng, thuận tiện cho người mới học lập trình. Cấu trúc của Python còn cho phép người sử dụng viết mã lệnh với số lần gõ phím tối thiểu.

Những đặc điểm chính của Python:

- Ngôn ngữ thông dịch
- Khả năng module hoá
- Thư viện toàn diện
- Có khả năng mở rộng với các ngôn ngữ khác
- Hướng đối tượng
- Hầu hết là mô hình lập trình thủ tục, hướng đối tượng

Do tính dễ đọc, dễ học và dễ nhớ như vậy, nên Python được rất nhiều các trường đại học trên thế giới lựa chọn làm ngôn ngữ để học lập trình cơ bản. 

Tuy nhiên, trong những năm gần đây, Python lại nổi lên như một ngôn ngữ ưa thích của các nhà khoa học dữ liệu. Nguyên nhân chính của điều này là bên cạnh việc dễ học và dễ sử dụng, thì Python còn có rất nhiều modules và thư viện mạnh mẽ hỗ trợ cho việc phân tích dữ liệu. 

Sau đây là những thư viện hay được sử dụng trong ML:

![ML Library](https://cdn-media-1.freecodecamp.org/images/1*SltpaprT6Vc6IhQqVsYKtA.png)

### [Numpy](https://numpy.org)

NumPy (Numerical Python) là một thư viện nguồn mở Python, nó được dùng trong hầu hết mọi khía cạnh của khoa học và kỹ thuật. Nó trở thành một chuẩn chung để làm việc với các dữ liệu số trong Python, và nó cũng góp phần tạo nên nền tảng của hệ sinh thái PyData và Python dùng trong khoa học. Người dùng Numpy có thể là bất kì ai, từ những lập trình viên non trẻ cho tới những nhà nghiên cứu nhiều kinh nghiệm. Numpy API cũng được dùng trong các thư viện Pandas, SciPy, Matplotlib, scikit-learn, scikit-image mà hầu hết các thư viện Python dùng cho khoa học dữ liệu.

Thư viện Numpy chứa các cấu trúc dữ liệu ma trận và mảng nhiều chiều, Nó cung cấp ndaray, một đối tượng mảng n chiều đồng nhất, với các phương thức để làm việc hiệu quả trên nó. NumPy có thể được dụng để tiến hành một lượng lớn các thao tác toán học trên các mảng. Nó cung cấp cho Python các cấu trúc dữ liệu đủ mạnh để đảm bảo các tính toán trên các mảng và ma trận khổng lồ một cách đầy hiệu quả.

### [Scipy](https://www.scipy.org/) 

SciPy là một thư viện mã nguồn mở cho Python, dùng để giải quyết các vấn đề toán học và khoa học. Nó được xây dựng dựa trên NumPy, cho phép người dùng thao tác và biểu diễn dữ liệu bằng một số lượng lớn các mệnh lệnh bậc cao. Như đã đề cập ở trên, SciPy được xây dựng dựa trên NumPy, vì vậy nếu bạn đã import SciPy trong source code, bạn không cần phải import NumPy nữa, tuy nhiên bạn vẫn phải cài đặt NumPy để có thể sử dụng SciPy.

NumPy chứa các dữ liệu và thao tác cơ bản với mảng như là sắp xếp, đánh index, v.v... Trong khi đó, SciPy thì bao gồm cả xử lý số học. Mặc dù NumPy cung cấp một số các hàm có thể giải quyết các vấn đề đại số tuyến tính (linear algebra), biến đổi Fourier...SciPy thì có tất cả các hàm đó và thêm nhiều hàm khác nữa vì nó được xây dựng dựa trên NumPy.

### [Matplotlib](https://matplotlib.org/)

Matplotlib là một package Python được dùng để xây dựng các biểu đồ. Đầu năm 2000, Matplotlib bắt đầu như một dự án sử dụng Python để biểu diễn các tín hiệu điện từ trong não bộ của các bệnh nhân động kinh. Tác giả của Matplotlib,  John D. Hunter là một nhà sinh học thần kinh. Ông đã tìm kiếm một cách để vẽ các biểu đồ bằng Python để thay thế cho MATLAB. Bên cạnh việc tạo ra Matplotlib, Tiến sĩ Hunter còn là thành viên sáng lập của Numfocus. Nhóm Numfocus giám sát một số dự án Python chính bao gồm Matplotlib, NumPy, Pandas, và Jupyter.

Tại sao lại cần Matplotlib?

Matplotlib được dùng để tạo các bản đồ 2D tĩnh, là các loại biểu đồ thường dùng trong các bài báo khoa học hoặc các bài thuyết trình. Hầu hết tất cả các biểu đồ trong Microsoft Excel đều có thể được tạo với Matplotlib. Matplotlib còn có thể được dùng để tạo các biểu đồ 3D và animation.

### [Pandas](https://pandas.pydata.org/)

Pandas là là thư viện mã nguồn mở với hiệu năng cao cho phân tích dữ liệu trong Python được phát triển bởi Wes McKinney năm 2008. Chỉ với hơn 1 năm phát triển nó đã trở thành một thư viện chuẩn trong việc phân tích dữ liệu cho người dùng Python. Một số tính năng nổi bật của pandas:

- Có thể xử lý tập dữ liệu khác nhau về định dạng: chuỗi thời gian, bảng không đồng nhất, ma trận dữ liệu
- Khả năng import dữ liệu từ nhiều nguồn khác nhau như CSV, DB/SQL
- Có thể xử lý vô số phép toán cho tập dữ liệu: subsetting, slicing, filtering, merging, groupBy, re-ordering, and re-shaping,..
- Xử lý dữ liệu mất mát theo ý người dùng mong muốn: bỏ qua hoặc chuyển sang 0
- Xử lý, phân tích dữ liệu tốt như mô hình hoá và thống kê
- Tích hợp tốt với các thư viện khác của python
- Cung cấp hiệu suất tốt và có thể tăng tốc thậm chí hơn cả sử dụng Cython ( extension C cho python)

Lợi ích của việc sử dụng pandas so với sử dụng các ngôn ngữ Java, C hoặc C++:

- Biểu diễn dữ liệu: Nó có thể dễ dàng biểu diễn tập dữ liệu một cách tự nhiên phù hợp với dữ liệu phân tích thông qua cấu trúc DataFrame và Series (Những khái niệm chúng ta sẽ tìm hiểu chi tiết ở các bài sau). Dùng với các ngôn ngữ khác mất nhiều công code hơn
- Tâp hợp và lọc dữ liệu: Nó cung cấp các phương thức để dễ dàng tập hợp và lọc dữ liệu, những thủ tục gắn liền với việc phân tích dữ liệu
- Code ngắn gọn và clear hơn: những API ngắn gọn và clear cho phép người dùng tập trung vào những mục tiêu chính hơn là việc phải viết một đoạn code dài từ đầu để thực hiện công việc

### [SciKit Learn](https://scikit-learn.org/stable/)

Là tập hợp các thuật toán và công cụ dành cho ML. Nó có hầu hết các thuật toán phân loại, hồi quy và phân cụm, và nó được thiết kế để làm việc với một thư viện Python khoa học và số học: NumPy và SciPy. Hầu hết các nhiệm vụ cần được thực hiện trong một pipeline học máy đã được triển khai trong Scikit Learn bao gồm tiền xử lý dữ liệu, lựa chọn tính năng, trích xuất tính năng, tách tập huấn luyện và thử nghiệm, xác định các thuật toán, mô hình phù hợp, điều chỉnh các tham số, dự đoán, đánh giá và xuất mô hình.



