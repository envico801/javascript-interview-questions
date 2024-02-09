==================== Question ====================  

### What is the output of below code

```javascript
let zero = new Number(0);
if (zero) {
  console.log('If');
} else {
  console.log('Else');
}
```

- 1: If
- 2: Else
- 3: NaN
- 4: SyntaxError  

==================== Answer ====================  

##### Answer: 1

1. The type of operator on new Number always returns object. i.e, typeof new
   Number(0) --> object.
2. Objects are always truthy in if block  
   Hence the above code block always goes to if section.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#503-What-is-the-output-of-below-code-jav

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
