==================== Question ====================  

### What is the purpose of double exclamation  

==================== Answer ====================  

The double exclamation or negation(!!) ensures the resulting type is a boolean.
If it was falsey (e.g. 0, null, undefined, etc.), it will be false, otherwise,
it will be true.  
For example, you can test IE version using this expression as below,

```javascript
let isIE8 = false;
isIE8 = !!navigator.userAgent.match(/MSIE 8.0/);
console.log(isIE8); // returns true or false
```

If you don't use this expression then it returns the original value.

```javascript
console.log(navigator.userAgent.match(/MSIE 8.0/)); // returns either an Array or null
```

**Note:** The expression !! is not an operator, but it is just twice of !
operator.

==================== Id ====================  
69

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#69-What-is-the-purpose-of-double-exclamation

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
