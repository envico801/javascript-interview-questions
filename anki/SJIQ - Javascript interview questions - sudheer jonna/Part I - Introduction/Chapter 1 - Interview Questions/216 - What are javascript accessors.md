Q: What are javascript accessors  
A: ECMAScript 5 introduced javascript object accessors or computed properties through getters and setters. Getters uses the `get` keyword whereas Setters uses the `set` keyword.
```javascript
var user = {
  firstName: "John",
  lastName: "Abraham",
  language: "en",
  get lang() {
    return this.language;
  },
  set lang(lang) {
    this.language = lang;
  },
};
console.log(user.lang); // getter access lang as en
user.lang = "fr";
console.log(user.lang); // setter used to set lang as fr
```
<!--ID: 1693596703497-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript #Interview

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store