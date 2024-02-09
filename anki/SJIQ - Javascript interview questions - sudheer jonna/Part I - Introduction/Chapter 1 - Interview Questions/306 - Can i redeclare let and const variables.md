==================== Question ====================  

### Can I redeclare let and const variables  

==================== Answer ====================  

No, you cannot redeclare let and const variables. If you do, it throws below
error

```bash
     Uncaught SyntaxError: Identifier 'someVariable' has already been declared
```

**Explanation:** The variable declaration with `var` keyword refers to a
function scope and the variable is treated as if it were declared at the top of
the enclosing scope due to hoisting feature. So all the multiple declarations
contributing to the same hoisted variable without any error. Let's take an
example of re-declaring variables in the same scope for both var and let/const
variables.

```javascript
var name = 'John';
function myFunc() {
  var name = 'Nick';
  var name = 'Abraham'; // Re-assigned in the same function block
  alert(name); // Abraham
}
myFunc();
alert(name); // John
```

The block-scoped multi-declaration throws syntax error,

```javascript
let name = 'John';
function myFunc() {
  let name = 'Nick';
  let name = 'Abraham'; // Uncaught SyntaxError: Identifier 'name' has already been declared
  alert(name);
}
myFunc();
alert(name);
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#306-Can-i-redeclare-let-and-const-variables

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
