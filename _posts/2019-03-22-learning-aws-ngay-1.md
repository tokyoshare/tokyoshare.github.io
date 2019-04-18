---
layout: blog
title: Học AWS trong 30 ngày (Ngày 1)
category: aws
tags: [AWS, Certification]  
summary: Amazon Web Service và hệ thống chứng chỉ
image: /images/blog/aws-certifications.png
---

# Amazon Web Services

Đầu tiên, chúng ta sẽ bàn qua một chút về Amazon Web Services (từ giờ về sau chúng ta sẽ gọi tắt là AWS trong tất cả các bài viết). Như các bạn đã biết, thì AWS hiện đang là dịch vụ điện toán đám mây (cloud computing) lớn nhất trên thế giới, chiếm tầm 50% thị phần (xếp trên cả Google Cloud và Azure của Microsoft). Đây là con gà đẻ trứng vàng cho Amazon vì từ ngày có cloud computing, tài sản của chủ tập đoàn Amazon tăng với tốc độ phi mã để lên đứng đầu thế giới, thế là đủ để bạn hiểu nó đóng vai trò lớn thế nào cho Amazon rồi đó. Nhưng điều gì khiến cloud computing trở nên hot như vậy?

Quay lại thời kì tầm 15-20 năm trước, khi công nghệ web bùng nổ dữ dội với sự phát triển của internet tốc độ cao (ADSL), lúc đó, người người làm web, nhà nhà làm web, đến bà bán bún cũng có trang web riêng để quảng cáo thương hiệu. Lúc đó, việc sở hữu một trang web cũng là mốt thời thượng giống như người ta sở hữu iphone, macbook ngày nay vậy. Và để đưa được trang web của bạn lên, bạn cần có một tên miền(domain), một server(host) để lưu trữ dữ liệu và database. Đấy là lúc những dedicated server và shared server trở thành trào lưu. Tuy nhiên, vấn đề đặt ra là, chi phí cho một dedicated server/shared server khá tốn kém (nhớ không nhầm thì đâu đó tầm 10-20$/tháng cho một cái host tầm 500MB vào tầm năm 2008). Đối với những doanh nghiệp nhỏ thì không vấn đề gì, vì họ sẽ chọn những gói rẻ nhất. Nhưng với các doanh nghiệp lớn, thì vấn đề kinh doanh phức tạp hơn nhiều, vì phải thuê những server khủng hàng nghìn đô/tháng hoặc phải tự lắp đặt vận hành server riêng tốn kém, nhưng lại không thể dùng hết công suất vì không phải lúc nào cũng có người dùng truy cập hệ thống. Lúc này, bài toán đặt ra là: Liệu có giải pháp nào giúp tối ưu hoá chi phí về hạ tầng cho các doanh nghiệp, dùng bao nhiêu thì trả tiền bấy nhiêu hay không? 

Và cloud computing (cụ thể là AWS) xuất hiện để trả lời cho câu hỏi đó. AWS không chỉ cung cấp  cho người dùng các nền tảng về tính toán (hệ điều hành trên đám mây) mà nó còn cung cấp nền tảng cho việc lưu trữ(storage), cơ sở dữ liệu (database).  

Bây giờ, bạn hãy nhìn tổng quan về những service mà AWS có thể cung cấp cho chúng ta:

![](/images/blog/aws1.jpg)

![](/images/blog/aws2.jpg)

Những dịch vụ này giúp doanh nghiệp tiết kiệm nhiều thời gian và chi phí trong việc phát triển và vận hành các sản phẩm/dịch vụ trên nền tảng internet. Nó ngày càng đóng vai trò sống còn cho nhiều doanh nghiệp. 

Vì nó quan trọng thế, nên nếu bạn muốn làm thì bạn phải biết, mà muốn biết thì bắt buộc phải học chứ chẳng ai lại đi giao tính mạng của cả doanh nghiệp cho những tay gà mờ được. Và vì thế Amazon cung cấp các gói chứng chỉ cho những người học, để bạn và doanh nghiệp biết bạn đang ở đâu để làm công việc phù hợp với trình độ và năng lực của mình. Chúng ta gọi đó là hệ thống chứng chỉ AWS (AWS Certifications).

