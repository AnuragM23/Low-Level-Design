
## Abstraction
Abstraction means hiding unnecessary details and showing only what is important.

### example
Suppose we have a payment system.

The user only needs to know:

makePayment()

They don't need to know how UPI processes the payment internally.

We can create an interface:

```java
interface Payment {
    void makePayment(double amount);
}
```

Then different payment methods can implement it:

```java
class UPI implements Payment {

    public void makePayment(double amount) {
        System.out.println("Payment through UPI");
    }
}

class CreditCard implements Payment {

    public void makePayment(double amount) {
        System.out.println("Payment through Credit Card");
    }
}
```

Now the user can simply do:

```
Payment payment = new UPI();

payment.makePayment(500);
```

The user knows what operation is available:
```
makePayment()
```
but doesn't need to know the internal implementation.