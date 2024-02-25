==================== Question ====================  

### What are the different kinds of generators  

==================== Answer ====================  

There are five kinds of generators,

1. **Generator function declaration:**
   ```javascript
   function* myGenFunc() {
     yield 1;
     yield 2;
     yield 3;
   }
   const genObj = myGenFunc();
   ```
2. **Generator function expressions:**
   ```javascript
   const myGenFunc = function* () {
     yield 1;
     yield 2;
     yield 3;
   };
   const genObj = myGenFunc();
   ```
3. **Generator method definitions in object literals:**
   ```javascript
   const myObj = {
     *myGeneratorMethod() {
       yield 1;
       yield 2;
       yield 3;
     },
   };
   const genObj = myObj.myGeneratorMethod();
   ```
4. **Generator method definitions in class:**
   ```javascript
   class MyClass {
     *myGeneratorMethod() {
       yield 1;
       yield 2;
       yield 3;
     }
   }
   const myObject = new MyClass();
   const genObj = myObject.myGeneratorMethod();
   ```
5. **Generator as a computed property:**
   ```javascript
   const SomeObj = {
     *[Symbol.iterator]() {
       yield 1;
       yield 2;
       yield 3;
     },
   };
   console.log(Array.from(SomeObj)); // [ 1, 2, 3 ]
   ```

==================== Id ====================  
416

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#416-What-are-the-different-kinds-of-generators

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
