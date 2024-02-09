==================== Question ====================  

### What is a pure function  

==================== Answer ====================  

A **Pure function** is a function where the return value is only determined by
its arguments without any side effects. i.e, If you call a function with the
same arguments 'n' number of times and 'n' number of places in the application
then it will always return the same value.  
Let's take an example to see the difference between pure and impure functions,

```javascript
//Impure
let numberArray = [];
const impureAddNumber = (number) => numberArray.push(number);
//Pure
const pureAddNumber = (number) => (argNumberArray) =>
  argNumberArray.concat([number]);
//Display the results
console.log(impureAddNumber(6)); // returns 1
console.log(numberArray); // returns [6]
console.log(pureAddNumber(7)(numberArray)); // returns [6, 7]
console.log(numberArray); // returns [6]
```

As per the above code snippets, the **Push** function is impure itself by
altering the array and returning a push number index independent of the
parameter value, whereas **Concat** on the other hand takes the array and
concatenates it with the other array producing a whole new array without side
effects. Also, the return value is a concatenation of the previous array.  
Remember that Pure functions are important as they simplify unit testing without
any side effects and no need for dependency injection. They also avoid tight
coupling and make it harder to break your application by not having any side
effects. These principles are coming together with the **Immutability** concept
of ES6: giving preference to **const** over **let** usage.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#16-What-is-a-pure-function

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
