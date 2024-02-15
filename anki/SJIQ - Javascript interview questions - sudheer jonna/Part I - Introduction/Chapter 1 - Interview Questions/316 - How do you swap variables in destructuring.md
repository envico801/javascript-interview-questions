==================== Question ====================  

### How do you swap variables in destructuring assignment  

==================== Answer ====================  

If you don't use destructuring assignment, swapping two values requires a
temporary variable. Whereas using a destructuring feature, two variable values
can be swapped in one destructuring expression. Let's swap two number variables
in array destructuring assignment,

```javascript
var x = 10,
  y = 20;
[x, y] = [y, x];
console.log(x); // 20
console.log(y); // 10
```

==================== Id ====================  
316
<!--ID: 1707879825812-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#316-How-do-you-swap-variables-in-destructuring

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
