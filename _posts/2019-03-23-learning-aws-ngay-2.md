---
layout: blog
title: Học AWS trong 30 ngày (Ngày 2)
category: aws
tags: [AWS, Certification]
summary: AWS gồm có những gì và Associate Cert sẽ thi những phần nào
image: /images/blog/aws2.png
---

# AWS gồm có những gì

![](E:\WebProjects\Tokyoshare\images\blog\aws8.png)

AWS gồm rất nhiều service phục vụ cho hầu hết các mảng. Các service này sẽ được gom lại theo group tính năng. Ví dụ như group Compute sẽ bao gồm những service cung cấp khả năng điện toán (computing) cho hệ thống, trong khi group Storage lại cung cấp những service chuyên phục vụ cho việc lưu trữ. Tương tự thế với group Databases và những mảng khác. Hiện nay, AWS có tổng cộng hơn 2000 service và tính năng. Một con số thực sự khủng khiếp, đấy cũng là lý do tại sao nó lại dẫn đầu trong thị trường điện toán đám mây.

![](/images/blog/aws2/service.png)

### AWS Certified Solutions Architect – Associate

Như bài trước đã có nói về các chứng chỉ AWS có nhiều career path khác nhau. Chúng ta sẽ lựa chọn career path AWS Certified Solutions Architect – Associate để đi xuyên suốt 30 ngày học của chúng ta. Thực ra không có lý do nào cho việc lựa chọn này cả, chỉ đơn giản là mình thích thì mình chọn thôi =)).

Về phương pháp học của cá nhân mình:

**Dành 30% thời gian để đọc tài liệu** hoặc luyện các khoá trên Udemy. Có một khóa trên Udemy được mọi người đánh giá rất cao đó là: [AWS Certified Solutions Architect – Associate 2018](https://www.udemy.com/aws-certified-solutions-architect-associate/). Khóa học này có phần thực hành khá là hay. 

**Dành 30% để thực hành**. Để thực hành, bạn có thể tạo 1 tài khoản [AWS miễn phí ](https://aws.amazon.com/free/)trong 1 năm. Lưu ý, tài khoản này chỉ cung cấp một số thứ miễn phí có giới hạn cho các dịch vụ cơ bản như: 750h/tháng cho EC2, 5 GB dung lượng S3, 750h/tháng cho RDS. Do đó, nhiều dịch vụ khác sẽ tính phí như bình thường, cần cẩn trọng theo dõi hoặc dùng xong thì tắt ngay để không mất tiền oan. 

**Dành khoảng 40% thời gian để luyện đề**. Theo mình thì học là một chuyện, quan trọng muốn đậu bất kì kì thi nào để phải luyện đề cả. Luyện đề cũng là cách để mình củng cố và học thêm kiến thức. 

### Nội dung thi

Đề thi của AWS sẽ tập trung vào các group kiến thức sau: Network, Compute, Storage, Database, Security và  Application Services. Phần lớn nội dung sẽ tập trung vào các dịch vụ:

**Network**: chiếm khoảng 20%, phần lớn hỏi về VPC, kết nối VPN, mạng con. Ngoài ra, một số ít kiến thức về chia IP của mạng con.

![](/images/blog/aws2/Others.png)

**Compute**: chiếm khoảng 20%, hỏi về EC2, Load balancing (Cân bằng tải) , Auto scaling và một phần rất ít về Lamda, Kinesis.

![](/images/blog/aws2/Compute.png)

**Storage**: chiếm khoảng 20%. Phần lớn sẽ hỏi về S3, CloudFont, EBS. Phần ít còn lại hỏi về Glacier, AWS Import/Export.

![](/images/blog/aws2/Storage.png)

**Security**: chiếm khoảng 10%. Hỏi nhiều về IAM, bảo mật cho VPC như Access Control List (ACL), bảo mật cho EC2 như Security Group, so sánh giữa ACL kết nối VPN, Ngoài ra, còn hỏi một ít về mã hóa dữ liệu trong các dịch vụ lưu trữ như S3, EBS.

![](/images/blog/aws2/Administration.png)

**Database**: chiếm khoảng 10%. Phần lớn sẽ hỏi mình nên dùng loại dịch vụ database nào để làm hệ thống có tính A,B,C gì đó : DynamoDB hay RDS. Ngoài ra, đâu đó cũng hỏi ít về Backup, Multi-AZ và Read Replica.

![](/images/blog/aws2/Database.png)

**Application Services**: chiếm khoảng 10%. Hỏi về Cloud Watch, Cloud Trail, SQS, SNS.

![](/images/blog/aws2/ApplicationService.png)

### Lộ trình học

Dựa vào những phân tích trên, chúng ta sẽ đi theo lộ trình học để luyện thi SAA như sau:

| Ngày  | Nội dung                                                     |
| ----- | ------------------------------------------------------------ |
| 3     | Region/AZ/Edge                                               |
| 4     | IAM                                                          |
| 5     | Networking: VPC/EC2/ACL                                      |
| 6     | Computing: EC2/AMI/EBS/Dedicated                             |
| 7     | Storage: S3/Glacier                                          |
| 8     | Database: RDS/ElastiCache/DynamoDB                           |
| 9     | Application Services:  Cloudwatch/SNS                        |
| 10    | ELB/Auto Scaling/SQS/SWF                                     |
| 11    | DNS and Content: Route 53/CloudFront                         |
| 12    | Provisioning/Deploy: CloudFormation/Elastic Beanstalk/OpsWorks |
| 13-20 | Thực hành                                                    |
| 10-30 | Luyện đề                                                     |

### Kết luận

Như vậy, hôm nay chúng ta đã đưa ra được nội dung thi và lộ trình học để có thể lấy được AWS trong vòng 1 tháng. Hẹn gặp lại các bản trong ngày tiếp theo.