==================== Question ====================  

### What are js labels  

==================== Answer ====================  

The label statement allows us to name loops and blocks in JavaScript. We can
then use these labels to refer back to the code later. For example, the below
code with labels avoids printing the numbers when they are same,

```javascript
var i, j;
loop1: for (i = 0; i < 3; i++) {
  loop2: for (j = 0; j < 3; j++) {
    if (i === j) {
      continue loop1;
    }
    console.log('i = ' + i + ', j = ' + j);
  }
}
// Output is:
//   "i = 1, j = 0"
//   "i = 2, j = 0"
//   "i = 2, j = 1"
```

==================== Id ====================  
144

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#144-What-are-js-labels

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
