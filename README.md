🔑 Các cú pháp cơ bản trong OOP Python
1. Định nghĩa lớp
python
class Person:
    pass
Từ khóa class dùng để khai báo lớp.

pass chỉ là placeholder khi chưa viết nội dung.

2. Hàm khởi tạo (__init__)
python
class Person:
    def __init__(self, name, age):
        self.name = name   # thuộc tính
        self.age = age
__init__ là constructor.

self đại diện cho đối tượng hiện tại.

3. Tạo đối tượng (instance)
python
p1 = Person("Alice", 25)
print(p1.name)  # Alice
Gọi lớp như một hàm để tạo đối tượng.

4. Phương thức (methods)
python
class Person:
    def __init__(self, name):
        self.name = name
    
    def greet(self):
        return f"Xin chào, tôi là {self.name}"
Phương thức là hàm bên trong lớp, luôn có tham số self.

5. Thuộc tính lớp vs thuộc tính đối tượng
python
class Dog:
    species = "Canis familiaris"  # thuộc tính lớp
    
    def __init__(self, name):
        self.name = name          # thuộc tính đối tượng
Thuộc tính lớp: dùng chung cho mọi đối tượng.

Thuộc tính đối tượng: riêng cho từng instance.

6. Kế thừa (Inheritance)
python
class Animal:
    def speak(self):
        print("Animal sound")

class Dog(Animal):
    def speak(self):
        print("Woof!")
Lớp Dog kế thừa từ Animal.

Có thể ghi đè phương thức (method overriding).

7. Đa hình (Polymorphism)
python
def make_sound(animal):
    animal.speak()

make_sound(Dog())   # Woof!
make_sound(Animal()) # Animal sound
Cùng một hàm nhưng hành vi khác nhau tùy đối tượng.

8. Đóng gói (Encapsulation)
python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance   # thuộc tính private
    
    def deposit(self, amount):
        self.__balance += amount
    
    def get_balance(self):
        return self.__balance
Dùng __ để tạo thuộc tính private.

Truy cập qua phương thức thay vì trực tiếp.

9. Phương thức đặc biệt (Magic methods)
