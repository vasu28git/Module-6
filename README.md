# 1.  🐍 Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## 💻 Program
```
from abc import ABC
class type_shape(ABC): 
    def area(self):
        pass

class Rectangle(type_shape):
    length = 6
    breadth = 4
    def area(self):
        return self.length * self.breadth

class Circle(type_shape):
    radius = 7
    def area(self):
        return 3.14*self.radius**2
class Square(type_shape):
    length = 4
    def area(self):
        return self.length**2

class triangle(type_shape):
    length = 5
    width = 4
    def area(self):
        return 0.5*self.length*self.width
  
r = Rectangle()
c = Circle() 
s = Square() 
t = triangle() 
print("Area of a rectangle:", r.area())
print("Area of a circle:", c.area()) 
print("Area of a square:", s.area()) 
print("Area of a triangle:", t.area())
```
## Output
![6 1](https://github.com/user-attachments/assets/9aa5c86d-ce39-484f-970c-f75e5af8a64b)
## Result
Thus the program to create an abstract class named Shape with an abstract method calculate_area, and implement this method in two subclasses: Rectangle and Circle is executed successfully.

# 2. 🐍 Python OOP: Encapsulation with Private Members

## 🎯 AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.

---

## 🧠 ALGORITHM

1. **Define the Class**:
   - Create a class `Rectangle` with two private attributes: `__length` and `__breadth`.

2. **Initialize Variables**:
   - Use the `__init__()` constructor to set initial values for `__length` and `__breadth`.

3. **Print Values**:
   - Display the private variables from within the class to demonstrate access.

4. **Instantiate the Object**:
   - Create an object of the `Rectangle` class to trigger the constructor.

---

## 💻 Program
```
  class Rectangle:
    __length = 0 
    __breadth = 0
    def __init__(self):
      self.__length = 5
      self.__breadth = 3
      print(self.__length)
      print(self.__breadth)
   
  obj = Rectangle()
```
## Output
![441831638-9bf23cd9-aaf2-4358-838e-539edd162088](https://github.com/user-attachments/assets/ea7daca5-648d-47d3-af23-0e0ce41ebbbe)

## Result
Thus the program has been verified successfully

# 3.  🐟 Method Overriding-Fish and Shark Class Inheritance in Python

## 🧠 AIM:
To write a Python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.

## 📋 ALGORITHM:

1. Define the `Fish` class with a method named `type()` that prints `"fish"`.
2. Define the `Shark` class as a subclass of `Fish`, and override the `type()` method to print `"shark"`.
3. Create an instance of the `Fish` class named `obj_goldfish`.
4. Create an instance of the `Shark` class named `obj_hammerhead`.
5. Use a `for` loop to iterate over both objects.
6. Within the loop, call the `type()` method using the loop variable.
7. Output will demonstrate method overriding: printing `"fish"` and `"shark"` accordingly.

## 💻 PROGRAM:
```
class Fish:
    def type(self):
        print("fish")

class Shark(Fish):
	def type(self):
	    print("shark")

obj_goldfish=Fish()
obj_hammerhead=Shark()

obj_goldfish.type()
obj_hammerhead.type()
```
## OUTPUT
![Screenshot 2025-05-26 092408](https://github.com/user-attachments/assets/a7e935c3-319a-42b1-a6e2-5d32bc8da01c)

## RESULT
Thus the program has been verified successfully

# 4.  🐍 Python OOP: Operator Overloading (Less Than `<`)

## 🎯 AIM

To write a Python program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class.

---

## 🧠 ALGORITHM

1. **Create Class `A`**:
   - Define the `__init__()` method to initialize the object with a value `a`.

2. **Overload the `<` Operator**:
   - Define the `__lt__()` method with logic:
     - If `self.a < o.a`, return `"ob1 is less than ob2"`
     - Else, return `"ob2 is less than ob1"`

3. **Create Objects**:
   - Instantiate two objects `ob1` and `ob2` with values.

4. **Use `<` Operator**:
   - Use `print(ob1 < ob2)` to trigger the overloaded behavior.

---

## 💻 Program
```
class A:
    def __init__(self,a):
        self.a=a
    def __lt__(self,other):
        return self.a<other.a
ob1 = A(2)

ob2 = A(3)
if ob2<ob1:
    print("ob2 is less than ob1")
else:
    print("ob1 is less than ob2")
```
## Output
![441831638-9bf23cd9-aaf2-4358-838e-539edd162088](https://github.com/user-attachments/assets/89fc85f2-0c24-4714-a9cf-9a3321aaaf34)

## Result
Thus the program has been verified successfully

# # 5.  🐍 Python OOP: Polymorphism with Classes

## 🎯 AIM

To create two specific classes — `Beans` and `Mango`. Then, create a **generic function** that can accept any object and determine its **type** (Fruit or Vegetable) and **color**, using polymorphism.

---

## 🧠 ALGORITHM

1. **Create Class `Beans`**:
   - Define `type()` method that prints `"Vegetable"`.
   - Define `color()` method that prints `"Green"`.

2. **Create Class `Mango`**:
   - Define `type()` method that prints `"Fruit"`.
   - Define `color()` method that prints `"Yellow"`.

3. **Define Generic Function `func(obj)`**:
   - Call `obj.type()` and `obj.color()` — this works with both `Beans` and `Mango` objects, showcasing **polymorphism**.

4. **Create Objects**:
   - Instantiate `Beans` and `Mango`.
   - Pass them to `func()` and execute the program.

---

## 💻 Program
```
  class Beans ():
     def type(self):
        print("Vegetable")
     def color(self):
        print("Green")

  class Mango ():
     def type(self):
        print("Fruit")
     def color(self):
        print("Yellow")

     def func(obj):
        obj.type()
        obj.color()

  obj_beans = Beans()
  obj_mango = Mango()
  func(obj_beans)
  func(obj_mango)
```
## Output
![441832871-456ee9ef-9f30-4670-abc4-7b8f042c077a](https://github.com/user-attachments/assets/8415e42e-64a9-4ecb-8608-db02f4e49217)

## Result
Thus the program has been verified successfully
