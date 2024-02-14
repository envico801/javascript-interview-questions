==================== Question ====================  

### What is referential transparency  

==================== Answer ====================  

An expression in javascript that can be replaced by its value without affecting
the behaviour of the program is called referential transparency. Pure functions
are referentially transparent.

```javascript
const add = (x, y) => x + y;
const multiplyBy2 = (x) => x * 2;
//Now add (2, 3) can be replaced by 5.
multiplyBy2(add(2, 3));
```

==================== Id ====================  
443
<!--ID: 1707879818113-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#443-What-is-referential-transparency

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
