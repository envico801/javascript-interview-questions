==================== Question ====================  

### How do you prevent an object to extend  

==================== Answer ====================  

The `Object.preventExtensions()` method is used to prevent new properties from
ever being added to an object. In other words, it prevents future extensions to
the object. Let's see the usage of this property,

```javascript
const newObject = {};
Object.preventExtensions(newObject); // NOT extendable
try {
  Object.defineProperty(newObject, 'newProperty', {
    // Adding new property
    value: 100,
  });
} catch (e) {
  console.log(e); // TypeError: Cannot define property newProperty, object is not extensible
}
```

==================== Id ====================  
262

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#262-How-do-you-prevent-an-object-to-extend

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
