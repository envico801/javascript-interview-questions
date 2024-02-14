==================== Question ====================  

### What is the easiest way to resize an array  

==================== Answer ====================  

The length property of an array is useful to resize or empty an array quickly.
Let's apply length property on number array to resize the number of elements
from 5 to 2,

```javascript
var array = [1, 2, 3, 4, 5];
console.log(array.length); // 5
array.length = 2;
console.log(array.length); // 2
console.log(array); // [1,2]
```

and the array can be emptied too

```javascript
var array = [1, 2, 3, 4, 5];
array.length = 0;
console.log(array.length); // 0
console.log(array); // []
```

==================== Id ====================  
404
<!--ID: 1707879806989-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#404-What-is-the-easiest-way-to-resize-an-array

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
