==================== Question ====================  

### What are the string methods available in Regular expression  

==================== Answer ====================  

Regular Expressions has two string methods: search() and replace().  
The search() method uses an expression to search for a match, and returns the
position of the match.

```javascript
var msg = 'Hello John';
var n = msg.search(/John/i); // 6
```

The replace() method is used to return a modified string where the pattern is
replaced.

```javascript
var msg = 'Hello John';
var n = msg.replace(/John/i, 'Buttler'); // Hello Buttler
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#155-What-are-the-string-methods-available-in-r

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
