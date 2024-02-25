==================== Question ====================  

### How do you trim a string at the beginning or ending  

==================== Answer ====================  

The `trim` method of string prototype is used to trim on both sides of a string.
But if you want to trim especially at the beginning or ending of the string then
you can use `trimStart/trimLeft` and `trimEnd/trimRight` methods. Let's see an
example of these methods on a greeting message,

```javascript
var greeting = '   Hello, Goodmorning!   ';
console.log(greeting); // "   Hello, Goodmorning!   "
console.log(greeting.trimStart()); // "Hello, Goodmorning!   "
console.log(greeting.trimLeft()); // "Hello, Goodmorning!   "
console.log(greeting.trimEnd()); // "   Hello, Goodmorning!"
console.log(greeting.trimRight()); // "   Hello, Goodmorning!"
```

==================== Id ====================  
348

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#348-How-do-you-trim-a-string-at-the-beginning

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
