==================== Question ====================  

### What are the placeholders from console object  

==================== Answer ====================  

Below are the list of placeholders available from console object,

1. %o — It takes an object,
2. %s — It takes a string,
3. %d — It is used for a decimal or integer  
   These placeholders can be represented in the console.log as below

```javascript
const user = { name: 'John', id: 1, city: 'Delhi' };
console.log(
  'Hello %s, your details %o are available in the object form',
  'John',
  user,
); // Hello John, your details {name: "John", id: 1, city: "Delhi"} are available in object
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#368-What-are-the-placeholders-from-console-obj

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
