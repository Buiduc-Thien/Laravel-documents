# Documentation

- [Documentation](#documentation)
  - [Validation](#validation)
    - [Syntax](#syntax)
    - [Validate](#validate)
  - [Query Builder](#query-builder)
    - [Syntax](#syntax-1)
  - [Error Handling](#error-handling)
    - [Syntax](#syntax-2)
    - [Exceptions](#exceptions)

## Validation

### Syntax

```
$request->validate([
    'variant_attribute_value_id' =>["required"],
]);
```

### Validate

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

## Query Builder

### Syntax

```
DB::table('table_name'): Đây là Query Builder cơ bản của Laravel để truy vấn một bảng trong CSDL. Nó cho phép bạn thực hiện các câu lệnh như select, insert, update và delete trên bảng.
```

```
select(): Phương thức select() cho phép bạn chọn các cột để trả về từ bảng.
```

```
where(): Phương thức where() cho phép bạn thêm điều kiện để lọc dữ liệu từ bảng.
```

```
orderBy(): Phương thức orderBy() cho phép bạn sắp xếp dữ liệu từ bảng theo thứ tự tăng dần hoặc giảm dần của một hoặc nhiều cột.
```

```
groupBy(): Phương thức groupBy() cho phép bạn nhóm các bản ghi từ bảng theo giá trị của một hoặc nhiều cột.
```

```
join(): Phương thức join() cho phép bạn kết hợp dữ liệu từ nhiều bảng trong CSDL.
```

```
insert(): Phương thức insert() cho phép bạn thêm dữ liệu mới vào bảng.
```

```
update(): Phương thức update() cho phép bạn cập nhật dữ liệu trong bảng.
```

```
delete(): Phương thức delete() cho phép bạn xóa dữ liệu từ bảng.
```

```
count(): Phương thức count() cho phép bạn đếm số lượng bản ghi từ bảng.
```

```
sum(): Phương thức sum() cho phép bạn tính tổng giá trị của một cột trong bảng.
```

```
avg(): Phương thức avg() cho phép bạn tính trung bình giá trị của một cột trong bảng.
```

```
max(): Phương thức max() cho phép bạn tìm giá trị lớn nhất của một cột trong bảng.
```

```
min(): Phương thức min() cho phép bạn tìm giá trị nhỏ nhất của một cột trong bảng.
```

```
whereHas(): Phương thức whereHas() cho phép bạn lọc dữ liệu từ bảng dựa trên sự tồn tại của các bản ghi liên quan đến bảng khác. Nó được sử dụng để truy vấn các mối quan hệ Eloquent (ORM) của Laravel.
```

```
whereIn(): Phương thức whereIn() cho phép bạn lọc dữ liệu từ bảng dựa trên giá trị của một cột nằm trong danh sách các giá trị được chỉ định. Nó cho phép bạn truy vấn các bản ghi với các giá trị cột nằm trong một tập hợp giá trị được chỉ định.
```

```
whereBetween(): Phương thức whereBetween() cho phép bạn lọc dữ liệu từ bảng dựa trên giá trị của một cột nằm trong một khoảng giá trị được chỉ định.
```

```
whereDate(): Phương thức whereDate() cho phép bạn lọc dữ liệu từ bảng dựa trên ngày của một cột.
```

```
whereNull(): Phương thức whereNull() cho phép bạn lọc dữ liệu từ bảng dựa trên giá trị NULL của một cột.
```

```
whereNotNull(): Phương thức whereNotNull() cho phép bạn lọc dữ liệu từ bảng dựa trên giá trị khác NULL của một cột.
```

```
whereRaw(): Phương thức whereRaw() cho phép bạn truy vấn dữ liệu bằng cách sử dụng các biểu thức SQL tùy chỉnh.
```

```
orderByDesc(): Phương thức orderByDesc() cho phép bạn sắp xếp dữ liệu từ bảng theo thứ tự giảm dần của một hoặc nhiều cột.
```

```
limit(): Phương thức limit() cho phép bạn giới hạn số lượng bản ghi trả về từ bảng.
```

## Error Handling

### Syntax

```
throw new BadRequestHttpException('Custom message');
```
### Exceptions

```
ValidationException: được sử dụng khi dữ liệu đầu vào không hợp lệ hoặc không vượt qua các quy tắc kiểm tra dữ liệu. Exception này có thể được kích hoạt bằng phương thức validate() trong các Controller của ứng dụng Laravel.
```

```
BadRequestHttpException: được sử dụng khi yêu cầu của người dùng không hợp lệ hoặc không đúng định dạng. Exception này có thể được kích hoạt bằng cách gọi phương thức abort(400) trong Laravel.
```

```
UnauthorizedHttpException: được sử dụng khi người dùng không có quyền truy cập vào tài nguyên được yêu cầu. Exception này có thể được kích hoạt bằng cách gọi phương thức abort(401) trong Laravel.
```

```
NotFoundHttpException: được sử dụng khi tài nguyên được yêu cầu không tồn tại. Exception này có thể được kích hoạt bằng cách gọi phương thức abort(404) trong Laravel.
```

```
MethodNotAllowedHttpException: được sử dụng khi phương thức HTTP được sử dụng không được phép cho tài nguyên được yêu cầu. Exception này có thể được kích hoạt bằng cách gọi phương thức abort(405) trong Laravel.
```
