==================== Question ====================  

### What is the output of below code

```javascript
const sym1 = Symbol('one');
const sym2 = Symbol('one');
const sym3 = Symbol.for('two');
const sym4 = Symbol.for('two');
console.log(sym1 === sym2, sym3 === sym4);
```

- 1: true, true
- 2: true, false
- 3: false, true
- 4: false, false  

==================== Answer ====================  

Answer: 3  
Symbol follows below conventions,

1. Every symbol value returned from Symbol() is unique irrespective of the
   optional string.
2. `Symbol.for()` function creates a symbol in a global symbol registry list.
   But it doesn't necessarily create a new symbol on every call, it checks first
   if a symbol with the given key is already present in the registry and returns
   the symbol if it is found. Otherwise a new symbol created in the registry.  
   **Note:** The symbol description is just useful for debugging purposes.

==================== Id ====================  
478

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#478-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
