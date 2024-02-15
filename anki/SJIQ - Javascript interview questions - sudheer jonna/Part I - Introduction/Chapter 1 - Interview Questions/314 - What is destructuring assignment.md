==================== Question ====================  

### What is destructuring assignment  

==================== Answer ====================  

The destructuring assignment is a JavaScript expression that makes it possible
to unpack values from arrays or properties from objects into distinct
variables.  
Let's get the month values from an array using destructuring assignment

```javascript
var [one, two, three] = ['JAN', 'FEB', 'MARCH'];
console.log(one); // "JAN"
console.log(two); // "FEB"
console.log(three); // "MARCH"
```

and you can get user properties of an object using destructuring assignment,

```javascript
var { name, age } = { name: 'John', age: 32 };
console.log(name); // John
console.log(age); // 32
```

==================== Id ====================  
314
<!--ID: 1707879809170-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#314-What-is-destructuring-assignment

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
