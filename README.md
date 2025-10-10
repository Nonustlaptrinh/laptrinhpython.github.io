GIÁO ÁN PYTHON CHI TIẾT##

**PHẦN 1: GIỚI THIỆU PYTHON VÀ CHƯƠNG TRÌNH ĐẦU TIÊN**

**1.1. Python là gì?**

Python là ngôn ngữ lập trình bậc cao, được tạo ra bởi Guido van Rossum và ra mắt lần đầu năm 1991.

**Đặc điểm nổi bật:**

- Cú pháp đơn giản, dễ học
- Mã nguồn mở, hoàn toàn miễn phí
- Đa nền tảng (Windows, macOS, Linux)
- Hỗ trợ nhiều mô hình lập trình

**Ứng dụng của Python:**

- Phát triển web (Django, Flask)
- Phân tích dữ liệu (Pandas, NumPy)
- Trí tuệ nhân tạo (TensorFlow, PyTorch)
- Tự động hóa các tác vụ
- Khoa học máy tính

**1.2. Cài đặt môi trường Python**

**Bước 1: Tải Python**

- Truy cập [python.org](https://python.org/)
- Tải phiên bản mới nhất (Python 3.x)
- Chọn đúng phiên bản cho hệ điều hành

**Bước 2: Cài đặt**

- Chạy file cài đặt
- Tick vào ô "Add Python to PATH"
- Chọn "Install Now"

**Bước 3: Kiểm tra cài đặt**\
Mở Command Prompt/Terminal và gõ:

bash

python --version

**1.3. Chương trình Hello World**

**Cách 1: Chế độ tương tác (Interactive Mode)**

```python

>>> print("Hello World!")
Hello World!
```
**Cách 2: Chạy từ file**\
Tạo file hello.py:

```python

# Đây là chương trình đầu tiên
message = "Hello World!"
print(message)
```
Chạy chương trình:

```bash

python hello.py
```
**Kết quả:**

```text
Hello World!
```
**1.4. Các công cụ lập trình Python**

**IDLE (Python's Integrated Development Environment)**

- Có sẵn khi cài đặt Python
- Giao diện đơn giản, dễ sử dụng
- Hỗ trợ highlight syntax

**Visual Studio Code (VS Code)**

- Editor mạnh mẽ, nhiều extension
- Debugging tích hợp
- Hỗ trợ nhiều ngôn ngữ

**PyCharm**

- IDE chuyên cho Python
- Nhiều tính năng nâng cao
- Phiên bản Community miễn phí
-----
**PHẦN 2: ĐỊNH DANH VÀ TỪ KHÓA**

**2.1. Định danh (Identifier) trong Python**

**Định nghĩa:** Định danh là tên dùng để nhận diện biến, hàm, lớp, đối tượng.

**Quy tắc đặt tên định danh:**

```python

# ĐÚNG - Bắt đầu bằng chữ cái*

ten_bien = "giá trị"
_bien_rieng = "private"
bien123 = 100
```
```python
# SAI - Không hợp lệ

2ten = "value"       # Bắt đầu bằng số
ten-bien = "value"   # Chứa ký tự đặc biệt
class = "Python"     # Trùng từ khóa
```
**Quy ước đặt tên:**

```python

# Biến thông thường (snake_case)

ten_bien_dai = "snake_case"
```
```python
# Hằng số (UPPER_CASE)

HANG_SO_PI = 3.14
MAX_SIZE = 100
```
```python
# Biến private

_bien_rieng_tu = "internal"
__bien_rat_rieng = "very private"
```
```python
# Tên đặc biệt (dunder methods)

__init__ = "constructor"
__name__ = "module name"
```
**2.2. Từ khóa trong Python**

**Danh sách đầy đủ các từ khóa:**

```python

# Các từ khóa cơ bản

False      class      finally    is         return
None       continue   for        lambda     try
True       def        from       nonlocal   while
and        del        global     not        with
as         elif       if         or         yield
assert     else       import     pass
break      except     in         raise
```
**Kiểm tra từ khóa:**

```python

import keyword
print("Tổng số từ khóa:", len(keyword.kwlist))
print("Danh sách từ khóa:")
for i, kw in enumerate(keyword.kwlist, 1):
    print(f"{i:2d}. {kw}")
```
**Kết quả:**

```text
Tổng số từ khóa: 35
Danh sách từ khóa:
 1. False
 2. None
 3. True
 4. and
 5. as
 6. assert
 7. async
 8. await
 9. break
10. class
11. continue
12. def
13. del
14. elif
15. else
16. except
17. finally
18. for
19. from
20. global
21. if
22. import
23. in
24. is
25. lambda
26. nonlocal
27. not
28. or
29. pass
30. raise
31. return
32. try
33. while
34. with
35. yield
```
-----
**PHẦN 3: CÚ PHÁP CƠ BẢN**

**3.1. Dòng lệnh và thụt lề**

**Quy tắc thụt lề:**

```python

# ĐÚNG - Thụt lề 4 spaces

def hello():
    print("Hello")      # 4 spaces
    return "World"      # 4 spaces
```
```python
# SAI - Không thụt lề

def hello():
print("Hello")          # Lỗi: expected an indented block
```
```python
# SAI - Thụt lề không nhất quán

def hello():
    print("Hello")      # 4 spaces
  return "World"        # 2 spaces - Lỗi
```
**Ví dụ về cấu trúc khối code:**

```python
# Khối code với thụt lề hợp lệ

def tinh_toan(a, b):
  ket_qua = a + b     # Thụt lề 4 spaces
  return ket_qua      # Thụt lề 4 spaces

# Gọi hàm

tinh_toan(5, 3)
```
**3.2. Các lệnh trên nhiều dòng**

**Sử dụng dấu \ cho các biểu thức dài:**

```python
# Phép tính dài trên nhiều dòng

tong = (so_thu_nhat + 
        so_thu_hai + 
        so_thu_ba + 
        so_thu_tu)
```
```python
# Hoặc sử dụng dấu \

tong = so_thu_nhat + \
        so_thu_hai + \
        so_thu_ba + \
        so_thu_tu
```
**Không cần \ với các cấu trúc container:**

```python
# List trên nhiều dòng*

danh_sach = [
    "item1",
    "item2", 
    "item3",
    "item4"
]
```
```python
# Dictionary trên nhiều dòng

sinh_vien = {
    "ten": "Nguyễn Văn A",
    "tuoi": 20,
    "diem": 8.5,
    "lop": "CNTT"
}
```
```python
# Tuple trên nhiều dòng

coordinates = (
    10.123456,
    106.654321,
    15.000000
)
```
**3.3. Comment trong Python**

**Comment một dòng:**

```python
# Đây là comment một dòng
gia_tri = 100  # Comment sau code
# Comment giải thích code phức tạp
# Tính tổng các số từ 1 đến n
# Sử dụng công thức n\*(n+1)/2
tong = n * (n + 1) // 2
```
**Comment nhiều dòng:**
```python
"""
ĐÂY LÀ COMMENT NHIỀU DÒNG
Chương trình: Quản lý sinh viên
Tác giả: Nguyễn Văn A
Ngày tạo: 2024-01-01
Phiên bản: 1.0
"""
```
```python
# Hoặc sử dụng nhiều comment một dòng
# ===============================
# CHƯƠNG TRÌNH QUẢN LÝ SINH VIÊN
# Tác giả: Nguyễn Văn A
# Ngày tạo: 2024-01-01
# ===============================
```
**Docstring - Comment đặc biệt cho hàm:**

```python
# Hàm tính bình phương với Docstring

def tinh_binh_phuong(x):
    """
    Tính bình phương của một số
    Args:
        x (int/float): Số cần tính bình phương
    Returns:
        int/float: Bình phương của x
    Ví dụ:
        >>> tinh_binh_phuong(5)
        25
        >>> tinh_binh_phuong(2.5)
        6.25
    """
    return x ** 2

# Xem docstring
print(tinh_binh_phuong.__doc__)
```
-----
**PHẦN 4: BIẾN VÀ KIỂU DỮ LIỆU**

**4.1. Biến trong Python**

**Khái niệm:** Biến là vùng nhớ dùng để lưu trữ dữ liệu.

**Khai báo biến:**

```python
# Khai báo biến đơn

ten = "Nguyễn Văn A"
tuoi = 20
diem_trung_binh = 8.5
la_sinh_vien = True
print("Tên:", ten)
print("Tuổi:", tuoi)
print("Điểm TB:", diem_trung_binh)
print("Là sinh viên:", la_sinh_vien)
```
**Kiểu động (Dynamic Typing):**

```python
# Biến có thể thay đổi kiểu dữ liệu

bien_linh_hoat = 10           # int
print(type(bien_linh_hoat))   # <class 'int'>
bien_linh_hoat = "Hello"      # str 
print(type(bien_linh_hoat))   # <class 'str'>
bien_linh_hoat = 3.14         # float
print(type(bien_linh_hoat))   # <class 'float'>
```
**4.2. Phép gán**

**Gán đơn:**

```python
a = 10
b = 20.5
c = "Python"
d = True
```
**Đa gán (Multiple Assignment):**

```python
# Gán một giá trị cho nhiều biến

x = y = z = 100
print(f"x={x}, y={y}, z={z}")  # x=100, y=100, z=100
```
```python
# Gán nhiều giá trị cho nhiều biến

a, b, c = 5, 10, 15
print(f"a={a}, b={b}, c={c}")  # a=5, b=10, c=15
```
```python
# Hoán đổi giá trị

x, y = 10, 20
x, y = y, x  # Hoán đổi
print(f"x={x}, y={y}")  # x=20, y=10
```
**4.3. Các kiểu dữ liệu cơ bản**

**Các kiểu dữ liệu cơ bản trong Python bao gồm:**

*   Number (Số): int, float, complex
    
*   String (Chuỗi): str
    
*   List (Danh sách): list
    
*   Tuple (Bộ): tuple
    
*   Dictionary (Từ điển): dict
    
*   Set (Tập hợp): set
    
*   Boolean (Logic): bool

**Kiểm tra kiểu dữ liệu:**

```python
# Các biến với kiểu dữ liệu khác nhau

so_nguyen = 42
so_thuc = 3.14159
chuoi = "Hello Python"
danh_sach = [1, 2, 3]
bo_gia_tri = (1, 2, 3)
tu_dien = {"tên": "Alice", "tuổi": 25}
tap_hop = {1, 2, 3}
la_dung = True
print(f"so_nguyen: {so_nguyen} - {type(so_nguyen)}")
print(f"so_thuc: {so_thuc} - {type(so_thuc)}")
print(f"chuoi: {chuoi} - {type(chuoi)}")
print(f"danh_sach: {danh_sach} - {type(danh_sach)}")
print(f"bo_gia_tri: {bo_gia_tri} - {type(bo_gia_tri)}")
print(f"tu_dien: {tu_dien} - {type(tu_dien)}")
print(f"tap_hop: {tap_hop} - {type(tap_hop)}")
print(f"la_dung: {la_dung} - {type(la_dung)}")
```
**Kết quả:**

```text
so_nguyen: 42 - <class 'int'>
so_thuc: 3.14159 - <class 'float'>
chuoi: Hello Python - <class 'str'>
danh_sach: [1, 2, 3] - <class 'list'>
bo_gia_tri: (1, 2, 3) - <class 'tuple'>
tu_dien: {'tên': 'Alice', 'tuổi': 25} - <class 'dict'>
tap_hop: {1, 2, 3} - <class 'set'>
la_dung: True - <class 'bool'>
```
-----
**PHẦN 5: TOÁN TỬ TRONG PYTHON**

**5.1. Toán tử số học (Arithmetic Operators)**

```python
a = 10
b = 3
print("=== TOÁN TỬ SỐ HỌC ===")
print(f"{a} + {b} = {a + b}")      # 13 - Cộng
print(f"{a} - {b} = {a - b}")      # 7  - Trừ
print(f"{a} * {b} = {a * b}")      # 30 - Nhân
print(f"{a} / {b} = {a / b}")      # 3.333... - Chia thường
print(f"{a} // {b} = {a // b}")    # 3 - Chia nguyên
print(f"{a} % {b} = {a % b}")      # 1 - Chia lấy dư
print(f"{a} ** {b} = {a ** b}")    # 1000 - Lũy thừa
```
**Toán tử trên chuỗi:**

```python
chuoi = "Python"
print(chuoi \* 3)        # PythonPythonPython
print("Hello " + chuoi)  # Hello Python
```
**5.2. Toán tử so sánh (Comparison Operators)**

```python
x = 10
y = 5
print("=== TOÁN TỬ SO SÁNH ===")
print(f"{x} == {y}: {x == y}")    # False - Bằng
print(f"{x} != {y}: {x != y}")    # True  - Khác
print(f"{x} > {y}: {x > y}")      # True  - Lớn hơn
print(f"{x} < {y}: {x < y}")      # False - Nhỏ hơn  
print(f"{x} >= {y}: {x >= y}")    # True  - Lớn hơn hoặc bằng
print(f"{x} <= {y}: {x <= y}")    # False - Nhỏ hơn hoặc bằng
```
**So sánh chuỗi:**

```python
print("apple" == "apple")    # True
print("apple" == "banana")   # False
print("a" < "b")             # True (so sánh theo thứ tự alphabet)
```
**5.3. Toán tử gán (Assignment Operators)**

```python
a = 10
print(f"Khởi tạo: a = {a}")
a += 5   # a = a + 5
print(f"Sau a += 5: a = {a}")
a -= 3   # a = a - 3  
print(f"Sau a -= 3: a = {a}")
a *= 2   # a = a * 2
print(f"Sau a *= 2: a = {a}")
a /= 4   # a = a / 4
print(f"Sau a /= 4: a = {a}")
a //= 2  # a = a // 2
print(f"Sau a //= 2: a = {a}")
a %= 3   # a = a % 3
print(f"Sau a %= 3: a = {a}")
a **= 3  # a = a ** 3
print(f"Sau a **= 3: a = {a}")
```
**5.4. Toán tử logic (Logical Operators)**

```python
x = True
y = False
print("=== TOÁN TỬ LOGIC ===")
print(f"{x} and {y}: {x and y}")   # False - VÀ (cả hai đều True)
print(f"{x} or {y}: {x or y}")     # True  - HOẶC (một trong hai True)  
print(f"not {x}: {not x}")         # False - PHỦ ĐỊNH
print(f"not {y}: {not y}")         # True  - PHỦ ĐỊNH
```
**Ứng dụng thực tế:**

```python
diem_toan = 8
diem_van = 6
# Kiểm tra điều kiện
dat_chuan = (diem_toan >= 5) and (diem_van >= 5)
hoc_sinh_gioi = (diem_toan >= 8) or (diem_van >= 8)
print(f"Đạt chuẩn: {dat_chuan}")            # True
print(f"Học sinh giỏi: {hoc_sinh_gioi}")    # True
```
**5.5. Toán tử membership (in, not in)**

```python
chuoi = "Hello Python"
danh_sach = [1, 2, 3, 4, 5]
print("=== TOÁN TỬ MEMBERSHIP ===")
print(f"'H' in '{chuoi}': {'H' in chuoi}")                 # True
print(f"'Z' in '{chuoi}': {'Z' in chuoi}")                 # False
print(f"3 in {danh_sach}: {3 in danh_sach}")               # True
print(f"10 in {danh_sach}: {10 in danh_sach}")             # False
print(f"10 not in {danh_sach}: {10 not in danh_sach}")     # True
```
**5.6. Toán tử identity (is, is not)**

```python
a = [1, 2, 3]
b = [1, 2, 3] 
c = a
print("=== TOÁN TỬ IDENTITY ===")
print(f"a is b: {a is b}")            # False - Khác đối tượng
print(f"a is c: {a is c}")            # True  - Cùng đối tượng
print(f"a == b: {a == b}")            # True  - Giá trị giống nhau
print(f"a is not b: {a is not b}")    # True
```
-----
**PHẦN 6: KIỂU DỮ LIỆU NUMBER**

**6.1. Các kiểu số trong Python**

**Số nguyên (int):**

python

so\_duong = 42

so\_am = -15

so\_0 = 0

so\_lon = 1\_000\_000  *# Dùng \_ để dễ đọc*

print(f"Kiểu của {so\_duong}: {type(so\_duong)}")

print(f"Kiểu của {so\_am}: {type(so\_am)}")

**Số thực (float):**

python

so\_thuc = 3.14159

so\_am\_thuc = -2.718

so\_khoa\_hoc = 1.5e3  *# 1500.0*

print(f"Kiểu của {so\_thuc}: {type(so\_thuc)}")

print(f"1.5e3 = {so\_khoa\_hoc}")

**Số phức (complex):**

python

so\_phuc = 3 + 4j

so\_phuc\_khac = complex(2, -5)  *# 2 - 5j*

print(f"Số phức: {so\_phuc}")

print(f"Phần thực: {so\_phuc.real}")

print(f"Phần ảo: {so\_phuc.imag}")

**6.2. Các phép toán trên số**

**Toán tử cơ bản:**

python

a = 15

b = 4

print(f"{a} + {b} = {a + b}")

print(f"{a} - {b} = {a - b}") 

print(f"{a} \* {b} = {a \* b}")

print(f"{a} / {b} = {a / b}")

print(f"{a} // {b} = {a // b}")

print(f"{a} % {b} = {a % b}")

**Làm việc với số thực:**

python

x = 10.5

y = 3.2

print(f"{x} + {y} = {x + y}")

print(f"{x} - {y} = {x - y}")

print(f"{x} \* {y} = {x \* y}")

print(f"{x} / {y} = {x / y}")

print(f"{x} // {y} = {x // y}")  *# Chia nguyên với số thực*

**6.3. Hàm toán học cơ bản**

**Sử dụng module math:**

python

import math

print("=== HÀM TOÁN HỌC ===")

print(f"math.sqrt(16) = {math.sqrt(16)}")        *# 4.0 - Căn bậc 2*

print(f"math.pow(2, 3) = {math.pow(2, 3)}")     *# 8.0 - Lũy thừa*

print(f"math.fabs(-5.5) = {math.fabs(-5.5)}")   *# 5.5 - Giá trị tuyệt đối*

print(f"math.ceil(3.2) = {math.ceil(3.2)}")     *# 4 - Làm tròn lên*

print(f"math.floor(3.8) = {math.floor(3.8)}")   *# 3 - Làm tròn xuống*

print(f"math.pi = {math.pi}")                   *# 3.14159... - Hằng số PI*

print(f"math.e = {math.e}")                     *# 2.71828... - Hằng số E*

**Hàm tích hợp sẵn:**

python

numbers = [1, 5, 3, 8, 2]

print(f"max{numbers} = {max(numbers)}")    *# 8 - Giá trị lớn nhất*

print(f"min{numbers} = {min(numbers)}")    *# 1 - Giá trị nhỏ nhất*

print(f"sum{numbers} = {sum(numbers)}")    *# 19 - Tổng*

print(f"abs(-10) = {abs(-10)}")           *# 10 - Giá trị tuyệt đối*

print(f"round(3.14159, 2) = {round(3.14159, 2)}")  *# 3.14 - Làm tròn*

-----
**PHẦN 7: KIỂU DỮ LIỆU STRING**

**7.1. Khai báo và truy cập chuỗi**

**Các cách khai báo chuỗi:**

python

*# Chuỗi đơn*

chuoi\_don = 'Hello World'

*# Chuỗi kép*  

chuoi\_kep = "Python Programming"

*# Chuỗi tam (triple quotes)*

chuoi\_tam = """Đây là chuỗi

nhiều dòng

trong Python"""

*# Chuỗi raw (không xử lý ký tự đặc biệt)*

duong\_dan = r"C:\Users\Name\Documents"

print(chuoi\_don)

print(chuoi\_kep)

print(chuoi\_tam)

print(duong\_dan)

**Truy cập ký tự trong chuỗi:**

python

s = "Python Programming"

print("Chuỗi gốc:", s)

print("Độ dài:", len(s))

print("Ký tự đầu:", s[0])           *# P*

print("Ký tự cuối:", s[-1])         *# g*

print("Ký tự thứ 7:", s[6])         *# P (trong Programming)*

**Cắt chuỗi (slicing):**

python

s = "Python Programming"

print("s[0:6] =", s[0:6])        *# Python*

print("s[7:] =", s[7:])          *# Programming*  

print("s[:6] =", s[:6])          *# Python*

print("s[-11:] =", s[-11:])      *# Programming*

print("s[::2] =", s[::2])        *# Pto rgamn (cách 2 ký tự)*

print("s[::-1] =", s[::-1])      *# gnimmargorP nohtyP (đảo ngược)*

**7.2. Các phương thức xử lý chuỗi cơ bản**

**Chuyển đổi chữ hoa/thường:**

python

s = "Hello Python"

print(s.upper())        *# HELLO PYTHON*

print(s.lower())        *# hello python*  

print(s.title())        *# Hello Python*

print(s.capitalize())   *# Hello python*

print(s.swapcase())     *# hELLO pYTHON*

**Xử lý khoảng trắng:**

python

s = "   Hello World   "

print(f"'{s}'")                    *# '   Hello World   '*

print(f"'{s.strip()}'")            *# 'Hello World' - Xóa cả 2 bên*

print(f"'{s.lstrip()}'")           *# 'Hello World   ' - Xóa trái*

print(f"'{s.rstrip()}'")           *# '   Hello World' - Xóa phải*

**Tìm kiếm và thay thế:**

python

s = "I love Python programming"

print(s.find("Python"))        *# 7 - Vị trí đầu tiên*

print(s.rfind("o"))            *# 20 - Vị trí cuối cùng*

print(s.count("o"))            *# 3 - Số lần xuất hiện*

print(s.replace("Python", "Java"))  *# I love Java programming*

**Kiểm tra chuỗi:**

python

s1 = "Hello123"

s2 = "HELLO"

s3 = "12345"

s4 = "hello"

s5 = "Hello World"

print(f"'{s1}'.isalnum(): {s1.isalnum()}")  *# True - Chữ và số*

print(f"'{s2}'.isalpha(): {s2.isalpha()}")  *# True - Chỉ chữ cái*

print(f"'{s3}'.isdigit(): {s3.isdigit()}")  *# True - Chỉ số*

print(f"'{s4}'.islower(): {s4.islower()}")  *# True - Chữ thường*

print(f"'{s2}'.isupper(): {s2.isupper()}")  *# True - Chữ hoa*

print(f"'{s5}'.istitle(): {s5.istitle()}")  *# True - Dạng title*

**7.3. Định dạng chuỗi**

**f-string (Python 3.6+):**

python

ten = "Minh"

tuoi = 22

diem = 8.5

*# Định dạng cơ bản*

gioi\_thieu = f"Tôi là {ten}, {tuoi} tuổi, điểm TB: {diem}"

print(gioi\_thieu)

*# Định dạng số*

print(f"Pi: {math.pi:.2f}")          *# 3.14*

print(f"Số lớn: {1000000:,}")        *# 1,000,000*

print(f"Phần trăm: {0.256:.1%}")     *# 25.6%*

*# Biểu thức trong f-string*

a, b = 5, 3

print(f"{a} + {b} = {a + b}")        *# 5 + 3 = 8*

**Phương thức format():**

python

*# Định vị trí*

print("{} + {} = {}".format(5, 3, 8))

print("{0} x {1} = {2}".format(4, 5, 20))

print("{a} - {b} = {c}".format(a=10, b=4, c=6))

*# Định dạng*

print("{:.2f}".format(3.14159))      *# 3.14*

print("{:10}".format("test"))        *# 'test      '*

print("{:<10}".format("test"))       *# 'test      ' (căn trái)*

print("{:>10}".format("test"))       *# '      test' (căn phải)*

print("{:^10}".format("test"))       *# '   test   ' (căn giữa)*

**7.4. Các phương thức chuỗi quan trọng khác**

**Nối và tách chuỗi:**

python

*# Nối chuỗi*

chuoi\_list = ["Python", "Java", "C++"]

ket\_qua = ", ".join(chuoi\_list)

print(ket\_qua)  *# Python, Java, C++*

*# Tách chuỗi*

s = "apple,banana,orange"

trai\_cay = s.split(",")

print(trai\_cay)  *# ['apple', 'banana', 'orange']*

*# Tách dòng*

multi\_line = "Dòng 1\nDòng 2\nDòng 3"

dong = multi\_line.splitlines()

print(dong)  *# ['Dòng 1', 'Dòng 2', 'Dòng 3']*

**Padding và căn chỉnh:**

python

s = "Python"

print(s.center(20, "-"))   *# -------Python-------*

print(s.ljust(15, "\*"))    *# Python\*\*\*\*\*\*\*\*\**

print(s.rjust(15, "\*"))    *# \*\*\*\*\*\*\*\*\*Python*

print(s.zfill(10))         *# 0000Python*

-----
**PHẦN 8: KIỂU DỮ LIỆU LIST**

**8.1. Khai báo và truy cập List**

**Tạo list:**

python

*# List rỗng*

list\_rong = []

*# List số*

so\_nguyen = [1, 2, 3, 4, 5]

so\_thuc = [1.5, 2.7, 3.14]

*# List chuỗi*

chuoi\_list = ["apple", "banana", "orange"]

*# List hỗn hợp*

hon\_hop = [1, "hello", 3.14, True, [1, 2, 3]]

print("List số:", so\_nguyen)

print("List chuỗi:", chuoi\_list)

print("List hỗn hợp:", hon\_hop)

**Truy cập phần tử:**

python

numbers = [10, 20, 30, 40, 50]

print("List:", numbers)

print("Độ dài:", len(numbers))

print("Phần tử đầu:", numbers[0])        *# 10*

print("Phần tử cuối:", numbers[-1])      *# 50*

print("Phần tử thứ 3:", numbers[2])      *# 30*

*# Cắt list (slicing)*

print("numbers[1:4]:", numbers[1:4])     *# [20, 30, 40]*

print("numbers[:3]:", numbers[:3])       *# [10, 20, 30]*

print("numbers[2:]:", numbers[2:])       *# [30, 40, 50]*

print("numbers[::2]:", numbers[::2])     *# [10, 30, 50] (cách 2)*

**8.2. Các phương thức cơ bản của List**

**Thêm phần tử:**

python

ds = [1, 2, 3]

ds.append(4)           *# [1, 2, 3, 4] - Thêm cuối*

ds.insert(1, 10)       *# [1, 10, 2, 3, 4] - Chèn tại vị trí*

ds.extend([5, 6, 7])   *# [1, 10, 2, 3, 4, 5, 6, 7] - Mở rộng*

print("Sau khi thêm:", ds)

**Xóa phần tử:**

python

ds = [1, 2, 3, 2, 4, 5, 2]

ds.remove(2)           *# [1, 3, 2, 4, 5, 2] - Xóa phần tử đầu tiên*

popped = ds.pop()      *# [1, 3, 2, 4, 5] - Xóa và trả về phần tử cuối*

popped2 = ds.pop(1)    *# [1, 2, 4, 5] - Xóa tại vị trí*

del ds[0]             *# [2, 4, 5] - Xóa theo chỉ mục*

ds.clear()            *# [] - Xóa toàn bộ*

print("Popped:", popped)

print("Popped2:", popped2)

print("List cuối:", ds)

**Tìm kiếm và sắp xếp:**

python

ds = [3, 1, 4, 1, 5, 9, 2]

print("Vị trí đầu tiên của 1:", ds.index(1))  *# 1*

print("Số lần xuất hiện của 1:", ds.count(1)) *# 2*

ds.sort()                    *# [1, 1, 2, 3, 4, 5, 9] - Tăng dần*

print("Sắp xếp tăng:", ds)

ds.sort(reverse=True)        *# [9, 5, 4, 3, 2, 1, 1] - Giảm dần*  

print("Sắp xếp giảm:", ds)

ds.reverse()                 *# [1, 1, 2, 3, 4, 5, 9] - Đảo ngược*

print("Đảo ngược:", ds)

**8.3. Các thao tác nâng cao với List**

**List comprehension:**

python

*# Tạo list bình phương*

binh\_phuong = [x\*\*2 for x in range(1, 6)]

print("Bình phương:", binh\_phuong)  *# [1, 4, 9, 16, 25]*

*# Tạo list số chẵn*

so\_chan = [x for x in range(10) if x % 2 == 0]

print("Số chẵn:", so\_chan)  *# [0, 2, 4, 6, 8]*

*# Chuyển đổi kiểu*

chuoi\_so = ["1", "2", "3", "4", "5"]

so = [int(x) for x in chuoi\_so]

print("Số nguyên:", so)  *# [1, 2, 3, 4, 5]*

**Copy list:**

python

*# Copy nông (shallow copy)*

ds\_goc = [1, 2, 3]

ds\_copy = ds\_goc.copy()      *# Hoặc ds\_copy = ds\_goc[:]*

ds\_goc[0] = 100

print("Gốc:", ds\_goc)        *# [100, 2, 3]*

print("Copy:", ds\_copy)      *# [1, 2, 3]*

*# Copy sâu (deep copy) cho list lồng nhau*

import copy

ds\_phuc\_tap = [[1, 2], [3, 4]]

ds\_copy\_sau = copy.deepcopy(ds\_phuc\_tap)

ds\_phuc\_tap[0][0] = 100

print("Gốc phức tạp:", ds\_phuc\_tap)      *# [[100, 2], [3, 4]]*

print("Copy sâu:", ds\_copy\_sau)          *# [[1, 2], [3, 4]]*

-----
**PHẦN 9: KIỂU DỮ LIỆU TUPLE**

**9.1. Khái niệm và khai báo Tuple**

**Tuple là gì?**

- Tương tự list nhưng không thể thay đổi (immutable)
- Thường dùng cho dữ liệu không thay đổi
- Hiệu suất tốt hơn list

**Khai báo tuple:**

python

*# Tuple rỗng*

tup\_rong = ()

*# Tuple một phần tử (cần dấu phẩy)*

tup\_don = (5,)  *# (5) sẽ là số 5, không phải tuple*

*# Tuple nhiều phần tử*

tup\_so = (1, 2, 3, 4, 5)

tup\_chuoi = ("apple", "banana", "orange")

*# Không cần dấu ngoặc (tuple packing)*

tup\_khong\_ngoac = 1, 2, 3

print("Tuple số:", tup\_so)

print("Tuple chuỗi:", tup\_chuoi)

print("Tuple không ngoặc:", tup\_khong\_ngoac)

**Truy cập tuple:**

python

tup = (10, 20, 30, 40, 50)

print("Tuple:", tup)

print("Độ dài:", len(tup))

print("Phần tử đầu:", tup[0])        *# 10*

print("Phần tử cuối:", tup[-1])      *# 50*

*# Cắt tuple*

print("tup[1:4]:", tup[1:4])         *# (20, 30, 40)*

print("tup[::2]:", tup[::2])         *# (10, 30, 50)*

**9.2. Các thao tác với Tuple**

**Tuple không thể thay đổi:**

python

tup = (1, 2, 3)

*# Các thao tác này sẽ gây lỗi:*

*# tup[0] = 10          # TypeError*

*# tup.append(4)        # AttributeError*

*# tup.remove(2)        # AttributeError*

print("Tuple không thể thay đổi sau khi tạo")

**Các phương thức có sẵn:**

python

tup = (1, 2, 3, 2, 4, 2)

print("Số lần xuất hiện của 2:", tup.count(2))    *# 3*

print("Vị trí đầu tiên của 3:", tup.index(3))     *# 2*

**Unpacking tuple:**

python

*# Gán nhiều biến cùng lúc*

x, y, z = (10, 20, 30)

print(f"x={x}, y={y}, z={z}")  *# x=10, y=20, z=30*

*# Dùng \* để gán nhiều giá trị*

first, \*middle, last = (1, 2, 3, 4, 5)

print(f"first={first}, middle={middle}, last={last}")  *# first=1, middle=[2, 3, 4], last=5*

-----
**PHẦN 10: KIỂU DỮ LIỆU DICTIONARY**

**10.1. Khai báo và truy cập Dictionary**

**Dictionary là gì?**

- Lưu trữ dữ liệu dạng key-value
- Key phải là immutable (string, number, tuple)
- Value có thể là bất kỳ kiểu dữ liệu nào

**Khai báo dictionary:**

python

*# Dictionary rỗng*

dict\_rong = {}

*# Dictionary với dữ liệu*

sinh\_vien = {

`    `"ma\_sv": "SV001",

`    `"ho\_ten": "Nguyễn Văn A", 

`    `"tuoi": 20,

`    `"diem": 8.5,

`    `"lop": "CNTT"

}

*# Sử dụng dict()*

mon\_hoc = dict(toan=9, van=8, anh=7.5)

print("Thông tin sinh viên:", sinh\_vien)

print("Điểm môn học:", mon\_hoc)

**Truy cập dictionary:**

python

print("Mã SV:", sinh\_vien["ma\_sv"])           *# SV001*

print("Họ tên:", sinh\_vien.get("ho\_ten"))     *# Nguyễn Văn A*

print("Tuổi:", sinh\_vien.get("tuoi"))         *# 20*

*# get() an toàn hơn [] khi key không tồn tại*

print("Địa chỉ:", sinh\_vien.get("dia\_chi", "Không có"))  *# Không có*

**10.2. Các thao tác với Dictionary**

**Thêm/Sửa phần tử:**

python

sinh\_vien = {"ten": "Minh", "tuoi": 22}

*# Thêm mới*

sinh\_vien["diem"] = 8.5

sinh\_vien["lop"] = "CNTT"

*# Sửa giá trị*

sinh\_vien["tuoi"] = 23

print("Sau khi thêm/sửa:", sinh\_vien)

**Xóa phần tử:**

python

sinh\_vien = {"ten": "Minh", "tuoi": 22, "diem": 8.5, "lop": "CNTT"}

*# pop() - xóa và trả về giá trị*

tuoi = sinh\_vien.pop("tuoi")

print(f"Đã xóa tuổi: {tuoi}")

*# popitem() - xóa phần tử cuối*

cuoi = sinh\_vien.popitem()  

print(f"Đã xóa phần tử cuối: {cuoi}")

*# del - xóa theo key*

del sinh\_vien["ten"]

*# clear() - xóa toàn bộ*

sinh\_vien.clear()

print("Dictionary cuối:", sinh\_vien)

**Các phương thức hữu ích:**

python

sinh\_vien = {"ten": "Minh", "tuoi": 22, "diem": 8.5}

print("Tất cả keys:", sinh\_vien.keys())      *# dict\_keys(['ten', 'tuoi', 'diem'])*

print("Tất cả values:", sinh\_vien.values())  *# dict\_values(['Minh', 22, 8.5])*

print("Tất cả items:", sinh\_vien.items())    *# dict\_items([('ten', 'Minh'), ('tuoi', 22), ('diem', 8.5)])*

*# Duyệt dictionary*

print("\nDuyệt bằng items():")

for key, value in sinh\_vien.items():

`    `print(f"{key}: {value}")

print("\nDuyệt bằng keys():")

for key in sinh\_vien.keys():

`    `print(f"{key}: {sinh\_vien[key]}")

**10.3. Dictionary comprehension**

**Tạo dictionary từ các nguồn khác:**

python

*# Từ list keys*

keys = ['a', 'b', 'c']

values = [1, 2, 3]

dict\_tu\_list = {k: v for k, v in zip(keys, values)}

print("Từ list:", dict\_tu\_list)  *# {'a': 1, 'b': 2, 'c': 3}*

*# Tạo dictionary với điều kiện*

so\_binh\_phuong = {x: x\*\*2 for x in range(1, 6)}

print("Bình phương:", so\_binh\_phuong)  *# {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}*

*# Lọc dictionary*

sinh\_vien = {"Minh": 8.5, "An": 7.0, "Binh": 9.0, "Chi": 6.5}

sinh\_vien\_gioi = {name: score for name, score in sinh\_vien.items() if score >= 8.0}

print("Sinh viên giỏi:", sinh\_vien\_gioi)  *# {'Minh': 8.5, 'Binh': 9.0}*

-----
**PHẦN 11: CHUYỂN ĐỔI KIỂU DỮ LIỆU**

**11.1. Chuyển đổi giữa các kiểu cơ bản**

**Chuyển đổi số:**

python

*# String → Number*

chuoi\_so = "123"

so\_nguyen = int(chuoi\_so)

so\_thuc = float("3.14")

*# Number → String*  

so = 456

chuoi = str(so)

*# Number các loại*

so\_nguyen = 10

so\_thuc = float(so\_nguyen)

so\_phuc = complex(so\_nguyen)

print(f"int('123') = {so\_nguyen} - {type(so\_nguyen)}")

print(f"float('3.14') = {so\_thuc} - {type(so\_thuc)}")

print(f"str(456) = '{chuoi}' - {type(chuoi)}")

print(f"complex(10) = {so\_phuc} - {type(so\_phuc)}")

**Chuyển đổi boolean:**

python

*# Các giá trị được coi là False*

print(f"bool(0) = {bool(0)}")           *# False*

print(f"bool('') = {bool('')}")         *# False*  

print(f"bool([]) = {bool([])}")         *# False*

print(f"bool({{}}) = {bool({})}")       *# False*

print(f"bool(None) = {bool(None)}")     *# False*

*# Các giá trị được coi là True*

print(f"bool(1) = {bool(1)}")           *# True*

print(f"bool('hello') = {bool('hello')}") *# True*

print(f"bool([1,2]) = {bool([1,2])}")   *# True*

**11.2. Chuyển đổi giữa các cấu trúc dữ liệu**

**List ↔ Tuple:**

python

*# List → Tuple*

danh\_sach = [1, 2, 3, 4, 5]

tup = tuple(danh\_sach)

print(f"tuple({danh\_sach}) = {tup} - {type(tup)}")

*# Tuple → List*  

tup = (10, 20, 30)

danh\_sach = list(tup)

print(f"list({tup}) = {danh\_sach} - {type(danh\_sach)}")

**List/Tuple ↔ Set:**

python

*# List → Set (loại bỏ trùng lặp)*

danh\_sach = [1, 2, 2, 3, 3, 3, 4]

tap\_hop = set(danh\_sach)

print(f"set({danh\_sach}) = {tap\_hop} - {type(tap\_hop)}")

*# Set → List*

tap\_hop = {1, 2, 3}

danh\_sach = list(tap\_hop)

print(f"list({tap\_hop}) = {danh\_sach} - {type(danh\_sach)}")

**Dictionary conversions:**

python

*# List of tuples → Dictionary*

danh\_sach\_tup = [('a', 1), ('b', 2), ('c', 3)]

dict\_tu\_list = dict(danh\_sach\_tup)

print(f"dict({danh\_sach\_tup}) = {dict\_tu\_list}")

*# Dictionary → List of keys/values*

dict\_goc = {'x': 10, 'y': 20, 'z': 30}

keys = list(dict\_goc.keys())

values = list(dict\_goc.values())

items = list(dict\_goc.items())

print(f"Keys: {keys}")

print(f"Values: {values}") 

print(f"Items: {items}")

**11.3. Các hàm chuyển đổi quan trọng khác**

**Hàm eval() và repr():**

python

*# eval() - thực thi chuỗi như biểu thức Python*

bieu\_thuc = "2 + 3 \* 4"

ket\_qua = eval(bieu\_thuc)

print(f"eval('{bieu\_thuc}') = {ket\_qua}")

*# repr() - biểu diễn chuỗi của đối tượng*

chuoi = "Hello"

dai\_dien = repr(chuoi)

print(f"repr('{chuoi}') = {dai\_dien}")

**Chuyển đổi hệ cơ số:**

python

so = 255

print(f"bin({so}) = {bin(so)}")      *# 0b11111111 - Nhị phân*

print(f"oct({so}) = {oct(so)}")      *# 0o377 - Bát phân*

print(f"hex({so}) = {hex(so)}")      *# 0xff - Thập lục phân*

*# Ngược lại*

print(f"int('0b11111111', 2) = {int('0b11111111', 2)}")  *# 255*

print(f"int('0o377', 8) = {int('0o377', 8)}")            *# 255*

print(f"int('0xff', 16) = {int('0xff', 16)}")            *# 255*

**PHẦN 12: KIỂU DỮ LIỆU SET**

**12.1. Khái niệm và khai báo Set**

**Set là gì?**

- Là tập hợp các phần tử không có thứ tự
- Không cho phép phần tử trùng lặp
- Có thể chứa các kiểu dữ liệu khác nhau nhưng phải là immutable (số, chuỗi, tuple)
- Set là mutable (có thể thêm, xóa phần tử) nhưng các phần tử trong set phải là immutable

**Khai báo set:**

python

*# Set rỗng*

set\_rong = set()  *# Chú ý: không dùng {} vì đó là dictionary*

*# Set với các phần tử*

set\_so = {1, 2, 3, 4, 5}

set\_chuoi = {"apple", "banana", "orange"}

set\_hop = {1, "hello", 3.14, (1, 2, 3)}  *# Có thể chứa tuple vì tuple immutable*

*# Tạo set từ list (loại bỏ trùng lặp)*

danh\_sach = [1, 2, 2, 3, 3, 3, 4, 5]

set\_tu\_list = set(danh\_sach)

print(set\_tu\_list)  *# {1, 2, 3, 4, 5}*

print("Set số:", set\_so)

print("Set chuỗi:", set\_chuoi)

print("Set từ list:", set\_tu\_list)

**12.2. Các thao tác cơ bản với Set**

**Thêm phần tử:**

python

s = {1, 2, 3}

s.add(4)           *# {1, 2, 3, 4} - Thêm một phần tử*

s.update([5, 6, 7]) *# {1, 2, 3, 4, 5, 6, 7} - Thêm nhiều phần tử*

print("Sau khi thêm:", s)

**Xóa phần tử:**

python

s = {1, 2, 3, 4, 5, 6, 7}

s.remove(3)        *# {1, 2, 4, 5, 6, 7} - Xóa phần tử, nếu không có sẽ lỗi*

s.discard(10)      *# {1, 2, 4, 5, 6, 7} - Xóa phần tử, nếu không có không lỗi*

xoa\_phan\_tu = s.pop()  *# Xóa và trả về một phần tử ngẫu nhiên*

s.clear()          *# set() - Xóa toàn bộ*

print("Phần tử bị xóa bởi pop:", xoa\_phan\_tu)

print("Set cuối:", s)

**Truy cập và duyệt set:**

python

s = {1, 2, 3, 4, 5}

*# Set không hỗ trợ indexing, vì không có thứ tự*

*# Muốn truy cập cần chuyển sang list*

print("Độ dài:", len(s))

print("Có 3 trong set?", 3 in s)

*# Duyệt set*

for phan\_tu in s:

`    `print(phan\_tu)

**12.3. Các phép toán trên Set**

**Hợp (union):**

python

A = {1, 2, 3}

B = {3, 4, 5}

hop = A | B        *# {1, 2, 3, 4, 5}*

hop2 = A.union(B)  *# {1, 2, 3, 4, 5}*

print("A | B =", hop)

print("A.union(B) =", hop2)

**Giao (intersection):**

python

A = {1, 2, 3, 4}

B = {3, 4, 5, 6}

giao = A & B           *# {3, 4}*

giao2 = A.intersection(B)  *# {3, 4}*

print("A & B =", giao)

print("A.intersection(B) =", giao2)

**Hiệu (difference):**

python

A = {1, 2, 3, 4}

B = {3, 4, 5, 6}

hieu\_AB = A - B            *# {1, 2} - Có trong A nhưng không có trong B*

hieu\_AB2 = A.difference(B) *# {1, 2}*

hieu\_BA = B - A            *# {5, 6} - Có trong B nhưng không có trong A*

print("A - B =", hieu\_AB)

print("B - A =", hieu\_BA)

**Hiệu đối xứng (symmetric difference):**

python

A = {1, 2, 3, 4}

B = {3, 4, 5, 6}

hieu\_dx = A ^ B                     *# {1, 2, 5, 6} - Các phần tử chỉ có trong A hoặc chỉ có trong B*

hieu\_dx2 = A.symmetric\_difference(B) *# {1, 2, 5, 6}*

print("A ^ B =", hieu\_dx)

**12.4. Các phương thức khác của Set**

**So sánh set:**

python

A = {1, 2, 3}

B = {1, 2, 3, 4, 5}

C = {1, 2, 3}

print("A là subset của B?", A.issubset(B))    *# True*

print("B là superset của A?", B.issuperset(A)) *# True*

print("A bằng C?", A == C)                    *# True*

print("A và B có phần tử chung?", A.isdisjoint(B)) *# False (có phần tử chung)*

**Set comprehension:**

python

*# Tạo set bình phương*

binh\_phuong = {x\*\*2 for x in range(1, 6)}

print("Bình phương:", binh\_phuong)  *# {1, 4, 9, 16, 25}*

*# Tạo set số chẵn*

so\_chan = {x for x in range(10) if x % 2 == 0}

print("Số chẵn:", so\_chan)  *# {0, 2, 4, 6, 8}*

**12.5. Ứng dụng của Set**

**Loại bỏ trùng lặp từ list:**

python

danh\_sach\_trung = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]

danh\_sach\_khong\_trung = list(set(danh\_sach\_trung))

print("List gốc:", danh\_sach\_trung)

print("List không trùng:", danh\_sach\_khong\_trung)  *# [1, 2, 3, 4]*

**Tìm phần tử chung/riêng giữa các list:**

python

list1 = [1, 2, 3, 4, 5]

list2 = [4, 5, 6, 7, 8]

set1 = set(list1)

set2 = set(list2)

phan\_tu\_chung = set1 & set2

phan\_tu\_rieng = set1 ^ set2

print("Phần tử chung:", phan\_tu\_chung)  *# {4, 5}*

print("Phần tử riêng:", phan\_tu\_rieng)  *# {1, 2, 3, 6, 7, 8}*

**Bài tập thực hành với Set**

**Bài 1: Quản lý danh sách thành viên**

python

*# Hai nhóm thành viên*

nhom\_a = {"An", "Bình", "Chi", "Dũng"}

nhom\_b = {"Chi", "Dũng", "Giang", "Hương"}

*# Thành viên cả hai nhóm*

print("Thành viên cả hai nhóm:", nhom\_a & nhom\_b)

*# Tất cả thành viên*

print("Tất cả thành viên:", nhom\_a | nhom\_b)

*# Thành viên chỉ thuộc một nhóm*

print("Thành viên chỉ thuộc một nhóm:", nhom\_a ^ nhom\_b)

*# Thêm thành viên mới*

nhom\_a.add("Long")

print("Nhóm A sau khi thêm:", nhom\_a)

**Bài 2: Phân tích từ trong câu**

python

cau = "Python là ngôn ngữ lập trình Python rất mạnh mẽ"

*# Tách từ và chuyển thành set để loại bỏ trùng lặp*

tu = set(cau.split())

print("Các từ duy nhất trong câu:", tu)

print("Số lượng từ duy nhất:", len(tu))

**CẬP NHẬT PHẦN TỔNG KẾT**

**4 KIỂU DỮ LIỆU COLLECTION TRONG PYTHON:**

|Kiểu dữ liệu|Đặc điểm|Có thứ tự|Có thể thay đổi|Cho phép trùng lặp|Cú pháp|
| :- | :- | :- | :- | :- | :- |
|**List**|Danh sách có thứ tự|✅|✅|✅|[]|
|**Tuple**|Danh sách không thay đổi|✅|❌|✅|()|
|**Set**|Tập hợp không trùng lặp|❌|✅|❌|set() hoặc {}|
|**Dictionary**|Cặp key-value|❌|✅|Key: ❌, Value: ✅|{}|

**So sánh chi tiết:**

python

*# List - có thứ tự, thay đổi được, cho phép trùng lặp*

danh\_sach = [1, 2, 2, 3, 4]

*# Tuple - có thứ tự, không thay đổi được, cho phép trùng lặp*  

tup = (1, 2, 2, 3, 4)

*# Set - không thứ tự, thay đổi được, không cho phép trùng lặp*

tap\_hop = {1, 2, 3, 4}  *# Tự động loại bỏ trùng lặp*

*# Dictionary - không thứ tự, thay đổi được, key không trùng lặp*

tu\_dien = {"a": 1, "b": 2, "c": 3}

print("List:", danh\_sach)

print("Tuple:", tup)

print("Set:", tap\_hop)

print("Dictionary:", tu\_dien)

**Kết quả:**

text

List: [1, 2, 2, 3, 4]

Tuple: (1, 2, 2, 3, 4)

Set: {1, 2, 3, 4}

Dictionary: {'a': 1, 'b': 2, 'c': 3}

