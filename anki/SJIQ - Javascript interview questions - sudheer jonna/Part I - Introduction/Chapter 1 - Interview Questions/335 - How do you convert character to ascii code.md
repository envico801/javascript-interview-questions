========== Question ==========  

### How do you convert character to ASCII code  

========== Answer ==========  

You can use the `String.prototype.charCodeAt()` method to convert string characters to ASCII numbers. For example, let's find ASCII code for the first letter of 'ABC' string,

```javascript
'ABC'.charCodeAt(0); // returns 65
```

Whereas `String.fromCharCode()` method converts numbers to equal ASCII characters.

```javascript
String.fromCharCode(65, 66, 67); // returns 'ABC'
```

========== Id ==========  
335

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#335-How-do-you-convert-character-to-ascii-code

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
