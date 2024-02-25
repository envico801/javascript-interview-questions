==================== Question ====================  

### What is the output of below code

```javascript
let myNumber = 100;
let myString = '100';
if (!typeof myNumber === 'string') {
  console.log('It is not a string!');
} else {
  console.log('It is a string!');
}
if (!typeof myString === 'number') {
  console.log('It is not a number!');
} else {
  console.log('It is a number!');
}
```

- 1: SyntaxError
- 2: It is not a string!, It is not a number!
- 3: It is not a string!, It is a number!
- 4: It is a string!, It is a number!  

==================== Answer ====================  

Answer: 4  
The return value of `typeof myNumber` or `typeof myString` is always a truthy
value (either "number" or "string"). The ! operator operates on either
`typeof myNumber` or `typeof myString`, converting them to boolean values. Since
the value of both `!typeof myNumber` and `!typeof myString` is false, the if
condition fails, and control goes to else block.  
To make the ! operator operate on the equality expression, one needs to add
parentheses:

```
if (!(typeof myNumber === "string"))
```

Or simply use the inequality operator:

```
if (typeof myNumber !== "string")
```

==================== Id ====================  
480

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#480-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
