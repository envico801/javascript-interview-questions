==================== Question ====================  

### What is the output of below code

```javascript
const myGenerator = (function* () {
  yield 1;
  yield 2;
  yield 3;
})();
for (const value of myGenerator) {
  console.log(value);
  break;
}
for (const value of myGenerator) {
  console.log(value);
}
```

- 1: 1,2,3 and 1,2,3
- 2: 1,2,3 and 4,5,6
- 3: 1 and 1
- 4: 1  

==================== Answer ====================  

Answer: 4  
The generator should not be re-used once the iterator is closed. i.e, Upon
exiting a loop(on completion or using break & return), the generator is closed
and trying to iterate over it again does not yield any more results. Hence, the
second loop doesn't print any value.

==================== Id ====================  
495
<!--ID: 1707879796107-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#495-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