# AWS Cerifications

![](/images/blog/aws3.jpg)

Hiện nay, hệ thống chứng chỉ của AWS bao gồm 4 cấp bậc, tuỳ thuộc vào kinh nghiệm sử dụng AWS của từng người:

**Foundational:** Dành cho những người sử dụng AWS khoảng tầm 6 tháng, biết cơ bản về AWS.

**Associate:** Dành cho những người có kinh nghiệm tầm 1 năm sử dụng và giải quyết các vấn đề liên quan cũng như thực thi các giải pháp sử dụng AWS.

**Professional:** Dành cho những người có tầm 2 năm kinh nghiệm về thiết kế, vận hành và đưa ra các giải pháp sử dụng AWS.

**Specialty:** Dùng cho các chuyên gia, những người có kinh nghiệm cực kì sâu sắc về một mảng chuyên biệt trên AWS.

Tuy nhiên trong từng cấp độ đó, thì nó lại chia thành nhiều loại chứng chỉ con. Ví dụ như cấp độ Associate thì bạn có thể lựa chọn học và thi chứng chỉ Solutions Architect, Developer hoặc SysOps Administor. Sang cấp độ Professional thì bạn có thể lựa chọn thi chứng chỉ Solution Architect Professional hoặc DevOps Engineer Professional v.v... Các chứng chỉ này tuỳ vào sở thích và sở trường của từng người để chúng ta có thể lựa chọn care path (tạm gọi là lộ trình) cho bản thân mình. 

# Lộ trình

Chúng ta tạm thời chia lộ trình học theo 4 role như sau:

**1. Cloud Practitioner (Tập sự):**

Lộ trình này được thiết kế dành cho **những cá nhân đang muốn xây dựng và chứng nhận hiểu biết chung về AWS Cloud**. Nó hữu ích với những người đang nắm giữ vị trí kỹ thuật, quản lý, bán hàng, mua hàng hoặc tài chính .v.v... mà có sử dụng liên quan tới AWS Cloud.

 ![](/images/blog/aws4.jpg)



**2. Architect (Kiến trúc hệ thống)**:

Lộ trình này được thiết kế cho **các kiến trúc sư giải pháp, kỹ sư thiết kế giải pháp **và tất cả những ai muốn **tìm hiểu cách thiết kế ứng dụng và hệ thống trên AWS**.  

Bạn sẽ xuất phát từ vị trí là một tập sự (Cloud Practitioner) hoặc có kiến thức tương đương, tham gia 1 khoá học về thiết kế kiến trúc trên AWS và tham gia kì thi AWS để đạt được chứng chỉ AWS Solution Architect Associate. 

Tiếp đó, sau khi đã có chứng nhận AWS Solution Architect Associate rồi, bạn sẽ tham gia một khoá học nâng cao về thiết kế và kiến trúc AWS và tham gia kì thi Solution Architect-Professional để đạt chứng chỉ chuyên nghiệp

![](/images/blog/aws5.jpg)

**3. Developer (Lập trình):**

Lộ trình này được thiết kế cho các nhà phát triển phần mềm, những người muốn học cách để phát triển các ứng dụng trên nền tảng AWS. 

Xuất phát điểm của bạn vẫn là vị trí tập sự (Cloud Practitioner) hoặc tương đương, sau đó bạn sẽ phải học về develop trên nền tảng AWS, cuối cùng là tham gia kì thi để đạt được chứng chỉ AWS Developer Assosicate.

