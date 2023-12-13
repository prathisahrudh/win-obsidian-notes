## Object Methods / Properties : 
- for..in
## Constructor , Constructor Functions and operator "new"
1. Constructor Function:
	Naming scheme must be capitalized.
	Must be executed only with the keyword "new".
	Constructors usually don't have a return statement. Constructors **"return statement"** as objects are ok, otherwise if return is in primitives it is ignored.

## Pointers:
- Computed Properties 
```
let fruit = prompt("Which fruit to buy?", "apple");

let bag = {
  [fruit]: 5, // the name of the property is taken from the variable fruit
};

alert( bag.apple ); 
```
[ fruit ] -- here is a computed property
- Cloning 
1. Using **Object.assign** 
	Good only for single level copying.
	Eg1 :
		let obj2 = { 'name': 'prathi' };
		Object.assign({} , obj2);
	Eg2 :
		let emptyObject = {}
		let obj1 = {"name": "janardhan"};
		Object.assign(emptyObject , obj1, obj2);

2. structuredClone
	This is not effective while copying functions
	Good for many level copying.
	Eg1 :
```
	let user = {
	  name: "John",
	  sizes: {
	    height: 182,
	    width: 50
	  }
	};
	
	let clone = structuredClone(user);
	
	alert( user.sizes === clone.sizes ); // false, different objects
	
	// user and clone are totally unrelated now
	user.sizes.width = 60;    // change a property from one place
	alert(clone.sizes.width); 
```

3. Method shorthand other ways:
```
// these objects do the same
user = {
  sayHi: function() {
    alert("Hello");
  }
};

// method shorthand looks better, right?
user = {
  sayHi() { // same as "sayHi: function(){...}"
    alert("Hello");
  }
};
```



.header_button{
	width: fit-content;
	background: #098558;
	color: white;
	border-radius:60px;
}

.header_button a{
	text-decoration: none;
	color: white;
	padding:8px 31px;
}