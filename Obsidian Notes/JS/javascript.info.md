#### Nullish Coalescing Operator ( ?? ) 
```
   The result of `a ?? b` is:
	   if `a` is defined, then `a`,
	   if `a` isn’t defined, then `b`.
```
Difference b/w '||' and '??'
	`||` returns the first _truthy_ value.
	`??` returns the first _defined_ value.

#### Objects 
- Checking for keys in Objects (**in operator**)
  "keyName" in object - returns true if it exists.
  for..in Loop : 
```
for..in Loop --> 
  let user = { name: "John", age: 30, isAdmin: true }; 
  
  for (let key in user) { 
	  // keys alert( key ); // name, age, isAdmin 
	  // values for the keys 
	  alert( user[key] ); 
	  // John, 30, true 
  }
```
	Using "isEmpty" to check if an Object is Empty.
	Syntax : ```isEmpty(Object Name);```

Copying Objects,
	1. Object.assign() -
	   For Shallow copying of Objects.
	   Eg: Object.assign(destObj , srcObj1, srcObj2 ....);
	2. structuredClone() -
	   Best to copy nested objects not by reference .
	   let oldObj = { name: "prathi" };
	   let newObj = structuredClone(oldObj);
	   Limitations:
		   Cant clone functions or methods .
		   Cant clone DOM elements 
-- 4.2 -- 

[[Mobile] Automatic sync with GitHub on iOS (for free) via a-shell - Share & showcase - Obsidian Forum](https://forum.obsidian.md/t/mobile-automatic-sync-with-github-on-ios-for-free-via-a-shell/46150/4)