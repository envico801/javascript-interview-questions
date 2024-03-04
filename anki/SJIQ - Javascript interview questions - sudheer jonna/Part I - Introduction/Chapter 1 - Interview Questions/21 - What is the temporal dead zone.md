========== Question ==========  

### What is the Temporal Dead Zone  

========== Answer ==========  

The Temporal Dead Zone(TDZ) is a specific period or area of a block where a
variable is inaccessible until it has been intialized with a value. This
behavior in JavaScript that occurs when declaring a variable with the let and
const keywords, but not with var. In ECMAScript 6, accessing a `let` or `const`
variable before its declaration (within its scope) causes a ReferenceError.

Let's see this behavior with an example,

```javascript
function somemethod() {
  console.log(counter1); // undefined
  console.log(counter2); // ReferenceError
  var counter1 = 1;
  let counter2 = 2;
}
```

========== Id ==========  
21

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#21-What-is-the-temporal-dead-zone

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