Sau khi đã có chứng chỉ rồi, lộ trình tiếp theo bạn sẽ theo đuổi là AWS DevOps Engineer Professional. Lúc này bạn sẽ phải tham gia các khoá học về DevOps Engineering trên AWS. Sau đó thì bạn cũng phải tham gia một kì thi để lấy chứng chỉ DevOps Engineer Professional. Muốn biết DevOps là gì mời bạn đọc bài viết khác của tôi [Link](<https://tokyoshare.github.io/blog/devops.html>)

![](/images/blog/aws6.jpg)

**4.Operations(Vận hành):**

Lộ trình này được thiết kế cho các **sysops administrator**, **systems administrator**, và những người làm việc ở vị trí DevOps (lộ trình 3) muốn học **cách để tạo deploy tự động cho các ứng dụng, network cũng như các hệ thống trên nền tảng AWS.** 

Xuất phát điểm của bạn vẫn là vị trí tập sự (Cloud Practitioner) hoặc tương đương, sau đó bạn sẽ phải học về SysOps Administrating trên AWS, bạn phải tham gia một kì thi để được cấp chứng chỉ AWS SysOps Administrator Associate. 

Tiếp theo đó, bạn sẽ phải học về DevOps Engineering trên AWS, rồi tham gia kì thi để được cấp chứng chỉ AWS DevOps Engineer Professional.

![](/images/blog/aws7.jpg)

# So sánh giữa các kì thi

Các kì thi chứng chỉ AWS đều có hình thức thi là thi trắc nghiệm dạng multi-choice trên máy tính tại các trung tâm dự thi. Bạn có thể thi bằng tiếng Anh, tiếng Nhật, Hàn hoặc Trung tuỳ thích. Trước khi thi một thời gian thì bạn phải tìm trung tâm dự thi ở gần khu vực mình sinh sống, đăng kí và đóng phí để hẹn lịch thi. Bạn có thể vào link sau và làm theo hướng dẫn để đăng kí dự thi: [Link đăng kí dự thi AWS](https://www.aws.training/certification).

Dưới đây là bảng so sánh thông ti cơ bản của các kì thi dựa trên tiêu chí Loại kì thi, Thời gian dự thi, Giá tiền và ngôn ngữ

| Tên chứng chỉ                                    | Kiểu thi    | Loại kì thi  | Thời gian dự thi | Giá tiền | Ngôn ngữ                              |
| ------------------------------------------------ | ----------- | ------------ | ---------------- | -------- | ------------------------------------- |
| AWS Certified Cloud Practitioner                 | Trắc nghiệm | Cơ bản       | 90 phút          | 100$     | English, Japanese, Korean, Trung Quốc |
| AWS Certified Solutions Architect – Associate    | -           | Asscociate   | 130 phút         | 150$     | -                                     |
| AWS Certified Developer - Associate              | -           | Asscociate   | 130 phút         | 150$     | -                                     |
| AWS Certified SysOps Administrator – Associate   | -           | Asscociate   | 130 phút         | 150$     | -                                     |
| AWS Certified Solutions Architect – Professional | -           | Professional | 170 phút         | 300$     | -                                     |
| AWS Certified DevOps Engineer – Professional     | -           | Professional | 170 phút         | 300$     | -                                     |
| AWS Certified Security – Specialty               | -           | Specialty    | 170 phút         | 300$     | -                                     |
| AWS Certified Big Data – Specialty               | -           | Specialty    | 170 phút         | 300$     | -                                     |
| AWS Certified Advanced Networking – Specialty    | -           | Specialty    | 170 phút         | 300$     | -                                     |
| AWS Certified Machine Learning – Specialty       | -           | Specialty    | 170 phút         | 300$     | -                                     |
| AWS Certified Alexa Skill Builder – Specialty    | -           | Specialty    | 170 phút         | 300$     | -                                     |

# KẾT THÚC

OK, như vậy hôm nay chúng ta đã biết được sơ lược về AWS, các hệ thống chứng chỉ và thông tin cơ bản về các kì thi. Ở bài tiếp theo trong loạt bài này, chúng ta sẽ tiếp tục học về loại chứng chỉ Architect Associate. Hẹn gặp lại các bạn ở bài viết sau.