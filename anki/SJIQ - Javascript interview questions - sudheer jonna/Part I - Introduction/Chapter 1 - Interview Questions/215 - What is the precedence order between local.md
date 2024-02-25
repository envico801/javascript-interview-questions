==================== Question ====================  

### What is the precedence order between local and global variables  

==================== Answer ====================  

A local variable takes precedence over a global variable with the same name.
Let's see this behavior in an example.

```javascript
var msg = 'Good morning';
function greeting() {
  msg = 'Good Evening';
  console.log(msg); // Good Evening
}
greeting();
```

==================== Id ====================  
215

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#215-What-is-the-precedence-order-between-local

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
