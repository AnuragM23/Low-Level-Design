## Polymorphism
Polymorphism means one interface or method can behave differently depending on the object using it.


### Example
Suppose we have an Animal class:
```java
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}
```
Now we have different animals:
```java
class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Cat meows");
    }
}
```
Now we can write:
```java
Animal animal;

animal = new Dog();
animal.sound();
```
Output:
```
Dog barks
```
And:
```
animal = new Cat();
animal.sound();
```
Output:
```
Cat meows
```
The method we call is the same:
```
animal.sound();
```
But the behavior changes depending on the actual object.
```
Animal
   ↑
   ├── Dog → sound() → "Dog barks"
   |
   └── Cat → sound() → "Cat meows"
```
This is runtime polymorphism, achieved through method overriding.
### Real-World Example
Think about a payment system:
```java
Payment payment;

payment = new UPI();
payment.pay();

payment = new CreditCard();
payment.pay();
```
The operation is the same:
```
pay()
```
But the implementation is different for UPI and Credit Card.

**Polymorphism = Same interface, different behavior.**