==================== Question ====================  

### What is the difference between isNaN and Number.isNaN  

==================== Answer ====================  

1. **isNaN**: The global function `isNaN` converts the argument to a Number and
   returns true if the resulting value is NaN.
2. **Number.isNaN**: This method does not convert the argument. But it returns
   true when the type is a Number and value is NaN.  
   Let's see the difference with an example,

```javascript
     isNaN(‘hello’);   // true
     Number.isNaN('hello'); // false
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#420-What-is-the-difference-between-isnan-and-n

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
