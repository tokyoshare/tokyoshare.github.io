---
layout: blog
title: Javascript Tips-Decapitalize một string
category: blog
tags: [NodeJS, CSV, JSON]
summary: Cách để chuyển chữ cái đầu tiên của string thành dạng chữ thường
image: /images/blog/decapitalize.jpg
---
Hôm nay mình sẽ hướng dẫn bạn cách để viết một hàm chuyển chữ cái đầu tiên của string thành dạng chữ thường. Giả sử bạn có một string, chúng ta sẽ dùng [...] để chuyển nó thành một mảng, và sau đó dùng **String.toLowerCase()** để chuyển chữ cái đầu tiên thành dạng chữ thường, **...rest** là mảng các kí tự ngay sau khí tự đầu tiên. Sau đó chúng ta sẽ dùng tiếp **Array.prototype.join('')** để merge mảng lại thành một string. Chúng ta bỏ qua parameter **upperRest** để giữ nguyên phần phía sau hoặc set nó bằng true để convert phần phía sau thành dạng chữ hoa.

```javascript
const decapitalize = ([first, ...rest], upperRest = false) =>{
  let after = upperRest ? rest.join('').toUpperCase() : rest.join('');
  return first.toLowerCase() + after;
}
```

```
Ví dụ:
decapitalize('FooBar'); 
// 'fooBar'
decapitalize('FooBar', true); 
// 'fOOBAR'
```

Link [Github](https://github.com/tokyoshare/awsome_nodejs)

