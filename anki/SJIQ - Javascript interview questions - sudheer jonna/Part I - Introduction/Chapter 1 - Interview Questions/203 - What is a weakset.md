==================== Question ====================  

### What is a WeakSet  

==================== Answer ====================  

WeakSet is used to store a collection of weakly(weak references) held objects.
The syntax would be as follows,

```javascript
new WeakSet([iterable]);
```

Let's see the below example to explain it's behavior,

```javascript
var ws = new WeakSet();
var user = {};
ws.add(user);
ws.has(user); // true
ws.delete(user); // removes user from the set
ws.has(user); // false, user has been removed
```

==================== Id ====================  
203
<!--ID: 1707879811859-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#203-What-is-a-weakset

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
