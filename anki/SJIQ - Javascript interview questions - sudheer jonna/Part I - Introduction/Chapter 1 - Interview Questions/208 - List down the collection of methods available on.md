Q: List down the collection of methods available on WeakMap  
A: Below are the list of methods available on WeakMap,
1. set(key, value): Sets the value for the key in the WeakMap object. Returns the WeakMap object.
2. delete(key): Removes any value associated to the key.
3. has(key): Returns a Boolean asserting whether a value has been associated to the key in the WeakMap object or not.
4. get(key): Returns the value associated to the key, or undefined if there is none.
   Let's see the functionality of all the above methods in an example,
```javascript
var weakMapObject = new WeakMap();
var firstObject = {};
var secondObject = {};
// set(key, value)
weakMapObject.set(firstObject, "John");
weakMapObject.set(secondObject, 100);
console.log(weakMapObject.has(firstObject)); //true
console.log(weakMapObject.get(firstObject)); // John
weakMapObject.delete(secondObject);
```
<!--ID: 1693596704350-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript #Interview

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store