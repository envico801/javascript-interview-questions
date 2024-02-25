==================== Question ====================  

### What is the output of below code

```javascript
function foo() {
  return;
  {
    message: 'Hello World';
  }
}
console.log(foo());
```

- 1: Hello World
- 2: Object {message: "Hello World"}
- 3: Undefined
- 4: SyntaxError  

==================== Answer ====================  

Answer: 3  
This is a semicolon issue. Normally semicolons are optional in JavaScript. So if
there are any statements(in this case, return) missing semicolon, it is
automatically inserted immediately. Hence, the function returned as undefined.  
Whereas if the opening curly brace is along with the return keyword then the
function is going to be returned as expected.

```javascript
function foo() {
  return {
    message: 'Hello World',
  };
}
console.log(foo()); // {message: "Hello World"}
```

==================== Id ====================  
455

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#455-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
