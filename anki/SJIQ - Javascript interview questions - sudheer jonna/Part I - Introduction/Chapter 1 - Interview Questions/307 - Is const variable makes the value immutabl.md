========== Question ==========  

### Is const variable makes the value immutable  

========== Answer ==========  

No, the const variable doesn't make the value immutable. But it disallows
subsequent assignments(i.e, You can declare with assignment but can't assign
another value later)

```javascript
const userList = [];
userList.push('John'); // Can mutate even though it can't re-assign
console.log(userList); // ['John']
```

========== Id ==========  
307

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#307-Is-const-variable-makes-the-value-immutabl

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
