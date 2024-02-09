==================== Question ====================  

### What is Function Composition  

==================== Answer ====================  

It is an approach where the result of one function is passed on to the next
function, which is passed to another until the final function is executed for
the final result.

```javascript
//example
const double = (x) => x * 2;
const square = (x) => x * x;
var output1 = double(2);
var output2 = square(output1);
console.log(output2);
var output_final = square(double(2));
console.log(output_final);
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#447-What-is-function-composition

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
