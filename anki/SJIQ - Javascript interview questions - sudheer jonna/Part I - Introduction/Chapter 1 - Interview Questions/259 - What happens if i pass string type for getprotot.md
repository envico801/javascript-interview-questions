Q: What happens If I pass string type for getPrototype method  
A: In ES5, it will throw a TypeError exception if the obj parameter isn't an object. Whereas in ES2015, the parameter will be coerced to an `Object`.
```javascript
// ES5
Object.getPrototypeOf("James"); // TypeError: "James" is not an object
// ES2015
Object.getPrototypeOf("James"); // String.prototype
```
<!--ID: 1693596699532-->

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