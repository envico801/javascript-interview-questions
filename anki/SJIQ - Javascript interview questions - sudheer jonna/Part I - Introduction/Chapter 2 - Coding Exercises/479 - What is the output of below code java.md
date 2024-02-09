==================== Question ====================  

### What is the output of below code

```javascript
const sym1 = new Symbol('one');
console.log(sym1);
```

- 1: SyntaxError
- 2: one
- 3: Symbol('one')
- 4: Symbol  

==================== Answer ====================  

##### Answer: 1

`Symbol` is a just a standard function and not an object constructor(unlike
other primitives new Boolean, new String and new Number). So if you try to call
it with the new operator will result in a TypeError

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#479-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
