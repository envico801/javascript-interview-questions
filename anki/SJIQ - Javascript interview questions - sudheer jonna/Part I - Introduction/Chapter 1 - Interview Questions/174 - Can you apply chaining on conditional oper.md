==================== Question ====================  

### Can you apply chaining on conditional operator  

==================== Answer ====================  

Yes, you can apply chaining on conditional operators similar to if … else if …
else if … else chain. The syntax is going to be as below,

```javascript
function traceValue(someParam) {
  return (
    condition1 ? value1
    : condition2 ? value2
    : condition3 ? value3
    : value4
  );
}
// The above conditional operator is equivalent to:
function traceValue(someParam) {
  if (condition1) {
    return value1;
  } else if (condition2) {
    return value2;
  } else if (condition3) {
    return value3;
  } else {
    return value4;
  }
}
```

==================== Id ====================  
174
<!--ID: 1707879834925-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#174-Can-you-apply-chaining-on-conditional-oper

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
