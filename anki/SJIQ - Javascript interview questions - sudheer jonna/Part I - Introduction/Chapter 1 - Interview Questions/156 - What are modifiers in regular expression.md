==================== Question ====================  

### What are modifiers in regular expression  

==================== Answer ====================  

Modifiers can be used to perform case-insensitive and global searches. Let's
list down some of the modifiers,

| Modifier | Description                                             |
| -------- | ------------------------------------------------------- |
| i        | Perform case-insensitive matching                       |
| g        | Perform a global match rather than stops at first match |
| m        | Perform multiline matching                              |

Let's take an example of global modifier,

```javascript
var text = 'Learn JS one by one';
var pattern = /one/g;
var result = text.match(pattern); // one,one
```

==================== Id ====================  
156
<!--ID: 1707879837157-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#156-What-are-modifiers-in-regular-expression

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
