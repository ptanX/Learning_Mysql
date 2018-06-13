#Tài liệu ghi chép Mysql





## 1. Cơ sở dữ liệu là gì.


### 1.1 Cơ sở dữ liệu là gì.

 Một Database (Cơ sở dữ liệu) là một ứng dụng riêng rẽ mà lưu trữ một tập hợp dữ liệu. Mỗi cơ sở dữ liệu có một hoặc nhiều
API riêng biệt để tạo, truy cập, quản lý, tìm kiếm và tái tạo dữ liệu nó đang giữ.

Ngày nay, chúng ta sử dụng các Hệ thống quản lý cơ sở dữ liệu quan hệ (RDBMS) lưu giữ và quản lý khối lượng lớn dữ liệu. Nó được gọi là cơ sở dữ liệu quan hệ, bởi vì tất cả dữ liệu được lưu giữ trong các bảng dữ liệu khác nhau và các mối quan hệ được thành lập bởi sử dụng các Primary Key (khóa chính) và một số khóa khác được biết đến như là Foreign Key.

Một **Hệ thống quản lý cơ sở dữ liệu quan hệ (RDBMS)** là một phần mềm mà:


- Cho bạn khả năng triển khai một Database với các bảng dữ liệu, cột (column), và các chỉ mục (Index).
- Bảo đảm Referential Integrity (có thể dịch là toàn vẹn quan hệ) giữa các hàng và các bảng đa dạng.
- Cập nhật tự động các chỉ mục..
- Thông dịch một truy vấn SQL và tổ hợp thông tin từ các bảng khác nhau..

### 1.2 Thuật ngữ RDBMS.

- **Database:** Một cơ sở dữ liệu là một tập hợp các bảng dữ liệu, với dữ liệu có liên quan.
- **Bảng dữ liệu:** Một bảng là một ma trận dữ liệu. Một bảng trong một cơ sở dữ liệu trông giống như một bảng tính đơn giản.
- **Cột:** Một cột chứa cùng một kiểu dữ liệu, ví dụ như tên khách hàng.
- **Hàng:** Một hàng (row, entry, record) là một nhóm dữ liệu có liên quan.
- **Redundancy:** (có thể hiểu là dữ liệu dự phòng) Dữ liệu được lưu giữ hai lần, để làm cho hệ thống nhanh hơn.
- **Primary Key:** Một Primary Key (Khóa chính) là duy nhất. Một giá trị key không thể xuất hiện hai lần trong một bảng. Với một key, bạn có thể tìm thấy phần lớn trên một hàng.
- **Foreign Key:** Bạn tưởng tượng về Foreign Key như là cái ghim liên kết giữa hai bảng.
- **Compound Key:** Một Compound Key (hay composite key) là một key mà gồm nhiều cột, bởi vì một cột là không duy nhất.
- **Index:** Một chỉ mục trong một cơ sở dữ liệu tương tự như chỉ mục trong một cuốn sách.
- **Referential Integrity:** Đảm bảo rằng một giá trị Foreign Key luôn luôn trỏ tới một hàng đang tồn tại.

##2. Thao tác với cơ sở dữ liệu trong mysql

- Để tạo một cơ sở dữ liệu ta sử dụng câu lệnh sau:

`CREATE DATABASE Ten_co_so_du_lieu;`

**Ví dụ:**

`CREATE database learning_mysql;`

- Để xóa một cơ sở dữ liệu ta thực hiện lệnh **DROP DATABASE**:

- Cú pháp của lệnh xóa database:

`DROP DATABASE ten_co_so_du_lieu;`

**Ví dụ:**

`DROP database learning_mysql;`

- Để chọn một cơ sở dữ liệu ta dùng lệnh sau:

`USE ten_co_so_du_lieu;`

**Ví dụ:**

`USE learning_mysql;`

##3. Thao tác với bảng trong cơ sở dữ liệu mysql.

###3.1 Tạo bảng trong mysql
- Lệnh tạo bảng trong mysql bao gồm:

- Tên bảng.
- Tên các trường.
- Định nghĩa cho mỗi trường.

**Cú pháp:**

- Dưới đây là cú pháp khai báo một bảng: 
`CREATE TABLE ten_bang (ten_cot kieu_du_lieu_cucot);`

**Ví dụ:** tạo bảng với thông tin nhân viên trong trung tâm: 

```
CREATE TABLE Nhanvien(
msnv INT NOT NULL AUTO_INCREMENT,
ho VARCHAR(255) NOT NULL,
ten VARCHAR(255) NOT NULL,
tuoi INT NOT NULL,
chucvu VARCHAR(255) NOT NULL,
PRIMARY KEY (msnv)
);
```
