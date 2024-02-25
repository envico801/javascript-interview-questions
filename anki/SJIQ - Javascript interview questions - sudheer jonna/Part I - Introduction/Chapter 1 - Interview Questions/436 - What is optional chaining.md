==================== Question ====================  

### What is optional chaining  

==================== Answer ====================  

According to MDN official docs, the optional chaining operator (?.) permits
reading the value of a property located deep within a chain of connected objects
without having to expressly validate that each reference in the chain is
valid.  
The ?. operator is like the . chaining operator, except that instead of causing
an error if a reference is nullish (null or undefined), the expression
short-circuits with a return value of undefined. When used with function calls,
it returns undefined if the given function does not exist.

```js
const adventurer = {
  name: 'Alice',
  cat: {
    name: 'Dinah',
  },
};
const dogName = adventurer.dog?.name;
console.log(dogName);
// expected output: undefined
console.log(adventurer.someNonExistentMethod?.());
// expected output: undefined
```

==================== Id ====================  
436

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#436-What-is-optional-chaining

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
