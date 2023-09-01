Q: How to use await outside of async function prior to ES2022?  
A: Prior to ES2022, if you attempted to use an await outside of an async function resulted in a SyntaxError.
```javascript
await Promise.resolve(console.log("Hello await")); // SyntaxError: await is only valid in async function
```
But you can fix this issue with an alternative IIFE (Immediately Invoked Function Expression) to get access to the feature.
```javascript
(async function () {
  await Promise.resolve(console.log("Hello await")); // Hello await
})();
```
In ES2022, you can write top-level await without writing any hacks.
```javascript
await Promise.resolve(console.log("Hello await")); //Hello await
```
<!--ID: 1693596681163-->

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