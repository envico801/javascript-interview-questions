==================== Question ====================  

### How to invoke an IIFE without any extra brackets  

==================== Answer ====================  

Immediately Invoked Function Expressions(IIFE) requires a pair of parenthesis to
wrap the function which contains set of statements.

```js
(function (dt) {
  console.log(dt.toLocaleTimeString());
})(new Date());
```

Since both IIFE and void operator discard the result of an expression, you can
avoid the extra brackets using `void operator` for IIFE as below,

```js
void (function (dt) {
  console.log(dt.toLocaleTimeString());
})(new Date());
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#421-How-to-invoke-an-iife-without-any-extra-br

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
