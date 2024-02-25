==================== Question ====================  

### What is the output of below code

```javascript
let message = 'Hello World!';
message[0] = 'J';
console.log(message);
let name = 'John';
name = name + ' Smith';
console.log(name);
```

- 1: Jello World!, John Smith
- 2: Jello World!, John
- 3: Hello World!, John Smith
- 4: Hello World!, John  

==================== Answer ====================  

Answer: 3  
In JavaScript, primitives are immutable i.e. there is no way to change a
primitive value once it gets created. So when you try to update the string's
first character, there is no change in the string value and prints the same
initial value `Hello World!`. Whereas in the later example, the concatenated
value is re-assigned to the same variable which will result into creation of new
memory block with the reference pointing to `John Smith` value and the old
memory block value(`John`) will be garbage collected.

==================== Id ====================  
521

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#521-What-is-the-output-of-below-code-jav

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
