==================== Question ====================  

### What is the output of below code

```javascript
var y = 1;
if (function f() {}) {
  y += typeof f;
}
console.log(y);
```

- 1: 1function
- 2: 1object
- 3: ReferenceError
- 4: 1undefined  

==================== Answer ====================  

##### Answer: 4

The main points in the above code snippets are,

1. You can see function expression instead function declaration inside if
   statement. So it always returns true.
2. Since it is not declared(or assigned) anywhere, f is undefined and typeof f
   is undefined too.  
   In other words, it is same as

```javascript
var y = 1;
if ('foo') {
  y += typeof f;
}
console.log(y);
```

**Note:** It returns 1object for MS Edge browser

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#454-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
