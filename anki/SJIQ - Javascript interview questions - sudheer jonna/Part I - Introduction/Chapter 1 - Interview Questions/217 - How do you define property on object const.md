==================== Question ====================  

### How do you define property on Object constructor  

==================== Answer ====================  

The Object.defineProperty() static method is used to define a new property
directly on an object, or modify an existing property on an object, and returns
the object. Let's see an example to know how to define property,

```javascript
const newObject = {};
Object.defineProperty(newObject, 'newProperty', {
  value: 100,
  writable: false,
});
console.log(newObject.newProperty); // 100
newObject.newProperty = 200; // It throws an error in strict mode due to writable setting
```

==================== Id ====================  
217
<!--ID: 1707879831840-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#217-How-do-you-define-property-on-object-const

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
