========== Question ==========  

### What is an Unary operator  

========== Answer ==========  

The unary(+) operator is used to convert a variable to a number.If the variable cannot be converted, it will still become a number but with the value NaN. Let's see this behavior in an action.

```javascript
var x = '100';
var y = +x;
console.log(typeof x, typeof y); // string, number
var a = 'Hello';
var b = +a;
console.log(typeof a, typeof b, b); // string, number, NaN
```

========== Id ==========  
241

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#241-What-is-an-unary-operator

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
