========== Question ==========  

### What is the output of below code

```javascript
const props = [
  { id: 1, name: 'John' },
  { id: 2, name: 'Jack' },
  { id: 3, name: 'Tom' },
];
const [, , { name }] = props;
console.log(name);
```

- 1: Tom

- 2: Error

- 3: undefined

- 4: John  

========== Answer ==========  

Answer: 1

It is possible to combine Array and Object destructuring. In this case, the
third element in the array props accessed first followed by name property in the
object.

========== Id ==========  
486

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#486-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
