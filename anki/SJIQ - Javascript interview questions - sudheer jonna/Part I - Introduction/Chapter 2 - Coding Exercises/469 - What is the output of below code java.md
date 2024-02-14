==================== Question ====================  

### What is the output of below code

```javascript
const numbers = new Set([1, 1, 2, 3, 4]);
console.log(numbers);
const browser = new Set('Firefox');
console.log(browser);
```

- 1: {1, 2, 3, 4}, {"F", "i", "r", "e", "f", "o", "x"}
- 2: {1, 2, 3, 4}, {"F", "i", "r", "e", "o", "x"}
- 3: [1, 2, 3, 4], ["F", "i", "r", "e", "o", "x"]
- 4: {1, 1, 2, 3, 4}, {"F", "i", "r", "e", "f", "o", "x"}  

==================== Answer ====================  

Answer: 1  
Since `Set` object is a collection of unique values, it won't allow duplicate
values in the collection. At the same time, it is case sensitive data structure.

==================== Id ====================  
469
<!--ID: 1707879791132-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#469-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
