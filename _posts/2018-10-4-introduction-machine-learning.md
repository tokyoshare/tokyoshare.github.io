---
layout: post
title: Giới thiệu về machine learning
---
Tôi cũng là một người mới tinh với machine learning như các bạn, vì vậy những gì tôi chia sẻ là nhận thức cá nhân, có thể đúng,có thể sai, nhưng sau hết là chúng ta sẽ rút được kinh nghiệm qua những trao đổi kiến thức với nhau. Phương châm của chúng tôi là: Xây dựng một cộng đồng IT Việt mạnh giữa lòng Tokyo bằng việc chia sẽ những kiến thức của mình. 
Để bắt đầu, chúng ta sẽ tìm hiểu Machine Learning thông qua cách đặt câu hỏi 5W1H:
1. What: Machine learning là gì và không là gì?
2. Why: Tại sao lại dùng machine learning và tại sao lại không dùng?
3. When: Lúc nào thì nên dùng machine learning và lúc nào thì không?
4. Who: Ai nên sử dụng machine learning và ai không nên sử dụng machine learning?
5. Where: Nên dùng machine learning ở đâu và không nên dùng ở đâu?
6. How: Sử dụng machine learning thế nào và không nên thế nào?
Nào chúng ta hãy cùng nhau bắt đầu bước vào thế giới của Machine Learning.

## 1. Machine learning là gì và không là gì?
Chúng ta thường nghe nói tới AI, Machine Learning và Deep learning, và thường bị nhầm lẫn rằng chúng là một (vì hầu hết các sách và các tiêu đề các bài viết đều dễ gây hiểu nhầm cho người đọc). Vậy đầu tiên chúng ta phải phân biệt rõ 3 khái niệm này trước hết:
### AI
><strong>Trí tuệ nhân tạo</strong> hay <strong>trí thông minh nhân tạo</strong> (tiếng Anh: Artificial intelligence hay tiếng Anh: Machine intelligence - AI) là một ngành thuộc lĩnh vực khoa học máy tính (tiếng Anh: Computer science). Là trí tuệ do con người lập trình tạo nên với mục tiêu giúp máy tính có thể tự động hóa các hành vi thông minh như con người.

Như vậy, trí tuệ nhân tạo khác với việc lập trình logic trong các ngôn ngữ lập trình là ở việc ứng dụng các hệ thống học máy (tiếng Anh: machine learning) để mô phỏng trí tuệ của con người trong các xử lý mà con người làm tốt hơn máy tính. 
Cụ thể, trí tuệ nhân tạo giúp máy tính có được những trí tuệ của con người như: biết suy nghĩ và lập luận để giải quyết vấn đề, biết giao tiếp do hiểu ngôn ngữ, tiếng nói, biết học và tự thích nghi.

### Machine Learning
><strong>Học máy</strong> (tiếng Anh: machine learning) là 
-một lĩnh vực của trí tuệ nhân tạo 
-liên quan đến việc nghiên cứu và xây dựng các kĩ thuật cho phép các hệ thống "học" tự động từ dữ liệu đầu vào
-để giải quyết những vấn đề cụ thể

Học máy rất gần với suy diễn thống kê (statistical inference) tuy có khác nhau về thuật ngữ. Tại sao chúng ta lại nói như vậy, vì cả hai lĩnh vực đều nghiên cứu việc phân tích dữ liệu. 
Nhưng khác với thống kê, học máy tập trung vào sự phức tạp của các giải thuật trong việc thực thi tính toán. Nhiều bài toán suy luận được xếp vào loại bài toán NP-khó, vì thế một phần của học máy là nghiên cứu các giải thuật suy luận xấp xỉ mà có thể xử lý được.. 
Types of machine learning problems

There are various ways to classify machine learning problems. Here, we discuss the most obvious ones.
1. On basis of the nature of the learning “signal” or “feedback” available to a learning system

Supervised learning: The computer is presented with example inputs and their desired outputs, given by a “teacher”, and the goal is to learn a general rule that maps inputs to outputs. The training process continues until the model achieves a desired level of accuracy on the training data. Some real life examples are:
Image Classification: You train with images/labels. Then in the future you give a new image expecting that the computer will recognize the new object.
Market Prediction/Regression: You train the computer with historical market data and ask the computer to predict the new price in the future.
Unsupervised learning: No labels are given to the learning algorithm, leaving it on its own to find structure in its input. It is used for clustering population in different groups. Unsupervised learning can be a goal in itself (discovering hidden patterns in data).
Clustering: You ask the computer to separate similar data into clusters, this is essential in research and science.
High Dimension Visualization: Use the computer to help us visualize high dimension data.
Generative Models: After a model captures the probability distribution of your input data, it will be able to generate more data. This can be very useful to make your classifier more robust.
A simple diagram which clears the concept of supervised and unsupervised learning is shown below: