==================== Question ====================  

### What is the output of below code

```javascript
function greeting() {
  setTimeout(function () {
    console.log(message);
  }, 5000);
  const message = 'Hello, Good morning';
}
greeting();
```

- 1: Undefined
- 2: Reference error:
- 3: Hello, Good morning
- 4: null  

==================== Answer ====================  

Answer: 3  
The variable `message` is still treated as closure(since it has been used in
inner function) eventhough it has been declared after setTimeout function. The
function with in setTimeout function will be sent to WebAPI and the variable
declaration executed with in 5 seconds with the assigned value. Hence, the text
declared for the variable will be displayed.

==================== Id ====================  
523
<!--ID: 1707879793228-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#523-What-is-the-output-of-below-code-jav

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
