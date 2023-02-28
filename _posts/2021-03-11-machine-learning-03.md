# Hồi quy

1. Hồi quy đơn (dựa trên một biến số)
   - Hồi quy tuyến tính
   - Hồi quy không tuyến tính
2. Đa hồi quy (tính toán hồi quy dựa trên đa biến số)
   - Đa hồi quy tuyến tính
   - Đa hồi quy không tuyến tính

## Các ứng dụng của hồi quy

- Dự báo bán hàng (tổng doanh thu cả năm)
- Phân tích độ hài lòng của khách hàng
- Estimate giá thành (giá bất động sản dựa trên diện tích, địa điểm)
- Dự đoán mức thu nhập 
- ...



## Hồi quy tuyến tính

Chúng ta có thể sử dụng hồi quy tuyến tính để dự đoán một giá trị liên tục chẳng hạn như lượng khí thải CO2 của động cơ ô tô bằng kích thước của bánh hoặc dung tích xi lanh. 

> Hồi quy tuyến tính là xấp xỉ của mô hình tuyến tính được sử dụng để mô tả mối quan hệ giữa hai hoặc nhiều biến.

Hồi quy tuyến tính có 2 loại: đơn và đa biến.

Trong hồi quy tuyến tính đơn, có hai biến, một biến phụ thuộc và một biến độc lập. Nó được định nghĩa bằng hàm số

$$
y = f(x)
$$
Trong đó, x được gọi là biến độc lập, y được gọi là biến phụ thuộc.

Điểm mấu chốt trong hồi quy tuyến tính là `x` là rời rạc (các giá trị không liên quan gì đến nhau), nhưng giá trị phụ thuộc `y` phải liên tục và không thể là giá trị rời rạc.

Khi biểu diễn bằng biểu đồ, chúng ta có thể xấp xỉ vẽ được một đường thẳng đi qua các điểm có toạ độ (x,y) từ tập dữ liệu được cho. Đường thẳng xấp xỉ này gọi là fiting line.

Trong bài toán hồi quy đơn biến, phương trình đường fitting line sẽ có dạng như sau:

$$
y={\theta_0} + {\theta_1}x
$$
$\theta_0$ và $\theta_1$ là các tham số của đường thẳng mà chúng ta phải điều chỉnh. 

$\theta_1$ được gọi là slope hoặc gradient (độ dốc/hệ số góc) của fit line (đường phù hợp) và $\theta_0$ được gọi là hệ số chặn.



Theta 0 và theta 1 cũng được gọi là các hệ số của phương trình tuyến tính.

Làm thế nào để bạn vẽ một đường qua các điểm? Và làm thế nào để bạn xác định đường nào phù hợp nhất?
Hồi quy tuyến tính ước tính các hệ số của đường. Điều này có nghĩa là chúng ta phải tính theta 0 và theta 1 để tìm đường thẳng tốt nhất để phù hợp với dữ liệu.

Chúng ta hãy xem làm thế nào chúng ta có thể tìm thấy đường này hoặc, chính xác hơn, làm thế nào chúng ta có thể điều chỉnh các tham số để làm cho đường thẳng phù hợp nhất với dữ liệu.

Giả sử chúng ta đã tìm được đường fitting line, phương trình đường thẳng cho ta giá trị y=340 ở tại vị trí x=200, nhưng giá trị thực tế mong muốn là y=250, nghĩa là có sai số 90. Giá trị sai số này chúng ta gọi là residual error(sai số dư).  Chúng ta có thể nói sai số này là khoảng cách từ điểm dữ liệu đến đường hồi quy đã được fit.

Giá trị trung bình cộng của sai số cho chúng ta biết được mức độ phù hợp của đường fitting line. Gía trị trung bình cộng sai số càng lớn, nghĩa là đường thẳng fitting line càng không phù hợp. Về mặt toán học, chúng ta biểu diễn trung bình cộng các sai số này bằng phương trình **sai số toàn phương trung bình** MSE (Meaning Squared Error).
$$
MSE = \frac{1}{n}\sum_{i=1}^n(Y_i - f(x_i))^2
$$
Trong đó Yi là giá trị thực tế, và f(xi) là giá trị của đường fitting line tại điểm xi.

Mục tiêu của chúng ta là tìm ra một đường thẳng trong đó giá trị trung bình của tất cả các lỗi này được giảm đến mức tối thiểu. Nói cách khác, nên giảm đến mức tối thiểu sai số trung bình của dự đoán khi sử dụng fit line (đường phù hợp).

Nói một cách kỹ thuật hơn, mục tiêu của hồi quy tuyến tính, là để giảm đến mức tối thiểu phương trình MSE này và để làm điều đó, chúng ta nên tìm các tham số tốt nhất theta 0 và theta 1. 

Bây giờ câu hỏi là làm thế nào để tìm theta 0 và theta 1 để nó giảm đến mức tối thiểu lỗi này?

Chúng ta có nên di chuyển đường thẳng rất nhiều một cách ngẫu nhiên và tính giá trị MSE mỗi lần và chọn giá trị tối thiểu? Không hẳn. Trên thực tế, chúng ta có hai lựa chọn ở đây. Lựa chọn thứ nhất, chúng ta có thể sử dụng một phương pháp toán học, hoặc lựa chọn hai, chúng ta có thể sử dụng một phương pháp tối ưu hóa.

Chúng ta sẽ có công thức để tính như sau
$$
{\theta_1} = \frac{\sum_{i=1}^s(x_i - x^{tb})(y_i - y^{tb})}{\sum_{i=1}^s(x_i - x^{tb})^2}\
$$

$$
{\theta_0} = y^{tb} - {\theta_1}x^{tb}
$$

với x(tb) là giá trị trung bình trung bình cộng của các mẫu x(i), y(tb) là giá trị trung bình của các đầu ra y(i).

![image-20210326224405121](/Users/hoquochuy/Library/Application Support/typora-user-images/image-20210326224405121.png)

![image-20210326224528506](/Users/hoquochuy/Library/Application Support/typora-user-images/image-20210326224528506.png)

### Lợi ích của hồi quy tuyến tính

- Rất nhanh
- Không yêu cầu điều chỉnh tham số (parameter tuning)
- Dể hiểu và dễ giải thích (highly interpretable)