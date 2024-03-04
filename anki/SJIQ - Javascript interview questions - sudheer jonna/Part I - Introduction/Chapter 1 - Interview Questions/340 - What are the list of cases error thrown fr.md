========== Question ==========  

### What are the list of cases error thrown from non-strict mode to strict mode  

========== Answer ==========  

When you apply 'use strict'; syntax, some of the below cases will throw a
SyntaxError before executing the script

1. When you use Octal syntax

```javascript
var n = 022;
```

1. Using `with` statement

2. When you use delete operator on a variable name

3. Using eval or arguments as variable or function argument name

4. When you use newly reserved keywords

5. When you declare a function in a block

```javascript
if (someCondition) {
  function f() {}
}
```

Hence, the errors from above cases are helpful to avoid errors in
development/production environments.

========== Id ==========  
340

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#340-What-are-the-list-of-cases-error-thrown-fr

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
