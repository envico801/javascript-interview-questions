==================== Question ====================  

### What is the way to find the number of parameters expected by a function  

==================== Answer ====================  

You can use `function.length` syntax to find the number of parameters expected
by a function. Let's take an example of `sum` function to calculate the sum of
numbers,

```javascript
function sum(num1, num2, num3, num4) {
  return num1 + num2 + num3 + num4;
}
sum.length; // 4 is the number of parameters expected.
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#141-What-is-the-way-to-find-the-number-of-para

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
