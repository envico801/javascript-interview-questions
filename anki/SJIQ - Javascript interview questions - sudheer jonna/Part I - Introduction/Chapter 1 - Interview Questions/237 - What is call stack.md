==================== Question ====================  

### What is call stack  

==================== Answer ====================  

Call Stack is a data structure for javascript interpreters to keep track of
function calls(creates execution context) in the program. It has two major
actions,

1. Whenever you call a function for its execution, you are pushing it to the
   stack.
2. Whenever the execution is completed, the function is popped out of the
   stack.  
   Let's take an example and it's state representation in a diagram format

```javascript
function hungry() {
  eatFruits();
}
function eatFruits() {
  return "I'm eating fruits";
}
// Invoke the `hungry` function
hungry();
```

The above code processed in a call stack as below,

1. Add the `hungry()` function to the call stack list and execute the code.
2. Add the `eatFruits()` function to the call stack list and execute the code.
3. Delete the `eatFruits()` function from our call stack list.
4. Delete the `hungry()` function from the call stack list since there are no
   items anymore.  
   ![call-stack](../../../../images/call-stack.png)

==================== Id ====================  
237

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#237-What-is-call-stack

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
