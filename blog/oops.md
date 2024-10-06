[Home](../index.md) | [Blog](../blog.md) | [Projects](../projects.md) | [About](../about.md)
--- 

# Learning Object-Oriented Programming (OOP) Using Python: A Beginner's Journey

Welcome to **Learning Hub**, where I'm documenting my journey of learning various topics with the help of AI. In this post, we'll cover two important topics: **Object-Oriented Programming (OOP)**. I'll explain them in a super simple way, perfect for beginners or anyone looking for a refresh!

## Table of Contents
- [What is Object-Oriented Programming (OOP)?](#what-is-object-oriented-programming-oop)
  - [Classes and Objects](#classes-and-objects)
  - [Attributes and Methods](#attributes-and-methods)
  - [Inheritance](#inheritance)
  - [Encapsulation](#encapsulation)
  - [Polymorphism](#polymorphism)

---

## What is Object-Oriented Programming (OOP)?

OOP is a way of organizing your code by creating "objects" that represent real-world things. These objects can store data (called **attributes**) and perform actions (called **methods**). Let's dive into the core concepts.

### Classes and Objects
- **Class**: Think of it as a blueprint for creating objects. For example, if you want to create a car, you'd start with a blueprint (a class) that describes what every car should have (like wheels and an engine).
- **Object**: This is the actual car built from the blueprint. You can create many objects (cars) from one class (blueprint).

```python
class Car:
    pass  # A blueprint for cars

my_car = Car()  # Creates a new car (object)
```

### Attributes and Methods

- **Attributes** are like the car’s color and speed.
- **Methods** are actions the car can take, like driving.

```python
class Car:
    def __init__(self, color, speed):
        self.color = color  # Attribute
        self.speed = speed  # Attribute

    def drive(self):  # Method
        print(f'The {self.color} car is driving at {self.speed} speed!')

my_car = Car('red', 100)
my_car.drive()  # Outputs: The red car is driving at 100 speed!
```

### Inheritance

Sometimes, we want to create a special kind of car, like a race car. Instead of building everything from scratch, we can inherit from the Car class and add new features.

```python
class RaceCar(Car):  # Inherit from Car
    def turbo(self):
        print(f'The {self.color} race car is using turbo!')

my_race_car = RaceCar('blue', 200)
my_race_car.turbo()  # Outputs: The blue race car is using turbo!
```

### Encapsulation

Encapsulation is like hiding the car’s engine so no one can change it directly. We provide methods to control the speed safely instead.

```python
class Car:
    def __init__(self, color, speed):
        self.color = color
        self._speed = speed  # Private attribute

    def get_speed(self):
        return self._speed

    def set_speed(self, speed):
        if speed > 0:
            self._speed = speed

my_car = Car('red', 100)
my_car.set_speed(150)
print(my_car.get_speed())  # Outputs: 150
```

### Polymorphism

This lets different objects (like cars and trucks) do the same action, but in their own way.

```python
class Truck(Car):
    def drive(self):
        print(f'The {self.color} truck is driving at {self.speed} speed!')

my_truck = Truck('green', 60)
my_car.drive()  # Outputs: The red car is driving at 100 speed!
my_truck.drive()  # Outputs: The green truck is driving at 60 speed!
```
