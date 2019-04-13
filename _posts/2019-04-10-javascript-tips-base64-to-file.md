---
layout: blog
title: Javascript Tips-Lưu base64 string thành file
category: dev
tags: [NodeJS, CLI, Todo]
summary: Cách để convert ba64 thành file
image: /images/blog/tip.jpg
---
Thông thường, người ta sẽ convert một file thành một chuỗi base64 để truyền qua mạng. Tuy nhiên, có đôi lúc bạn cần phải convert một chuỗi base64 lại thành một file. Hôm nay mình sẽ hướng dẫn các bạn cách làm điều đó.

Ví dụ chúng ta có một file ảnh base 64 như sau:

```
data:image/png;base64,iVBORw0KGgoAAAANSUhEUgA...
```

Để convert nó thành file ảnh, code của chúng ta như sau

```javascript
import fs from 'fs';
// Base64 image string
let base64String = 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgA'; 
// Remove header
let base64Image = base64String.split(';base64,').pop();
// Write file
fs.writeFile('image.png', base64Image, {encoding: 'base64'}, function(err) {
    console.log('File created');
});
```
Bạn nhớ phải có tham số **{encoding: 'base64'}** để nó nhận biết là ghi file từ base64 string nhé.

Link [Github](https://github.com/tokyoshare/awsome_nodejs)