Q: How do you create your own bind method using either call or apply method?  
A: The custom bind function needs to be created on Function prototype inorder to use it as other builtin functions. This custom function should return a function similar to original bind method and the implementation of inner function needs to use apply method call.  
The function which is going to bind using custom `myOwnBind` method act as the attached function(`boundTargetFunction`) and argument as the object for `apply` method call.
```js
Function.prototype.myOwnBind = function (whoIsCallingMe) {
  if (typeof this !== "function") {
    throw new Error(this + "cannot be bound as it's not callable");
  }
  const boundTargetFunction = this;
  return function () {
    boundTargetFunction.apply(whoIsCallingMe, arguments);
  };
};
```
<!--ID: 1693596681837-->

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