==================== Question ====================  

### What is the output of below code

```javascript
console.log(
  JSON.stringify({ myArray: ['one', undefined, function () {}, Symbol('')] }),
);
console.log(
  JSON.stringify({ [Symbol.for('one')]: 'one' }, [Symbol.for('one')]),
);
```

- 1: {"myArray":['one', undefined, {}, Symbol]}, {}
- 2: {"myArray":['one', null,null,null]}, {}
- 3: {"myArray":['one', null,null,null]}, "{ [Symbol.for('one')]: 'one' },
  [Symbol.for('one')]"
- 4: {"myArray":['one', undefined, function(){}, Symbol('')]}, {}  

==================== Answer ====================  

Answer: 2  
The symbols has below constraints,

1. The undefined, Functions, and Symbols are not valid JSON values. So those
   values are either omitted (in an object) or changed to null (in an array).
   Hence, it returns null values for the value array.
2. All Symbol-keyed properties will be completely ignored. Hence it returns an
   empty object({}).

==================== Id ====================  
481
<!--ID: 1707879798325-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#481-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
