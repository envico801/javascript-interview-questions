==================== Question ====================  

### What is the output of below code in latest Chrome

```javascript
var array1 = new Array(3);
console.log(array1);
var array2 = [];
array2[2] = 100;
console.log(array2);
var array3 = [, , ,];
console.log(array3);
```

- 1: [undefined × 3], [undefined × 2, 100], [undefined × 3]
- 2: [empty × 3], [empty × 2, 100], [empty × 3]
- 3: [null × 3], [null × 2, 100], [null × 3]
- 4: [], [100], []  

==================== Answer ====================  

##### Answer: 2

The latest chrome versions display `sparse array`(they are filled with holes)
using this empty x n notation. Whereas the older versions have undefined x n
notation.  
**Note:** The latest version of FF displays `n empty slots` notation.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#457-What-is-the-output-of-below-code-in-latest

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
