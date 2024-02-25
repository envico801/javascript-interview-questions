==================== Question ====================  

### What is the purpose of uneval  

==================== Answer ====================  

The uneval() is an inbuilt function which is used to create a string
representation of the source code of an Object. It is a top-level function and
is not associated with any object. Let's see the below example to know more
about it's functionality,

```javascript
var a = 1;
uneval(a); // returns a String containing 1
uneval(function user() {}); // returns "(function user(){})"
```

The `uneval()` function has been deprecated. It is recommended to use
`toString()` for functions and `JSON.toStringify()` for other cases.

```javascript
function user() {}
console.log(user.toString()); // returns "(function user(){})"
```

==================== Id ====================  
209

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#209-What-is-the-purpose-of-uneval

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
