## Inheritance
Inheritance means creating a new class from an existing class so that the new class can reuse its properties and methods.


### Example
Suppose we have a general Vehicle class:
```java
class Vehicle {
    void start() {
        System.out.println("Vehicle started");
    }
}
```

Now we can create a Car class that inherits from Vehicle:
```java
class Car extends Vehicle {
    void drive() {
        System.out.println("Car is driving");
    }
}
```
Now Car automatically gets the ```start()``` method from Vehicle.
We can use:
```java 
Car car = new Car();

car.start();
car.drive();
```
Output:
Vehicle started
Car is driving

Here:
```
Vehicle
   ↑
   |
  Car
```
Vehicle is the parent/superclass, while Car is the child/subclass.
The Car class can:
- Use methods from Vehicle
- Add its own methods
- Override methods from Vehicle
### Why use inheritance?
Inheritance is useful when there is a clear "is-a" relationship.
For example:
```
Car is a Vehicle
Dog is an Animal
Manager is an Employee
```
Inheritance = Reuse and extend the features of an existing class.