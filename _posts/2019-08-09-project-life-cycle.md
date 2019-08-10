---
layout: blog
title: Vòng đời dự án
category: pmp
tags: [PMP, PLC, Project, Life Cycle]
summary: Cách để chuyển chữ cái đầu tiên của string thành dạng chữ thường
image: /images/blog/git-logo.png
---

Chương 3: Các process của việc quản lý dự án

Trước khi đi vào các action cụ thể cho từng nhóm process của việc quản lý dự án, chúng ta sẽ trao đổi qua về định nghĩa của vòng đời dự án (Project Life Cycle) và process của việc quản lý dự án.

**Vòng đời dự án (Project Life Cycles)**

Một vòng đời dự án là một chuỗi các phase mà một project sẽ trải qua từ lúc bắt đầu đến lúc kết thúc dự án. 

**Project phase:** là một tập hợp các hoạt động liên quan về mặt logic được kết hợp với nhau để đưa ra một hoặc nhiều output hoàn chỉnh. 

Các phase trong vòng đời dự án có thể tuần tự, không liên tục hoặc là overlap lên nhau. 

> **Kiểu tuần tự (Sequential):** Kết thúc phase này mới tiếp tục phase tiếp theo.
>
> **Không liên tục(Iterative):** Các phase có thể tiến hành ngắt quãng, không theo thứ tự nhất định.
>
> **Kiểu chồng chập(Overlap):** Các phase có thể tiến hành song song, trong lúc tiến hành phase này thì có thể tiến hành phase khác luôn. 

Tên, số lượng và thời hạn của các phase của project được xác định theo yêu cầu của cty, tính chất và lĩnh vực của dự án. 

Các phase là hữu hạn về thời gian(time bound), nó sẽ phải có điểm bắt đầu và kết thúc hoặc điểm kiểm soát (control point). Chúng ta có thể gọi những điểm kiểm soát này là phase view, phase gate, control gate. Ở thời điểm control point này, project charter và business document sẽ được xem xét/đánh giá lại dựa trên hoàn cảnh hiện tại. Lúc đó, perfomance của dự án sẽ được so sánh với plan của dự án để xác định xem project nên thay đổi, đóng hay tiếp tục như đã lên kế hoạch

Trong từng phase chúng ta lại phải chia thành nhiều phase con khác nhau, và tập hợp các phase con này chúng ta gọi nó là vòng đời phát triển (development life cycle). Nhiệm vụ của vòng đời phát triển này là để đảm bảo rằng performance cũng như mục tiêu của dự án được đảm bảo và kiểm soát. Một ví dụ của vòng đời phát triển là trong một dự án phầm mềm, chúng ta sẽ có các phase sau: research-> design-> code -> test -> implement.

Vòng đời dự án có thể có 2 kiểu: hướng kế hoạch (plan-driven) hoặc hướng theo thay đổi (change-driven).

> Vòng đời hướng kế hoạch (Plan-driven): Các project có vòng đời kiểu này sẽ có các vòng đời phát triển có thể dự đoán trước được. Vòng đời kiểu này có thường gọi bằng tên là mô hình thác nước (waterfall) hoặc vòng đời truyền thống(traditional life cycle). Thường những dự án kiểu này thì scope, schedule và costs sẽ được xác định chi tiết từ rất sớm - trước khi dự án được bắt đầu. 
>
> Ví dụ: Một dự án xây dựng thường sẽ dùng vòng đời kiểu này, vì scope, schedule và dự toán đều có thể dự đoán khá chính xác từ sớm.

> Vòng đời hướng thay đổi (Change-driven): dùng các vòng đời phát triển kiểu lặp(iterative), tăng trưởng(incremental) hoặc thích nghi (adptive-agile) và thường là sẽ có các mức độ chi tiết khác nhau của việc lên plan sớm cho scope, schedule và cost của dự án.
>
> Đối với vòng đời phát triển kiểu lặp và tăng trưởng thì plan sớm sẽ ở mức chi tiết đủ để cho phép ước tính thời gian, giá. Phạm vi của dự án sẽ được nâng dần từng chút sau mỗi lần lặp lại.
>
> Vòng đời phát triển kiểu tăng trưởng: sẽ cung cấp từng phần hoàn chỉnh, có thể sử dụng của sản phẩm sau mỗi lần lặp. Ví dụ, một dự án phần mềm có nhiều module, mỗi lần lặp chúng ta sẽ bàn giao một module hoàn chỉnh từ đầu đến cuối.
>
> Vòng đời phát triển kiểu lặp: chúng ta sẽ tạo ra nhữn
>
> Change-driven projects use iterative, incremental, or adaptive
> (agile) development life cycles, and have varying levels of early planning for scope, schedule, and cost.
> Incremental and iterative life cycles involve early planning of high-level scope sufficient enough to allow for
> preliminary estimates of time and cost; scope is developed a little more with each iteration.
> An incremental development life cycle delivers a complete, usable portion of the product for each iteration.
> For example, a project to build a website using an incremental life cycle would involve prioritizing
> requirements into iterations that deliver a fully functioning portion of the website at the end of each iteration.
> With an iterative development life cycle, the complete concept is built in successive levels of detail to create
> the end result. To build the website mentioned in the previous paragraph using an iterative life cycle,
> planning for the first iteration would focus on planning to create a prototype of the entire website. After the
> basic skeleton of the site is built, each successive iteration would be planned to add more detail until a
> complete and fully functioning site is achieved.
> Note that a project may use a combination of incremental and iterative life cycles throughout the project or
> for phases of the project.
> Adaptive development life cycles involve a fixed schedule as well as fixed costs. Scope is broadly defined
> with the understanding that it will be refined throughout the life of the project. The customer s requirements
> are documented and prioritized in a backlog, which can be adjusted as the project progresses. Work is
> planned in short increments to allow the customer to change and reprioritize requirements within the time
> and cost constraints. A new software development project may follow an adaptive approach, using phases
> that might include high-level feasibility, design, and planning followed by short, iterative phases of detailed
> design, coding, testing, and release. 