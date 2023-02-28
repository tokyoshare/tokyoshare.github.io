- Contents

  - [1. AWS VPC là gì ?](https://cuongquach.com/aws-vpc-la-gi.html#1_AWS_VPC_la_gi)
  - [2. Lợi ích của VPC](https://cuongquach.com/aws-vpc-la-gi.html#2_Loi_ich_cua_VPC)
  - [3. Các tính năng của VPC](https://cuongquach.com/aws-vpc-la-gi.html#3_Cac_tinh_nang_cua_VPC)
  - [4. Các thành phần cốt lõi của VPC](https://cuongquach.com/aws-vpc-la-gi.html#4_Cac_thanh_phan_cot_loi_cua_VPC)
  - [Tổng kết](https://cuongquach.com/aws-vpc-la-gi.html#Tong_ket)

  ## 1. AWS VPC là gì ?

  **[Amazon](https://cuongquach.com/tag/amazon) Virtual Private Cloud** giúp bạn tạo ra một môi trường mạng riêng ảo nơi mà bạn có thể sử dụng để kết nối nội bộ giữa các dịch vụ **AWS** theo cách bạn quản trị phục vụ cho các mục tiêu bảo mật hệ thống. Bạn sẽ có toàn quyền quản lý môi trường hệ thống mạng riêng ảo của bạn bao gồm : *tạo subnet, cấu hình bảng routing, gateway mạng, lựa chọn sử dụng IPv4 hay IPv6 trong VPC*.

  

  ![amazon vpc là gì - 1](https://cuongquach.com/resources/images/2019/03/default-vpc-diagram.png)amazon vpc là gì – 1

  Bạn dễ dàng tuỳ biến cấu hình mạng đối với **Amazon VPC**. Ví dụ như bạn có thể tạo ra một subnet mạng public dành cho web server để bên ngoài truy cập vào, còn lại bạn cấu hình cho hệ thống backend như database hoặc ứng dụng server nằm trong lớp mạng nội bộ (private) không có đường kết nối Internet public. Bạn còn có thể gia cố thêm nhiều lớp bảo mật cho hệ thống mạng dịch vụ AWS của bạn với : *security group, access control list network,*… giúp bạn kiểm soát chặt chẽ hơn nữa quyền truy cập vào các Amazon EC2 Instance chẳng hạn.

  Một số dịch vụ AWS có thể sử dụng **AWS VPC** như sau :

  - Amazon EC2
  - Amazon Route 53
  - Amazon WorkSpaces
  - Auto Scaling
  - Elastic Load Balancing
  - AWS Data Pipeline
  - Elastic Beanstalk
  - Amazon Elastic Cache
  - Amazon EMR
  - Amazon OpsWorks
  - Amazon RDS
  - Amazon Redshift

  ## 2. Lợi ích của VPC

  ![amazon vpc là gì - 2](https://cuongquach.com/resources/images/2019/03/subnets-diagram.png)amazon vpc là gì – 2

  - **Bảo mật**

  Amazon VPC cung cấp các tính năng bảo mật nâng cao, chẳng hạn như Security Group và ACL cho mạng VPC, giúp bạn được phép lọc các lưu lượng đi vào (inbound) và đi ra (outbound). Ngoài ra, bạn có thể lưu trữ dữ liệu trong Amazon S3 và hạn chế quyền truy cập đến S3 từ các máy chủ trong VPC của bạn.

  - **Đơn giản**

  Bạn có thể tạo VPC nhanh chóng và dễ dàng bằng “**Bảng điều khiển quản lý AWS**” (*AWS Management Console*). Nếu bạn không muốn thiết lập VPC kĩ càng thì có thể chọn những thiết lập VPC phổ biến phù hợp với nhu cầu của bạn. Từ đó các thông tin như Subnet, dải IP, bảng định tuyến và **Security Group** sẽ được tạo tự động cho bạn để bạn có thể tập trung vào việc tạo các ứng dụng để chạy trong VPC của mình.

  - **Mở rộng**

  **Amazon VPC** cung cấp tất cả các lợi ích giống như các phần còn lại của nền tảng AWS. Bạn có thể ngay lập tức mở rộng quy mô tài nguyên của mình lên hoặc xuống,

  ## 3. Các tính năng của VPC

  ![amazon vpc là gì - 3](https://cuongquach.com/resources/images/2019/03/virtual-private-gateway-diagram.png)amazon vpc là gì – 3

  - Kết nối trực tiếp Internet public từ lớp mạng public. Bạn có thể khởi tạo instance từ một subnet public có thể gửi và nhận dữ liệu trực tiếp với Internet.
  - Kết nối đến Internet Public thông qua **NAT (private subnet)**. Nếu bạn chạy các Instance ở phía trong mạng nội bộ và có nhu cầu muốn truy xuất ra Internet public thì có thể định tuyến lưu lượng qua **NAT Gateway** ở lớp mạng public.
  - Kết nối an toàn tới trung tâm dữ liệu của bạn. Mọi lưu lượng vào và ra máy chủ Instance trong **VPC** có thể được định tuyến tới Data Center, hỗ trợ VPN phần cứng IPSec.
  - Kết nối riêng (private connect) giữa các VPC peer VPC giúp chia sẻ tài nguyên qua lớp mạng ảo hoá sở hữu của nhiều tài khoản AWS.
  - Kết nối riêng với các dịch vụ của AWS thông qua **VPC Endpoint** bao gồm các dịch vụ : S3, DynamoDB, Kinesis Streams, Service Catalog, AWS Systems Manager, Elastic Load Balancing (ELB) API, Amazon Elastic Compute Cloud (EC2) API và SNS.
  - Kết nối riêng (private connect) đến các giải pháp SaaS do **[AWS](https://cuongquach.com/tag/aws) PrivateLink** hỗ trợ.
  - Kết nối riêng (private connect) đến các dịch vụ nội bộ thông qua các tài khoản khác nhau và mô hình **VPC** khác trong hệ thống của tổ chức/doanh nghiệp của bạn nhằm giúp đơn giản hoá kiến trúc mạng nội bộ.

  ## 4. Các thành phần cốt lõi của VPC

  ![amazon vpc là gì - 4](https://cuongquach.com/resources/images/2019/03/vpc-endpoint.png)amazon vpc là gì – 4

  - **Subnet**: là một dải địa chỉ IP trong VPC của bạn. Bạn có thể khởi tạo tài nguyên AWS với một Subnet chỉ định. Ví dụ sử dụng public subnet để các dịch vụ của bạn truy cập được Internet, còn thì sử dụng Private Subnet để các dịch vụ của bạn trong lớp mạng nội bộ bảo mật không truy cập Internet.
  - **Internet Gateway**: Internet Gateway cho phép bạn tạo một subnet public có route kết nối ra Internet public. Tất cả Instance sẽ kết nối Internet public qua Gateway này.
  - **Security Group**: là lớp bảo mật đầu tiên dành cho các Instance, hoạt động như một  ảo firewall và bạn sẽ phải định nghĩa rule firewall trước khi traffic ra vào Instance.
  - **Route Table**: Một bảng định tuyến bao gồm các rule được gọi là ‘route’, các route này sẽ giúp xác định đường đi của lưu lượng mạng ra vào. Mỗi subnet trong VPC của bạn sẽ được liên kết với một bảng định tuyến (route table), bảng định tuyến này sẽ quản lý route trong subnet. Một subnet chỉ có thể liên kế với 1 bảng định tuyến tại 1 thời điểm, nhưng chiều ngược lại bạn có thể liên kết nhiều subnet với 1 bảng định tuyến.
  - **Network Access Control Lists (ACLs)** : là một lớp bảo mật hoạt động không khác như một firewall giúp bạn kiểm soát lưu lượng ra vào của một hoặc nhiều Subnet khác nhau. Bạn có thể sẽ cấu hình Network ACL
  - **VPC CIDR Block** : mỗi VPC được liên kết (associated) với một dải địa chỉ IP là một phần của Classless Inter-Domain Routing (CIDR) block mà được sử dụng để cấp phát ( hay phân bổ ) địa chỉ IP private đến EC2 Instances ,tất cả VPC mặc định sẽ được liên kết 1 dải địa chỉ 172.31.0.0/16 với IPv4 CIDR block

  ## Tổng kết

  Vậy là bạn đã tìm hiểu cơ bản về[ **Amazon VPC**](https://cuongquach.com/aws-vpc-la-gi.html) rồi phải không nào ? Ở các phần kế tiếp chúng ta sẽ tiếp tục tìm hiểu về : *cách tạo VPC, các tính năng nâng cao khác trong VPC như ACL, Internet Gateway,…*