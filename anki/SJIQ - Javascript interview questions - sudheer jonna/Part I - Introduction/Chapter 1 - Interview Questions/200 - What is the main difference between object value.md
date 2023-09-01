Q: What is the main difference between Object.values and Object.entries method  
A: The Object.values() method's behavior is similar to Object.entries() method but it returns an array of values instead [key,value] pairs.
```javascript
const object = {
  a: "Good morning",
  b: 100,
};
for (let value of Object.values(object)) {
  console.log(`${value}`); // 'Good morning'
  100;
}
```
<!--ID: 1693596705096-->

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