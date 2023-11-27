- Regex Intro - [Learn Regular Expressions In 20 Minutes - YouTube](https://www.youtube.com/watch?v=rhzKDrUiJVk)


## Objects and Object Constructors
- Object Constructors : 
	- These are created when specific type of object is required and may be duplicated multiple times.
	  Eg 1:
		```javascript
		function Player(name, marker) {
		  this.name = name;
		  this.marker = marker;
		}
		
		const player = new Player('steve', 'X');
		console.log(player.name); // 'steve'
		```
	Eg 2:
	```javascript
	function Player(name, marker) {
	  this.name = name;
	  this.marker = marker;
	  this.sayName = function() {
	    console.log(name)
	  };
	}
	
	const player1 = new Player('steve', 'X');
	const player2 = new Player('also steve', 'O');
	player1.sayName(); // logs 'steve'
	player2.sayName(); // logs 'also steve'
	```
	- **getPrototypeOf()** -
		This is used to get the prototype of an Object.
		Object.getPrototypeOf(ObjectName);
	- **hasOwnProperty()** -
		Tells if the property is the objects own property or inherited.
		Eg:
		```javascript
		Object.prototype.hasOwnProperty('hasOwnProperty');
		```
	- setPrototypeOf - 
		Use this to mutate the Prototype of an Object.
		Eg:
		```javascript
		Object.setPrototypeOf(Player.prototype, Person.prototype);
		Player.prototype inherits Prototype from Person.prototype
		```

## Closures 
	When inner Function has access to the parent/outer function.
## Factory Function
	Work as a Constructor, but functions are written.
	No need to use "new" keyword.
	Write a function which returns an Object.
	Eg:
```javascript
	function createPerson(firstName, lastName) {
	  return {
	    firstName: firstName,
	    lastName: lastName,
	    getFullName() {
	      return firstName + ' ' + lastName;
	    },
	  };
	}
	
	let person1 = createPerson('John', 'Doe');
	let person2 = createPerson('Jane', 'Doe');
	
	console.log(person1.getFullName());
	console.log(person2.getFullName());
```

**Bad when it is used multiple to attach multiple functions to the factory function, instead use Object.create() to create a new Object**
Use Object.create() here to create a new object using an existing object as a prototype.
Eg:
```javascript
	var personActions = {
	  getFullName() {
	    return this.firstName + ' ' + this.lastName;
	  },
	};
	
	function createPerson(firstName, lastName) {
	  let person = Object.create(personActions);
	  person.firstName = firstName;
	  person.lastName = lastName;
	  return person;
	}
	
	let person1 = createPerson('John', 'Doe');
	let person2 = createPerson('Jane', 'Doe');
	
	console.log(person1.getFullName());
	console.log(person2.getFullName());
```

Prototypal Inheritance with Factory Function -
i.e extens one function into another.
	Eg1 :Extract a function and assign it to the needed function
```javascript
function createPlayer (name, level) {
  const { discordName, getReputation } = createUser(name);

  const increaseLevel = () => level++;
  return { name, discordName, getReputation, increaseLevel };
}
```
	Eg2: Use Object.assign():
```javascript
function createPlayer (name, level) {
  const user = createUser(name);

  const increaseLevel = () => level++;
  return Object.assign({}, user, { increaseLevel });
}
```
## Module Pattern 
Using an IIFE to call a factory function is called Module Pattern.
	Eg:
```javascript
const calculator = (function () {
  const add = (a, b) => a + b;
  const sub = (a, b) => a - b;
  const mul = (a, b) => a * b;
  const div = (a, b) => a / b;
  return { add, sub, mul, div };
})();

calculator.add(3,5); // 8
calculator.sub(6,2); // 4
calculator.mul(14,5534); // 77476
```

## Classes
	Eg:
```
class MyClass {
  prop = value; // property

  constructor(...) { // constructor
    // ...
  }

  method(...) {} // method

  get something(...) {} // getter method
  set something(...) {} // setter method

  [Symbol.iterator]() {} // method with computed name (symbol here)
  // ...
}
```