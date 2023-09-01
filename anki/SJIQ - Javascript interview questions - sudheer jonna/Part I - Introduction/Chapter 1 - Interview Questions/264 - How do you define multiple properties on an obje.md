Q: How do you define multiple properties on an object  
A: The `Object.defineProperties()` method is used to define new or modify existing properties directly on an object and returning the object. Let's define multiple properties on an empty object,
```javascript
const newObject = {};
Object.defineProperties(newObject, {
  newProperty1: {
    value: "John",
    writable: true,
  },
  newProperty2: {},
});
```
<!--ID: 1693596699049-->

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