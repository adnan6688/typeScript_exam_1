Question 04 : How do the four pillars of OOP—Inheritance, Polymorphism, Abstraction, and Encapsulation—help manage logic and reduce complexity in large-scale TypeScript projects?

Title: OOP’s Four Pillars: Clean and Scalable Code

Introduction:
The four main pillars of Object-Oriented Programming—Encapsulation, Abstraction, Inheritance, and Polymorphism—play a key role in organizing code, reducing complexity, and improving maintainability in large TypeScript projects.

Body:

1. Encapsulation:

class User {
  private password: string;

  constructor(password: string) {
    this.password = password;
  }

  checkPassword(input: string): boolean {
    return this.password === input;
  }
}

The password is kept private  it cannot be accessed directly from outside, only controlled through methods.

2. Abstraction:

abstract class Payment {
  abstract pay(amount: number): void;
}

class BkashPayment extends Payment {
  pay(amount: number) {
    console.log(`Paid ${amount} via bKash`);
  }
}

Users only use the pay() method  internal complex logic is hidden.

3. Inheritance:

class Animal {
  move() {
    console.log("Moving...");
  }
}

class Dog extends Animal {
  bark() {
    console.log("Barking...");
  }
}

The Dog class reuses methods from Animal → reducing code duplication.

4. Polymorphism:

class Shape {
  draw() {
    console.log("Drawing shape");
  }
}

class Circle extends Shape {
  draw() {
    console.log("Drawing circle");
  }
}

The same draw() method behaves differently  providing flexible behavior.

Conclusion:
Using these four OOP principles makes code more secure, reusable, flexible, and scalable, making large TypeScript projects much easier to manage.