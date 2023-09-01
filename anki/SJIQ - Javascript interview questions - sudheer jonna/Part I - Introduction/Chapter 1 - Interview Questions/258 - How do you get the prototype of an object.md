Q: How do you get the prototype of an object  
A: You can use the `Object.getPrototypeOf(obj)` method to return the prototype of the specified object. i.e. The value of the internal `prototype` property. If there are no inherited properties then `null` value is returned.
```javascript
const newPrototype = {};
const newObject = Object.create(newPrototype);
console.log(Object.getPrototypeOf(newObject) === newPrototype); // true
```
<!--ID: 1693596699622-->

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