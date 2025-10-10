# LẬP TRÌNH PYTHON
*Tác giả: Tạ Nguyễn Mạnh Trung*
## 📑 MỤC LỤC
- [1. GIỚI THIỆU PYTHON VÀ NHỮNG CHƯƠNG TRÌNH ĐẦU TIÊN](1-giới-thiệu-python-và-những-chương-trình-đầu-tiên)

## 1. GIỚI THIỆU PYTHON VÀ NHỮNG CHƯƠNG TRÌNH ĐẦU TIÊN
[▲ Về mục lục](#-mục-lục)

### Phần 1: GIỚI THIỆU PYTHON VÀ NHỮNG CHƯƠNG TRÌNH ĐẦU TIÊN
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

- Truy cập [python.org](https://python.org/)
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
Tạo file hello.py:

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

**Định nghĩa:** Định danh là tên dùng để nhận diện biến, hàm, lớp, đối tượng.

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

**Khái niệm:** Biến là vùng nhớ dùng để lưu trữ dữ liệu.

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

*   Number (Số): int, float, complex
    
*   String (Chuỗi): str
    
*   List (Danh sách): list
    
*   Tuple (Bộ): tuple
    
*   Dictionary (Từ điển): dict
    
*   Set (Tập hợp): set
    
*   Boolean (Logic): bool

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
print(chuoi * 3)        # PythonPythonPython
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

