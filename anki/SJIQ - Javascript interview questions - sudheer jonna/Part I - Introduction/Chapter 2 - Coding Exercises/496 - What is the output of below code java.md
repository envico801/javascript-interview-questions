==================== Question ====================  

### What is the output of below code

```javascript
const num = 0o38;
console.log(num);
```

- 1: SyntaxError
- 2: 38  

==================== Answer ====================  

##### Answer: 1

If you use an invalid number(outside of 0-7 range) in the octal literal,
JavaScript will throw a SyntaxError. In ES5, it treats the octal literal as a
decimal number.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#496-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
