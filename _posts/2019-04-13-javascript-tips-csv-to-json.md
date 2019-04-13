---
layout: blog
title: Javascript Tips-Convert CSV file thành JSON
category: blog
tags: [NodeJS, CSV, JSON]
summary: Cách để convert file csv thành JSON
image: /images/blog/csv.png
---
Hôm nay mình sẽ giới thiệu cho các bạn cách convert một file CSV(comma-separated values) thnahf một mảng object 2 chiều với hàng đầu tiên được dùng như các field của object.

Chúng ta sẽ dùng **Array.prototype.slice()** và **Array.prototype.indexOf('\n')**  và **String.prototype.split(delimiter)** để lấy mảng tên column. Tiếp đến, ta sẽ dùng **String.prototype.split('\n')** để lấy mảng các hàng, sau đó dùng **Array.prototype.map()** và **String.prototype.split(delimiter)** để chia các giá trị này thành từng dòng. Cuối cùng, chúng ta dùng **Array.prototype.reduce()** để tạo object cho từng dòng, với key chính là tên của cột trong file csv. Khi gọi hàm CSVToJSON, bạn có thể bỏ qua tham số delimiter để dùng giá trị mặc định là dấu ","

```javascript
const CSVToJSON = (data, delimiter = ',') => {
  //get array of column names
  const titles = data.slice(0, data.indexOf('\n')).split(delimiter);
  //get array of rows
  const rows = data.slice(data.indexOf('\n') + 1) .split('\n');
  //return array of json objects
  return rows.map(v => {
      const values = v.split(delimiter);
      return titles.reduce((obj, title, index) => ((obj[title] = values[index]), obj), {});
    });
};
```

```
Ví dụ:
CSVToJSON('col1,col2\na,b\nc,d'); 
// [{'col1': 'a', 'col2': 'b'}, {'col1': 'c', 'col2': 'd'}];

CSVToJSON('col1;col2\na;b\nc;d', ';'); 
// [{'col1': 'a', 'col2': 'b'}, {'col1': 'c', 'col2': 'd'}];
```

Link [Github](https://github.com/tokyoshare/awsome_nodejs)

