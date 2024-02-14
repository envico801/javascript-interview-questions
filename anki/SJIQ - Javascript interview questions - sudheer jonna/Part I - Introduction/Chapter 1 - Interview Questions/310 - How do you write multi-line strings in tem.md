==================== Question ====================  

### How do you write multi-line strings in template literals  

==================== Answer ====================  

In ES5, you would have to use newline escape characters('\\n') and concatenation
symbols(+) in order to get multi-line strings.

```javascript
console.log('This is string sentence 1\n' + 'This is string sentence 2');
```

Whereas in ES6, You don't need to mention any newline sequence character,

```javascript
console.log(`This is string sentence  
     'This is string sentence 2`);
```

==================== Id ====================  
310
<!--ID: 1707879809627-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#310-How-do-you-write-multi-line-strings-in-tem

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
