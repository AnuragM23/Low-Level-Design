

## Encapsulation
Encapsulation means wrapping data and the methods that work on that data into a single unit, usually a class.

### example
Think about a bank account.
You don't directly change your bank balance.

You use operations like:

```
Deposit money
Withdraw money
Check balance
```

You cannot simply say:
```java
balance = -50000
```

**Suppose we create an Account class:**
```java
class Account {

    private double balance;

    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
        }
    }

    public void withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
        }
    }

    public double getBalance() {
        return balance;
    }
}
```

Here:
```java
private double balance;
```
means that balance cannot be directly accessed from outside the class.

Instead, we use methods:
```java
account.deposit(500);
account.withdraw(200);
account.getBalance();
```
The class controls how its data is accessed and modified.

How Do We Achieve Encapsulation in Java?

## Encapsulation is mainly achieved using:

### 1. private

Keep variables hidden from outside classes.
```java
private int age;
```
### 2. Getters and Setters

Provide controlled access to the data.
```java
public int getAge() {
    return age;
}

public void setAge(int age) {
    if (age > 0) {
        this.age = age;
    }
}
```
### 3. Methods

Instead of allowing direct modification, expose meaningful operations.
```java
account.deposit(500);
account.withdraw(200);
```

## Key takeaways
```
        Object
          ↓
   ┌──────────────┐
   │ Private Data │
   └──────┬───────┘
          ↓
     Public Methods
          ↓
    Controlled Access
```

**Encapsulation = Protect the data and control how it is accessed.**