## Java and Swift Classes

#### Defining

Java: Classes can be defined as a template that can describe an objects behavior. Instantiating an Object is accomplished with the 'new' keyword. Dog dog = new Dog(breed, age, color);l

public class Dog {
   String breed;
   int age;
   String color;
}

Swift: Swift classes are the general purpose building blocks of your code. Similar to Java, they are used to add functionality to your code. Compared to Java's new keyword for instantiating objects, swift uses init().

class Dog { /
	var breed: String /
	var age: Int /
	var color: String /
}

#### Creating new instances.

Java: Instantiating an Object is accomplished with the 'new' keyword and the classname, followed with the paramaters that the class holds. 

Dog dog = new Dog(breed, age, color);

Swift: As stated above, new instances in Swift are created with the init() keyword

//initalizing dog for the class written above
init() {
	breed = lab
	age = 7
	color = golden
}

#### Destructing/de-initializing

Java: Java, in order to destruct an object, you simple set the object equal to null

Dog dog = new Dog(breed, age, color);
dog = null

Swift: In Swift, in order to deconstruct a class, you call the definit() keyword, versus the init() keyword for initialization

definit() { //deinitializing the Dog class
	Dog.breed
	Dog.age
	Dog.color
}
