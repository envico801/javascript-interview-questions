========== Question ==========  

### What is the output of below code?

```javascript
const numbers = [11, 25, 31, 23, 33, 18, 200];
numbers.sort();
console.log(numbers);
```

- 1: [11, 18, 23, 25, 31, 33, 200]

- 2: [11, 18, 200, 23, 25, 31, 33]

- 3: [11, 25, 31, 23, 33, 18, 200]

- 4: Cannot sort numbers  

========== Answer ==========  

Answer: 2

By default, the sort method sorts elements alphabetically. This is because
elemented converted to strings and strings compared in UTF-16 code units order.
Hence, you will see the above numbers not sorted as expected. In order to sort
numerically just supply a comparator function which handles numeric sorts.

```javascript
const numbers = [11, 25, 31, 23, 33, 18, 200];
numbers.sort((a, b) => a - b);
console.log(numbers);
```

**Note:** Sort() method changes the original array.

========== Id ==========  
513

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#513-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
