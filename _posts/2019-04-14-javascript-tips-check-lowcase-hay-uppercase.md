---
layout: blog
title: Javascript Tips-Check một string là uppercase hay là lowercase bằng 1 dòng code
category: blog
tags: [NodeJS, CSV, JSON]
summary: Cách để check một string là uppercase hay là lowercase bằng 1 dòng code
image: /images/blog/up-low.png
---
Hôm nay mình sẽ hướng dẫn bạn cách để viết 2 hàm để check xem một chuỗi là lower case(chữ thường) hay upper-case(chữ hoa) chỉ bằng 1 dòng code.

```javascript
const isLowerCase = str => str === str.toLowerCase();
```
```javascript
const isUpperCase = str => str === str.toUpperCase();
```

```
Ví dụ:
isLowerCase('abc'); // true
isLowerCase('Abc'); // false
isUpperCase('ABC'); // true
isUpperCase('aBC'); // false
```

Link [Github](https://github.com/tokyoshare/awsome_nodejs)

