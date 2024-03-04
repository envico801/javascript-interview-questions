========== Question ==========  

### What is the output of below code?

```javascript
var of = ['of'];
for (var of of of) {
  console.log(of);
}
```

- 1: of

- 2: SyntaxError: Unexpected token of

- 3: SyntaxError: Identifier 'of' has already been declared

- 4: ReferenceError: of is not defined  

========== Answer ==========  

Answer: 1

In JavaScript, `of` is not considered as a reserved keyword. So the variable
declaration with `of` is accepted and prints the array value `of` using for..of
loop.

But if you use reserved keyword such as `in` then there will be a syntax error
saying `SyntaxError: Unexpected token in`,

```javascript
var in = ['in'];
for(var in in in) {
console.log(in[in]);
}
```

========== Id ==========  
512

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#512-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
