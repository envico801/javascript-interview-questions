==================== Question ====================  

### What is the output of below code

- 1: console.log(true && 'hi');
- 2: console.log(true && 'hi' && 1);
- 3: console.log(true && '' && 0);  

==================== Answer ====================  

- 1: hi
- 2: 1
- 3: ''  
  Reason : The operator returns the value of the first falsy operand encountered
  when evaluating from left to right, or the value of the last operand if they
  are all truthy.  
  **Note:** Below these values are consider as falsy value
- 1: 0
- 2: ''
- 3: null
- 4: undefined
- 5: NAN

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#506-What-is-the-output-of-below-code-1

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
