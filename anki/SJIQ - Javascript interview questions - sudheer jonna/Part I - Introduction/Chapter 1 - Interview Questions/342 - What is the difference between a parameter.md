==================== Question ====================  

### What is the difference between a parameter and an argument  

==================== Answer ====================  

Parameter is the variable name of a function definition whereas an argument
represents the value given to a function when it is invoked. Let's explain this
with a simple function

```javascript
function myFunction(parameter1, parameter2, parameter3) {
  console.log(arguments[0]); // "argument1"
  console.log(arguments[1]); // "argument2"
  console.log(arguments[2]); // "argument3"
}
myFunction('argument1', 'argument2', 'argument3');
```

==================== Id ====================  
342
<!--ID: 1707879824566-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#342-What-is-the-difference-between-a-parameter

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
