Q: What is typescript  
A: TypeScript is a typed superset of JavaScript created by Microsoft that adds optional types, classes, async/await, and many other features, and compiles to plain JavaScript. Angular built entirely in TypeScript and used as a primary language. You can install it globally as
```bash
npm install -g typescript
```
Let's see a simple example of TypeScript usage,
```typescript
function greeting(name: string): string {
  return "Hello, " + name;
}
let user = "Sudheer";
console.log(greeting(user));
```
The greeting method allows only string type as argument.
<!--ID: 1693596700347-->

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