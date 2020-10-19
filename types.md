# Data Types trong Javascript

#### Có 2 loại dữ liệu trong Javascript
- Primitive
- Object
#### Primitive
- Có 6 loại:
  - undefined : typeof instance === "undefined"
  - Boolean : typeof instance === "boolean"
  - Number : typeof instance === "number"
  - String : typeof instance === "string"
  - Symbol : typeof instance === "symbol"
- Có 1 loại primitive đặc biệt đó là null
  - Chúng ta có typeof null === "object"?!? WTF :D
- Chúng ta không thể tự định nghĩa ra thêm kiểu dữ liệu primitive 
- Luôn luôn immutable
```javascript
var s = "JavaScript";
s.length = 11;
console.log(s.length); // => 10
```
- So sánh: bằng giá trị
```javascript
'javascript' === 'javascript'
true === true;
11 === 11
```
#### Object
- Tất cả những kiểu dữ con lại đều là Object:  
  - Function
  - Array
  - Wrapper Class
- Đối với object chúng ta có thể khởi tạo instance bằng từ khoá new
#### Lưu ý:
- Javascript Engine trong quá trình biên dịch sẽ quyết định biến nào là loại dữ liệu nào
#### Javascript có 1 số phần gây cho chúng ta rất confuse: 
- Xem thêm ở https://github.com/denysdovhan/wtfjs
#### Vì sao null là object
- Đây là 1 bug trong JS, nó nằm trong function typeof cho đến bây giờ vẫn chưa được sửa
#### Vì sao NaN là number?
- Bởi vì định nghĩa nó define là như vậy :D. Thật ra NaN là 1 loại number nhưng không phải là number, nó là kết quả của 1 phép tính nhưng không valid as number. Ví dụ  2 * 'a'
