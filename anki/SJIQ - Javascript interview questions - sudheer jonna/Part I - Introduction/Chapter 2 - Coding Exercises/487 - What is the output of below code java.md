==================== Question ====================  

### What is the output of below code

```javascript
function checkType(num = 1) {
  console.log(typeof num);
}
checkType();
checkType(undefined);
checkType('');
checkType(null);
```

- 1: number, undefined, string, object
- 2: undefined, undefined, string, object
- 3: number, number, string, object
- 4: number, number, number, number  

==================== Answer ====================  

Answer: 3  
If the function argument is set implicitly(not passing argument) or explicitly
to undefined, the value of the argument is the default parameter. Whereas for
other falsy values('' or null), the value of the argument is passed as a
parameter.  
Hence, the result of function calls categorized as below,

1. The first two function calls logs number type since the type of default value
   is number
2. The type of '' and null values are string and object type respectively.

==================== Id ====================  
487
<!--ID: 1707879797566-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#487-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
