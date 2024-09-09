
Subclass:
A class that is derived from another class.
Also known as child class, extended class or derived class.

static member:
Part of a class that is accessible through the class and belongs to the class.
# Access Modifiers
Allows us to determine programmatically where certain variables and methods can be accessed in our code.

## Summary Table

| Modifier               | Within Class | Within Same Package | From Subclass | From Other Packages |
| ---------------------- | ------------ | ------------------- | ------------- | ------------------- |
| Public                 | ==Allowed==  | ==Allowed==         | ==Allowed==   | ==Allowed==         |
| Protected              | ==Allowed==  | ==Allowed==         | ==Allowed==   | Denied              |
| Default (No Modifiers) | ==Allowed==  | ==Allowed==         | Denied        | Denied              |
| Private                | ==Allowed==  | Denied              | Denied        | Denied              |

# Non-Access Modifiers
## Info
List of non-access modifiers:
- static
- final
- abstract
- synchronised
- volatile
- transient
- native

## Summary Table


| Modifier     | Description                                                                                                                                                                                                                           | Used On                         |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------- |
| static   Variable: One copy is created and shared among Objects. If an Object changes this variable, it will reflect on all other Objects. Variable of this level is usually declared in Class Level.<br>Methods: Can only be used within   :  :  :  | Variable, Methods, Class, Block |
| final        | Restrict its inheritance by any other                                                                                                                                                                                                 | Methods, Class                  |
| abstract     | Methods without definition. Indicates necessary `@Override`                                                                                                                                                                           | Methods                         |
| synchronised | Prevent access of method from multiple threads. Used in m                                                                                                                                                                             | Methods                         |                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                          |                                 |

## Constructors


## References
- https://stackabuse.com/non-access-modifiers-in-java/
- https://www.educba.com/non-access-modifiers-in-java/

## OOP Concepts
### Encapsulation
- java classes allow us to bind together data and related functionality.
- Can implement parts of the encapsulation principle in Java with classes.
**Benefits:**
- Prevent classes from being too coupled
- Can easily modify the inner workings of one class without affecting the rest of the program.
**Restriction Requirements:**
- Needs clear interface between a given class and the rest of the program.
- Everything can't have direct access. Needs some restriction on what and how some things can be accessed. 

Making a class's attribute hidden from other classes allows for more control of the flow. Other classes can still access the attribute but ONLY through the class and method.

### Inheritance
## Usage
Use the keyword `extends`.
```java
// Super class / Parent class
public class Employee {
	private String name;
	private int age;
	protected double salary;

	// constructor
	public Employee(String name, int age, double salary){
		this.name = name;
		this.age = age;
		this.salary = salary;
	}
}
```

```java
// Sub class / Child class
public class Salesperson extends Employee {
	private double commision;

	// constructor
	public Salesperson(String name, int age, double salary, double bonus){
		super(name, age, salary);
		this.commision = commision;
	}

	public void raiseComission() {
		this.commision = this.commison + 5;
	}

	public void raiseSalary(){
		super.salary = super.salary + 5;
	}

}
```

The keyword `super` is used to call attributes/variables from the super class. 
The keyword `protected` is used instead of `private` to enable editing from subclasses.

Code is organised through class hierarchies.

The relation from child to parent is also known as an `is-a` relationship. 

Subclass/ child class:
	- inherits property
Super Class/ parent class:
	- Is inherited from

**Benefits:**
- Avoids/reduces code duplication -> Common properties and functionality are written in class.
- Child classes inherits from parent and adds on their unique functionality.
- Modifications on the parent class will be reflected automatically to the child classes.
- Promotes code reusability.
- Makes codes scalable.

#### Single-Level Inheritance
One super class to one subclass.

![[Pasted image 20240906162056.png]]
#### Hierarchical Inheritance
One parent many subclasses.
![[Pasted image 20240906162129.png]]
#### Multi-level Inheritance
Class inherits from one class but also can be a parent of another subclass.
![[Pasted image 20240906162214.png]]
# Random Notes
`@Override` keyword is placed to let programmers know that the method in the current class is superseding the one found in the Parent Class. 

`interfaces` are all `public` by default.