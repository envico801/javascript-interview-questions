==================== Question ====================  

### What is the output of below code

```javascript
const a = new Number(10);
const b = 10;
console.log(a === b);
```

- 1: False
- 2: True  

==================== Answer ====================  

Answer: 1  
Eventhough both variables `a` and `b` refer a number value, the first
declaration is based on constructor function and the type of the variable is
going to be `object` type. Whereas the second declaration is primitive
assignment with a number and the type is `number` type. Hence, the equality
operator `===` will output `false` value.

==================== Id ====================  
524

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#524-What-is-the-output-of-below-code-jav

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
