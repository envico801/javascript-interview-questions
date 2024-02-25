==================== Question ====================  

### How do you list all properties of an object  

==================== Answer ====================  

You can use the `Object.getOwnPropertyNames()` method which returns an array of
all properties found directly in a given object. Let's the usage of it in an
example,

```javascript
const newObject = {
  a: 1,
  b: 2,
  c: 3,
};
console.log(Object.getOwnPropertyNames(newObject));
['a', 'b', 'c'];
```

==================== Id ====================  
280

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#280-How-do-you-list-all-properties-of-an-objec

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
