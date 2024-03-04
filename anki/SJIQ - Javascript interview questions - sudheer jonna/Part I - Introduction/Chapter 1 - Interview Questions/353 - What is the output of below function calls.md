========== Question ==========  

### What is the output of below function calls

**Code snippet:**

```javascript
const circle = {
  radius: 20,
  diameter() {
     return this.radius * 2;
  },
  perimeter: () => 2 * Math.PI * this.radius,
};
```

```javascript
console.log(circle.diameter());
console.log(circle.perimeter());
```  

========== Answer ==========  

**Output:**

The output is 40 and NaN. Remember that diameter is a regular function, whereas
the value of perimeter is an arrow function. The `this` keyword of a regular
function(i.e, diameter) refers to the surrounding scope which is a class(i.e,
Shape object). Whereas this keyword of perimeter function refers to the
surrounding scope which is a window object. Since there is no radius property on
window objects it returns an undefined value and the multiple of number value
returns NaN value.

========== Id ==========  
353

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#353-What-is-the-output-of-below-function-calls

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
