==================== Question ====================  

### What is nullish coalescing operator (??)  

==================== Answer ====================  

It is a logical operator that returns its right-hand side operand when its
left-hand side operand is null or undefined, and otherwise returns its left-hand
side operand. This can be contrasted with the logical OR (||) operator, which
returns the right-hand side operand if the left operand is any falsy value, not
only null or undefined.

```js
console.log(null ?? true); // true
console.log(false ?? true); // false
console.log(undefined ?? true); // true
```

==================== Id ====================  
425
<!--ID: 1707879819053-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#425-What-is-nullish-coalescing-operator

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
