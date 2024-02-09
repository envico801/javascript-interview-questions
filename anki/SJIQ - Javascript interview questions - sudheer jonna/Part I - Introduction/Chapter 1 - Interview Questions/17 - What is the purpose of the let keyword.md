==================== Question ====================  

### What is the purpose of the let keyword  

==================== Answer ====================  

The `let` statement declares a **block scope local variable**. Hence the
variables defined with let keyword are limited in scope to the block, statement,
or expression on which it is used. Whereas variables declared with the `var`
keyword used to define a variable globally, or locally to an entire function
regardless of block scope.  
Let's take an example to demonstrate the usage,

```javascript
let counter = 30;
if (counter === 30) {
  let counter = 31;
  console.log(counter); // 31
}
console.log(counter); // 30 (because the variable in if block won't exist here)
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#17-What-is-the-purpose-of-the-let-keyword

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
