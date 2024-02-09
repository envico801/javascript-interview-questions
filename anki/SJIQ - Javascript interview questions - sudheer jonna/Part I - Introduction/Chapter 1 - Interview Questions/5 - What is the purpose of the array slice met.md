==================== Question ====================  

### What is the purpose of the array slice method  

==================== Answer ====================  

The **slice()** method returns the selected elements in an array as a new array
object. It selects the elements starting at the given start argument, and ends
at the given optional end argument without including the last element. If you
omit the second argument then it selects till the end of the array.  
Some of the examples of this method are,

```javascript
let arrayIntegers = [1, 2, 3, 4, 5];
let arrayIntegers1 = arrayIntegers.slice(0, 2); // returns [1,2]
let arrayIntegers2 = arrayIntegers.slice(2, 3); // returns [3]
let arrayIntegers3 = arrayIntegers.slice(4); //returns [5]
```

**Note:** Slice method doesn't mutate the original array but it returns the
subset as a new array.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#5-What-is-the-purpose-of-the-array-slice-met

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
