========== Question ==========  

### How do you test for an empty object  

========== Answer ==========  

There are different solutions based on ECMAScript versions

1. **Using Object entries(ECMA 7+):** You can use object entries length along
    with constructor type.

```javascript
Object.entries(obj).length === 0 && obj.constructor === Object; // Since date object length is 0, you need to check constructor check as well
```

1. **Using Object keys(ECMA 5+):** You can use object keys length along with
    constructor type.

```javascript
Object.keys(obj).length === 0 && obj.constructor === Object; // Since date object length is 0, you need to check constructor check as well
```

1. **Using for-in with hasOwnProperty(Pre-ECMA 5):** You can use a for-in loop
    along with hasOwnProperty.

```javascript
function isEmpty(obj) {
  for (var prop in obj) {
     if (obj.hasOwnProperty(prop)) {
       return false;
     }
  }
  return JSON.stringify(obj) === JSON.stringify({});
}
```

========== Id ==========  
127

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#127-How-do-you-test-for-an-empty-object

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
