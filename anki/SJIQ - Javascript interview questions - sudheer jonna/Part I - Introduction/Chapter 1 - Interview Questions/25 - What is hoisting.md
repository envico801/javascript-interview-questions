==================== Question ====================  

### What is Hoisting  

==================== Answer ====================  

Hoisting is a JavaScript mechanism where variables, function declarations and
classes are moved to the top of their scope before code execution. Remember that
JavaScript only hoists declarations, not initialisation.  
Let's take a simple example of variable hoisting,

```javascript
console.log(message); //output : undefined
var message = 'The variable Has been hoisted';
```

The above code looks like as below to the interpreter,

```javascript
var message;
console.log(message);
message = 'The variable Has been hoisted';
```

In the same fashion, function declarations are hoisted too

```javascript
message('Good morning'); //Good morning
function message(name) {
  console.log(name);
}
```

This hoisting makes functions to be safely used in code before they are
declared.

==================== Id ====================  
25

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#25-What-is-hoisting

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
