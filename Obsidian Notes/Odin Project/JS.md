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
	Write a function which returns an Object.
	Eg:
```

```