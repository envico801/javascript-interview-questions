==================== Question ====================  

### What is a Proper Tail Call  

==================== Answer ====================  

First, we should know about tail call before talking about "Proper Tail Call". A
tail call is a subroutine or function call performed as the final action of a
calling function. Whereas **Proper tail call(PTC)** is a technique where the
program or code will not create additional stack frames for a recursion when the
function call is a tail call.  
For example, the below classic or head recursion of factorial function relies on
stack for each step. Each step need to be processed upto `n * factorial(n - 1)`

```javascript
function factorial(n) {
  if (n === 0) {
    return 1;
  }
  return n * factorial(n - 1);
}
console.log(factorial(5)); //120
```

But if you use Tail recursion functions, they keep passing all the necessary
data it needs down the recursion without relying on the stack.

```javascript
function factorial(n, acc = 1) {
  if (n === 0) {
    return acc;
  }
  return factorial(n - 1, n * acc);
}
console.log(factorial(5)); //120
```

The above pattern returns the same output as the first one. But the accumulator
keeps track of total as an argument without using stack memory on recursive
calls.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#411-What-is-a-proper-tail-call

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
