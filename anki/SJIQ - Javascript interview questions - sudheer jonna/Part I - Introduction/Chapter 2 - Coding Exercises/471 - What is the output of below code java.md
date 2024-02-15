==================== Question ====================  

### What is the output of below code

```javascript
let numbers = [1, 2, 3, 4, NaN];
console.log(numbers.indexOf(NaN));
```

- 1: 4
- 2: NaN
- 3: SyntaxError
- 4: -1  

==================== Answer ====================  

Answer: 4  
The `indexOf` uses strict equality operator(===) internally and `NaN === NaN`
evaluates to false. Since indexOf won't be able to find NaN inside an array, it
returns -1 always.  
But you can use `Array.prototype.findIndex` method to find out the index of NaN
in an array or You can use `Array.prototype.includes` to check if NaN is present
in an array or not.

```javascript
let numbers = [1, 2, 3, 4, NaN];
console.log(numbers.findIndex(Number.isNaN)); // 4
console.log(numbers.includes(NaN)); // true
```

==================== Id ====================  
471
<!--ID: 1707879788740-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#471-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
