==================== Question ====================  

### What is the output of below code

```javascript
console.log(name);
console.log(message());
var name = 'John';
(function message() {
  console.log('Hello John: Welcome');
});
```

- 1: John, Hello John: Welcome
- 2: undefined, Hello John, Welcome
- 3: Reference error: name is not defined, Reference error: message is not
  defined
- 4: undefined, Reference error: message is not defined  

==================== Answer ====================  

Answer: 4  
IIFE(Immediately Invoked Function Expression) is just like any other function
expression which won't be hoisted. Hence, there will be a reference error for
message call.  
The behavior would be the same with below function expression of message1,

```javascript
console.log(name);
console.log(message());
var name = 'John';
var message = function () {
console.log('Hello John: Welcome');
});
```

==================== Id ====================  
515

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#515-What-is-the-output-of-below-code-jav

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
