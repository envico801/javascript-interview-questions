==================== Question ====================  

### What is the output of below code

```javascript
var myChars = ['a', 'b', 'c', 'd'];
delete myChars[0];
console.log(myChars);
console.log(myChars[0]);
console.log(myChars.length);
```

- 1: [empty, 'b', 'c', 'd'], empty, 3
- 2: [null, 'b', 'c', 'd'], empty, 3
- 3: [empty, 'b', 'c', 'd'], undefined, 4
- 4: [null, 'b', 'c', 'd'], undefined, 4  

==================== Answer ====================  

Answer: 3  
The `delete` operator will delete the object property but it will not reindex
the array or change its length. So the number or elements or length of the array
won't be changed.  
If you try to print myChars then you can observe that it doesn't set an
undefined value, rather the property is removed from the array. The newer
versions of Chrome use `empty` instead of `undefined` to make the difference a
bit clearer.

==================== Id ====================  
456
<!--ID: 1707879801095-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#456-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
