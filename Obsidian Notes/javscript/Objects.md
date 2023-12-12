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
	Using Object.assign .
	Eg1
		let obj2 = { 'name': 'prathi' };
		console.log(obj2.name);
	Eg2 
		let obj1 = {"name": "janardhan"};
		