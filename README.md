# Documention

## Validation

### Syntax
```
$request->validate([
    'variant_attribute_value_id' =>["required"],
]);
```
### Helper
```
required: Kiểm tra xem trường dữ liệu có được nhập hay không.
```
```
nullable: Cho phép trường dữ liệu có thể null.
```
```
filled: Kiểm tra xem trường dữ liệu có được nhập và không trống hay không.
```
```
email: Kiểm tra xem trường dữ liệu có định dạng email hợp lệ hay không.
```
```
url: Kiểm tra xem trường dữ liệu có định dạng URL hợp lệ hay không.
```
```
alpha: Kiểm tra xem trường dữ liệu chỉ chứa các ký tự chữ cái.
```
```
alpha_num: Kiểm tra xem trường dữ liệu chỉ chứa các ký tự chữ cái và số.
```
```
alpha_dash: Kiểm tra xem trường dữ liệu chỉ chứa các ký tự chữ cái, số và dấu gạch ngang.
```
```
numeric: Kiểm tra xem trường dữ liệu có phải là một số hay không.
```
```
integer: Kiểm tra xem trường dữ liệu có phải là một số nguyên hay không.
```
```
boolean: Kiểm tra xem trường dữ liệu có phải là một giá trị boolean hay không.
```
```
array: Kiểm tra xem trường dữ liệu có phải là một mảng hay không.
```
```
date: Kiểm tra xem trường dữ liệu có định dạng ngày hợp lệ hay không.
```
```
date_format:format: Kiểm tra xem trường dữ liệu có đúng định dạng ngày cho trước hay không. Định dạng phải được xác định bằng cú pháp format (ví dụ: date_format:Y-m-d).
```
```
before:date: Kiểm tra xem trường dữ liệu có trước ngày được chỉ định hay không. Ngày phải được định dạng theo cú pháp YYYY-MM-DD.
```
```
after:date: Kiểm tra xem trường dữ liệu có sau ngày được chỉ định hay không. Ngày phải được định dạng theo cú pháp YYYY-MM-DD.
```
```
unique:table,column,except,idColumn: Kiểm tra xem giá trị của trường dữ liệu có duy nhất trong cột column của bảng table hay không. Có thể bỏ qua một giá trị cụ thể với cột idColumn và giá trị tương ứng của nó với except.
```
```
exists:table,column: Kiểm tra xem giá trị của trường dữ liệu có tồn tại trong cột column của bảng table hay không.
```
```
regex:pattern: Kiểm tra xem giá trị của trường dữ liệu có khớp với mẫu biểu thức chính quy pattern hay không
```

