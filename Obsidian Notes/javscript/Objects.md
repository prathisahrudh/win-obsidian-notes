## Object Methods / Properties : 
- for..in

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
	