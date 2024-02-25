==================== Question ====================  

### What is the output of below code

```javascript
console.log(String.prototype.trimLeft.name === 'trimLeft');
console.log(String.prototype.trimLeft.name === 'trimStart');
```

- 1: True, False
- 2: False, True  

==================== Answer ====================  

Answer: 2  
In order to be consistent with functions like `String.prototype.padStart`, the
standard method name for trimming the whitespaces is considered as `trimStart`.
Due to web web compatibility reasons, the old method name 'trimLeft' still acts
as an alias for 'trimStart'. Hence, the prototype for 'trimLeft' is always
'trimStart'

==================== Id ====================  
463

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#463-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
