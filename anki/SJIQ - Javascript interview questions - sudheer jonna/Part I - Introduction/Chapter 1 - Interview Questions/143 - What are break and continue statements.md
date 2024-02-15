==================== Question ====================  

### What are break and continue statements  

==================== Answer ====================  

The break statement is used to "jump out" of a loop. i.e, It breaks the loop and
continues executing the code after the loop.

```javascript
for (i = 0; i < 10; i++) {
  if (i === 5) {
    break;
  }
  text += 'Number: ' + i + '<br>';
}
```

The continue statement is used to "jump over" one iteration in the loop. i.e, It
breaks one iteration (in the loop), if a specified condition occurs, and
continues with the next iteration in the loop.

```javascript
for (i = 0; i < 10; i++) {
  if (i === 5) {
    continue;
  }
  text += 'Number: ' + i + '<br>';
}
```

==================== Id ====================  
143
<!--ID: 1707879813316-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#143-What-are-break-and-continue-statements

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
