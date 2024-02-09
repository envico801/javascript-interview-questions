==================== Question ====================  

### What is the output of below code in non strict mode

```javascript
let msg = 'Good morning!!';
msg.name = 'John';
console.log(msg.name);
```

- 1: ""
- 2: Error
- 3: John
- 4: Undefined  

==================== Answer ====================  

##### Answer: 4

It returns undefined for non-strict mode and returns Error for strict mode. In
non-strict mode, the wrapper object is going to be created and get the mentioned
property. But the object get disappeared after accessing the property in next
line.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#504-What-is-the-output-of-below-code-in-non-st

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
