---
layout: blog
title: React Fragment là gì và sử dụng nó như thế nào?
category: dev
tags: [ReactJS, Javascript, Fragment]
summary: Tại sao lại cần React Fragment và cách sử dụng
image: /images/blog/react-js.png
---
### Đặt vấn đề:

Khi lập trình ReactJS, đoạn chương trình sau sẽ bị lỗi lúc biên dịch:

```javascript
class ChilComponent extends React.Component {
    render() {
        return (
           <p>This is</p>
           <p>a list</p>
           <p>of label</p>
           <p>that I want to render</p>
        );
    }
}
```

Nguyên nhân là vì hàm `return` của React luôn yêu cầu phải đặt nội dung bạn muốn render vào trong một thẻ đóng mở. 

Ví dụ, đoạn mã trên nếu chúng ta đặt vào một thẻ đóng mở <div></div> như sau, thì nó sẽ hết lỗi:

```javascript
class ChilComponent extends React.Component {
    render() {
        return (
            <div>
                <p>This is</p>
                <p>a list</p>
                <p>of label</p>
                <p>that I want to render</p>
            </div>
        );
    }
}
```

Tuy nhiên, thẻ đóng mở được thêm vào  này là điều chúng ta không thực sự mong muốn. Vì cấu trúc của chương trình ngày càng phức tạp, thì số lượng component và phân cấp của component ngày càng nhiều hơn. Hậu quả là, khi ReactJS render ra html, bạn sẽ rơi vào một "hố đen phân cấp" kiểu như này:

```javascript
<div class="level1">
    <div class="level2">
        <div class="level3">
            ...
            <div class="leveln">
               	<div class="help-me">
                    Take me out of here!
                </div>
            </div>
            ...
        </div>
    </div>
</di>
```

Việc phân cấp thẻ div như thế này, thứ nhất là nhìn code html được render ra nhìn nó rất tệ, nhưng điều quan trọng hơn cả, là khiến cho việc bạn thiết kế css gần như sẽ thất bại về mặt tổ chức. Bạn thử hình dung lúc muốn truy cập vào một class name ở thẻ div trong cùng của "hố đen phân cấp kia" thì css của bạn cũng sẽ hoành tráng không kém:

```
.level1{
    .level2{
        ...
        .leveln{
            //I come here
            .help-me{
                
            }
        }
    }
}
```

Vậy, cách giải quyết vấn đề này là gì, rõ ràng là nó bị sinh ra chỉ vì những thẻ div đóng mở không cần thiết mà ta đã thêm vào ở trên. Nếu như chúng ta có thể render nội dung của thằng ChildComponent cùng cấp luôn với những thẻ trong thằng Component cha, thì mọi chuyện sẽ dễ dàng được giải quyết, đúng không? Và React Fragement được sinh ra vì mục đích đó.

### Cách sử dụng:

React Fragement được release vào cuối năm 2018 React v 16.2.0. Cách sử dụng nó hết sức đơn giản:

```javascript
class ChildComponent extends React.Component {
    render() {
        return (
            <React.Fragment>
                <div className="header"/>
                <div className="content"/>
            </React.Fragment>
        );
    }
}

class Component extends React.Component{
	render() {
        return (
            <div className="main">
                <div className="topnav"/>
                <ChildComponent/>
                <div className="footer"/>
            </div>
        );
    }   
}
```

Nếu như thay dùng thẻ div thay vì React Fragment, thì kết quả render sẽ ra như thế này:

```javascript
<div class="main">
    <div className="topnav"/>
    <div>
        <div className="header"/>
        <div className="content"/>
    </div>
    <div className="footer"/>
</div>
#css:
.main{
	.topnav{}
	div{
		.header{}
		.content{}
	}
	.footer{}
}
```

Tuy nhiên, vì chúng ta dùng Fragment, nên kết quả sẽ render ra như sau:
```javascript
<div class="main">
    <div className="topnav"/>
    <div className="header"/>
    <div className="content"/>
    <div className="footer"/>
</div>
#scss
.main{
	.topnav{}
	.header{}
	.content{}
	.footer{}
}
```

Bạn đã thấy sự khác biệt chưa. Thẻ React Fragment nó sẽ cho phép react render content bên trong nó ra mức ngang hàng với thằng cha của nó. Code nhìn "sạch" hơn và làm css cũng sẽ đỡ vất hơn nhiều.

※ Một lưu ý nhỏ, là thẻ <React.Fragment> chúng ta có thể khai báo bằng kiểu thẻ đóng mở `<></>` . Tuy nhiên mình khuyên các bạn không nên lạm dụng kiểu này, vì khó để check code hơn

### **Kết Luận:**

Hôm nay mình đã giới thiệu cho các bạn React Fragment là gì, và vì sao phải cần dùng đến nó, hi vọng lần sau chúng ta sẽ tìm hiểu về những vấn đề khác hay ho hơn. Hẹn gặp lại.

