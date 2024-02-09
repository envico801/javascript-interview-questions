==================== Question ====================  

### How do you assign default values to variables  

==================== Answer ====================  

You can use the logical or operator `||` in an assignment expression to provide
a default value. The syntax looks like as below,

```javascript
var a = b || c;
```

As per the above expression, variable 'a 'will get the value of 'c' only if 'b'
is falsy (if is null, false, undefined, 0, empty string, or NaN), otherwise 'a'
will get the value of 'b'.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#137-How-do-you-assign-default-values-to-variab

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
