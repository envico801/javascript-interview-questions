==================== Question ====================  

### What is the output of below code

```javascript
let a = 10;
if (true) {
  let a = 20;
  console.log(a, 'inside');
}
console.log(a, 'outside');
```

- 1: 20, "inside" and 20, "outside"
- 2: 20, "inside" and 10, "outside"
- 3: 10, "inside" and 10, "outside"
- 4: 10, "inside" and 20, "outside"  

==================== Answer ====================  

Answer: 2  
The variable "a" declared inside "if" has block scope and does not affect the
value of the outer "a" variable.

==================== Id ====================  
528
<!--ID: 1707879792334-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#528-What-is-the-output-of-below-code-jav

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
