Q: How do you encode an URL  
A: The encodeURI() function is used to encode complete URI which has special characters except (, / ? : @ & = + $ #) characters.
```javascript
var uri = "https://mozilla.org/?x=шеллы";
var encoded = encodeURI(uri);
console.log(encoded); // https://mozilla.org/?x=%D1%88%D0%B5%D0%BB%D0%BB%D1%8B
```
<!--ID: 1693596704129-->

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