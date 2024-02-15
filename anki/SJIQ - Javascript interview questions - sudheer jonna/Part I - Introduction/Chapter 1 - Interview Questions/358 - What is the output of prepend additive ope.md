==================== Question ====================  

### What is the output of prepend additive operator on falsy values  

==================== Answer ====================  

If you prepend the additive(+) operator on falsy values(null, undefined, NaN,
false, ""), the falsy value converts to a number value zero. Let's display them
on browser console as below,

```javascript
console.log(+null); // 0
console.log(+undefined); // NaN
console.log(+false); // 0
console.log(+NaN); // NaN
console.log(+''); // 0
```

==================== Id ====================  
358
<!--ID: 1707879822955-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#358-What-is-the-output-of-prepend-additive-ope

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
