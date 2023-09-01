Q: What are the possible side-effects in javascript?  
A: A side effect is the modification of state through the invocation of a function or expression. These side effects makes our function impure by default. Below are some side effects which makes function impure,
1. Making an HTTP request. Asynchronous functions such as fetch and promise are impure.
2. DOM manipulations
3. Mutating the input data
4. Printing to a screen or console: For example, console.log() and alert()
5. Fetching the current time
6. Math.random() calls: Modifies the internal state of Math object
<!--ID: 1693596681521-->

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