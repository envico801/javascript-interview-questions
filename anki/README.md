# SJIQ - Javascript interview questions - sudheer jonna

## Questions

### Part I - Introduction

#### Chapter 1 - Interview Questions

Q:: What are the possible ways to create objects in JavaScript  
A:: There are many ways to create objects in javascript as below

1. **Object constructor:**
   The simplest way to create an empty object is using the Object constructor. Currently this approach is not recommended.
   ```javascript
   var object = new Object();
   ```
2. **Object's create method:**
   The create method of Object creates a new object by passing the prototype object as a parameter
   ```javascript
   var object = Object.create(null);
   ```
3. **Object literal syntax:**
   The object literal syntax (or object initializer), is a comma-separated set of name-value pairs wrapped in curly braces.
   ```javascript
      var object = {
           name: "Sudheer",
           age: 34
      };
      Object literal property values can be of any data type, including array, function, and nested object.
   ```
   **Note:** This is an easiest way to create an object
4. **Function constructor:**
   Create any function and apply the new operator to create object instances,
   ```javascript
   function Person(name) {
     this.name = name;
     this.age = 21;
   }
   var object = new Person("Sudheer");
   ```
5. **Function constructor with prototype:**
   This is similar to function constructor but it uses prototype for their properties and methods,
   ```javascript
   function Person() {}
   Person.prototype.name = "Sudheer";
   var object = new Person();
   ```
   This is equivalent to an instance created with an object create method with a function prototype and then call that function with an instance and parameters as arguments.
   ```javascript
   function func() {}
   new func(x, y, z);
   ```
   **(OR)**
   ```javascript
      // Create a new instance using function prototype.
      var newInstance = Object.create(func.prototype)
      // Call the function
      var result = func.call(newInstance, x, y, z),
      // If the result is a non-null object then use it otherwise just use the new instance.
      console.log(result && typeof result === 'object' ? result : newInstance);
   ```
6. **ES6 Class syntax:**
   ES6 introduces class feature to create the objects
   ```javascript
   class Person {
     constructor(name) {
       this.name = name;
     }
   }
   var object = new Person("Sudheer");
   ```
7. **Singleton pattern:**
   A Singleton is an object which can only be instantiated one time. Repeated calls to its constructor return the same instance and this way one can ensure that they don't accidentally create multiple instances.
   ```javascript
   var object = new (function () {
     this.name = "Sudheer";
   })();
   ```

Q:: What is a prototype chain  
A:: **Prototype chaining** is used to build new types of objects based on existing ones. It is similar to inheritance in a class based language.  
The prototype on object instance is available through **Object.getPrototypeOf(object)** or **\_\_proto\_\_** property whereas prototype on constructors function is available through **Object.prototype**.  
![prototype_chain](../images/prototype_chain.png)

Q:: What is the difference between Call, Apply and Bind  
A:: The difference between Call, Apply and Bind can be explained with below examples,  
**Call:** The call() method invokes a function with a given `this` value and arguments provided one by one

```javascript
var employee1 = { firstName: "John", lastName: "Rodson" };
var employee2 = { firstName: "Jimmy", lastName: "Baily" };
function invite(greeting1, greeting2) {
  console.log(
    greeting1 + " " + this.firstName + " " + this.lastName + ", " + greeting2,
  );
}
invite.call(employee1, "Hello", "How are you?"); // Hello John Rodson, How are you?
invite.call(employee2, "Hello", "How are you?"); // Hello Jimmy Baily, How are you?
```

**Apply:** Invokes the function with a given `this` value and allows you to pass in arguments as an array

```javascript
var employee1 = { firstName: "John", lastName: "Rodson" };
var employee2 = { firstName: "Jimmy", lastName: "Baily" };
function invite(greeting1, greeting2) {
  console.log(
    greeting1 + " " + this.firstName + " " + this.lastName + ", " + greeting2,
  );
}
invite.apply(employee1, ["Hello", "How are you?"]); // Hello John Rodson, How are you?
invite.apply(employee2, ["Hello", "How are you?"]); // Hello Jimmy Baily, How are you?
```

**bind:** returns a new function, allowing you to pass any number of arguments

```javascript
var employee1 = { firstName: "John", lastName: "Rodson" };
var employee2 = { firstName: "Jimmy", lastName: "Baily" };
function invite(greeting1, greeting2) {
  console.log(
    greeting1 + " " + this.firstName + " " + this.lastName + ", " + greeting2,
  );
}
var inviteEmployee1 = invite.bind(employee1);
var inviteEmployee2 = invite.bind(employee2);
inviteEmployee1("Hello", "How are you?"); // Hello John Rodson, How are you?
inviteEmployee2("Hello", "How are you?"); // Hello Jimmy Baily, How are you?
```

Call and apply are pretty interchangeable. Both execute the current function immediately. You need to decide whether it’s easier to send in an array or a comma separated list of arguments. You can remember by treating Call is for **comma** (separated list) and Apply is for **Array**.
Whereas Bind creates a new function that will have `this` set to the first parameter passed to bind().

Q:: What is JSON and its common operations  
A:: **JSON** is a text-based data format following JavaScript object syntax, which was popularized by `Douglas Crockford`. It is useful when you want to transmit data across a network and it is basically just a text file with an extension of .json, and a MIME type of application/json  
**Parsing:** Converting a string to a native object

```javascript
JSON.parse(text);
```

**Stringification:** converting a native object to a string so it can be transmitted across the network

```javascript
JSON.stringify(object);
```

Q:: What is the purpose of the array slice method  
A:: The **slice()** method returns the selected elements in an array as a new array object. It selects the elements starting at the given start argument, and ends at the given optional end argument without including the last element. If you omit the second argument then it selects till the end.  
Some of the examples of this method are,

```javascript
let arrayIntegers = [1, 2, 3, 4, 5];
let arrayIntegers1 = arrayIntegers.slice(0, 2); // returns [1,2]
let arrayIntegers2 = arrayIntegers.slice(2, 3); // returns [3]
let arrayIntegers3 = arrayIntegers.slice(4); //returns [5]
```

**Note:** Slice method won't mutate the original array but it returns the subset as a new array.

Q:: What is the purpose of the array splice method  
A:: The **splice()** method is used either adds/removes items to/from an array, and then returns the removed item. The first argument specifies the array position for insertion or deletion whereas the optional second argument indicates the number of elements to be deleted. Each additional argument is added to the array.  
Some of the examples of this method are,

```javascript
let arrayIntegersOriginal1 = [1, 2, 3, 4, 5];
let arrayIntegersOriginal2 = [1, 2, 3, 4, 5];
let arrayIntegersOriginal3 = [1, 2, 3, 4, 5];
let arrayIntegers1 = arrayIntegersOriginal1.splice(0, 2); // returns [1, 2]; original array: [3, 4, 5]
let arrayIntegers2 = arrayIntegersOriginal2.splice(3); // returns [4, 5]; original array: [1, 2, 3]
let arrayIntegers3 = arrayIntegersOriginal3.splice(3, 1, "a", "b", "c"); //returns [4]; original array: [1, 2, 3, "a", "b", "c", 5]
```

**Note:** Splice method modifies the original array and returns the deleted array.

Q:: What is the difference between slice and splice  
A:: Some of the major difference in a tabular form

| Slice                                        | Splice                                          |
| -------------------------------------------- | ----------------------------------------------- |
| Doesn't modify the original array(immutable) | Modifies the original array(mutable)            |
| Returns the subset of original array         | Returns the deleted elements as array           |
| Used to pick the elements from array         | Used to insert or delete elements to/from array |

Q:: How do you compare Object and Map  
A:: **Objects** are similar to **Maps** in that both let you set keys to values, retrieve those values, delete keys, and detect whether something is stored at a key. Due to this reason, Objects have been used as Maps historically. But there are important differences that make using a Map preferable in certain cases.

1. The keys of an Object are Strings and Symbols, whereas they can be any value for a Map, including functions, objects, and any primitive.
2. The keys in Map are ordered while keys added to Object are not. Thus, when iterating over it, a Map object returns keys in order of insertion.
3. You can get the size of a Map easily with the size property, while the number of properties in an Object must be determined manually.
4. A Map is an iterable and can thus be directly iterated, whereas iterating over an Object requires obtaining its keys in some fashion and iterating over them.
5. An Object has a prototype, so there are default keys in the map that could collide with your keys if you're not careful. As of ES5 this can be bypassed by using map = Object.create(null), but this is seldom done.
6. A Map may perform better in scenarios involving frequent addition and removal of key pairs.

Q:: What is the difference between == and === operators  
A:: JavaScript provides both strict(===, !==) and type-converting(==, !=) equality comparison. The strict operators take type of variable in consideration, while non-strict operators make type correction/conversion based upon values of variables. The strict operators follow the below conditions for different types,

1. Two strings are strictly equal when they have the same sequence of characters, same length, and same characters in corresponding positions.
2. Two numbers are strictly equal when they are numerically equal. i.e, Having the same number value.
   There are two special cases in this,
   1. NaN is not equal to anything, including NaN.
   2. Positive and negative zeros are equal to one another.
3. Two Boolean operands are strictly equal if both are true or both are false.
4. Two objects are strictly equal if they refer to the same Object.
5. Null and Undefined types are not equal with ===, but equal with ==. i.e,
   null===undefined --> false but null==undefined --> true
   Some of the example which covers the above cases,
   ```javascript
   0 == false   // true
   0 === false  // false
   1 == "1"     // true
   1 === "1"    // false
   null == undefined // true
   null === undefined // false
   '0' == false // true
   '0' === false // false
   []==[] or []===[] //false, refer different objects in memory
   {}=={} or {}==={} //false, refer different objects in memory
   ```

Q:: What are lambda or arrow functions  
A:: An arrow function is a shorter syntax for a function expression and does not have its own **this, arguments, super, or new.target**. These functions are best suited for non-method functions, and they cannot be used as constructors.

Q:: What is a first class function  
A:: In Javascript, functions are first class objects. First-class functions means when functions in that language are treated like any other variable.  
For example, in such a language, a function can be passed as an argument to other functions, can be returned by another function and can be assigned as a value to a variable. For example, in the below example, handler functions assigned to a listener

```javascript
const handler = () => console.log("This is a click handler function");
document.addEventListener("click", handler);
```

Q:: What is a first order function  
A:: First-order function is a function that doesn’t accept another function as an argument and doesn’t return a function as its return value.

```javascript
const firstOrder = () => console.log("I am a first order function!");
```

Q:: What is a higher order function  
A:: Higher-order function is a function that accepts another function as an argument or returns a function as a return value or both.

```javascript
const firstOrderFunc = () => console.log("Hello, I am a First order function");
const higherOrder = (ReturnFirstOrderFunc) => ReturnFirstOrderFunc();
higherOrder(firstOrderFunc);
```

Q:: What is a unary function  
A:: Unary function (i.e. monadic) is a function that accepts exactly one argument. It stands for a single argument accepted by a function.  
Let us take an example of unary function,

```javascript
const unaryFunction = (a) => console.log(a + 10); // Add 10 to the given argument and display the value
```

Q:: What is the currying function  
A:: Currying is the process of taking a function with multiple arguments and turning it into a sequence of functions each with only a single argument. Currying is named after a mathematician **Haskell Curry**. By applying currying, a n-ary function turns it into a unary function.  
Let's take an example of n-ary function and how it turns into a currying function,

```javascript
const multiArgFunction = (a, b, c) => a + b + c;
console.log(multiArgFunction(1, 2, 3)); // 6
const curryUnaryFunction = (a) => (b) => (c) => a + b + c;
curryUnaryFunction(1); // returns a function: b => c =>  1 + b + c
curryUnaryFunction(1)(2); // returns a function: c => 3 + c
curryUnaryFunction(1)(2)(3); // returns the number 6
```

Curried functions are great to improve **code reusability** and **functional composition**.

Q:: What is a pure function  
A:: A **Pure function** is a function where the return value is only determined by its arguments without any side effects. i.e, If you call a function with the same arguments 'n' number of times and 'n' number of places in the application then it will always return the same value.  
Let's take an example to see the difference between pure and impure functions,

```javascript
//Impure
let numberArray = [];
const impureAddNumber = (number) => numberArray.push(number);
//Pure
const pureAddNumber = (number) => (argNumberArray) =>
  argNumberArray.concat([number]);
//Display the results
console.log(impureAddNumber(6)); // returns 1
console.log(numberArray); // returns [6]
console.log(pureAddNumber(7)(numberArray)); // returns [6, 7]
console.log(numberArray); // returns [6]
```

As per the above code snippets, the **Push** function is impure itself by altering the array and returning a push number index independent of the parameter value. . Whereas **Concat** on the other hand takes the array and concatenates it with the other array producing a whole new array without side effects. Also, the return value is a concatenation of the previous array.
Remember that Pure functions are important as they simplify unit testing without any side effects and no need for dependency injection. They also avoid tight coupling and make it harder to break your application by not having any side effects. These principles are coming together with **Immutability** concept of ES6 by giving preference to **const** over **let** usage.

Q:: What is the purpose of the let keyword  
A:: The `let` statement declares a **block scope local variable**. Hence the variables defined with let keyword are limited in scope to the block, statement, or expression on which it is used. Whereas variables declared with the `var` keyword used to define a variable globally, or locally to an entire function regardless of block scope.  
Let's take an example to demonstrate the usage,

```javascript
let counter = 30;
if (counter === 30) {
  let counter = 31;
  console.log(counter); // 31
}
console.log(counter); // 30 (because the variable in if block won't exist here)
```

Q:: What is the difference between let and var  
A:: You can list out the differences in a tabular format

| var                                                   | let                         |
| ----------------------------------------------------- | --------------------------- |
| It is been available from the beginning of JavaScript | Introduced as part of ES6   |
| It has function scope                                 | It has block scope          |
| Variables will be hoisted                             | Hoisted but not initialized |

Let's take an example to see the difference,

```javascript
function userDetails(username) {
  if (username) {
    console.log(salary); // undefined due to hoisting
    console.log(age); // ReferenceError: Cannot access 'age' before initialization
    let age = 30;
    var salary = 10000;
  }
  console.log(salary); //10000 (accessible due to function scope)
  console.log(age); //error: age is not defined(due to block scope)
}
userDetails("John");
```

Q:: What is the reason to choose the name let as a keyword  
A:: `let` is a mathematical statement that was adopted by early programming languages like **Scheme** and **Basic**. It has been borrowed from dozens of other languages that use `let` already as a traditional keyword as close to `var` as possible.

Q:: How do you redeclare variables in switch block without an error  
A:: If you try to redeclare variables in a `switch block` then it will cause errors because there is only one block. For example, the below code block throws a syntax error as below,

```javascript
let counter = 1;
switch (x) {
  case 0:
    let name;
    break;
  case 1:
    let name; // SyntaxError for redeclaration.
    break;
}
```

To avoid this error, you can create a nested block inside a case clause and create a new block scoped lexical environment.

```javascript
let counter = 1;
switch (x) {
  case 0: {
    let name;
    break;
  }
  case 1: {
    let name; // No SyntaxError for redeclaration.
    break;
  }
}
```

Q:: What is the Temporal Dead Zone  
A:: The Temporal Dead Zone is a behavior in JavaScript that occurs when declaring a variable with the let and const keywords, but not with var. In ECMAScript 6, accessing a `let` or `const` variable before its declaration (within its scope) causes a ReferenceError. The time span when that happens, between the creation of a variable’s binding and its declaration, is called the temporal dead zone.  
Let's see this behavior with an example,

```javascript
function somemethod() {
  console.log(counter1); // undefined
  console.log(counter2); // ReferenceError
  var counter1 = 1;
  let counter2 = 2;
}
```

Q:: What is IIFE(Immediately Invoked Function Expression)  
A:: IIFE (Immediately Invoked Function Expression) is a JavaScript function that runs as soon as it is defined. The signature of it would be as below,

```javascript
(function () {
  // logic here
})();
```

The primary reason to use an IIFE is to obtain data privacy because any variables declared within the IIFE cannot be accessed by the outside world. i.e, If you try to access variables with IIFE then it throws an error as below,

```javascript
(function () {
  var message = "IIFE";
  console.log(message);
})();
console.log(message); //Error: message is not defined
```

Q:: How do you decode or encode a URL in JavaScript?  
A:: `encodeURI()` function is used to encode an URL. This function requires a URL string as a parameter and return that encoded string.  
`decodeURI()` function is used to decode an URL. This function requires an encoded URL string as parameter and return that decoded string.  
**Note:** If you want to encode characters such as `/ ? : @ & = + $ #` then you need to use `encodeURIComponent()`.

```javascript
let uri = "employeeDetails?name=john&occupation=manager";
let encoded_uri = encodeURI(uri);
let decoded_uri = decodeURI(encoded_uri);
```

Q:: What is memoization  
A:: Memoization is a programming technique which attempts to increase a function’s performance by caching its previously computed results. Each time a memoized function is called, its parameters are used to index the cache. If the data is present, then it can be returned, without executing the entire function. Otherwise the function is executed and then the result is added to the cache.  
Let's take an example of adding function with memoization,

```javascript
const memoizAddition = () => {
  let cache = {};
  return (value) => {
    if (value in cache) {
      console.log("Fetching from cache");
      return cache[value]; // Here, cache.value cannot be used as property name starts with the number which is not a valid JavaScript  identifier. Hence, can only be accessed using the square bracket notation.
    } else {
      console.log("Calculating result");
      let result = value + 20;
      cache[value] = result;
      return result;
    }
  };
};
// returned function from memoizAddition
const addition = memoizAddition();
console.log(addition(20)); //output: 40 calculated
console.log(addition(20)); //output: 40 cached
```

Q:: What is Hoisting  
A:: Hoisting is a JavaScript mechanism where variables, function declarations and classes are moved to the top of their scope before code execution. Remember that JavaScript only hoists declarations, not initialisation.  
Let's take a simple example of variable hoisting,

```javascript
console.log(message); //output : undefined
var message = "The variable Has been hoisted";
```

The above code looks like as below to the interpreter,

```javascript
var message;
console.log(message);
message = "The variable Has been hoisted";
```

In the same fashion, function declarations are hoisted too

```javascript
message("Good morning"); //Good morning
function message(name) {
  console.log(name);
}
```

This hoisting makes functions to be safely used in code before they are declared.

Q:: What are classes in ES6  
A:: In ES6, Javascript classes are primarily syntactic sugar over JavaScript’s existing prototype-based inheritance.  
For example, the prototype based inheritance written in function expression as below,

```javascript
function Bike(model, color) {
  this.model = model;
  this.color = color;
}
Bike.prototype.getDetails = function () {
  return this.model + " bike has" + this.color + " color";
};
```

Whereas ES6 classes can be defined as an alternative

```javascript
class Bike {
  constructor(color, model) {
    this.color = color;
    this.model = model;
  }
  getDetails() {
    return this.model + " bike has" + this.color + " color";
  }
}
```

Q:: What are closures  
A:: A closure is the combination of a function and the lexical environment within which that function was declared. i.e, It is an inner function that has access to the outer or enclosing function’s variables. The closure has three scope chains

1. Own scope where variables defined between its curly brackets
2. Outer function’s variables
3. Global variables
   Let's take an example of closure concept,

```javascript
function Welcome(name) {
  var greetingInfo = function (message) {
    console.log(message + " " + name);
  };
  return greetingInfo;
}
var myFunction = Welcome("John");
myFunction("Welcome "); //Output: Welcome John
myFunction("Hello Mr."); //output: Hello Mr.John
```

As per the above code, the inner function(i.e, greetingInfo) has access to the variables in the outer function scope(i.e, Welcome) even after the outer function has returned.

Q:: What are modules  
A:: Modules refer to small units of independent, reusable code and also act as the foundation of many JavaScript design patterns. Most of the JavaScript modules export an object literal, a function, or a constructor

Q:: Why do you need modules  
A:: Below are the list of benefits using modules in javascript ecosystem

1. Maintainability
2. Reusability
3. Namespacing

Q:: What is scope in javascript  
A:: Scope is the accessibility of variables, functions, and objects in some particular part of your code during runtime. In other words, scope determines the visibility of variables and other resources in areas of your code.

Q:: What is a service worker  
A:: A Service worker is basically a script (JavaScript file) that runs in the background, separate from a web page and provides features that don't need a web page or user interaction. Some of the major features of service workers are Rich offline experiences(offline first web application development), periodic background syncs, push notifications, intercept and handle network requests and programmatically managing a cache of responses.

Q:: How do you manipulate DOM using a service worker  
A:: Service worker can't access the DOM directly. But it can communicate with the pages it controls by responding to messages sent via the `postMessage` interface, and those pages can manipulate the DOM.

Q:: How do you reuse information across service worker restarts  
A:: The problem with service worker is that it gets terminated when not in use, and restarted when it's next needed, so you cannot rely on global state within a service worker's `onfetch` and `onmessage` handlers. In this case, service workers will have access to IndexedDB API in order to persist and reuse across restarts.

Q:: What is IndexedDB  
A:: IndexedDB is a low-level API for client-side storage of larger amounts of structured data, including files/blobs. This API uses indexes to enable high-performance searches of this data.

Q:: What is web storage  
A:: Web storage is an API that provides a mechanism by which browsers can store key/value pairs locally within the user's browser, in a much more intuitive fashion than using cookies. The web storage provides two mechanisms for storing data on the client.

1. **Local storage:** It stores data for current origin with no expiration date.
2. **Session storage:** It stores data for one session and the data is lost when the browser tab is closed.

Q:: What is a post message  
A:: Post message is a method that enables cross-origin communication between Window objects.(i.e, between a page and a pop-up that it spawned, or between a page and an iframe embedded within it). Generally, scripts on different pages are allowed to access each other if and only if the pages follow same-origin policy(i.e, pages share the same protocol, port number, and host).

Q:: What is a Cookie  
A:: A cookie is a piece of data that is stored on your computer to be accessed by your browser. Cookies are saved as key/value pairs.  
For example, you can create a cookie named username as below,

```javascript
document.cookie = "username=John";
```

![cookie](../images/cookie.png)

Q:: Why do you need a Cookie  
A:: Cookies are used to remember information about the user profile(such as username). It basically involves two steps,

1. When a user visits a web page, the user profile can be stored in a cookie.
2. Next time the user visits the page, the cookie remembers the user profile.

Q:: What are the options in a cookie  
A:: There are few below options available for a cookie,

1. By default, the cookie is deleted when the browser is closed but you can change this behavior by setting expiry date (in UTC time).

```javascript
document.cookie = "username=John; expires=Sat, 8 Jun 2019 12:00:00 UTC";
```

1. By default, the cookie belongs to a current page. But you can tell the browser what path the cookie belongs to using a path parameter.

```javascript
document.cookie = "username=John; path=/services";
```

Q:: How do you delete a cookie  
A:: You can delete a cookie by setting the expiry date as a passed date. You don't need to specify a cookie value in this case.  
For example, you can delete a username cookie in the current page as below.

```javascript
document.cookie = "username=; expires=Fri, 07 Jun 2019 00:00:00 UTC; path=/;";
```

**Note:** You should define the cookie path option to ensure that you delete the right cookie. Some browsers doesn't allow to delete a cookie unless you specify a path parameter.

Q:: What are the differences between cookie, local storage and session storage  
A:: Below are some of the differences between cookie, local storage and session storage,

| Feature                           | Cookie                             | Local storage    | Session storage     |
| --------------------------------- | ---------------------------------- | ---------------- | ------------------- |
| Accessed on client or server side | Both server-side & client-side     | client-side only | client-side only    |
| Lifetime                          | As configured using Expires option | until deleted    | until tab is closed |
| SSL support                       | Supported                          | Not supported    | Not supported       |
| Maximum data size                 | 4KB                                | 5 MB             | 5MB                 |

Q:: What is the main difference between localStorage and sessionStorage  
A:: LocalStorage is the same as SessionStorage but it persists the data even when the browser is closed and reopened(i.e it has no expiration time) whereas in sessionStorage data gets cleared when the page session ends.

Q:: How do you access web storage  
A:: The Window object implements the `WindowLocalStorage` and `WindowSessionStorage` objects which has `localStorage`(window.localStorage) and `sessionStorage`(window.sessionStorage) properties respectively. These properties create an instance of the Storage object, through which data items can be set, retrieved and removed for a specific domain and storage type (session or local).  
For example, you can read and write on local storage objects as below

```javascript
localStorage.setItem("logo", document.getElementById("logo").value);
localStorage.getItem("logo");
```

Q:: What are the methods available on session storage  
A:: The session storage provided methods for reading, writing and clearing the session data

```javascript
// Save data to sessionStorage
sessionStorage.setItem("key", "value");
// Get saved data from sessionStorage
let data = sessionStorage.getItem("key");
// Remove saved data from sessionStorage
sessionStorage.removeItem("key");
// Remove all saved data from sessionStorage
sessionStorage.clear();
```

Q:: What is a storage event and its event handler  
A:: The StorageEvent is an event that fires when a storage area has been changed in the context of another document. Whereas onstorage property is an EventHandler for processing storage events.  
The syntax would be as below

```javascript
window.onstorage = functionRef;
```

Let's take the example usage of onstorage event handler which logs the storage key and it's values

```javascript
window.onstorage = function (e) {
  console.log(
    "The " +
      e.key +
      " key has been changed from " +
      e.oldValue +
      " to " +
      e.newValue +
      ".",
  );
};
```

Q:: Why do you need web storage  
A:: Web storage is more secure, and large amounts of data can be stored locally, without affecting website performance. Also, the information is never transferred to the server. Hence this is a more recommended approach than Cookies.

Q:: How do you check web storage browser support  
A:: You need to check browser support for localStorage and sessionStorage before using web storage,

```javascript
if (typeof Storage !== "undefined") {
  // Code for localStorage/sessionStorage.
} else {
  // Sorry! No Web Storage support..
}
```

Q:: How do you check web workers browser support  
A:: You need to check browser support for web workers before using it

```javascript
if (typeof Worker !== "undefined") {
  // code for Web worker support.
} else {
  // Sorry! No Web Worker support..
}
```

Q:: Give an example of a web worker  
A:: You need to follow below steps to start using web workers for counting example

1. Create a Web Worker File: You need to write a script to increment the count value. Let's name it as counter.js

```javascript
let i = 0;
function timedCount() {
  i = i + 1;
  postMessage(i);
  setTimeout("timedCount()", 500);
}
timedCount();
```

Here postMessage() method is used to post a message back to the HTML page

1. Create a Web Worker Object: You can create a web worker object by checking for browser support. Let's name this file as web_worker_example.js

```javascript
if (typeof w == "undefined") {
  w = new Worker("counter.js");
}
```

and we can receive messages from web worker

```javascript
w.onmessage = function (event) {
  document.getElementById("message").innerHTML = event.data;
};
```

1. Terminate a Web Worker:
   Web workers will continue to listen for messages (even after the external script is finished) until it is terminated. You can use the terminate() method to terminate listening to the messages.

```javascript
w.terminate();
```

1. Reuse the Web Worker: If you set the worker variable to undefined you can reuse the code

```javascript
w = undefined;
```

Q:: What are the restrictions of web workers on DOM  
A:: WebWorkers don't have access to below javascript objects since they are defined in an external files

1. Window object
2. Document object
3. Parent object

Q:: What is a promise  
A:: A promise is an object that may produce a single value some time in the future with either a resolved value or a reason that it’s not resolved(for example, network error). It will be in one of the 3 possible states: fulfilled, rejected, or pending.  
The syntax of Promise creation looks like below,

```javascript
const promise = new Promise(function (resolve, reject) {
  // promise description
});
```

The usage of a promise would be as below,

```javascript
const promise = new Promise(
  (resolve) => {
    setTimeout(() => {
      resolve("I'm a Promise!");
    }, 5000);
  },
  (reject) => {},
);
promise.then((value) => console.log(value));
```

The action flow of a promise will be as below,
![promises](../images/promises.png)

Q:: Why do you need a promise  
A:: Promises are used to handle asynchronous operations. They provide an alternative approach for callbacks by reducing the callback hell and writing the cleaner code.

Q:: What are the three states of promise  
A:: Promises have three states:

1. **Pending:** This is an initial state of the Promise before an operation begins
2. **Fulfilled:** This state indicates that the specified operation was completed.
3. **Rejected:** This state indicates that the operation did not complete. In this case an error value will be thrown.

Q:: What is a callback function  
A:: A callback function is a function passed into another function as an argument. This function is invoked inside the outer function to complete an action.  
Let's take a simple example of how to use callback function

```javascript
function callbackFunction(name) {
  console.log("Hello " + name);
}
function outerFunction(callback) {
  let name = prompt("Please enter your name.");
  callback(name);
}
outerFunction(callbackFunction);
```

Q:: Why do we need callbacks  
A:: The callbacks are needed because javascript is an event driven language. That means instead of waiting for a response javascript will keep executing while listening for other events.  
Let's take an example with the first function invoking an API call(simulated by setTimeout) and the next function which logs the message.

```javascript
function firstFunction() {
  // Simulate a code delay
  setTimeout(function () {
    console.log("First function called");
  }, 1000);
}
function secondFunction() {
  console.log("Second function called");
}
firstFunction();
secondFunction();
Output;
// Second function called
// First function called
```

As observed from the output, javascript didn't wait for the response of the first function and the remaining code block got executed. So callbacks are used in a way to make sure that certain code doesn’t execute until the other code finishes execution.

Q:: What is a callback hell  
A:: Callback Hell is an anti-pattern with multiple nested callbacks which makes code hard to read and debug when dealing with asynchronous logic. The callback hell looks like below,

```javascript
async1(function(){
async2(function(){
async3(function(){
async4(function(){
....
});
});
});
});
```

Q:: What are server-sent events  
A:: Server-sent events (SSE) is a server push technology enabling a browser to receive automatic updates from a server via HTTP connection without resorting to polling. These are a one way communications channel - events flow from server to client only. This has been used in Facebook/Twitter updates, stock price updates, news feeds etc.

Q:: How do you receive server-sent event notifications  
A:: The EventSource object is used to receive server-sent event notifications. For example, you can receive messages from server as below,

```javascript
if (typeof EventSource !== "undefined") {
  var source = new EventSource("sse_generator.js");
  source.onmessage = function (event) {
    document.getElementById("output").innerHTML += event.data + "<br>";
  };
}
```

Q:: How do you check browser support for server-sent events  
A:: You can perform browser support for server-sent events before using it as below,

```javascript
if (typeof EventSource !== "undefined") {
  // Server-sent events supported. Let's have some code here!
} else {
  // No server-sent events supported
}
```

Q:: What are the events available for server sent events  
A:: Below are the list of events available for server sent events

| Event     | Description                                          |
| --------- | ---------------------------------------------------- |
| onopen    | It is used when a connection to the server is opened |
| onmessage | This event is used when a message is received        |
| onerror   | It happens when an error occurs                      |

Q:: What are the main rules of promise  
A:: A promise must follow a specific set of rules:

1. A promise is an object that supplies a standard-compliant `.then()` method
2. A pending promise may transition into either fulfilled or rejected state
3. A fulfilled or rejected promise is settled and it must not transition into any other state.
4. Once a promise is settled, the value must not change.

Q:: What is callback in callback  
A:: You can nest one callback inside in another callback to execute the actions sequentially one by one. This is known as callbacks in callbacks.

```javascript
loadScript("/script1.js", function (script) {
  console.log("first script is loaded");
  loadScript("/script2.js", function (script) {
    console.log("second script is loaded");
    loadScript("/script3.js", function (script) {
      console.log("third script is loaded");
      // after all scripts are loaded
    });
  });
});
```

Q:: What is promise chaining  
A:: The process of executing a sequence of asynchronous tasks one after another using promises is known as Promise chaining. Let's take an example of promise chaining for calculating the final result,

```javascript
new Promise(function (resolve, reject) {
  setTimeout(() => resolve(1), 1000);
})
  .then(function (result) {
    console.log(result); // 1
    return result * 2;
  })
  .then(function (result) {
    console.log(result); // 2
    return result * 3;
  })
  .then(function (result) {
    console.log(result); // 6
    return result * 4;
  });
```

In the above handlers, the result is passed to the chain of .then() handlers with the below work flow,

1. The initial promise resolves in 1 second,
2. After that `.then` handler is called by logging the result(1) and then return a promise with the value of result \* 2.
3. After that the value passed to the next `.then` handler by logging the result(2) and return a promise with result \* 3.
4. Finally the value passed to the last `.then` handler by logging the result(6) and return a promise with result \* 4.

Q:: What is promise.all  
A:: Promise.all is a promise that takes an array of promises as an input (an iterable), and it gets resolved when all the promises get resolved or any one of them gets rejected. For example, the syntax of promise.all method is below,

```javascript
Promise.all([Promise1, Promise2, Promise3]) .then(result) => {   console.log(result) }) .catch(error => console.log(`Error in promises ${error}`))
```

**Note:** Remember that the order of the promises(output the result) is maintained as per input order.

Q:: What is the purpose of the race method in promise  
A:: Promise.race() method will return the promise instance which is firstly resolved or rejected. Let's take an example of race() method where promise2 is resolved first

```javascript
var promise1 = new Promise(function (resolve, reject) {
  setTimeout(resolve, 500, "one");
});
var promise2 = new Promise(function (resolve, reject) {
  setTimeout(resolve, 100, "two");
});
Promise.race([promise1, promise2]).then(function (value) {
  console.log(value); // "two" // Both promises will resolve, but promise2 is faster
});
```

Q:: What is a strict mode in javascript  
A:: Strict Mode is a new feature in ECMAScript 5 that allows you to place a program, or a function, in a “strict” operating context. This way it prevents certain actions from being taken and throws more exceptions. The literal expression `"use strict";` instructs the browser to use the javascript code in the Strict mode.

Q:: Why do you need strict mode  
A:: Strict mode is useful to write "secure" JavaScript by notifying "bad syntax" into real errors. For example, it eliminates accidentally creating a global variable by throwing an error and also throws an error for assignment to a non-writable property, a getter-only property, a non-existing property, a non-existing variable, or a non-existing object.

Q:: How do you declare strict mode  
A:: The strict mode is declared by adding "use strict"; to the beginning of a script or a function.  
If declared at the beginning of a script, it has global scope.

```javascript
"use strict";
x = 3.14; // This will cause an error because x is not declared
```

and if you declare inside a function, it has local scope

```javascript
x = 3.14; // This will not cause an error.
myFunction();
function myFunction() {
  "use strict";
  y = 3.14; // This will cause an error
}
```

Q:: What is the purpose of double exclamation  
A:: The double exclamation or negation(!!) ensures the resulting type is a boolean. If it was falsey (e.g. 0, null, undefined, etc.), it will be false, otherwise, it will be true.  
For example, you can test IE version using this expression as below,

```javascript
let isIE8 = false;
isIE8 = !!navigator.userAgent.match(/MSIE 8.0/);
console.log(isIE8); // returns true or false
```

If you don't use this expression then it returns the original value.

```javascript
console.log(navigator.userAgent.match(/MSIE 8.0/)); // returns either an Array or null
```

**Note:** The expression !! is not an operator, but it is just twice of ! operator.

Q:: What is the purpose of the delete operator  
A:: The delete keyword is used to delete the property as well as its value.

```javascript
var user = { name: "John", age: 20 };
delete user.age;
console.log(user); // {name: "John"}
```

Q:: What is typeof operator  
A:: You can use the JavaScript typeof operator to find the type of a JavaScript variable. It returns the type of a variable or an expression.

```javascript
typeof "John Abraham"; // Returns "string"
typeof (1 + 2); // Returns "number"
typeof [1, 2, 3]; // Returns "object" because all arrays are also objects
```

Q:: What is undefined property  
A:: The undefined property indicates that a variable has not been assigned a value, or declared but not initialized at all. The type of undefined value is undefined too.

```javascript
var user; // Value is undefined, type is undefined
console.log(typeof user); //undefined
```

Any variable can be emptied by setting the value to undefined.

```javascript
user = undefined;
```

Q:: What is null value  
A:: The value null represents the intentional absence of any object value. It is one of JavaScript's primitive values. The type of null value is object.  
You can empty the variable by setting the value to null.

```javascript
var user = null;
console.log(typeof user); //object
```

Q:: What is the difference between null and undefined  
A:: Below are the main differences between null and undefined,

| Null                                                                                            | Undefined                                                                                               |
| ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| It is an assignment value which indicates that variable points to no object.                    | It is not an assignment value where a variable has been declared but has not yet been assigned a value. |
| Type of null is object                                                                          | Type of undefined is undefined                                                                          |
| The null value is a primitive value that represents the null, empty, or non-existent reference. | The undefined value is a primitive value used when a variable has not been assigned a value.            |
| Indicates the absence of a value for a variable                                                 | Indicates absence of variable itself                                                                    |
| Converted to zero (0) while performing primitive operations                                     | Converted to NaN while performing primitive operations                                                  |

Q:: What is eval  
A:: The eval() function evaluates JavaScript code represented as a string. The string can be a JavaScript expression, variable, statement, or sequence of statements.

```javascript
console.log(eval("1 + 2")); //  3
```

Q:: What is the difference between window and document  
A:: Below are the main differences between window and document,

| Window                                                                        | Document                                                                                      |
| ----------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| It is the root level element in any web page                                  | It is the direct child of the window object. This is also known as Document Object Model(DOM) |
| By default window object is available implicitly in the page                  | You can access it via window.document or document.                                            |
| It has methods like alert(), confirm() and properties like document, location | It provides methods like getElementById, getElementsByTagName, createElement etc              |

Q:: How do you access history in javascript  
A:: The window.history object contains the browser's history. You can load previous and next URLs in the history using back() and next() methods.

```javascript
function goBack() {
  window.history.back();
}
function goForward() {
  window.history.forward();
}
```

**Note:** You can also access history without window prefix.

Q:: How do you detect caps lock key turned on or not  
A:: The `mouseEvent getModifierState()` is used to return a boolean value that indicates whether the specified modifier key is activated or not. The modifiers such as CapsLock, ScrollLock and NumLock are activated when they are clicked, and deactivated when they are clicked again.  
Let's take an input element to detect the CapsLock on/off behavior with an example,

```html
<input type="password" onmousedown="enterInput(event)" />
<p id="feedback"></p>
<script>
  function enterInput(e) {
    var flag = e.getModifierState("CapsLock");
    if (flag) {
      document.getElementById("feedback").innerHTML = "CapsLock activated";
    } else {
      document.getElementById("feedback").innerHTML = "CapsLock not activated";
    }
  }
</script>
```

Q:: What is isNaN  
A:: The isNaN() function is used to determine whether a value is an illegal number (Not-a-Number) or not. i.e, This function returns true if the value equates to NaN. Otherwise it returns false.

```javascript
isNaN("Hello"); //true
isNaN("100"); //false
```

Q:: What are the differences between undeclared and undefined variables  
A:: Below are the major differences between undeclared(not defined) and undefined variables,

| undeclared                                                                                  | undefined                                                                              |
| ------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| These variables do not exist in a program and are not declared                              | These variables declared in the program but have not assigned any value                |
| If you try to read the value of an undeclared variable, then a runtime error is encountered | If you try to read the value of an undefined variable, an undefined value is returned. |

Q:: What are global variables  
A:: Global variables are those that are available throughout the length of the code without any scope. The var keyword is used to declare a local variable but if you omit it then it will become global variable

```javascript
msg = "Hello"; // var is missing, it becomes global variable
```

Q:: What are the problems with global variables  
A:: The problem with global variables is the conflict of variable names of local and global scope. It is also difficult to debug and test the code that relies on global variables.

Q:: What is NaN property  
A:: The NaN property is a global property that represents "Not-a-Number" value. i.e, It indicates that a value is not a legal number. It is very rare to use NaN in a program but it can be used as return value for few cases

```javascript
Math.sqrt(-1);
parseInt("Hello");
```

Q:: What is the purpose of isFinite function  
A:: The isFinite() function is used to determine whether a number is a finite, legal number. It returns false if the value is +infinity, -infinity, or NaN (Not-a-Number), otherwise it returns true.

```javascript
isFinite(Infinity); // false
isFinite(NaN); // false
isFinite(-Infinity); // false
isFinite(100); // true
```

Q:: What is an event flow  
A:: Event flow is the order in which event is received on the web page. When you click an element that is nested in various other elements, before your click actually reaches its destination, or target element, it must trigger the click event for each of its parent elements first, starting at the top with the global window object.  
There are two ways of event flow

1. Top to Bottom(Event Capturing)
2. Bottom to Top (Event Bubbling)

Q:: What is event bubbling  
A:: Event bubbling is a type of event propagation where the event first triggers on the innermost target element, and then successively triggers on the ancestors (parents) of the target element in the same nesting hierarchy till it reaches the outermost DOM element.

Q:: What is event capturing  
A:: Event capturing is a type of event propagation where the event is first captured by the outermost element, and then successively triggers on the descendants (children) of the target element in the same nesting hierarchy till it reaches the innermost DOM element.

Q:: How do you submit a form using JavaScript  
A:: You can submit a form using `document.forms[0].submit()`. All the form input's information is submitted using onsubmit event handler

```javascript
function submit() {
  document.forms[0].submit();
}
```

Q:: How do you find operating system details  
A:: The window.navigator object contains information about the visitor's browser OS details. Some of the OS properties are available under platform property,

```javascript
console.log(navigator.platform);
```

Q:: What is the difference between document load and DOMContentLoaded events  
A:: The `DOMContentLoaded` event is fired when the initial HTML document has been completely loaded and parsed, without waiting for assets(stylesheets, images, and subframes) to finish loading. Whereas The load event is fired when the whole page has loaded, including all dependent resources(stylesheets, images).

Q:: What is the difference between native, host and user objects  
A:: `Native objects` are objects that are part of the JavaScript language defined by the ECMAScript specification. For example, String, Math, RegExp, Object, Function etc core objects defined in the ECMAScript spec.  
`Host objects` are objects provided by the browser or runtime environment (Node). For example, window, XmlHttpRequest, DOM nodes etc are considered as host objects.  
`User objects` are objects defined in the javascript code. For example, User objects created for profile information.

Q:: What are the tools or techniques used for debugging JavaScript code  
A:: You can use below tools or techniques for debugging javascript

1. Chrome Devtools
2. debugger statement
3. Good old console.log statement

Q:: What are the pros and cons of promises over callbacks  
A:: Below are the list of pros and cons of promises over callbacks,  
**Pros:**

1. It avoids callback hell which is unreadable
2. Easy to write sequential asynchronous code with .then()
3. Easy to write parallel asynchronous code with Promise.all()
4. Solves some of the common problems of callbacks(call the callback too late, too early, many times and swallow errors/exceptions)
   **Cons:**
5. It makes little complex code
6. You need to load a polyfill if ES6 is not supported

Q:: What is the difference between an attribute and a property  
A:: Attributes are defined on the HTML markup whereas properties are defined on the DOM. For example, the below HTML element has 2 attributes type and value,

```javascript
<input type="text" value="Name:">
```

You can retrieve the attribute value as below,

```javascript
const input = document.querySelector("input");
console.log(input.getAttribute("value")); // Good morning
console.log(input.value); // Good morning
```

And after you change the value of the text field to "Good evening", it becomes like

```javascript
console.log(input.getAttribute("value")); // Good evening
console.log(input.value); // Good evening
```

Q:: What is same-origin policy  
A:: The same-origin policy is a policy that prevents JavaScript from making requests across domain boundaries. An origin is defined as a combination of URI scheme, hostname, and port number. If you enable this policy then it prevents a malicious script on one page from obtaining access to sensitive data on another web page using Document Object Model(DOM).

Q:: What is the purpose of void 0  
A:: Void(0) is used to prevent the page from refreshing. This will be helpful to eliminate the unwanted side-effect, because it will return the undefined primitive value. It is commonly used for HTML documents that use href="JavaScript:Void(0);" within an `<a>` element. i.e, when you click a link, the browser loads a new page or refreshes the same page. But this behavior will be prevented using this expression.  
For example, the below link notify the message without reloading the page

```javascript
<a href="JavaScript:void(0);" onclick="alert('Well done!')">
  Click Me!
</a>
```

Q:: Is JavaScript a compiled or interpreted language  
A:: JavaScript is an interpreted language, not a compiled language. An interpreter in the browser reads over the JavaScript code, interprets each line, and runs it. Nowadays modern browsers use a technology known as Just-In-Time (JIT) compilation, which compiles JavaScript to executable bytecode just as it is about to run.

Q:: Is JavaScript a case-sensitive language  
A:: Yes, JavaScript is a case sensitive language. The language keywords, variables, function & object names, and any other identifiers must always be typed with a consistent capitalization of letters.

Q:: Is there any relation between Java and JavaScript  
A:: No, they are entirely two different programming languages and have nothing to do with each other. But both of them are Object Oriented Programming languages and like many other languages, they follow similar syntax for basic features(if, else, for, switch, break, continue etc).

Q:: What are events  
A:: Events are "things" that happen to HTML elements. When JavaScript is used in HTML pages, JavaScript can `react` on these events. Some of the examples of HTML events are,

1. Web page has finished loading
2. Input field was changed
3. Button was clicked
   Let's describe the behavior of click event for button element,

```javascript
<!doctype html>
<html>
<head>
<script>
function greeting() {
alert('Hello! Good morning');
}
</script>
</head>
<body>
<button type="button" onclick="greeting()">Click me</button>
</body>
</html>
```

Q:: Who created javascript  
A:: JavaScript was created by Brendan Eich in 1995 during his time at Netscape Communications. Initially it was developed under the name `Mocha`, but later the language was officially called `LiveScript` when it first shipped in beta releases of Netscape.

Q:: What is the use of preventDefault method  
A:: The preventDefault() method cancels the event if it is cancelable, meaning that the default action or behaviour that belongs to the event will not occur. For example, prevent form submission when clicking on submit button and prevent opening the page URL when clicking on hyperlink are some common use cases.

```javascript
document.getElementById("link").addEventListener("click", function (event) {
  event.preventDefault();
});
```

**Note:** Remember that not all events are cancelable.

Q:: What is the use of stopPropagation method  
A:: The stopPropagation method is used to stop the event from bubbling up the event chain. For example, the below nested divs with stopPropagation method prevents default event propagation when clicking on nested div(Div1)

```javascript
<p>Click DIV1 Element</p>
<div onclick="secondFunc()">DIV 2
<div onclick="firstFunc(event)">DIV 1</div>
</div>
<script>
function firstFunc(event) {
alert("DIV 1");
event.stopPropagation();
}
function secondFunc() {
alert("DIV 2");
}
</script>
```

Q:: What are the steps involved in return false usage  
A:: The return false statement in event handlers performs the below steps,

1. First it stops the browser's default action or behaviour.
2. It prevents the event from propagating the DOM
3. Stops callback execution and returns immediately when called.

Q:: What is BOM  
A:: The Browser Object Model (BOM) allows JavaScript to "talk to" the browser. It consists of the objects navigator, history, screen, location and document which are children of the window. The Browser Object Model is not standardized and can change based on different browsers.  
![bom](../images/bom.png)

Q:: What is the use of setTimeout  
A:: The setTimeout() method is used to call a function or evaluate an expression after a specified number of milliseconds. For example, let's log a message after 2 seconds using setTimeout method,

```javascript
setTimeout(function () {
  console.log("Good morning");
}, 2000);
```

Q:: What is the use of setInterval  
A:: The setInterval() method is used to call a function or evaluate an expression at specified intervals (in milliseconds). For example, let's log a message after 2 seconds using setInterval method,

```javascript
setInterval(function () {
  console.log("Good morning");
}, 2000);
```

Q:: Why is JavaScript treated as Single threaded  
A:: JavaScript is a single-threaded language. Because the language specification does not allow the programmer to write code so that the interpreter can run parts of it in parallel in multiple threads or processes. Whereas languages like java, go, C++ can make multi-threaded and multi-process programs.

Q:: What is an event delegation  
A:: Event delegation is a technique for listening to events where you delegate a parent element as the listener for all of the events that happen inside it.  
For example, if you wanted to detect field changes in inside a specific form, you can use event delegation technique,

```javascript
var form = document.querySelector("#registration-form");
// Listen for changes to fields inside the form
form.addEventListener(
  "input",
  function (event) {
    // Log the field that was changed
    console.log(event.target);
  },
  false,
);
```

Q:: What is ECMAScript  
A:: ECMAScript is the scripting language that forms the basis of JavaScript. ECMAScript standardized by the ECMA International standards organization in the ECMA-262 and ECMA-402 specifications. The first edition of ECMAScript was released in 1997.

Q:: What is JSON  
A:: JSON (JavaScript Object Notation) is a lightweight format that is used for data interchanging. It is based on a subset of JavaScript language in the way objects are built in JavaScript.

Q:: What are the syntax rules of JSON  
A:: Below are the list of syntax rules of JSON

1. The data is in name/value pairs
2. The data is separated by commas
3. Curly braces hold objects
4. Square brackets hold arrays

Q:: What is the purpose JSON stringify  
A:: When sending data to a web server, the data has to be in a string format. You can achieve this by converting JSON object into a string using stringify() method.

```javascript
var userJSON = { name: "John", age: 31 };
var userString = JSON.stringify(userJSON);
console.log(userString); //"{"name":"John","age":31}"
```

Q:: How do you parse JSON string  
A:: When receiving the data from a web server, the data is always in a string format. But you can convert this string value to a javascript object using parse() method.

```javascript
var userString = '{"name":"John","age":31}';
var userJSON = JSON.parse(userString);
console.log(userJSON); // {name: "John", age: 31}
```

Q:: Why do you need JSON  
A:: When exchanging data between a browser and a server, the data can only be text. Since JSON is text only, it can easily be sent to and from a server, and used as a data format by any programming language.

Q:: What are PWAs  
A:: Progressive web applications (PWAs) are a type of mobile app delivered through the web, built using common web technologies including HTML, CSS and JavaScript. These PWAs are deployed to servers, accessible through URLs, and indexed by search engines.

Q:: What is the purpose of clearTimeout method  
A:: The clearTimeout() function is used in javascript to clear the timeout which has been set by setTimeout()function before that. i.e, The return value of setTimeout() function is stored in a variable and it’s passed into the clearTimeout() function to clear the timer.  
For example, the below setTimeout method is used to display the message after 3 seconds. This timeout can be cleared by the clearTimeout() method.

```javascript
<script>
var msg;
function greeting() {
alert('Good morning');
}
function start() {
msg =setTimeout(greeting, 3000);
}
function stop() {
clearTimeout(msg);
}
</script>
```

Q:: What is the purpose of clearInterval method  
A:: The clearInterval() function is used in javascript to clear the interval which has been set by setInterval() function. i.e, The return value returned by setInterval() function is stored in a variable and it’s passed into the clearInterval() function to clear the interval.  
For example, the below setInterval method is used to display the message for every 3 seconds. This interval can be cleared by the clearInterval() method.

```javascript
<script>
var msg;
function greeting() {
alert('Good morning');
}
function start() {
msg = setInterval(greeting, 3000);
}
function stop() {
clearInterval(msg);
}
</script>
```

Q:: How do you redirect new page in javascript  
A:: In vanilla javascript, you can redirect to a new page using the `location` property of window object. The syntax would be as follows,

```javascript
function redirect() {
  window.location.href = "newPage.html";
}
```

Q:: How do you check whether a string contains a substring  
A:: There are 3 possible ways to check whether a string contains a substring or not,

1. **Using includes:** ES6 provided `String.prototype.includes` method to test a string contains a substring

```javascript
var mainString = "hello",
  subString = "hell";
mainString.includes(subString);
```

1. **Using indexOf:** In an ES5 or older environment, you can use `String.prototype.indexOf` which returns the index of a substring. If the index value is not equal to -1 then it means the substring exists in the main string.

```javascript
var mainString = "hello",
  subString = "hell";
mainString.indexOf(subString) !== -1;
```

1. **Using RegEx:** The advanced solution is using Regular expression's test method(`RegExp.test`), which allows for testing for against regular expressions

```javascript
var mainString = "hello",
  regex = /hell/;
regex.test(mainString);
```

Q:: How do you validate an email in javascript  
A:: You can validate an email in javascript using regular expressions. It is recommended to do validations on the server side instead of the client side. Because the javascript can be disabled on the client side.

```javascript
function validateEmail(email) {
  var re =
    /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
  return re.test(String(email).toLowerCase());
}
```

The above regular expression accepts unicode characters.
Q:: How do you get the current url with javascript  
A:: You can use `window.location.href` expression to get the current url path and you can use the same expression for updating the URL too. You can also use `document.URL` for read-only purposes but this solution has issues in FF.

```javascript
console.log("location.href", window.location.href); // Returns full URL
```

Q:: What are the various url properties of location object  
A:: The below `Location` object properties can be used to access URL components of the page,

1. href - The entire URL
2. protocol - The protocol of the URL
3. host - The hostname and port of the URL
4. hostname - The hostname of the URL
5. port - The port number in the URL
6. pathname - The path name of the URL
7. search - The query portion of the URL
8. hash - The anchor portion of the URL

Q:: How do get query string values in javascript  
A:: You can use URLSearchParams to get query string values in javascript. Let's see an example to get the client code value from URL query string,

```javascript
const urlParams = new URLSearchParams(window.location.search);
const clientCode = urlParams.get("clientCode");
```

Q:: How do you check if a key exists in an object  
A:: You can check whether a key exists in an object or not using three approaches,

1. **Using in operator:** You can use the in operator whether a key exists in an object or not

```javascript
"key" in obj;
```

and If you want to check if a key doesn't exist, remember to use parenthesis,

```javascript
!("key" in obj);
```

1. **Using hasOwnProperty method:** You can use `hasOwnProperty` to particularly test for properties of the object instance (and not inherited properties)

```javascript
obj.hasOwnProperty("key"); // true
```

1. **Using undefined comparison:** If you access a non-existing property from an object, the result is undefined. Let’s compare the properties against undefined to determine the existence of the property.

```javascript
const user = {
  name: "John",
};
console.log(user.name !== undefined); // true
console.log(user.nickName !== undefined); // false
```

Q:: How do you loop through or enumerate javascript object  
A:: You can use the `for-in` loop to loop through javascript object. You can also make sure that the key you get is an actual property of an object, and doesn't come from the prototype using `hasOwnProperty` method.

```javascript
var object = {
  k1: "value1",
  k2: "value2",
  k3: "value3",
};
for (var key in object) {
  if (object.hasOwnProperty(key)) {
    console.log(key + " -> " + object[key]); // k1 -> value1 ...
  }
}
```

Q:: How do you test for an empty object  
A:: There are different solutions based on ECMAScript versions

1. **Using Object entries(ECMA 7+):** You can use object entries length along with constructor type.

```javascript
Object.entries(obj).length === 0 && obj.constructor === Object; // Since date object length is 0, you need to check constructor check as well
```

1. **Using Object keys(ECMA 5+):** You can use object keys length along with constructor type.

```javascript
Object.keys(obj).length === 0 && obj.constructor === Object; // Since date object length is 0, you need to check constructor check as well
```

1. **Using for-in with hasOwnProperty(Pre-ECMA 5):** You can use a for-in loop along with hasOwnProperty.

```javascript
function isEmpty(obj) {
  for (var prop in obj) {
    if (obj.hasOwnProperty(prop)) {
      return false;
    }
  }
  return JSON.stringify(obj) === JSON.stringify({});
}
```

Q:: What is an arguments object  
A:: The arguments object is an Array-like object accessible inside functions that contains the values of the arguments passed to that function. For example, let's see how to use arguments object inside sum function,

```javascript
function sum() {
  var total = 0;
  for (var i = 0, len = arguments.length; i < len; ++i) {
    total += arguments[i];
  }
  return total;
}
sum(1, 2, 3); // returns 6
```

**Note:** You can't apply array methods on arguments object. But you can convert into a regular array as below.

```javascript
var argsArray = Array.prototype.slice.call(arguments);
```

Q:: How do you make first letter of the string in an uppercase  
A:: You can create a function which uses a chain of string methods such as charAt, toUpperCase and slice methods to generate a string with the first letter in uppercase.

```javascript
function capitalizeFirstLetter(string) {
  return string.charAt(0).toUpperCase() + string.slice(1);
}
```

Q:: What are the pros and cons of for loop  
A:: The for-loop is a commonly used iteration syntax in javascript. It has both pros and cons

#### Pros

1. Works on every environment
2. You can use break and continue flow control statements

#### Cons

1. Too verbose
2. Imperative
3. You might face one-by-off errors

Q:: How do you display the current date in javascript  
A:: You can use `new Date()` to generate a new Date object containing the current date and time. For example, let's display the current date in mm/dd/yyyy

```javascript
var today = new Date();
var dd = String(today.getDate()).padStart(2, "0");
var mm = String(today.getMonth() + 1).padStart(2, "0"); //January is 0!
var yyyy = today.getFullYear();
today = mm + "/" + dd + "/" + yyyy;
document.write(today);
```

Q:: How do you compare two date objects  
A:: You need to use date.getTime() method to compare date values instead of comparison operators (==, !=, ===, and !== operators)

```javascript
var d1 = new Date();
var d2 = new Date(d1);
console.log(d1.getTime() === d2.getTime()); //True
console.log(d1 === d2); // False
```

Q:: How do you check if a string starts with another string  
A:: You can use ECMAScript 6's `String.prototype.startsWith()` method to check if a string starts with another string or not. But it is not yet supported in all browsers. Let's see an example to see this usage,

```javascript
"Good morning".startsWith("Good"); // true
"Good morning".startsWith("morning"); // false
```

Q:: How do you trim a string in javascript  
A:: JavaScript provided a trim method on string types to trim any whitespaces present at the beginning or ending of the string.

```javascript
"  Hello World   ".trim(); //Hello World
```

If your browser(<IE9) doesn't support this method then you can use below polyfill.

```javascript
if (!String.prototype.trim) {
  (function () {
    // Make sure we trim BOM and NBSP
    var rtrim = /^[\s\uFEFF\xA0]+|[\s\uFEFF\xA0]+$/g;
    String.prototype.trim = function () {
      return this.replace(rtrim, "");
    };
  })();
}
```

Q:: How do you add a key value pair in javascript  
A:: There are two possible solutions to add new properties to an object. Let's take a simple object to explain these solutions.

```javascript
var object = {
  key1: value1,
  key2: value2,
};
```

1. **Using dot notation:** This solution is useful when you know the name of the property

```javascript
object.key3 = "value3";
```

1. **Using square bracket notation:** This solution is useful when the name of the property is dynamically determined.

```javascript
obj["key3"] = "value3";
```

Q:: Is the !-- notation represents a special operator  
A:: No,that's not a special operator. But it is a combination of 2 standard operators one after the other,

1. A logical not (!)
2. A prefix decrement (--)
   At first, the value decremented by one and then tested to see if it is equal to zero or not for determining the truthy/falsy value.

Q:: How do you assign default values to variables  
A:: You can use the logical or operator `||` in an assignment expression to provide a default value. The syntax looks like as below,

```javascript
var a = b || c;
```

As per the above expression, variable 'a 'will get the value of 'c' only if 'b' is falsy (if is null, false, undefined, 0, empty string, or NaN), otherwise 'a' will get the value of 'b'.

Q:: How do you define multiline strings  
A:: You can define multiline string literals using the '\\' character followed by line terminator.

```javascript
var str =
  "This is a \
very lengthy \
sentence!";
```

But if you have a space after the '\\' character, the code will look exactly the same, but it will raise a SyntaxError.

Q:: What is an app shell model  
A:: An application shell (or app shell) architecture is one way to build a Progressive Web App that reliably and instantly loads on your users' screens, similar to what you see in native applications. It is useful for getting some initial HTML to the screen fast without a network.

Q:: Can we define properties for functions  
A:: Yes, We can define properties for functions because functions are also objects.

```javascript
fn = function (x) {
  //Function code goes here
};
fn.name = "John";
fn.profile = function (y) {
  //Profile code goes here
};
```

Q:: What is the way to find the number of parameters expected by a function  
A:: You can use `function.length` syntax to find the number of parameters expected by a function. Let's take an example of `sum` function to calculate the sum of numbers,

```javascript
function sum(num1, num2, num3, num4) {
  return num1 + num2 + num3 + num4;
}
sum.length; // 4 is the number of parameters expected.
```

Q:: What is a polyfill  
A:: A polyfill is a piece of JS code used to provide modern functionality on older browsers that do not natively support it. For example, Silverlight plugin polyfill can be used to mimic the functionality of an HTML Canvas element on Microsoft Internet Explorer 7.

Q:: What are break and continue statements  
A:: The break statement is used to "jump out" of a loop. i.e, It breaks the loop and continues executing the code after the loop.

```javascript
for (i = 0; i < 10; i++) {
  if (i === 5) {
    break;
  }
  text += "Number: " + i + "<br>";
}
```

The continue statement is used to "jump over" one iteration in the loop. i.e, It breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.

```javascript
for (i = 0; i < 10; i++) {
  if (i === 5) {
    continue;
  }
  text += "Number: " + i + "<br>";
}
```

Q:: What are js labels  
A:: The label statement allows us to name loops and blocks in JavaScript. We can then use these labels to refer back to the code later. For example, the below code with labels avoids printing the numbers when they are same,

```javascript
var i, j;
loop1: for (i = 0; i < 3; i++) {
  loop2: for (j = 0; j < 3; j++) {
    if (i === j) {
      continue loop1;
    }
    console.log("i = " + i + ", j = " + j);
  }
}
// Output is:
//   "i = 1, j = 0"
//   "i = 2, j = 0"
//   "i = 2, j = 1"
```

Q:: What are the benefits of keeping declarations at the top  
A:: It is recommended to keep all declarations at the top of each script or function. The benefits of doing this are,

1. Gives cleaner code
2. It provides a single place to look for local variables
3. Easy to avoid unwanted global variables
4. It reduces the possibility of unwanted re-declarations

Q:: What are the benefits of initializing variables  
A:: It is recommended to initialize variables because of the below benefits,

1. It gives cleaner code
2. It provides a single place to initialize variables
3. Avoid undefined values in the code

Q:: What are the recommendations to create new object  
A:: It is recommended to avoid creating new objects using `new Object()`. Instead you can initialize values based on it's type to create the objects.

1. Assign {} instead of new Object()
2. Assign "" instead of new String()
3. Assign 0 instead of new Number()
4. Assign false instead of new Boolean()
5. Assign [] instead of new Array()
6. Assign /()/ instead of new RegExp()
7. Assign function (){} instead of new Function()
   You can define them as an example,

```javascript
var v1 = {};
var v2 = "";
var v3 = 0;
var v4 = false;
var v5 = [];
var v6 = /()/;
var v7 = function () {};
```

Q:: How do you define JSON arrays  
A:: JSON arrays are written inside square brackets and arrays contain javascript objects. For example, the JSON array of users would be as below,

```javascript
"users":[
{"firstName":"John", "lastName":"Abrahm"},
{"firstName":"Anna", "lastName":"Smith"},
{"firstName":"Shane", "lastName":"Warn"}
]
```

Q:: How do you generate random integers  
A:: You can use Math.random() with Math.floor() to return random integers. For example, if you want generate random integers between 1 to 10, the multiplication factor should be 10,

```javascript
Math.floor(Math.random() * 10) + 1; // returns a random integer from 1 to 10
Math.floor(Math.random() * 100) + 1; // returns a random integer from 1 to 100
```

**Note:** Math.random() returns a random number between 0 (inclusive), and 1 (exclusive)

Q:: Can you write a random integers function to print integers with in a range  
A:: Yes, you can create a proper random function to return a random number between min and max (both included)

```javascript
function randomInteger(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}
randomInteger(1, 100); // returns a random integer from 1 to 100
randomInteger(1, 1000); // returns a random integer from 1 to 1000
```

Q:: What is tree shaking  
A:: Tree shaking is a form of dead code elimination. It means that unused modules will not be included in the bundle during the build process and for that it relies on the static structure of ES2015 module syntax,( i.e. import and export). Initially this has been popularized by the ES2015 module bundler `rollup`.

Q:: What is the need of tree shaking  
A:: Tree Shaking can significantly reduce the code size in any application. i.e, The less code we send over the wire the more performant the application will be. For example, if we just want to create a “Hello World” Application using SPA frameworks then it will take around a few MBs, but by tree shaking it can bring down the size to just a few hundred KBs. Tree shaking is implemented in Rollup and Webpack bundlers.

Q:: Is it recommended to use eval  
A:: No, it allows arbitrary code to be run which causes a security problem. As we know that the eval() function is used to run text as code. In most of the cases, it should not be necessary to use it.

Q:: What is a Regular Expression  
A:: A regular expression is a sequence of characters that forms a search pattern. You can use this search pattern for searching data in a text. These can be used to perform all types of text search and text replace operations. Let's see the syntax format now,

```javascript
/pattern/modifiers;
```

For example, the regular expression or search pattern with case-insensitive username would be,

```javascript
/John/i;
```

Q:: What are the string methods available in Regular expression  
A:: Regular Expressions has two string methods: search() and replace().  
The search() method uses an expression to search for a match, and returns the position of the match.

```javascript
var msg = "Hello John";
var n = msg.search(/John/i); // 6
```

The replace() method is used to return a modified string where the pattern is replaced.

```javascript
var msg = "Hello John";
var n = msg.replace(/John/i, "Buttler"); // Hello Buttler
```

Q:: What are modifiers in regular expression  
A:: Modifiers can be used to perform case-insensitive and global searches. Let's list down some of the modifiers,

| Modifier | Description                                             |
| -------- | ------------------------------------------------------- |
| i        | Perform case-insensitive matching                       |
| g        | Perform a global match rather than stops at first match |
| m        | Perform multiline matching                              |

Let's take an example of global modifier,

```javascript
var text = "Learn JS one by one";
var pattern = /one/g;
var result = text.match(pattern); // one,one
```

Q:: What are regular expression patterns  
A:: Regular Expressions provide a group of patterns in order to match characters. Basically they are categorized into 3 types,

1. **Brackets:** These are used to find a range of characters.
   For example, below are some use cases,
1. [abc]: Used to find any of the characters between the brackets(a,b,c)
1. [0-9]: Used to find any of the digits between the brackets
1. (a|b): Used to find any of the alternatives separated with |
1. **Metacharacters:** These are characters with a special meaning
   For example, below are some use cases,
1. \\d: Used to find a digit
1. \\s: Used to find a whitespace character
1. \\b: Used to find a match at the beginning or ending of a word
1. **Quantifiers:** These are useful to define quantities
   For example, below are some use cases,
1. n+: Used to find matches for any string that contains at least one n
1. n\*: Used to find matches for any string that contains zero or more occurrences of n
1. n?: Used to find matches for any string that contains zero or one occurrences of n

Q:: What is a RegExp object  
A:: RegExp object is a regular expression object with predefined properties and methods. Let's see the simple usage of RegExp object,

```javascript
var regexp = new RegExp("\\w+");
console.log(regexp);
// expected output: /\w+/
```

Q:: How do you search a string for a pattern  
A:: You can use the test() method of regular expression in order to search a string for a pattern, and return true or false depending on the result.

```javascript
var pattern = /you/;
console.log(pattern.test("How are you?")); //true
```

Q:: What is the purpose of exec method  
A:: The purpose of exec method is similar to test method but it executes a search for a match in a specified string and returns a result array, or null instead of returning true/false.

```javascript
var pattern = /you/;
console.log(pattern.exec("How are you?")); //["you", index: 8, input: "How are you?", groups: undefined]
```

Q:: How do you change the style of a HTML element  
A:: You can change inline style or classname of a HTML element using javascript

1. **Using style property:** You can modify inline style using style property

```javascript
document.getElementById("title").style.fontSize = "30px";
```

1. **Using ClassName property:** It is easy to modify element class using className property

```javascript
document.getElementById("title").className = "custom-title";
```

Q:: What would be the result of 1+2+'3'  
A:: The output is going to be `33`. Since `1` and `2` are numeric values, the result of the first two digits is going to be a numeric value `3`. The next digit is a string type value because of that the addition of numeric value `3` and string type value `3` is just going to be a concatenation value `33`.

Q:: What is a debugger statement  
A:: The debugger statement invokes any available debugging functionality, such as setting a breakpoint. If no debugging functionality is available, this statement has no effect.  
For example, in the below function a debugger statement has been inserted. So  
execution is paused at the debugger statement just like a breakpoint in the script source.

```javascript
function getProfile() {
  // code goes here
  debugger;
  // code goes here
}
```

Q:: What is the purpose of breakpoints in debugging  
A:: You can set breakpoints in the javascript code once the debugger statement is executed and the debugger window pops up. At each breakpoint, javascript will stop executing, and let you examine the JavaScript values. After examining values, you can resume the execution of code using the play button.

Q:: Can I use reserved words as identifiers  
A:: No, you cannot use the reserved words as variables, labels, object or function names. Let's see one simple example,

```javascript
var else = "hello"; // Uncaught SyntaxError: Unexpected token else
```

Q:: How do you detect a mobile browser  
A:: You can use regex which returns a true or false value depending on whether or not the user is browsing with a mobile.

```javascript
window.mobilecheck = function () {
  var mobileCheck = false;
  (function (a) {
    if (
      /(android|bb\d+|meego).+mobile|avantgo|bada\/|blackberry|blazer|compal|elaine|fennec|hiptop|iemobile|ip(hone|od)|iris|kindle|lge |maemo|midp|mmp|mobile.+firefox|netfront|opera m(ob|in)i|palm( os)?|phone|p(ixi|re)\/|plucker|pocket|psp|series(4|6)0|symbian|treo|up\.(browser|link)|vodafone|wap|windows ce|xda|xiino/i.test(
        a,
      ) ||
      /1207|6310|6590|3gso|4thp|50[1-6]i|770s|802s|a wa|abac|ac(er|oo|s\-)|ai(ko|rn)|al(av|ca|co)|amoi|an(ex|ny|yw)|aptu|ar(ch|go)|as(te|us)|attw|au(di|\-m|r |s )|avan|be(ck|ll|nq)|bi(lb|rd)|bl(ac|az)|br(e|v)w|bumb|bw\-(n|u)|c55\/|capi|ccwa|cdm\-|cell|chtm|cldc|cmd\-|co(mp|nd)|craw|da(it|ll|ng)|dbte|dc\-s|devi|dica|dmob|do(c|p)o|ds(12|\-d)|el(49|ai)|em(l2|ul)|er(ic|k0)|esl8|ez([4-7]0|os|wa|ze)|fetc|fly(\-|_)|g1 u|g560|gene|gf\-5|g\-mo|go(\.w|od)|gr(ad|un)|haie|hcit|hd\-(m|p|t)|hei\-|hi(pt|ta)|hp( i|ip)|hs\-c|ht(c(\-| |_|a|g|p|s|t)|tp)|hu(aw|tc)|i\-(20|go|ma)|i230|iac( |\-|\/)|ibro|idea|ig01|ikom|im1k|inno|ipaq|iris|ja(t|v)a|jbro|jemu|jigs|kddi|keji|kgt( |\/)|klon|kpt |kwc\-|kyo(c|k)|le(no|xi)|lg( g|\/(k|l|u)|50|54|\-[a-w])|libw|lynx|m1\-w|m3ga|m50\/|ma(te|ui|xo)|mc(01|21|ca)|m\-cr|me(rc|ri)|mi(o8|oa|ts)|mmef|mo(01|02|bi|de|do|t(\-| |o|v)|zz)|mt(50|p1|v )|mwbp|mywa|n10[0-2]|n20[2-3]|n30(0|2)|n50(0|2|5)|n7(0(0|1)|10)|ne((c|m)\-|on|tf|wf|wg|wt)|nok(6|i)|nzph|o2im|op(ti|wv)|oran|owg1|p800|pan(a|d|t)|pdxg|pg(13|\-([1-8]|c))|phil|pire|pl(ay|uc)|pn\-2|po(ck|rt|se)|prox|psio|pt\-g|qa\-a|qc(07|12|21|32|60|\-[2-7]|i\-)|qtek|r380|r600|raks|rim9|ro(ve|zo)|s55\/|sa(ge|ma|mm|ms|ny|va)|sc(01|h\-|oo|p\-)|sdk\/|se(c(\-|0|1)|47|mc|nd|ri)|sgh\-|shar|sie(\-|m)|sk\-0|sl(45|id)|sm(al|ar|b3|it|t5)|so(ft|ny)|sp(01|h\-|v\-|v )|sy(01|mb)|t2(18|50)|t6(00|10|18)|ta(gt|lk)|tcl\-|tdg\-|tel(i|m)|tim\-|t\-mo|to(pl|sh)|ts(70|m\-|m3|m5)|tx\-9|up(\.b|g1|si)|utst|v400|v750|veri|vi(rg|te)|vk(40|5[0-3]|\-v)|vm40|voda|vulc|vx(52|53|60|61|70|80|81|83|85|98)|w3c(\-| )|webc|whit|wi(g |nc|nw)|wmlb|wonu|x700|yas\-|your|zeto|zte\-/i.test(
        a.substr(0, 4),
      )
    )
      mobileCheck = true;
  })(navigator.userAgent || navigator.vendor || window.opera);
  return mobileCheck;
};
```

Q:: How do you detect a mobile browser without regexp  
A:: You can detect mobile browsers by simply running through a list of devices and checking if the useragent matches anything. This is an alternative solution for RegExp usage,

```javascript
function detectmob() {
  if (
    navigator.userAgent.match(/Android/i) ||
    navigator.userAgent.match(/webOS/i) ||
    navigator.userAgent.match(/iPhone/i) ||
    navigator.userAgent.match(/iPad/i) ||
    navigator.userAgent.match(/iPod/i) ||
    navigator.userAgent.match(/BlackBerry/i) ||
    navigator.userAgent.match(/Windows Phone/i)
  ) {
    return true;
  } else {
    return false;
  }
}
```

Q:: How do you get the image width and height using JS  
A:: You can programmatically get the image and check the dimensions(width and height) using Javascript.

```javascript
var img = new Image();
img.onload = function () {
  console.log(this.width + "x" + this.height);
};
img.src = "http://www.google.com/intl/en_ALL/images/logo.gif";
```

Q:: How do you make synchronous HTTP request  
A:: Browsers provide an XMLHttpRequest object which can be used to make synchronous HTTP requests from JavaScript

```javascript
function httpGet(theUrl) {
  var xmlHttpReq = new XMLHttpRequest();
  xmlHttpReq.open("GET", theUrl, false); // false for synchronous request
  xmlHttpReq.send(null);
  return xmlHttpReq.responseText;
}
```

Q:: How do you make asynchronous HTTP request  
A:: Browsers provide an XMLHttpRequest object which can be used to make asynchronous HTTP requests from JavaScript by passing the 3rd parameter as true.

```javascript
function httpGetAsync(theUrl, callback) {
  var xmlHttpReq = new XMLHttpRequest();
  xmlHttpReq.onreadystatechange = function () {
    if (xmlHttpReq.readyState == 4 && xmlHttpReq.status == 200)
      callback(xmlHttpReq.responseText);
  };
  xmlHttp.open("GET", theUrl, true); // true for asynchronous
  xmlHttp.send(null);
}
```

Q:: How do you convert date to another timezone in javascript  
A:: You can use the toLocaleString() method to convert dates in one timezone to another. For example, let's convert current date to British English timezone as below,

```javascript
console.log(event.toLocaleString("en-GB", { timeZone: "UTC" })); //29/06/2019, 09:56:00
```

Q:: What are the properties used to get size of window  
A:: You can use innerWidth, innerHeight, clientWidth, clientHeight properties of windows, document element and document body objects to find the size of a window. Let's use them combination of these properties to calculate the size of a window or document,

```javascript
var width =
  window.innerWidth ||
  document.documentElement.clientWidth ||
  document.body.clientWidth;
var height =
  window.innerHeight ||
  document.documentElement.clientHeight ||
  document.body.clientHeight;
```

Q:: What is a conditional operator in javascript  
A:: The conditional (ternary) operator is the only JavaScript operator that takes three operands which acts as a shortcut for if statements.

```javascript
var isAuthenticated = false;
console.log(
  isAuthenticated ? "Hello, welcome" : "Sorry, you are not authenticated",
); //Sorry, you are not authenticated
```

Q:: Can you apply chaining on conditional operator  
A:: Yes, you can apply chaining on conditional operators similar to if … else if … else if … else chain. The syntax is going to be as below,

```javascript
function traceValue(someParam) {
  return condition1
    ? value1
    : condition2
    ? value2
    : condition3
    ? value3
    : value4;
}
// The above conditional operator is equivalent to:
function traceValue(someParam) {
  if (condition1) {
    return value1;
  } else if (condition2) {
    return value2;
  } else if (condition3) {
    return value3;
  } else {
    return value4;
  }
}
```

Q:: What are the ways to execute javascript after page load  
A:: You can execute javascript after page load in many different ways,

1. **window.onload:**

```javascript
window.onload = function ...
```

1. **document.onload:**

```javascript
document.onload = function ...
```

1. **body onload:**

```javascript
<body onload="script();">
```

Q:: What is the difference between proto and prototype  
A:: The `__proto__` object is the actual object that is used in the lookup chain to resolve methods, etc. Whereas `prototype` is the object that is used to build `__proto__` when you create an object with new.

```javascript
new Employee().__proto__ === Employee.prototype;
new Employee().prototype === undefined;
```

There are few more differences,
| feature | Prototype | proto |
| ------------------- | ------------------------------------- | ----------------------------------------------- |
| Access | All the function constructors have prototype properties. | All the objects have \_\_proto\_\_ property |
| Purpose | Used to reduce memory wastage with a single copy of function | Used in lookup chain to resolve methods, constructors etc. |
| ECMAScript | Introduced in ES6 | Introduced in ES5 |
| Usage | Frequently used | Rarely used |

Q:: Give an example where do you really need semicolon  
A:: It is recommended to use semicolons after every statement in JavaScript. For example, in the below case it throws an error ".. is not a function" at runtime due to missing semicolon.

```javascript
// define a function
var fn = (function () {
  //...
})(
  // semicolon missing at this line
  // then execute some code inside a closure
  function () {
    //...
  },
)();
```

and it will be interpreted as

```javascript
var fn = (function () {
  //...
})(function () {
  //...
})();
```

In this case, we are passing the second function as an argument to the first function and then trying to call the result of the first function call as a function. Hence, the second function will fail with a "... is not a function" error at runtime.

Q:: What is a freeze method  
A:: The **freeze()** method is used to freeze an object. Freezing an object does not allow adding new properties to an object,prevents from removing and prevents changing the enumerability, configurability, or writability of existing properties. i.e, It returns the passed object and does not create a frozen copy.

```javascript
const obj = {
  prop: 100,
};
Object.freeze(obj);
obj.prop = 200; // Throws an error in strict mode
console.log(obj.prop); //100
```

Remember freezing is only applied to the top-level properties in objects but not for nested objects.
For example, let's try to freeze user object which has employment details as nested object and observe that details have been changed.

```javascript
const user = {
  name: "John",
  employment: {
    department: "IT",
  },
};
Object.freeze(user);
user.employment.department = "HR";
```

**Note:** It causes a TypeError if the argument passed is not an object.

Q:: What is the purpose of freeze method  
A:: Below are the main benefits of using freeze method,

1. It is used for freezing objects and arrays.
2. It is used to make an object immutable.

Q:: Why do I need to use freeze method  
A:: In the Object-oriented paradigm, an existing API contains certain elements that are not intended to be extended, modified, or re-used outside of their current context. Hence it works as the `final` keyword which is used in various languages.

Q:: How do you detect a browser language preference  
A:: You can use navigator object to detect a browser language preference as below,

```javascript
var language =
  (navigator.languages && navigator.languages[0]) || // Chrome / Firefox
  navigator.language || // All browsers
  navigator.userLanguage; // IE <= 10
console.log(language);
```

Q:: How to convert string to title case with javascript  
A:: Title case means that the first letter of each word is capitalized. You can convert a string to title case using the below function,

```javascript
function toTitleCase(str) {
  return str.replace(/\w\S*/g, function (txt) {
    return txt.charAt(0).toUpperCase() + txt.substring(1).toLowerCase();
  });
}
toTitleCase("good morning john"); // Good Morning John
```

Q:: How do you detect javascript disabled in the page  
A:: You can use the `<noscript>` tag to detect javascript disabled or not. The code block inside `<noscript>` gets executed when JavaScript is disabled, and is typically used to display alternative content when the page generated in JavaScript.

```javascript
<script type="javascript">
// JS related code goes here
</script>
<noscript>
<a href="next_page.html?noJS=true">JavaScript is disabled in the page. Please click Next Page</a>
</noscript>
```

Q:: What are various operators supported by javascript  
A:: An operator is capable of manipulating(mathematical and logical computations) a certain value or operand. There are various operators supported by JavaScript as below,

1. **Arithmetic Operators:** Includes + (Addition),– (Subtraction), \* (Multiplication), / (Division), % (Modulus), + + (Increment) and – – (Decrement)
2. **Comparison Operators:** Includes = =(Equal),!= (Not Equal), ===(Equal with type), > (Greater than),> = (Greater than or Equal to),< (Less than),<= (Less than or Equal to)
3. **Logical Operators:** Includes &&(Logical AND),||(Logical OR),!(Logical NOT)
4. **Assignment Operators:** Includes = (Assignment Operator), += (Add and Assignment Operator), – = (Subtract and Assignment Operator), \*= (Multiply and Assignment), /= (Divide and Assignment), %= (Modules and Assignment)
5. **Ternary Operators:** It includes conditional(: ?) Operator
6. **typeof Operator:** It uses to find type of variable. The syntax looks like `typeof variable`

Q:: What is a rest parameter  
A:: Rest parameter is an improved way to handle function parameters which allows us to represent an indefinite number of arguments as an array. The syntax would be as below,

```javascript
function f(a, b, ...theArgs) {
  // ...
}
```

For example, let's take a sum example to calculate on dynamic number of parameters,

```javascript
function sum(...args) {
  let total = 0;
  for (const i of args) {
    total += i;
  }
  return total;
}
console.log(sum(1, 2)); //3
console.log(sum(1, 2, 3)); //6
console.log(sum(1, 2, 3, 4)); //13
console.log(sum(1, 2, 3, 4, 5)); //15
```

**Note:** Rest parameter is added in ES2015 or ES6

Q:: What happens if you do not use rest parameter as a last argument  
A:: The rest parameter should be the last argument, as its job is to collect all the remaining arguments into an array. For example, if you define a function like below it doesn’t make any sense and will throw an error.

```javascript
function someFunc(a,…b,c){
//You code goes here
return;
}
```

Q:: What are the bitwise operators available in javascript  
A:: Below are the list of bitwise logical operators used in JavaScript

1. Bitwise AND ( & )
2. Bitwise OR ( | )
3. Bitwise XOR ( ^ )
4. Bitwise NOT ( ~ )
5. Left Shift ( << )
6. Sign Propagating Right Shift ( >> )
7. Zero fill Right Shift ( >>> )

Q:: What is a spread operator  
A:: Spread operator allows iterables( arrays / objects / strings ) to be expanded into single arguments/elements. Let's take an example to see this behavior,

```javascript
function calculateSum(x, y, z) {
  return x + y + z;
}
const numbers = [1, 2, 3];
console.log(calculateSum(...numbers)); // 6
```

Q:: How do you determine whether object is frozen or not  
A:: Object.isFrozen() method is used to determine if an object is frozen or not.An object is frozen if all of the below conditions hold true,

1. If it is not extensible.
2. If all of its properties are non-configurable.
3. If all its data properties are non-writable.
   The usage is going to be as follows,

```javascript
const object = {
  property: "Welcome JS world",
};
Object.freeze(object);
console.log(Object.isFrozen(object));
```

Q:: How do you determine two values same or not using object  
A:: The Object.is() method determines whether two values are the same value. For example, the usage with different types of values would be,

```javascript
Object.is("hello", "hello"); // true
Object.is(window, window); // true
Object.is([], []); // false
```

Two values are the same if one of the following holds:

1. both undefined
2. both null
3. both true or both false
4. both strings of the same length with the same characters in the same order
5. both the same object (means both object have same reference)
6. both numbers and
   both +0
   both -0
   both NaN
   both non-zero and both not NaN and both have the same value.

Q:: What is the purpose of using object is method  
A:: Some of the applications of Object's `is` method are follows,

1. It is used for comparison of two strings.
2. It is used for comparison of two numbers.
3. It is used for comparing the polarity of two numbers.
4. It is used for comparison of two objects.

Q:: How do you copy properties from one object to other  
A:: You can use the Object.assign() method which is used to copy the values and properties from one or more source objects to a target object. It returns the target object which has properties and values copied from the source objects. The syntax would be as below,

```javascript
Object.assign(target, ...sources);
```

Let's take example with one source and one target object,

```javascript
const target = { a: 1, b: 2 };
const source = { b: 3, c: 4 };
const returnedTarget = Object.assign(target, source);
console.log(target); // { a: 1, b: 3, c: 4 }
console.log(returnedTarget); // { a: 1, b: 3, c: 4 }
```

As observed in the above code, there is a common property(`b`) from source to target so it's value has been overwritten.

Q:: What are the applications of assign method  
A:: Below are the some of main applications of Object.assign() method,

1. It is used for cloning an object.
2. It is used to merge objects with the same properties.

Q:: What is a proxy object  
A:: The Proxy object is used to define custom behavior for fundamental operations such as property lookup, assignment, enumeration, function invocation, etc. The syntax would be as follows,

```javascript
var p = new Proxy(target, handler);
```

Let's take an example of proxy object,

```javascript
var handler = {
  get: function (obj, prop) {
    return prop in obj ? obj[prop] : 100;
  },
};
var p = new Proxy({}, handler);
p.a = 10;
p.b = null;
console.log(p.a, p.b); // 10, null
console.log("c" in p, p.c); // false, 100
```

In the above code, it uses `get` handler which define the behavior of the proxy when an operation is performed on it

Q:: What is the purpose of seal method  
A:: The **Object.seal()** method is used to seal an object, by preventing new properties from being added to it and marking all existing properties as non-configurable. But values of present properties can still be changed as long as they are writable. Let's see the below example to understand more about seal() method

```javascript
const object = {
  property: "Welcome JS world",
};
Object.seal(object);
object.property = "Welcome to object world";
console.log(Object.isSealed(object)); // true
delete object.property; // You cannot delete when sealed
console.log(object.property); //Welcome to object world
```

Q:: What are the applications of seal method  
A:: Below are the main applications of Object.seal() method,

1. It is used for sealing objects and arrays.
2. It is used to make an object immutable.

Q:: What are the differences between freeze and seal methods  
A:: If an object is frozen using the Object.freeze() method then its properties become immutable and no changes can be made in them whereas if an object is sealed using the Object.seal() method then the changes can be made in the existing properties of the object.

Q:: How do you determine if an object is sealed or not  
A:: The Object.isSealed() method is used to determine if an object is sealed or not. An object is sealed if all of the below conditions hold true

1. If it is not extensible.
2. If all of its properties are non-configurable.
3. If it is not removable (but not necessarily non-writable).
   Let's see it in the action

```javascript
const object = {
  property: "Hello, Good morning",
};
Object.seal(object); // Using seal() method to seal the object
console.log(Object.isSealed(object)); // checking whether the object is sealed or not
```

Q:: How do you get enumerable key and value pairs  
A:: The Object.entries() method is used to return an array of a given object's own enumerable string-keyed property [key, value] pairs, in the same order as that provided by a for...in loop. Let's see the functionality of object.entries() method in an example,

```javascript
const object = {
  a: "Good morning",
  b: 100,
};
for (let [key, value] of Object.entries(object)) {
  console.log(`${key}: ${value}`); // a: 'Good morning'
  // b: 100
}
```

**Note:** The order is not guaranteed as object defined.

Q:: What is the main difference between Object.values and Object.entries method  
A:: The Object.values() method's behavior is similar to Object.entries() method but it returns an array of values instead [key,value] pairs.

```javascript
const object = {
  a: "Good morning",
  b: 100,
};
for (let value of Object.values(object)) {
  console.log(`${value}`); // 'Good morning'
  100;
}
```

Q:: How can you get the list of keys of any object  
A:: You can use the `Object.keys()` method which is used to return an array of a given object's own property names, in the same order as we get with a normal loop. For example, you can get the keys of a user object,

```javascript
const user = {
  name: "John",
  gender: "male",
  age: 40,
};
console.log(Object.keys(user)); //['name', 'gender', 'age']
```

Q:: How do you create an object with prototype  
A:: The Object.create() method is used to create a new object with the specified prototype object and properties. i.e, It uses an existing object as the prototype of the newly created object. It returns a new object with the specified prototype object and properties.

```javascript
const user = {
  name: "John",
  printInfo: function () {
    console.log(`My name is ${this.name}.`);
  },
};
const admin = Object.create(user);
admin.name = "Nick"; // Remember that "name" is a property set on "admin" but not on "user" object
admin.printInfo(); // My name is Nick
```

Q:: What is a WeakSet  
A:: WeakSet is used to store a collection of weakly(weak references) held objects. The syntax would be as follows,

```javascript
new WeakSet([iterable]);
```

Let's see the below example to explain it's behavior,

```javascript
var ws = new WeakSet();
var user = {};
ws.add(user);
ws.has(user); // true
ws.delete(user); // removes user from the set
ws.has(user); // false, user has been removed
```

Q:: What are the differences between WeakSet and Set  
A:: The main difference is that references to objects in Set are strong while references to objects in WeakSet are weak. i.e, An object in WeakSet can be garbage collected if there is no other reference to it.  
Other differences are,

1. Sets can store any value Whereas WeakSets can store only collections of objects
2. WeakSet does not have size property unlike Set
3. WeakSet does not have methods such as clear, keys, values, entries, forEach.
4. WeakSet is not iterable.

Q:: List down the collection of methods available on WeakSet  
A:: Below are the list of methods available on WeakSet,

1. add(value): A new object is appended with the given value to the weakset
2. delete(value): Deletes the value from the WeakSet collection.
3. has(value): It returns true if the value is present in the WeakSet Collection, otherwise it returns false.
   Let's see the functionality of all the above methods in an example,

```javascript
var weakSetObject = new WeakSet();
var firstObject = {};
var secondObject = {};
// add(value)
weakSetObject.add(firstObject);
weakSetObject.add(secondObject);
console.log(weakSetObject.has(firstObject)); //true
weakSetObject.delete(secondObject);
```

Q:: What is a WeakMap  
A:: The WeakMap object is a collection of key/value pairs in which the keys are weakly referenced. In this case, keys must be objects and the values can be arbitrary values. The syntax is looking like as below,

```javascript
new WeakMap([iterable]);
```

Let's see the below example to explain it's behavior,

```javascript
var ws = new WeakMap();
var user = {};
ws.set(user);
ws.has(user); // true
ws.delete(user); // removes user from the map
ws.has(user); // false, user has been removed
```

Q:: What are the differences between WeakMap and Map  
A:: The main difference is that references to key objects in Map are strong while references to key objects in WeakMap are weak. i.e, A key object in WeakMap can be garbage collected if there is no other reference to it.  
Other differences are,

1. Maps can store any key type Whereas WeakMaps can store only collections of key objects
2. WeakMap does not have size property unlike Map
3. WeakMap does not have methods such as clear, keys, values, entries, forEach.
4. WeakMap is not iterable.

Q:: List down the collection of methods available on WeakMap  
A:: Below are the list of methods available on WeakMap,

1. set(key, value): Sets the value for the key in the WeakMap object. Returns the WeakMap object.
2. delete(key): Removes any value associated to the key.
3. has(key): Returns a Boolean asserting whether a value has been associated to the key in the WeakMap object or not.
4. get(key): Returns the value associated to the key, or undefined if there is none.
   Let's see the functionality of all the above methods in an example,

```javascript
var weakMapObject = new WeakMap();
var firstObject = {};
var secondObject = {};
// set(key, value)
weakMapObject.set(firstObject, "John");
weakMapObject.set(secondObject, 100);
console.log(weakMapObject.has(firstObject)); //true
console.log(weakMapObject.get(firstObject)); // John
weakMapObject.delete(secondObject);
```

Q:: What is the purpose of uneval  
A:: The uneval() is an inbuilt function which is used to create a string representation of the source code of an Object. It is a top-level function and is not associated with any object. Let's see the below example to know more about it's functionality,

```javascript
var a = 1;
uneval(a); // returns a String containing 1
uneval(function user() {}); // returns "(function user(){})"
```

Q:: How do you encode an URL  
A:: The encodeURI() function is used to encode complete URI which has special characters except (, / ? : @ & = + $ #) characters.

```javascript
var uri = "https://mozilla.org/?x=шеллы";
var encoded = encodeURI(uri);
console.log(encoded); // https://mozilla.org/?x=%D1%88%D0%B5%D0%BB%D0%BB%D1%8B
```

Q:: How do you decode an URL  
A:: The decodeURI() function is used to decode a Uniform Resource Identifier (URI) previously created by encodeURI().

```javascript
var uri = "https://mozilla.org/?x=шеллы";
var encoded = encodeURI(uri);
console.log(encoded); // https://mozilla.org/?x=%D1%88%D0%B5%D0%BB%D0%BB%D1%8B
try {
  console.log(decodeURI(encoded)); // "https://mozilla.org/?x=шеллы"
} catch (e) {
  // catches a malformed URI
  console.error(e);
}
```

Q:: How do you print the contents of web page  
A:: The window object provided a print() method which is used to print the contents of the current window. It opens a Print dialog box which lets you choose between various printing options. Let's see the usage of print method in an example,

```html
<input type="button" value="Print" onclick="window.print()" />
```

**Note:** In most browsers, it will block while the print dialog is open.

Q:: What is the difference between uneval and eval  
A:: The `uneval` function returns the source of a given object; whereas the `eval` function does the opposite, by evaluating that source code in a different memory area. Let's see an example to clarify the difference,

```javascript
var msg = uneval(function greeting() {
  return "Hello, Good morning";
});
var greeting = eval(msg);
greeting(); // returns "Hello, Good morning"
```

Q:: What is an anonymous function  
A:: An anonymous function is a function without a name! Anonymous functions are commonly assigned to a variable name or used as a callback function. The syntax would be as below,

```javascript
function (optionalParameters) {
//do something
}
const myFunction = function(){ //Anonymous function assigned to a variable
//do something
};
[1, 2, 3].map(function(element){ //Anonymous function used as a callback function
//do something
});
```

Let's see the above anonymous function in an example,

```javascript
var x = function (a, b) {
  return a * b;
};
var z = x(5, 10);
console.log(z); // 50
```

Q:: What is the precedence order between local and global variables  
A:: A local variable takes precedence over a global variable with the same name. Let's see this behavior in an example.

```javascript
var msg = "Good morning";
function greeting() {
  msg = "Good Evening";
  console.log(msg); // Good Evening
}
greeting();
```

Q:: What are javascript accessors  
A:: ECMAScript 5 introduced javascript object accessors or computed properties through getters and setters. Getters uses the `get` keyword whereas Setters uses the `set` keyword.

```javascript
var user = {
  firstName: "John",
  lastName: "Abraham",
  language: "en",
  get lang() {
    return this.language;
  },
  set lang(lang) {
    this.language = lang;
  },
};
console.log(user.lang); // getter access lang as en
user.lang = "fr";
console.log(user.lang); // setter used to set lang as fr
```

Q:: How do you define property on Object constructor  
A:: The Object.defineProperty() static method is used to define a new property directly on an object, or modify an existing property on an object, and returns the object. Let's see an example to know how to define property,

```javascript
const newObject = {};
Object.defineProperty(newObject, "newProperty", {
  value: 100,
  writable: false,
});
console.log(newObject.newProperty); // 100
newObject.newProperty = 200; // It throws an error in strict mode due to writable setting
```

Q:: What is the difference between get and defineProperty  
A:: Both have similar results until unless you use classes. If you use `get` the property will be defined on the prototype of the object whereas using `Object.defineProperty()` the property will be defined on the instance it is applied to.

Q:: What are the advantages of Getters and Setters  
A:: Below are the list of benefits of Getters and Setters,

1. They provide simpler syntax
2. They are used for defining computed properties, or accessors in JS.
3. Useful to provide equivalence relation between properties and methods
4. They can provide better data quality
5. Useful for doing things behind the scenes with the encapsulated logic.

Q:: Can I add getters and setters using defineProperty method  
A:: Yes, You can use the `Object.defineProperty()` method to add Getters and Setters. For example, the below counter object uses increment, decrement, add and subtract properties,

```javascript
var obj = { counter: 0 };
// Define getters
Object.defineProperty(obj, "increment", {
  get: function () {
    this.counter++;
  },
});
Object.defineProperty(obj, "decrement", {
  get: function () {
    this.counter--;
  },
});
// Define setters
Object.defineProperty(obj, "add", {
  set: function (value) {
    this.counter += value;
  },
});
Object.defineProperty(obj, "subtract", {
  set: function (value) {
    this.counter -= value;
  },
});
obj.add = 10;
obj.subtract = 5;
console.log(obj.increment); //6
console.log(obj.decrement); //5
```

Q:: What is the purpose of switch-case  
A:: The switch case statement in JavaScript is used for decision making purposes. In a few cases, using the switch case statement is going to be more convenient than if-else statements. The syntax would be as below,

```javascript
switch (expression)
{
case value1:
statement1;
break;
case value2:
statement2;
break;
.
.
case valueN:
statementN;
break;
default:
statementDefault;
}
```

The above multi-way branch statement provides an easy way to dispatch execution to different parts of code based on the value of the expression.

Q:: What are the conventions to be followed for the usage of switch case  
A:: Below are the list of conventions should be taken care,

1. The expression can be of type either number or string.
2. Duplicate values are not allowed for the expression.
3. The default statement is optional. If the expression passed to switch does not match with any case value then the statement within default case will be executed.
4. The break statement is used inside the switch to terminate a statement sequence.
5. The break statement is optional. But if it is omitted, the execution will continue on into the next case.

Q:: What are primitive data types  
A:: A primitive data type is data that has a primitive value (which has no properties or methods). There are 7 types of primitive data types.

1. string
2. number
3. boolean
4. null
5. undefined
6. bigint
7. symbol

Q:: What are the different ways to access object properties  
A:: There are 3 possible ways for accessing the property of an object.

1. **Dot notation:** It uses dot for accessing the properties

```javascript
objectName.property;
```

1. **Square brackets notation:** It uses square brackets for property access

```javascript
objectName["property"];
```

1. **Expression notation:** It uses expression in the square brackets

```javascript
objectName[expression];
```

Q:: What are the function parameter rules  
A:: JavaScript functions follow below rules for parameters,

1. The function definitions do not specify data types for parameters.
2. Do not perform type checking on the passed arguments.
3. Do not check the number of arguments received.
   i.e, The below function follows the above rules,

```javascript
function functionName(parameter1, parameter2, parameter3) {
  console.log(parameter1); // 1
}
functionName(1);
```

Q:: What is an error object  
A:: An error object is a built in error object that provides error information when an error occurs. It has two properties: name and message. For example, the below function logs error details,

```javascript
try {
  greeting("Welcome");
} catch (err) {
  console.log(err.name + "<br>" + err.message);
}
```

Q:: When you get a syntax error  
A:: A SyntaxError is thrown if you try to evaluate code with a syntax error. For example, the below missing quote for the function parameter throws a syntax error

```javascript
try {
  eval("greeting('welcome)"); // Missing ' will produce an error
} catch (err) {
  console.log(err.name);
}
```

Q:: What are the different error names from error object  
A:: There are 6 different types of error names returned from error object,

| Error Name     | Description                                        |
| -------------- | -------------------------------------------------- |
| EvalError      | An error has occurred in the eval() function       |
| RangeError     | An error has occurred with a number "out of range" |
| ReferenceError | An error due to an illegal reference               |
| SyntaxError    | An error due to a syntax error                     |
| TypeError      | An error due to a type error                       |
| URIError       | An error due to encodeURI()                        |

Q:: What are the various statements in error handling  
A:: Below are the list of statements used in an error handling,

1. **try:** This statement is used to test a block of code for errors
2. **catch:** This statement is used to handle the error
3. **throw:** This statement is used to create custom errors.
4. **finally:** This statement is used to execute code after try and catch regardless of the result.

Q:: What are the two types of loops in javascript  
A:: 1. **Entry Controlled loops:** In this kind of loop type, the test condition is tested before entering the loop body. For example, For Loop and While Loop comes under this category. 2. **Exit Controlled Loops:** In this kind of loop type, the test condition is tested or evaluated at the end of the loop body. i.e, the loop body will execute at least once irrespective of test condition true or false. For example, do-while loop comes under this category.

Q:: What is nodejs  
A:: Node.js is a server-side platform built on Chrome's JavaScript runtime for easily building fast and scalable network applications. It is an event-based, non-blocking, asynchronous I/O runtime that uses Google's V8 JavaScript engine and libuv library.

Q:: What is an Intl object  
A:: The Intl object is the namespace for the ECMAScript Internationalization API, which provides language sensitive string comparison, number formatting, and date and time formatting. It provides access to several constructors and language sensitive functions.

Q:: How do you perform language specific date and time formatting  
A:: You can use the `Intl.DateTimeFormat` object which is a constructor for objects that enable language-sensitive date and time formatting. Let's see this behavior with an example,

```javascript
var date = new Date(Date.UTC(2019, 07, 07, 3, 0, 0));
console.log(new Intl.DateTimeFormat("en-GB").format(date)); // 07/08/2019
console.log(new Intl.DateTimeFormat("en-AU").format(date)); // 07/08/2019
```

Q:: What is an Iterator  
A:: An iterator is an object which defines a sequence and a return value upon its termination. It implements the Iterator protocol with a `next()` method which returns an object with two properties: `value` (the next value in the sequence) and `done` (which is true if the last value in the sequence has been consumed).

Q:: How does synchronous iteration works  
A:: Synchronous iteration was introduced in ES6 and it works with below set of components,  
**Iterable:** It is an object which can be iterated over via a method whose key is Symbol.iterator.  
**Iterator:** It is an object returned by invoking `[Symbol.iterator]()` on an iterable. This iterator object wraps each iterated element in an object and returns it via `next()` method one by one.  
**IteratorResult:** It is an object returned by `next()` method. The object contains two properties; the `value` property contains an iterated element and the `done` property determines whether the element is the last element or not.  
Let's demonstrate synchronous iteration with an array as below,

```javascript
const iterable = ["one", "two", "three"];
const iterator = iterable[Symbol.iterator]();
console.log(iterator.next()); // { value: 'one', done: false }
console.log(iterator.next()); // { value: 'two', done: false }
console.log(iterator.next()); // { value: 'three', done: false }
console.log(iterator.next()); // { value: 'undefined, done: true }
```

Q:: What is an event loop  
A:: The event loop is a process that continuously monitors both the call stack and the event queue and checks whether or not the call stack is empty. If the call stack is empty and there are pending events in the event queue, the event loop dequeues the event from the event queue and pushes it to the call stack. The call stack executes the event, and any additional events generated during the execution are added to the end of the event queue.  
**Note:** The event loop allows Node.js to perform non-blocking I/O operations, even though JavaScript is single-threaded, by offloading operations to the system kernel whenever possible. Since most modern kernels are multi-threaded, they can handle multiple operations executing in the background.

Q:: What is call stack  
A:: Call Stack is a data structure for javascript interpreters to keep track of function calls(creates execution context) in the program. It has two major actions,

1. Whenever you call a function for its execution, you are pushing it to the stack.
2. Whenever the execution is completed, the function is popped out of the stack.
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
4. Delete the `hungry()` function from the call stack list since there are no items anymore.
   ![call-stack](../images/call-stack.png)

Q:: What is an event queue  
A:: The event queue follows the queue data structure. It stores async callbacks to be added to the call stack. It is also known as the Callback Queue or Macrotask Queue.  
Whenever the call stack receives an async function, it is moved into the Web API. Based on the function, Web API executes it and awaits the result. Once it is finished, it moves the callback into the event queue (the callback of the promise is moved into the microtask queue).  
The event queue constantly checks whether or not the call stack is empty. Once the call stack is empty and there is a callback in the event queue, the event queue moves the callback into the call stack. If there is a callback in the microtask queue as well, it is moved first. The microtask queue has a higher priority than the event queue.

Q:: What is a decorator  
A:: A decorator is an expression that evaluates to a function and that takes the target, name, and decorator descriptor as arguments. Also, it optionally returns a decorator descriptor to install on the target object. Let's define admin decorator for user class at design time,

```javascript
function admin(isAdmin) {
return function(target) {
target.isAdmin = isAdmin;
}
}
@admin(true)
class User() {
}
console.log(User.isAdmin); //true
@admin(false)
class User() {
}
console.log(User.isAdmin); //false
```

Q:: What are the properties of Intl object  
A:: Below are the list of properties available on Intl object,

1. **Collator:** These are the objects that enable language-sensitive string comparison.
2. **DateTimeFormat:** These are the objects that enable language-sensitive date and time formatting.
3. **ListFormat:** These are the objects that enable language-sensitive list formatting.
4. **NumberFormat:** Objects that enable language-sensitive number formatting.
5. **PluralRules:** Objects that enable plural-sensitive formatting and language-specific rules for plurals.
6. **RelativeTimeFormat:** Objects that enable language-sensitive relative time formatting.

Q:: What is an Unary operator  
A:: The unary(+) operator is used to convert a variable to a number.If the variable cannot be converted, it will still become a number but with the value NaN. Let's see this behavior in an action.

```javascript
var x = "100";
var y = +x;
console.log(typeof x, typeof y); // string, number
var a = "Hello";
var b = +a;
console.log(typeof a, typeof b, b); // string, number, NaN
```

Q:: How do you sort elements in an array  
A:: The sort() method is used to sort the elements of an array in place and returns the sorted array. The example usage would be as below,

```javascript
var months = ["Aug", "Sep", "Jan", "June"];
months.sort();
console.log(months); //  ["Aug", "Jan", "June", "Sep"]
```

Q:: What is the purpose of compareFunction while sorting arrays  
A:: The compareFunction is used to define the sort order. If omitted, the array elements are converted to strings, then sorted according to each character's Unicode code point value. Let's take an example to see the usage of compareFunction,

```javascript
let numbers = [1, 2, 5, 3, 4];
numbers.sort((a, b) => b - a);
console.log(numbers); // [5, 4, 3, 2, 1]
```

Q:: How do you reversing an array  
A:: You can use the reverse() method to reverse the elements in an array. This method is useful to sort an array in descending order. Let's see the usage of reverse() method in an example,

```javascript
let numbers = [1, 2, 5, 3, 4];
numbers.sort((a, b) => b - a);
numbers.reverse();
console.log(numbers); // [1, 2, 3, 4 ,5]
```

Q:: How do you find min and max value in an array  
A:: You can use `Math.min` and `Math.max` methods on array variables to find the minimum and maximum elements within an array. Let's create two functions to find the min and max value with in an array,

```javascript
var marks = [50, 20, 70, 60, 45, 30];
function findMin(arr) {
  return Math.min.apply(null, arr);
}
function findMax(arr) {
  return Math.max.apply(null, arr);
}
console.log(findMin(marks));
console.log(findMax(marks));
```

Q:: How do you find min and max values without Math functions  
A:: You can write functions which loop through an array comparing each value with the lowest value or highest value to find the min and max values. Let's create those functions to find min and max values,

```javascript
var marks = [50, 20, 70, 60, 45, 30];
function findMin(arr) {
  var length = arr.length;
  var min = Infinity;
  while (length--) {
    if (arr[length] < min) {
      min = arr[length];
    }
  }
  return min;
}
function findMax(arr) {
  var length = arr.length;
  var max = -Infinity;
  while (length--) {
    if (arr[length] > max) {
      max = arr[length];
    }
  }
  return max;
}
console.log(findMin(marks));
console.log(findMax(marks));
```

Q:: What is an empty statement and purpose of it  
A:: The empty statement is a semicolon (;) indicating that no statement will be executed, even if JavaScript syntax requires one. Since there is no action with an empty statement you might think that it's usage is quite less, but the empty statement is occasionally useful when you want to create a loop that has an empty body. For example, you can initialize an array with zero values as below,

```javascript
// Initialize an array a
for (let i = 0; i < a.length; a[i++] = 0);
```

Q:: How do you get metadata of a module  
A:: You can use the `import.meta` object which is a meta-property exposing context-specific meta data to a JavaScript module. It contains information about the current module, such as the module's URL. In browsers, you might get different meta data than NodeJS.

```javascript
<script type="module" src="welcome-module.js"></script>;
console.log(import.meta); // { url: "file:///home/user/welcome-module.js" }
```

Q:: What is a comma operator  
A:: The comma operator is used to evaluate each of its operands from left to right and returns the value of the last operand. This is totally different from comma usage within arrays, objects, and function arguments and parameters. For example, the usage for numeric expressions would be as below,

```javascript
var x = 1;
x = (x++, x);
console.log(x); // 2
```

Q:: What is the advantage of a comma operator  
A:: It is normally used to include multiple expressions in a location that requires a single expression. One of the common usages of this comma operator is to supply multiple parameters in a `for` loop. For example, the below for loop uses multiple expressions in a single location using comma operator,

```javascript
for (var a = 0, b =10; a <= 10; a++, b--)
```

You can also use the comma operator in a return statement where it processes before returning.

```javascript
function myFunction() {
  var a = 1;
  return (a += 10), a; // 11
}
```

Q:: What is typescript  
A:: TypeScript is a typed superset of JavaScript created by Microsoft that adds optional types, classes, async/await, and many other features, and compiles to plain JavaScript. Angular built entirely in TypeScript and used as a primary language. You can install it globally as

```bash
npm install -g typescript
```

Let's see a simple example of TypeScript usage,

```typescript
function greeting(name: string): string {
  return "Hello, " + name;
}
let user = "Sudheer";
console.log(greeting(user));
```

The greeting method allows only string type as argument.

Q:: What are the differences between javascript and typescript  
A:: Below are the list of differences between javascript and typescript,

| feature             | typescript                            | javascript                                      |
| ------------------- | ------------------------------------- | ----------------------------------------------- |
| Language paradigm   | Object oriented programming language  | Scripting language                              |
| Typing support      | Supports static typing                | It has dynamic typing                           |
| Modules             | Supported                             | Not supported                                   |
| Interface           | It has interfaces concept             | Doesn't support interfaces                      |
| Optional parameters | Functions support optional parameters | No support of optional parameters for functions |

Q:: What are the advantages of typescript over javascript  
A:: Below are some of the advantages of typescript over javascript,

1. TypeScript is able to find compile time errors at the development time only and it makes sures less runtime errors. Whereas javascript is an interpreted language.
2. TypeScript is strongly-typed or supports static typing which allows for checking type correctness at compile time. This is not available in javascript.
3. TypeScript compiler can compile the .ts files into ES3,ES4 and ES5 unlike ES6 features of javascript which may not be supported in some browsers.

Q:: What is an object initializer  
A:: An object initializer is an expression that describes the initialization of an Object. The syntax for this expression is represented as a comma-delimited list of zero or more pairs of property names and associated values of an object, enclosed in curly braces ({}). This is also known as literal notation. It is one of the ways to create an object.

```javascript
var initObject = { a: "John", b: 50, c: {} };
console.log(initObject.a); // John
```

Q:: What is a constructor method  
A:: The constructor method is a special method for creating and initializing an object created within a class. If you do not specify a constructor method, a default constructor is used. The example usage of constructor would be as below,

```javascript
class Employee {
  constructor() {
    this.name = "John";
  }
}
var employeeObject = new Employee();
console.log(employeeObject.name); // John
```

Q:: What happens if you write constructor more than once in a class  
A:: The "constructor" in a class is a special method and it should be defined only once in a class. i.e, If you write a constructor method more than once in a class it will throw a `SyntaxError` error.

```javascript
class Employee {
constructor() {
this.name = "John";
}
constructor() {   //  Uncaught SyntaxError: A class may only have one constructor
this.age = 30;
}
}
var employeeObject = new Employee();
console.log(employeeObject.name);
```

Q:: How do you call the constructor of a parent class  
A:: You can use the `super` keyword to call the constructor of a parent class. Remember that `super()` must be called before using 'this' reference. Otherwise it will cause a reference error. Let's the usage of it,

```javascript
class Square extends Rectangle {
  constructor(length) {
    super(length, length);
    this.name = "Square";
  }
  get area() {
    return this.width * this.height;
  }
  set area(value) {
    this.area = value;
  }
}
```

Q:: How do you get the prototype of an object  
A:: You can use the `Object.getPrototypeOf(obj)` method to return the prototype of the specified object. i.e. The value of the internal `prototype` property. If there are no inherited properties then `null` value is returned.

```javascript
const newPrototype = {};
const newObject = Object.create(newPrototype);
console.log(Object.getPrototypeOf(newObject) === newPrototype); // true
```

Q:: What happens If I pass string type for getPrototype method  
A:: In ES5, it will throw a TypeError exception if the obj parameter isn't an object. Whereas in ES2015, the parameter will be coerced to an `Object`.

```javascript
// ES5
Object.getPrototypeOf("James"); // TypeError: "James" is not an object
// ES2015
Object.getPrototypeOf("James"); // String.prototype
```

Q:: How do you set prototype of one object to another  
A:: You can use the `Object.setPrototypeOf()` method that sets the prototype (i.e., the internal `Prototype` property) of a specified object to another object or null. For example, if you want to set prototype of a square object to rectangle object would be as follows,

```javascript
Object.setPrototypeOf(Square.prototype, Rectangle.prototype);
Object.setPrototypeOf({}, null);
```

Q:: How do you check whether an object can be extendable or not  
A:: The `Object.isExtensible()` method is used to determine if an object is extendable or not. i.e, Whether it can have new properties added to it or not.

```javascript
const newObject = {};
console.log(Object.isExtensible(newObject)); //true
```

**Note:** By default, all the objects are extendable. i.e, The new properties can be added or modified.

Q:: How do you prevent an object to extend  
A:: The `Object.preventExtensions()` method is used to prevent new properties from ever being added to an object. In other words, it prevents future extensions to the object. Let's see the usage of this property,

```javascript
const newObject = {};
Object.preventExtensions(newObject); // NOT extendable
try {
  Object.defineProperty(newObject, "newProperty", {
    // Adding new property
    value: 100,
  });
} catch (e) {
  console.log(e); // TypeError: Cannot define property newProperty, object is not extensible
}
```

Q:: What are the different ways to make an object non-extensible  
A:: You can mark an object non-extensible in 3 ways,

1. Object.preventExtensions
2. Object.seal
3. Object.freeze

```javascript
var newObject = {};
Object.preventExtensions(newObject); // Prevent objects are non-extensible
Object.isExtensible(newObject); // false
var sealedObject = Object.seal({}); // Sealed objects are non-extensible
Object.isExtensible(sealedObject); // false
var frozenObject = Object.freeze({}); // Frozen objects are non-extensible
Object.isExtensible(frozenObject); // false
```

Q:: How do you define multiple properties on an object  
A:: The `Object.defineProperties()` method is used to define new or modify existing properties directly on an object and returning the object. Let's define multiple properties on an empty object,

```javascript
const newObject = {};
Object.defineProperties(newObject, {
  newProperty1: {
    value: "John",
    writable: true,
  },
  newProperty2: {},
});
```

Q:: What is MEAN in javascript  
A:: The MEAN (MongoDB, Express, AngularJS, and Node.js) stack is the most popular open-source JavaScript software tech stack available for building dynamic web apps where you can write both the server-side and client-side halves of the web project entirely in JavaScript.

Q:: What Is Obfuscation in javascript  
A:: Obfuscation is the deliberate act of creating obfuscated javascript code(i.e, source or machine code) that is difficult for humans to understand. It is something similar to encryption, but a machine can understand the code and execute it.  
Let's see the below function before Obfuscation,

```javascript
function greeting() {
  console.log("Hello, welcome to JS world");
}
```

And after the code Obfuscation, it would be appeared as below,

```javascript
eval(
  (function (p, a, c, k, e, d) {
    e = function (c) {
      return c;
    };
    if (!"".replace(/^/, String)) {
      while (c--) {
        d[c] = k[c] || c;
      }
      k = [
        function (e) {
          return d[e];
        },
      ];
      e = function () {
        return "\\w+";
      };
      c = 1;
    }
    while (c--) {
      if (k[c]) {
        p = p.replace(new RegExp("\\b" + e(c) + "\\b", "g"), k[c]);
      }
    }
    return p;
  })(
    "2 1(){0.3('4, 7 6 5 8')}",
    9,
    9,
    "console|greeting|function|log|Hello|JS|to|welcome|world".split("|"),
    0,
    {},
  ),
);
```

Q:: Why do you need Obfuscation  
A:: Below are the few reasons for Obfuscation,

1. The Code size will be reduced. So data transfers between server and client will be fast.
2. It hides the business logic from outside world and protects the code from others
3. Reverse engineering is highly difficult
4. The download time will be reduced

Q:: What is Minification  
A:: Minification is the process of removing all unnecessary characters(empty spaces are removed) and variables will be renamed without changing it's functionality. It is also a type of obfuscation .

Q:: What are the advantages of minification  
A:: Normally it is recommended to use minification for heavy traffic and intensive requirements of resources. It reduces file sizes with below benefits,

1. Decreases loading times of a web page
2. Saves bandwidth usages

Q:: What are the differences between Obfuscation and Encryption  
A:: Below are the main differences between Obfuscation and Encryption,

| Feature            | Obfuscation                                     | Encryption                                                              |
| ------------------ | ----------------------------------------------- | ----------------------------------------------------------------------- |
| Definition         | Changing the form of any data in any other form | Changing the form of information to an unreadable format by using a key |
| A key to decode    | It can be decoded without any key               | It is required                                                          |
| Target data format | It will be converted to a complex form          | Converted into an unreadable format                                     |

Q:: What are the common tools used for minification  
A:: There are many online/offline tools to minify the javascript files,

1. Google's Closure Compiler
2. UglifyJS2
3. jsmin
4. javascript-minifier.com/
5. prettydiff.com

Q:: How do you perform form validation using javascript  
A:: JavaScript can be used to perform HTML form validation. For example, if the form field is empty, the function needs to notify, and return false, to prevent the form being submitted.  
Lets' perform user login in an html form,

```html
<form name="myForm" onsubmit="return validateForm()" method="post">
  User name: <input type="text" name="uname" />
  <input type="submit" value="Submit" />
</form>
```

And the validation on user login is below,

```javascript
function validateForm() {
  var x = document.forms["myForm"]["uname"].value;
  if (x == "") {
    alert("The username shouldn't be empty");
    return false;
  }
}
```

Q:: How do you perform form validation without javascript  
A:: You can perform HTML form validation automatically without using javascript. The validation enabled by applying the `required` attribute to prevent form submission when the input is empty.

```html
<form method="post">
  <input type="text" name="uname" required />
  <input type="submit" value="Submit" />
</form>
```

**Note:** Automatic form validation does not work in Internet Explorer 9 or earlier.

Q:: What are the DOM methods available for constraint validation  
A:: The below DOM methods are available for constraint validation on an invalid input,

1. checkValidity(): It returns true if an input element contains valid data.
2. setCustomValidity(): It is used to set the validationMessage property of an input element.
   Let's take an user login form with DOM validations

```javascript
function myFunction() {
  var userName = document.getElementById("uname");
  if (!userName.checkValidity()) {
    document.getElementById("message").innerHTML = userName.validationMessage;
  } else {
    document.getElementById("message").innerHTML = "Entered a valid username";
  }
}
```

Q:: What are the available constraint validation DOM properties  
A:: Below are the list of some of the constraint validation DOM properties available,

1. validity: It provides a list of boolean properties related to the validity of an input element.
2. validationMessage: It displays the message when the validity is false.
3. willValidate: It indicates if an input element will be validated or not.

Q:: What are the list of validity properties  
A:: The validity property of an input element provides a set of properties related to the validity of data.

1. customError: It returns true, if a custom validity message is set.
2. patternMismatch: It returns true, if an element's value does not match its pattern attribute.
3. rangeOverflow: It returns true, if an element's value is greater than its max attribute.
4. rangeUnderflow: It returns true, if an element's value is less than its min attribute.
5. stepMismatch: It returns true, if an element's value is invalid according to step attribute.
6. tooLong: It returns true, if an element's value exceeds its maxLength attribute.
7. typeMismatch: It returns true, if an element's value is invalid according to type attribute.
8. valueMissing: It returns true, if an element with a required attribute has no value.
9. valid: It returns true, if an element's value is valid.

Q:: Give an example usage of rangeOverflow property  
A:: If an element's value is greater than its max attribute then rangeOverflow property returns true. For example, the below form submission throws an error if the value is more than 100,

```html
<input id="age" type="number" max="100" />
<button onclick="myOverflowFunction()">OK</button>
```

```javascript
function myOverflowFunction() {
  if (document.getElementById("age").validity.rangeOverflow) {
    alert("The mentioned age is not allowed");
  }
}
```

Q:: Is enums feature available in javascript  
A:: No, javascript does not natively support enums. But there are different kinds of solutions to simulate them even though they may not provide exact equivalents. For example, you can use freeze or seal on object,

```javascript
var DaysEnum = Object.freeze({"monday":1, "tuesday":2, "wednesday":3, ...})
```

Q:: What is an enum  
A:: An enum is a type restricting variables to one value from a predefined set of constants. JavaScript has no enums but typescript provides built-in enum support.

```javascript
enum Color {
RED, GREEN, BLUE
}
```

Q:: How do you list all properties of an object  
A:: You can use the `Object.getOwnPropertyNames()` method which returns an array of all properties found directly in a given object. Let's the usage of it in an example,

```javascript
const newObject = {
  a: 1,
  b: 2,
  c: 3,
};
console.log(Object.getOwnPropertyNames(newObject));
["a", "b", "c"];
```

Q:: How do you get property descriptors of an object  
A:: You can use the `Object.getOwnPropertyDescriptors()` method which returns all own property descriptors of a given object. The example usage of this method is below,

```javascript
const newObject = {
  a: 1,
  b: 2,
  c: 3,
};
const descriptorsObject = Object.getOwnPropertyDescriptors(newObject);
console.log(descriptorsObject.a.writable); //true
console.log(descriptorsObject.a.configurable); //true
console.log(descriptorsObject.a.enumerable); //true
console.log(descriptorsObject.a.value); // 1
```

Q:: What are the attributes provided by a property descriptor  
A:: A property descriptor is a record which has the following attributes

1. value: The value associated with the property
2. writable: Determines whether the value associated with the property can be changed or not
3. configurable: Returns true if the type of this property descriptor can be changed and if the property can be deleted from the corresponding object.
4. enumerable: Determines whether the property appears during enumeration of the properties on the corresponding object or not.
5. set: A function which serves as a setter for the property
6. get: A function which serves as a getter for the property

Q:: How do you extend classes  
A:: The `extends` keyword is used in class declarations/expressions to create a class which is a child of another class. It can be used to subclass custom classes as well as built-in objects. The syntax would be as below,

```javascript
class ChildClass extends ParentClass { ... }
```

Let's take an example of Square subclass from Polygon parent class,

```javascript
class Square extends Rectangle {
  constructor(length) {
    super(length, length);
    this.name = "Square";
  }
  get area() {
    return this.width * this.height;
  }
  set area(value) {
    this.area = value;
  }
}
```

Q:: How do I modify the url without reloading the page  
A:: The `window.location.href` property will be helpful to modify the url but it reloads the page. HTML5 introduced the `history.pushState()` and `history.replaceState()` methods, which allow you to add and modify history entries, respectively. For example, you can use pushState as below,

```javascript
window.history.pushState("page2", "Title", "/page2.html");
```

Q:: How do you check whether an array includes a particular value or not  
A:: The `Array#includes()` method is used to determine whether an array includes a particular value among its entries by returning either true or false. Let's see an example to find an element(numeric and string) within an array.

```javascript
var numericArray = [1, 2, 3, 4];
console.log(numericArray.includes(3)); // true
var stringArray = ["green", "yellow", "blue"];
console.log(stringArray.includes("blue")); //true
```

Q:: How do you compare scalar arrays  
A:: You can use length and every method of arrays to compare two scalar(compared directly using ===) arrays. The combination of these expressions can give the expected result,

```javascript
const arrayFirst = [1, 2, 3, 4, 5];
const arraySecond = [1, 2, 3, 4, 5];
console.log(
  arrayFirst.length === arraySecond.length &&
    arrayFirst.every((value, index) => value === arraySecond[index]),
); // true
```

If you would like to compare arrays irrespective of order then you should sort them before,

```javascript
const arrayFirst = [2, 3, 1, 4, 5];
const arraySecond = [1, 2, 3, 4, 5];
console.log(
  arrayFirst.length === arraySecond.length &&
    arrayFirst.sort().every((value, index) => value === arraySecond[index]),
); //true
```

Q:: How to get the value from get parameters  
A:: The `new URL()` object accepts the url string and `searchParams` property of this object can be used to access the get parameters. Remember that you may need to use polyfill or `window.location` to access the URL in older browsers(including IE).

```javascript
let urlString = "http://www.some-domain.com/about.html?x=1&y=2&z=3"; //window.location.href
let url = new URL(urlString);
let parameterZ = url.searchParams.get("z");
console.log(parameterZ); // 3
```

Q:: How do you print numbers with commas as thousand separators  
A:: You can use the `Number.prototype.toLocaleString()` method which returns a string with a language-sensitive representation such as thousand separator,currency etc of this number.

```javascript
function convertToThousandFormat(x) {
  return x.toLocaleString(); // 12,345.679
}
console.log(convertToThousandFormat(12345.6789));
```

Q:: What is the difference between java and javascript  
A:: Both are totally unrelated programming languages and no relation between them. Java is statically typed, compiled, runs on its own VM. Whereas Javascript is dynamically typed, interpreted, and runs in a browser and nodejs environments. Let's see the major differences in a tabular format,

| Feature     | Java                           | JavaScript                                            |
| ----------- | ------------------------------ | ----------------------------------------------------- |
| Typed       | It's a strongly typed language | It's a dynamic typed language                         |
| Paradigm    | Object oriented programming    | Prototype based programming                           |
| Scoping     | Block scoped                   | Function-scoped                                       |
| Concurrency | Thread based                   | event based                                           |
| Memory      | Uses more memory               | Uses less memory. Hence it will be used for web pages |

Q:: Does JavaScript supports namespace  
A:: JavaScript doesn’t support namespace by default. So if you create any element(function, method, object, variable) then it becomes global and pollutes the global namespace. Let's take an example of defining two functions without any namespace,

```javascript
function func1() {
  console.log("This is a first definition");
}
function func1() {
  console.log("This is a second definition");
}
func1(); // This is a second definition
```

It always calls the second function definition. In this case, namespace will solve the name collision problem.

Q:: How do you declare namespace  
A:: Even though JavaScript lacks namespaces, we can use Objects , IIFE to create namespaces.

1. **Using Object Literal Notation:** Let's wrap variables and functions inside an Object literal which acts as a namespace. After that you can access them using object notation

```javascript
var namespaceOne = {
function func1() {
console.log("This is a first definition");
}
}
var namespaceTwo = {
function func1() {
console.log("This is a second definition");
}
}
namespaceOne.func1(); // This is a first definition
namespaceTwo.func1(); // This is a second definition
```

1. **Using IIFE (Immediately invoked function expression):** The outer pair of parentheses of IIFE creates a local scope for all the code inside of it and makes the anonymous function a function expression. Due to that, you can create the same function in two different function expressions to act as a namespace.

```javascript
(function () {
  function fun1() {
    console.log("This is a first definition");
  }
  fun1();
})();
(function () {
  function fun1() {
    console.log("This is a second definition");
  }
  fun1();
})();
```

1. **Using a block and a let/const declaration:** In ECMAScript 6, you can simply use a block and a let declaration to restrict the scope of a variable to a block.

```javascript
{
  let myFunction = function fun1() {
    console.log("This is a first definition");
  };
  myFunction();
}
//myFunction(): ReferenceError: myFunction is not defined.
{
  let myFunction = function fun1() {
    console.log("This is a second definition");
  };
  myFunction();
}
//myFunction(): ReferenceError: myFunction is not defined.
```

Q:: How do you invoke javascript code in an iframe from parent page  
A:: Initially iFrame needs to be accessed using either `document.getElementBy` or `window.frames`. After that `contentWindow` property of iFrame gives the access for targetFunction

```javascript
document.getElementById("targetFrame").contentWindow.targetFunction();
window.frames[0].frameElement.contentWindow.targetFunction(); // Accessing iframe this way may not work in latest versions chrome and firefox
```

Q:: How do get the timezone offset from date  
A:: You can use the `getTimezoneOffset` method of the date object. This method returns the time zone difference, in minutes, from current locale (host system settings) to UTC

```javascript
var offset = new Date().getTimezoneOffset();
console.log(offset); // -480
```

Q:: How do you load CSS and JS files dynamically  
A:: You can create both link and script elements in the DOM and append them as child to head tag. Let's create a function to add script and style resources as below,

```javascript
function loadAssets(filename, filetype) {
  if (filetype == "css") {
    // External CSS file
    var fileReference = document.createElement("link");
    fileReference.setAttribute("rel", "stylesheet");
    fileReference.setAttribute("type", "text/css");
    fileReference.setAttribute("href", filename);
  } else if (filetype == "js") {
    // External JavaScript file
    var fileReference = document.createElement("script");
    fileReference.setAttribute("type", "text/javascript");
    fileReference.setAttribute("src", filename);
  }
  if (typeof fileReference != "undefined")
    document.getElementsByTagName("head")[0].appendChild(fileReference);
}
```

Q:: What are the different methods to find HTML elements in DOM  
A:: If you want to access any element in an HTML page, you need to start with accessing the document object. Later you can use any of the below methods to find the HTML element,

1. document.getElementById(id): It finds an element by Id
2. document.getElementsByTagName(name): It finds an element by tag name
3. document.getElementsByClassName(name): It finds an element by class name

Q:: What is jQuery  
A:: jQuery is a popular cross-browser JavaScript library that provides Document Object Model (DOM) traversal, event handling, animations and AJAX interactions by minimizing the discrepancies across browsers. It is widely famous with its philosophy of “Write less, do more”. For example, you can display welcome message on the page load using jQuery as below,

```javascript
$(document).ready(function () {
  // It selects the document and apply the function on page load
  alert("Welcome to jQuery world");
});
```

**Note:** You can download it from jquery's official site or install it from CDNs, like google.

Q:: What is V8 JavaScript engine  
A:: V8 is an open source high-performance JavaScript engine used by the Google Chrome browser, written in C++. It is also being used in the node.js project. It implements ECMAScript and WebAssembly, and runs on Windows 7 or later, macOS 10.12+, and Linux systems that use x64, IA-32, ARM, or MIPS processors.  
**Note:** It can run standalone, or can be embedded into any C++ application.

Q:: Why do we call javascript as dynamic language  
A:: JavaScript is a loosely typed or a dynamic language because variables in JavaScript are not directly associated with any particular value type, and any variable can be assigned/reassigned with values of all types.

```javascript
let age = 50; // age is a number now
age = "old"; // age is a string now
age = true; // age is a boolean
```

Q:: What is a void operator  
A:: The `void` operator evaluates the given expression and then returns undefined(i.e, without returning value). The syntax would be as below,

```javascript
void expression;
void expression;
```

Let's display a message without any redirection or reload

```javascript
<a href="javascript:void(alert('Welcome to JS world'))">
  Click here to see a message
</a>
```

**Note:** This operator is often used to obtain the undefined primitive value, using "void(0)".

Q:: How to set the cursor to wait  
A:: The cursor can be set to wait in JavaScript by using the property "cursor". Let's perform this behavior on page load using the below function.

```javascript
function myFunction() {
  window.document.body.style.cursor = "wait";
}
```

and this function invoked on page load

```html
<body onload="myFunction()"></body>
```

Q:: How do you create an infinite loop  
A:: You can create infinite loops using for and while loops without using any expressions. The for loop construct or syntax is better approach in terms of ESLint and code optimizer tools,

```javascript
for (;;) {}
while (true) {}
```

Q:: Why do you need to avoid with statement  
A:: JavaScript's with statement was intended to provide a shorthand for writing recurring accesses to objects. So it can help reduce file size by reducing the need to repeat a lengthy object reference without performance penalty. Let's take an example where it is used to avoid redundancy when accessing an object several times.

```javascript
a.b.c.greeting = "welcome";
a.b.c.age = 32;
```

Using `with` it turns this into:

```javascript
with (a.b.c) {
  greeting = "welcome";
  age = 32;
}
```

But this `with` statement creates performance problems since one cannot predict whether an argument will refer to a real variable or to a property inside the with argument.

Q:: What is the output of below for loops  
A:: ```javascript  
for (var i = 0; i < 4; i++) {  
// global scope  
setTimeout(() => console.log(i));  
}  
for (let i = 0; i < 4; i++) {  
// block scope  
setTimeout(() => console.log(i));  
}

````
The output of the above for loops is 4 4 4 4 and 0 1 2 3
**Explanation:** Due to the event queue/loop of javascript, the `setTimeout` callback function is called after the loop has been executed. Since the variable i is declared with the `var` keyword it became a global variable and the value was equal to 4 using iteration when the time `setTimeout` function is invoked. Hence, the output of the first loop is `4 4 4 4`.
Whereas in the second loop, the variable i is declared as the `let` keyword it becomes a block scoped variable and it holds a new value(0, 1 ,2 3) for each iteration. Hence, the output of the first loop is `0 1 2 3`.

Q:: List down some of the features of ES6
A:: Below are the list of some new features of ES6,
1. Support for constants or immutable variables
2. Block-scope support for variables, constants and functions
3. Arrow functions
4. Default parameters
5. Rest and Spread Parameters
6. Template Literals
7. Multi-line Strings
8. Destructuring Assignment
9. Enhanced Object Literals
10. Promises
11. Classes
12. Modules

Q:: What is ES6
A:: ES6 is the sixth edition of the javascript language and it was released in June 2015. It was initially known as ECMAScript 6 (ES6) and later renamed to ECMAScript 2015. Almost all the modern browsers support ES6 but for the old browsers there are many transpilers, like Babel.js etc.

Q:: Can I redeclare let and const variables
A:: No, you cannot redeclare let and const variables. If you do, it throws below error
```bash
Uncaught SyntaxError: Identifier 'someVariable' has already been declared
````

**Explanation:** The variable declaration with `var` keyword refers to a function scope and the variable is treated as if it were declared at the top of the enclosing scope due to hoisting feature. So all the multiple declarations contributing to the same hoisted variable without any error. Let's take an example of re-declaring variables in the same scope for both var and let/const variables.

```javascript
var name = "John";
function myFunc() {
  var name = "Nick";
  var name = "Abraham"; // Re-assigned in the same function block
  alert(name); // Abraham
}
myFunc();
alert(name); // John
```

The block-scoped multi-declaration throws syntax error,

```javascript
let name = "John";
function myFunc() {
  let name = "Nick";
  let name = "Abraham"; // Uncaught SyntaxError: Identifier 'name' has already been declared
  alert(name);
}
myFunc();
alert(name);
```

Q:: Is const variable makes the value immutable  
A:: No, the const variable doesn't make the value immutable. But it disallows subsequent assignments(i.e, You can declare with assignment but can't assign another value later)

```javascript
const userList = [];
userList.push("John"); // Can mutate even though it can't re-assign
console.log(userList); // ['John']
```

Q:: What are default parameters  
A:: In ES5, we need to depend on logical OR operators to handle default values of function parameters. Whereas in ES6, Default function parameters feature allows parameters to be initialized with default values if no value or undefined is passed. Let's compare the behavior with an examples,

```javascript
//ES5
var calculateArea = function (height, width) {
  height = height || 50;
  width = width || 60;
  return width * height;
};
console.log(calculateArea()); //300
```

The default parameters makes the initialization more simpler,

```javascript
//ES6
var calculateArea = function (height = 50, width = 60) {
  return width * height;
};
console.log(calculateArea()); //300
```

Q:: What are template literals  
A:: Template literals or template strings are string literals allowing embedded expressions. These are enclosed by the back-tick (`) character instead of double or single quotes.  
In ES6, this feature enables using dynamic expressions as below,

```javascript
var greeting = `Welcome to JS World, Mr. ${firstName} ${lastName}.`;
```

In ES5, you need break string like below,

```javascript
var greeting = 'Welcome to JS World, Mr. ' + firstName + ' ' + lastName.`
```

**Note:** You can use multi-line strings and string interpolation features with template literals.

Q:: How do you write multi-line strings in template literals  
A:: In ES5, you would have to use newline escape characters('\\n') and concatenation symbols(+) in order to get multi-line strings.

```javascript
console.log("This is string sentence 1\n" + "This is string sentence 2");
```

Whereas in ES6, You don't need to mention any newline sequence character,

```javascript
console.log(`This is string sentence
'This is string sentence 2`);
```

Q:: What are nesting templates  
A:: The nesting template is a feature supported within template literals syntax to allow inner backticks inside a placeholder ${ } within the template. For example, the below nesting template is used to display the icons based on user permissions whereas outer template checks for platform type,

```javascript
const iconStyles = `icon ${
  isMobilePlatform() ? "" : `icon-${user.isAuthorized ? "submit" : "disabled"}`
}`;
```

You can write the above use case without nesting template features as well. However, the nesting template feature is more compact and readable.

```javascript
//Without nesting templates
const iconStyles = `icon ${
  isMobilePlatform() ? "" : user.isAuthorized ? "icon-submit" : "icon-disabled"
}`;
```

Q:: What are tagged templates  
A:: Tagged templates are the advanced form of templates in which tags allow you to parse template literals with a function. The tag function accepts the first parameter as an array of strings and remaining parameters as expressions. This function can also return manipulated strings based on parameters. Let's see the usage of this tagged template behavior of an IT professional skill set in an organization,

```javascript
var user1 = "John";
var skill1 = "JavaScript";
var experience1 = 15;
var user2 = "Kane";
var skill2 = "JavaScript";
var experience2 = 5;
function myInfoTag(strings, userExp, experienceExp, skillExp) {
  var str0 = strings[0]; // "Mr/Ms. "
  var str1 = strings[1]; // " is a/an "
  var str2 = strings[2]; // "in"
  var expertiseStr;
  if (experienceExp > 10) {
    expertiseStr = "expert developer";
  } else if (skillExp > 5 && skillExp <= 10) {
    expertiseStr = "senior developer";
  } else {
    expertiseStr = "junior developer";
  }
  return `${str0}${userExp}${str1}${expertiseStr}${str2}${skillExp}`;
}
var output1 = myInfoTag`Mr/Ms. ${user1} is a/an ${experience1} in ${skill1}`;
var output2 = myInfoTag`Mr/Ms. ${user2} is a/an ${experience2} in ${skill2}`;
console.log(output1); // Mr/Ms. John is a/an expert developer in JavaScript
console.log(output2); // Mr/Ms. Kane is a/an junior developer in JavaScript
```

Q:: What are raw strings  
A:: ES6 provides a raw strings feature using the `String.raw()` method which is used to get the raw string form of template strings. This feature allows you to access the raw strings as they were entered, without processing escape sequences. For example, the usage would be as below,

```javascript
var calculationString = String.raw`The sum of numbers is \n${1 + 2 + 3 + 4}!`;
console.log(calculationString); // The sum of numbers is \n10!
```

If you don't use raw strings, the newline character sequence will be processed by displaying the output in multiple lines

```javascript
var calculationString = `The sum of numbers is \n${1 + 2 + 3 + 4}!`;
console.log(calculationString);
// The sum of numbers is
// 10!
```

Also, the raw property is available on the first argument to the tag function

```javascript
function tag(strings) {
  console.log(strings.raw[0]);
}
```

Q:: What is destructuring assignment  
A:: The destructuring assignment is a JavaScript expression that makes it possible to unpack values from arrays or properties from objects into distinct variables.  
Let's get the month values from an array using destructuring assignment

```javascript
var [one, two, three] = ["JAN", "FEB", "MARCH"];
console.log(one); // "JAN"
console.log(two); // "FEB"
console.log(three); // "MARCH"
```

and you can get user properties of an object using destructuring assignment,

```javascript
var { name, age } = { name: "John", age: 32 };
console.log(name); // John
console.log(age); // 32
```

Q:: What are default values in destructuring assignment  
A:: A variable can be assigned a default value when the value unpacked from the array or object is undefined during destructuring assignment. It helps to avoid setting default values separately for each assignment. Let's take an example for both arrays and object use cases,  
**Arrays destructuring:**

```javascript
var x, y, z;
[x = 2, y = 4, z = 6] = [10];
console.log(x); // 10
console.log(y); // 4
console.log(z); // 6
```

**Objects destructuring:**

```javascript
var { x = 2, y = 4, z = 6 } = { x: 10 };
console.log(x); // 10
console.log(y); // 4
console.log(z); // 6
```

Q:: How do you swap variables in destructuring assignment  
A:: If you don't use destructuring assignment, swapping two values requires a temporary variable. Whereas using a destructuring feature, two variable values can be swapped in one destructuring expression. Let's swap two number variables in array destructuring assignment,

```javascript
var x = 10,
  y = 20;
[x, y] = [y, x];
console.log(x); // 20
console.log(y); // 10
```

Q:: What are enhanced object literals  
A:: Object literals make it easy to quickly create objects with properties inside the curly braces. For example, it provides shorter syntax for common object property definition as below.

```javascript
//ES6
var x = 10,
  y = 20;
obj = { x, y };
console.log(obj); // {x: 10, y:20}
//ES5
var x = 10,
  y = 20;
obj = { x: x, y: y };
console.log(obj); // {x: 10, y:20}
```

Q:: What are dynamic imports  
A:: The dynamic imports using `import()` function syntax allows us to load modules on demand by using promises or the async/await syntax. Currently this feature is in [stage4 proposal](https://github.com/tc39/proposal-dynamic-import). The main advantage of dynamic imports is reduction of our bundle's sizes, the size/payload response of our requests and overall improvements in the user experience.  
The syntax of dynamic imports would be as below,

```javascript
import("./Module").then((Module) => Module.method());
```

Q:: What are the use cases for dynamic imports  
A:: Below are some of the use cases of using dynamic imports over static imports,

1. Import a module on-demand or conditionally. For example, if you want to load a polyfill on legacy browser

```javascript
if (isLegacyBrowser()) {
import(···)
.then(···);
}
```

1. Compute the module specifier at runtime. For example, you can use it for internationalization.

```javascript
import(`messages_${getLocale()}.js`).then(···);
```

1. Import a module from within a regular script instead a module.

Q:: What are typed arrays  
A:: Typed arrays are array-like objects from ECMAScript 6 API for handling binary data. JavaScript provides 8 Typed array types,

1. Int8Array: An array of 8-bit signed integers
2. Int16Array: An array of 16-bit signed integers
3. Int32Array: An array of 32-bit signed integers
4. Uint8Array: An array of 8-bit unsigned integers
5. Uint16Array: An array of 16-bit unsigned integers
6. Uint32Array: An array of 32-bit unsigned integers
7. Float32Array: An array of 32-bit floating point numbers
8. Float64Array: An array of 64-bit floating point numbers
   For example, you can create an array of 8-bit signed integers as below

```javascript
const a = new Int8Array();
// You can pre-allocate n bytes
const bytes = 1024;
const a = new Int8Array(bytes);
```

Q:: What are the advantages of module loaders  
A:: The module loaders provides the below features,

1. Dynamic loading
2. State isolation
3. Global namespace isolation
4. Compilation hooks
5. Nested virtualization

Q:: What is collation  
A:: Collation is used for sorting a set of strings and searching within a set of strings. It is parameterized by locale and aware of Unicode. Let's take comparison and sorting features,

1. **Comparison:**

```javascript
var list = ["ä", "a", "z"]; // In German,  "ä" sorts with "a" Whereas in Swedish, "ä" sorts after "z"
var l10nDE = new Intl.Collator("de");
var l10nSV = new Intl.Collator("sv");
console.log(l10nDE.compare("ä", "z") === -1); // true
console.log(l10nSV.compare("ä", "z") === +1); // true
```

1. **Sorting:**

```javascript
var list = ["ä", "a", "z"]; // In German,  "ä" sorts with "a" Whereas in Swedish, "ä" sorts after "z"
var l10nDE = new Intl.Collator("de");
var l10nSV = new Intl.Collator("sv");
console.log(list.sort(l10nDE.compare)); // [ "a", "ä", "z" ]
console.log(list.sort(l10nSV.compare)); // [ "a", "z", "ä" ]
```

Q:: What is for...of statement  
A:: The for...of statement creates a loop iterating over iterable objects or elements such as built-in String, Array, Array-like objects (like arguments or NodeList), TypedArray, Map, Set, and user-defined iterables. The basic usage of for...of statement on arrays would be as below,

```javascript
let arrayIterable = [10, 20, 30, 40, 50];
for (let value of arrayIterable) {
  value++;
  console.log(value); // 11 21 31 41 51
}
```

Q:: What is the output of below spread operator array  
A:: ```javascript  
[..."John Resig"];

````
The output of the array is ['J', 'o', 'h', 'n', '', 'R', 'e', 's', 'i', 'g']
**Explanation:** The string is an iterable type and the spread operator within an array maps every character of an iterable to one element. Hence, each character of a string becomes an element within an Array.

Q:: Is PostMessage secure
A:: Yes, postMessages can be considered very secure as long as the programmer/developer is careful about checking the origin and source of an arriving message. But if you try to send/receive a message without verifying its source will create cross-site scripting attacks.

Q:: What are the problems with postmessage target origin as wildcard
A:: The second argument of postMessage method specifies which origin is allowed to receive the message. If you use the wildcard “\*” as an argument then any origin is allowed to receive the message. In this case, there is no way for the sender window to know if the target window is at the target origin when sending the message. If the target window has been navigated to another origin, the other origin would receive the data. Hence, this may lead to XSS vulnerabilities.
```javascript
targetWindow.postMessage(message, "*");
````

Q:: How do you avoid receiving postMessages from attackers  
A:: Since the listener listens for any message, an attacker can trick the application by sending a message from the attacker’s origin, which gives an impression that the receiver received the message from the actual sender’s window. You can avoid this issue by validating the origin of the message on the receiver's end using the “message.origin” attribute. For examples, let's check the sender's origin [http://www.some-sender.com](http://www.some-sender.com) on receiver side [www.some-receiver.com](www.some-receiver.com),

```javascript
//Listener on http://www.some-receiver.com/
window.addEventListener("message", function(message){
if(/^http://www\.some-sender\.com$/.test(message.origin)){
console.log('You received the data from valid sender', message.data);
}
});
```

Q:: Can I avoid using postMessages completely  
A:: You cannot avoid using postMessages completely(or 100%). Even though your application doesn’t use postMessage considering the risks, a lot of third party scripts use postMessage to communicate with the third party service. So your application might be using postMessage without your knowledge.

Q:: Is postMessages synchronous  
A:: The postMessages are synchronous in IE8 browser but they are asynchronous in IE9 and all other modern browsers (i.e, IE9+, Firefox, Chrome, Safari).Due to this asynchronous behaviour, we use a callback mechanism when the postMessage is returned.

Q:: What paradigm is Javascript  
A:: JavaScript is a multi-paradigm language, supporting imperative/procedural programming, Object-Oriented Programming and functional programming. JavaScript supports Object-Oriented Programming with prototypical inheritance.

Q:: What is the difference between internal and external javascript  
A:: **Internal JavaScript:** It is the source code within the script tag.  
**External JavaScript:** The source code is stored in an external file(stored with .js extension) and referred with in the tag.

Q:: Is JavaScript faster than server side script  
A:: Yes, JavaScript is faster than server side scripts. Because JavaScript is a client-side script it does not require any web server’s help for its computation or calculation. So JavaScript is always faster than any server-side script like ASP, PHP, etc.

Q:: How do you get the status of a checkbox  
A:: You can apply the `checked` property on the selected checkbox in the DOM. If the value is `true` it means the checkbox is checked, otherwise it is unchecked. For example, the below HTML checkbox element can be access using javascript as below:

```html
<input type="checkbox" id="checkboxname" value="Agree" /> Agree the
conditions<br />
```

```javascript
console.log(document.getElementById(‘checkboxname’).checked); // true or false
```

Q:: What is the purpose of double tilde operator  
A:: The double tilde operator(~~) is known as double NOT bitwise operator. This operator is a slightly quicker substitute for Math.floor().

Q:: How do you convert character to ASCII code  
A:: You can use the `String.prototype.charCodeAt()` method to convert string characters to ASCII numbers. For example, let's find ASCII code for the first letter of 'ABC' string,

```javascript
"ABC".charCodeAt(0); // returns 65
```

Whereas `String.fromCharCode()` method converts numbers to equal ASCII characters.

```javascript
String.fromCharCode(65, 66, 67); // returns 'ABC'
```

Q:: What is ArrayBuffer  
A:: An ArrayBuffer object is used to represent a generic, fixed-length raw binary data buffer. You can create it as below,

```javascript
let buffer = new ArrayBuffer(16); // create a buffer of length 16
alert(buffer.byteLength); // 16
```

To manipulate an ArrayBuffer, we need to use a “view” object.

```javascript
//Create a DataView referring to the buffer
let view = new DataView(buffer);
```

Q:: What is the output of below string expression  
A:: ```javascript  
console.log("Welcome to JS world"[0]);

````
The output of the above expression is "W".
**Explanation:** The bracket notation with specific index on a string returns the character at a specific location. Hence, it returns the character "W" of the string. Since this is not supported in IE7 and below versions, you may need to use the .charAt() method to get the desired result.

Q:: What is the purpose of Error object
A:: The Error constructor creates an error object and the instances of error objects are thrown when runtime errors occur. The Error object can also be used as a base object for user-defined exceptions. The syntax of error object would be as below,
```javascript
new Error([message[, fileName[, lineNumber]]])
````

You can throw user defined exceptions or errors using Error object in try...catch block as below,

```javascript
try {
  if (withdraw > balance)
    throw new Error("Oops! You don't have enough balance");
} catch (e) {
  console.log(e.name + ": " + e.message);
}
```

Q:: What is the purpose of EvalError object  
A:: The EvalError object indicates an error regarding the global `eval()` function. Even though this exception is not thrown by JavaScript anymore, the EvalError object remains for compatibility. The syntax of this expression would be as below,

```javascript
new EvalError([message[, fileName[, lineNumber]]])
```

You can throw EvalError with in try...catch block as below,

```javascript
try {
throw new EvalError('Eval function error', 'someFile.js', 100);
} catch (e) {
console.log(e.message, e.name, e.fileName);              // "Eval function error", "EvalError", "someFile.js"
```

Q:: What are the list of cases error thrown from non-strict mode to strict mode  
A:: When you apply 'use strict'; syntax, some of the below cases will throw a SyntaxError before executing the script

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

Hence, the errors from above cases are helpful to avoid errors in development/production environments.

Q:: Do all objects have prototypes  
A:: No. All objects have prototypes except for the base object which is created by the user, or an object that is created using the new keyword.

Q:: What is the difference between a parameter and an argument  
A:: Parameter is the variable name of a function definition whereas an argument represents the value given to a function when it is invoked. Let's explain this with a simple function

```javascript
function myFunction(parameter1, parameter2, parameter3) {
  console.log(arguments[0]); // "argument1"
  console.log(arguments[1]); // "argument2"
  console.log(arguments[2]); // "argument3"
}
myFunction("argument1", "argument2", "argument3");
```

Q:: What is the purpose of some method in arrays  
A:: The some() method is used to test whether at least one element in the array passes the test implemented by the provided function. The method returns a boolean value. Let's take an example to test for any odd elements,

```javascript
var array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
var odd = (element) => element % 2 !== 0;
console.log(array.some(odd)); // true (the odd element exists)
```

Q:: How do you combine two or more arrays  
A:: The concat() method is used to join two or more arrays by returning a new array containing all the elements. The syntax would be as below,

```javascript
array1.concat(array2, array3, ..., arrayX)
```

Let's take an example of array's concatenation with veggies and fruits arrays,

```javascript
var veggies = ["Tomato", "Carrot", "Cabbage"];
var fruits = ["Apple", "Orange", "Pears"];
var veggiesAndFruits = veggies.concat(fruits);
console.log(veggiesAndFruits); // Tomato, Carrot, Cabbage, Apple, Orange, Pears
```

Q:: What is the difference between Shallow and Deep copy  
A:: There are two ways to copy an object,  
**Shallow Copy:**  
Shallow copy is a bitwise copy of an object. A new object is created that has an exact copy of the values in the original object. If any of the fields of the object are references to other objects, just the reference addresses are copied i.e., only the memory address is copied.  
**Example**

```javascript
var empDetails = {
  name: "John",
  age: 25,
  expertise: "Software Developer",
};
```

to create a duplicate

```javascript
var empDetailsShallowCopy = empDetails; //Shallow copying!
```

if we change some property value in the duplicate one like this:

```javascript
empDetailsShallowCopy.name = "Johnson";
```

The above statement will also change the name of `empDetails`, since we have a shallow copy. That means we're losing the original data as well.
**Deep copy:**
A deep copy copies all fields, and makes copies of dynamically allocated memory pointed to by the fields. A deep copy occurs when an object is copied along with the objects to which it refers.
**Example**

```javascript
var empDetails = {
  name: "John",
  age: 25,
  expertise: "Software Developer",
};
```

Create a deep copy by using the properties from the original object into new variable

```javascript
var empDetailsDeepCopy = {
  name: empDetails.name,
  age: empDetails.age,
  expertise: empDetails.expertise,
};
```

Now if you change `empDetailsDeepCopy.name`, it will only affect `empDetailsDeepCopy` & not `empDetails`

Q:: How do you create specific number of copies of a string  
A:: The `repeat()` method is used to construct and return a new string which contains the specified number of copies of the string on which it was called, concatenated together. Remember that this method has been added to the ECMAScript 2015 specification.  
Let's take an example of Hello string to repeat it 4 times,

```javascript
"Hello".repeat(4); // 'HelloHelloHelloHello'
```

Q:: How do you return all matching strings against a regular expression  
A:: The `matchAll()` method can be used to return an iterator of all results matching a string against a regular expression. For example, the below example returns an array of matching string results against a regular expression,

```javascript
let regexp = /Hello(\d?))/g;
let greeting = "Hello1Hello2Hello3";
let greetingList = [...greeting.matchAll(regexp)];
console.log(greetingList[0]); //Hello1
console.log(greetingList[1]); //Hello2
console.log(greetingList[2]); //Hello3
```

Q:: How do you trim a string at the beginning or ending  
A:: The `trim` method of string prototype is used to trim on both sides of a string. But if you want to trim especially at the beginning or ending of the string then you can use `trimStart/trimLeft` and `trimEnd/trimRight` methods. Let's see an example of these methods on a greeting message,

```javascript
var greeting = "   Hello, Goodmorning!   ";
console.log(greeting); // "   Hello, Goodmorning!   "
console.log(greeting.trimStart()); // "Hello, Goodmorning!   "
console.log(greeting.trimLeft()); // "Hello, Goodmorning!   "
console.log(greeting.trimEnd()); // "   Hello, Goodmorning!"
console.log(greeting.trimRight()); // "   Hello, Goodmorning!"
```

Q:: What is the output of below console statement with unary operator  
A:: Let's take console statement with unary operator as given below,

```javascript
console.log(+"Hello");
```

The output of the above console log statement returns NaN. Because the element is prefixed by the unary operator and the JavaScript interpreter will try to convert that element into a number type. Since the conversion fails, the value of the statement results in NaN value.

Q:: Does javascript uses mixins  
A:: Mixin is a generic object-oriented programming term - is a class containing methods that can be used by other classes without a need to inherit from it. In JavaScript we can only inherit from a single object. ie. There can be only one `[[prototype]]` for an object.  
But sometimes we require to extend more than one, to overcome this we can use Mixin which helps to copy methods to the prototype of another class.  
Say for instance, we've two classes `User` and `CleanRoom`. Suppose we need to add `CleanRoom` functionality to `User`, so that user can clean the room at demand. Here's where concept called mixins comes into picture.

```javascript
// mixin
let cleanRoomMixin = {
  cleanRoom() {
    alert(`Hello ${this.name}, your room is clean now`);
  },
  sayBye() {
    alert(`Bye ${this.name}`);
  },
};
// usage:
class User {
  constructor(name) {
    this.name = name;
  }
}
// copy the methods
Object.assign(User.prototype, cleanRoomMixin);
// now User can clean the room
new User("Dude").cleanRoom(); // Hello Dude, your room is clean now!
```

Q:: What is a thunk function  
A:: A thunk is just a function which delays the evaluation of the value. It doesn’t take any arguments but gives the value whenever you invoke the thunk. i.e, It is used not to execute now but it will be sometime in the future. Let's take a synchronous example,

```javascript
const add = (x, y) => x + y;
const thunk = () => add(2, 3);
thunk(); // 5
```

Q:: What are asynchronous thunks  
A:: The asynchronous thunks are useful to make network requests. Let's see an example of network requests,

```javascript
function fetchData(fn) {
  fetch("https://jsonplaceholder.typicode.com/todos/1")
    .then((response) => response.json())
    .then((json) => fn(json));
}
const asyncThunk = function () {
  return fetchData(function getData(data) {
    console.log(data);
  });
};
asyncThunk();
```

The `getData` function won't be called immediately but it will be invoked only when the data is available from API endpoint. The setTimeout function is also used to make our code asynchronous. The best real time example is redux state management library which uses the asynchronous thunks to delay the actions to dispatch.

Q:: What is the output of below function calls  
A:: **Code snippet:**

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

**Output:**
The output is 40 and NaN. Remember that diameter is a regular function, whereas the value of perimeter is an arrow function. The `this` keyword of a regular function(i.e, diameter) refers to the surrounding scope which is a class(i.e, Shape object). Whereas this keyword of perimeter function refers to the surrounding scope which is a window object. Since there is no radius property on window objects it returns an undefined value and the multiple of number value returns NaN value.

Q:: How to remove all line breaks from a string  
A:: The easiest approach is using regular expressions to detect and replace newlines in the string. In this case, we use replace function along with string to replace with, which in our case is an empty string.

```javascript
function remove_linebreaks( var message ) {
return message.replace( /[\r\n]+/gm, "" );
}
```

In the above expression, g and m are for global and multiline flags.

Q:: What is the difference between reflow and repaint  
A:: A _repaint_ occurs when changes are made which affect the visibility of an element, but not its layout. Examples of this include outline, visibility, or background color. A _reflow_ involves changes that affect the layout of a portion of the page (or the whole page). Resizing the browser window, changing the font, content changing (such as user typing text), using JavaScript methods involving computed styles, adding or removing elements from the DOM, and changing an element's classes are a few of the things that can trigger reflow. Reflow of an element causes the subsequent reflow of all child and ancestor elements as well as any elements following it in the DOM.

Q:: What happens with negating an array  
A:: Negating an array with `!` character will coerce the array into a boolean. Since Arrays are considered to be truthy So negating it will return `false`.

```javascript
console.log(![]); // false
```

Q:: What happens if we add two arrays  
A:: If you add two arrays together, it will convert them both to strings and concatenate them. For example, the result of adding arrays would be as below,

```javascript
console.log(["a"] + ["b"]); // "ab"
console.log([] + []); // ""
console.log(![] + []); // "false", because ![] returns false.
```

Q:: What is the output of prepend additive operator on falsy values  
A:: If you prepend the additive(+) operator on falsy values(null, undefined, NaN, false, ""), the falsy value converts to a number value zero. Let's display them on browser console as below,

```javascript
console.log(+null); // 0
console.log(+undefined); // NaN
console.log(+false); // 0
console.log(+NaN); // NaN
console.log(+""); // 0
```

Q:: How do you create self string using special characters  
A:: The self string can be formed with the combination of `[]()!+` characters. You need to remember the below conventions to achieve this pattern.

1. Since Arrays are truthful values, negating the arrays will produce false: ![] === false
2. As per JavaScript coercion rules, the addition of arrays together will toString them: [] + [] === ""
3. Prepend an array with + operator will convert an array to false, the negation will make it true and finally converting the result will produce value '1': +(!(+[])) === 1
   By applying the above rules, we can derive below conditions

```javascript
(![] + [] === "false" + !+[]) === 1;
```

Now the character pattern would be created as below,

```javascript
s               e               l               f
^^^^^^^^^^^^^   ^^^^^^^^^^^^^   ^^^^^^^^^^^^^   ^^^^^^^^^^^^^
(![] + [])[3] + (![] + [])[4] + (![] + [])[2] + (![] + [])[0]
^^^^^^^^^^^^^   ^^^^^^^^^^^^^   ^^^^^^^^^^^^^   ^^^^^^^^^^^^^
(![] + [])[+!+[]+!+[]+!+[]] +
(![] + [])[+!+[]+!+[]+!+[]+!+[]] +
(![] + [])[+!+[]+!+[]] +
(![] + [])[+[]]
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
(![]+[])[+!+[]+!+[]+!+[]]+(![]+[])[+!+[]+!+[]+!+[]+!+[]]+(![]+[])[+!+[]+!+[]]+(![]+[])[+[]]
```

Q:: How do you remove falsy values from an array  
A:: You can apply the filter method on the array by passing Boolean as a parameter. This way it removes all falsy values(0, undefined, null, false and "") from the array.

```javascript
const myArray = [false, null, 1, 5, undefined];
myArray.filter(Boolean); // [1, 5] // is same as myArray.filter(x => x);
```

Q:: How do you get unique values of an array  
A:: You can get unique values of an array with the combination of `Set` and rest expression/spread(...) syntax.

```javascript
console.log([...new Set([1, 2, 4, 4, 3])]); // [1, 2, 4, 3]
```

Q:: What is destructuring aliases  
A:: Sometimes you would like to have a destructured variable with a different name than the property name. In that case, you'll use a `: newName` to specify a name for the variable. This process is called destructuring aliases.

```javascript
const obj = { x: 1 };
// Grabs obj.x as as { otherName }
const { x: otherName } = obj;
```

Q:: How do you map the array values without using map method  
A:: You can map the array values without using the `map` method by just using the `from` method of Array. Let's map city names from Countries array,

```javascript
const countries = [
  { name: "India", capital: "Delhi" },
  { name: "US", capital: "Washington" },
  { name: "Russia", capital: "Moscow" },
  { name: "Singapore", capital: "Singapore" },
  { name: "China", capital: "Beijing" },
  { name: "France", capital: "Paris" },
];
const cityNames = Array.from(countries, ({ capital }) => capital);
console.log(cityNames); // ['Delhi, 'Washington', 'Moscow', 'Singapore', 'Beijing', 'Paris']
```

Q:: How do you empty an array  
A:: You can empty an array quickly by setting the array length to zero.

```javascript
let cities = ["Singapore", "Delhi", "London"];
cities.length = 0; // cities becomes []
```

Q:: How do you rounding numbers to certain decimals  
A:: You can round numbers to a certain number of decimals using `toFixed` method from native javascript.

```javascript
let pie = 3.141592653;
pie = pie.toFixed(3); // 3.142
```

Q:: What is the easiest way to convert an array to an object  
A:: You can convert an array to an object with the same data using spread(...) operator.

```javascript
var fruits = ["banana", "apple", "orange", "watermelon"];
var fruitsObject = { ...fruits };
console.log(fruitsObject); // {0: "banana", 1: "apple", 2: "orange", 3: "watermelon"}
```

Q:: How do you create an array with some data  
A:: You can create an array with some data or an array with the same values using `fill` method.

```javascript
var newArray = new Array(5).fill("0");
console.log(newArray); // ["0", "0", "0", "0", "0"]
```

Q:: What are the placeholders from console object  
A:: Below are the list of placeholders available from console object,

1. %o — It takes an object,
2. %s — It takes a string,
3. %d — It is used for a decimal or integer
   These placeholders can be represented in the console.log as below

```javascript
const user = { name: "John", id: 1, city: "Delhi" };
console.log(
  "Hello %s, your details %o are available in the object form",
  "John",
  user,
); // Hello John, your details {name: "John", id: 1, city: "Delhi"} are available in object
```

Q:: Is it possible to add CSS to console messages  
A:: Yes, you can apply CSS styles to console messages similar to html text on the web page.

```javascript
console.log(
  "%c The text has blue color, with large font and red background",
  "color: blue; font-size: x-large; background: red",
);
```

The text will be displayed as below,
![console-css](../images/console-css.png)
**Note:** All CSS styles can be applied to console messages.

Q:: What is the purpose of dir method of console object  
A:: The `console.dir()` is used to display an interactive list of the properties of the specified JavaScript object as JSON.

```javascript
const user = { name: "John", id: 1, city: "Delhi" };
console.dir(user);
```

The user object displayed in JSON representation
![console-dir](../images/console-dir.png)

Q:: Is it possible to debug HTML elements in console  
A:: Yes, it is possible to get and debug HTML elements in the console just like inspecting elements.

```javascript
const element = document.getElementsByTagName("body")[0];
console.log(element);
```

It prints the HTML element in the console,
![console-html](../images/console-html.png)

Q:: How do you display data in a tabular format using console object  
A:: The `console.table()` is used to display data in the console in a tabular format to visualize complex arrays or objects.

```js
const users = [
  { name: "John", id: 1, city: "Delhi" },
  { name: "Max", id: 2, city: "London" },
  { name: "Rod", id: 3, city: "Paris" },
];
console.table(users);
```

The data visualized in a table format,
![console-table](../images/console-table.png)
**Not:** Remember that `console.table()` is not supported in IE.

Q:: How do you verify that an argument is a Number or not  
A:: The combination of IsNaN and isFinite methods are used to confirm whether an argument is a number or not.

```javascript
function isNumber(n) {
  return !isNaN(parseFloat(n)) && isFinite(n);
}
```

Q:: How do you create copy to clipboard button  
A:: You need to select the content(using .select() method) of the input element and execute the copy command with execCommand (i.e, execCommand('copy')). You can also execute other system commands like cut and paste.

```javascript
document.querySelector("#copy-button").onclick = function () {
  // Select the content
  document.querySelector("#copy-input").select();
  // Copy to the clipboard
  document.execCommand("copy");
};
```

Q:: What is the shortcut to get timestamp  
A:: You can use `new Date().getTime()` to get the current timestamp. There is an alternative shortcut to get the value.

```javascript
console.log(+new Date());
console.log(Date.now());
```

Q:: How do you flattening multi dimensional arrays  
A:: Flattening bi-dimensional arrays is trivial with Spread operator.

```javascript
const biDimensionalArr = [11, [22, 33], [44, 55], [66, 77], 88, 99];
const flattenArr = [].concat(...biDimensionalArr); // [11, 22, 33, 44, 55, 66, 77, 88, 99]
```

But you can make it work with multi-dimensional arrays by recursive calls,

```javascript
function flattenMultiArray(arr) {
  const flattened = [].concat(...arr);
  return flattened.some((item) => Array.isArray(item))
    ? flattenMultiArray(flattened)
    : flattened;
}
const multiDimensionalArr = [11, [22, 33], [44, [55, 66, [77, [88]], 99]]];
const flatArr = flattenMultiArray(multiDimensionalArr); // [11, 22, 33, 44, 55, 66, 77, 88, 99]
```

Also you can use the `flat` method of Array.

```javascript
const arr = [1, [2, 3], 4, 5, [6, 7]];
const fllattenArr = arr.flat(); // [1, 2, 3, 4, 5, 6, 7]
// And for multiDemensional arrays
const multiDimensionalArr = [11, [22, 33], [44, [55, 66, [77, [88]], 99]]];
const oneStepFlat = multiDimensionalArr.flat(1); // [11, 22, 33, 44, [55, 66, [77, [88]], 99]]
const towStep = multiDimensionalArr.flat(2); // [11, 22, 33, 44, 55, 66, [77, [88]], 99]
const fullyFlatArray = multiDimensionalArr.flat(Infinity); // [11, 22, 33, 44, 55, 66, 77, 88, 99]
```

Q:: What is the easiest multi condition checking  
A:: You can use `indexOf` to compare input with multiple values instead of checking each value as one condition.

```javascript
// Verbose approach
if (input === "first" || input === 1 || input === "second" || input === 2) {
  someFunction();
}
// Shortcut
if (["first", 1, "second", 2].indexOf(input) !== -1) {
  someFunction();
}
```

Q:: How do you capture browser back button  
A:: The `window.onbeforeunload` method is used to capture browser back button events. This is helpful to warn users about losing the current data.

```javascript
window.onbeforeunload = function () {
  alert("You work will be lost");
};
```

Q:: How do you disable right click in the web page  
A:: The right click on the page can be disabled by returning false from the `oncontextmenu` attribute on the body element.

```html
<body oncontextmenu="return false;"></body>
```

Q:: What are wrapper objects  
A:: Primitive Values like string,number and boolean don't have properties and methods but they are temporarily converted or coerced to an object(Wrapper object) when you try to perform actions on them. For example, if you apply toUpperCase() method on a primitive string value, it does not throw an error but returns uppercase of the string.

```javascript
let name = "john";
console.log(name.toUpperCase()); // Behind the scenes treated as console.log(new String(name).toUpperCase());
```

i.e, Every primitive except null and undefined have Wrapper Objects and the list of wrapper objects are String,Number,Boolean,Symbol and BigInt.

Q:: What is AJAX  
A:: AJAX stands for Asynchronous JavaScript and XML and it is a group of related technologies(HTML, CSS, JavaScript, XMLHttpRequest API etc) used to display data asynchronously. i.e. We can send data to the server and get data from the server without reloading the web page.

Q:: What are the different ways to deal with Asynchronous Code  
A:: Below are the list of different ways to deal with Asynchronous code.

1. Callbacks
2. Promises
3. Async/await
4. Third-party libraries such as async.js,bluebird etc

Q:: How to cancel a fetch request  
A:: Until a few days back, One shortcoming of native promises is no direct way to cancel a fetch request. But the new `AbortController` from js specification allows you to use a signal to abort one or multiple fetch calls.  
The basic flow of cancelling a fetch request would be as below,

1. Create an `AbortController` instance
2. Get the signal property of an instance and pass the signal as a fetch option for signal
3. Call the AbortController's abort property to cancel all fetches that use that signal
   For example, let's pass the same signal to multiple fetch calls will cancel all requests with that signal,

```javascript
const controller = new AbortController();
const { signal } = controller;
fetch("http://localhost:8000", { signal })
  .then((response) => {
    console.log(`Request 1 is complete!`);
  })
  .catch((e) => {
    if (e.name === "AbortError") {
      // We know it's been canceled!
    }
  });
fetch("http://localhost:8000", { signal })
  .then((response) => {
    console.log(`Request 2 is complete!`);
  })
  .catch((e) => {
    if (e.name === "AbortError") {
      // We know it's been canceled!
    }
  });
// Wait 2 seconds to abort both requests
setTimeout(() => controller.abort(), 2000);
```

Q:: What is web speech API  
A:: Web speech API is used to enable modern browsers recognize and synthesize speech(i.e, voice data into web apps). This API has been introduced by W3C Community in the year 2012. It has two main parts,

1. **SpeechRecognition (Asynchronous Speech Recognition or Speech-to-Text):** It provides the ability to recognize voice context from an audio input and respond accordingly. This is accessed by the `SpeechRecognition` interface.
   The below example shows on how to use this API to get text from speech,

```javascript
window.SpeechRecognition =
  window.webkitSpeechRecognition || window.SpeechRecognition; // webkitSpeechRecognition for Chrome and SpeechRecognition for FF
const recognition = new window.SpeechRecognition();
recognition.onresult = (event) => {
  // SpeechRecognitionEvent type
  const speechToText = event.results[0][0].transcript;
  console.log(speechToText);
};
recognition.start();
```

In this API, browser is going to ask you for permission to use your microphone

1. **SpeechSynthesis (Text-to-Speech):** It provides the ability to recognize voice context from an audio input and respond. This is accessed by the `SpeechSynthesis` interface.
   For example, the below code is used to get voice/speech from text,

```javascript
if ("speechSynthesis" in window) {
  var speech = new SpeechSynthesisUtterance("Hello World!");
  speech.lang = "en-US";
  window.speechSynthesis.speak(speech);
}
```

The above examples can be tested on chrome(33+) browser's developer console.
**Note:** This API is still a working draft and only available in Chrome and Firefox browsers(ofcourse Chrome only implemented the specification)

Q:: What is minimum timeout throttling  
A:: Both browser and NodeJS javascript environments throttles with a minimum delay that is greater than 0ms. That means even though setting a delay of 0ms will not happen instantaneously.  
**Browsers:** They have a minimum delay of 4ms. This throttle occurs when successive calls are triggered due to callback nesting(certain depth) or after a certain number of successive intervals.  
Note: The older browsers have a minimum delay of 10ms.  
**Nodejs:** They have a minimum delay of 1ms. This throttle happens when the delay is larger than 2147483647 or less than 1.  
The best example to explain this timeout throttling behavior is the order of below code snippet.

```javascript
function runMeFirst() {
  console.log("My script is initialized");
}
setTimeout(runMeFirst, 0);
console.log("Script loaded");
```

and the output would be in

```cmd
Script loaded
My script is initialized
```

If you don't use `setTimeout`, the order of logs will be sequential.

```javascript
function runMeFirst() {
  console.log("My script is initialized");
}
runMeFirst();
console.log("Script loaded");
```

and the output is,

```cmd
My script is initialized
Script loaded
```

Q:: How do you implement zero timeout in modern browsers  
A:: You can't use setTimeout(fn, 0) to execute the code immediately due to minimum delay of greater than 0ms. But you can use window.postMessage() to achieve this behavior.

Q:: What are tasks in event loop  
A:: A task is any javascript code/program which is scheduled to be run by the standard mechanisms such as initially starting to run a program, run an event callback, or an interval or timeout being fired. All these tasks are scheduled on a task queue.  
Below are the list of use cases to add tasks to the task queue,

1. When a new javascript program is executed directly from console or running by the `<script>` element, the task will be added to the task queue.
2. When an event fires, the event callback added to task queue
3. When a setTimeout or setInterval is reached, the corresponding callback added to task queue

Q:: What is microtask  
A:: Microtask is the javascript code which needs to be executed immediately after the currently executing task/microtask is completed. They are kind of blocking in nature. i.e, The main thread will be blocked until the microtask queue is empty.  
The main sources of microtasks are Promise.resolve, Promise.reject, MutationObservers, IntersectionObservers etc  
**Note:** All of these microtasks are processed in the same turn of the event loop.

Q:: What are different event loops  
A:: In JavaScript, there are multiple event loops that can be used depending on the context of your application. The most common event loops are:

1. The Browser Event Loop
2. The Node.js Event Loop

- Browser Event Loop: The Browser Event Loop is used in client-side JavaScript applications and is responsible for handling events that occur within the browser environment, such as user interactions (clicks, keypresses, etc.), HTTP requests, and other asynchronous actions.
- The Node.js Event Loop is used in server-side JavaScript applications and is responsible for handling events that occur within the Node.js runtime environment, such as file I/O, network I/O, and other asynchronous actions.

Q:: What is the purpose of queueMicrotask  
A:: The `queueMicrotask` function is used to schedule a microtask, which is a function that will be executed asynchronously in the microtask queue. The purpose of `queueMicrotask` is to ensure that a function is executed after the current task has finished, but before the browser performs any rendering or handles user events.  
Example:

```javascript
console.log("Start"); //1
queueMicrotask(() => {
  console.log("Inside microtask"); // 3
});
console.log("End"); //2
```

By using queueMicrotask, you can ensure that certain tasks or callbacks are executed at the earliest opportunity during the JavaScript event loop, making it useful for performing work that needs to be done asynchronously but with higher priority than regular `setTimeout` or `setInterval` callbacks.

Q:: How do you use javascript libraries in typescript file  
A:: It is known that not all JavaScript libraries or frameworks have TypeScript declaration files. But if you still want to use libraries or frameworks in our TypeScript files without getting compilation errors, the only solution is `declare` keyword along with a variable declaration. For example, let's imagine you have a library called `customLibrary` that doesn’t have a TypeScript declaration and have a namespace called `customLibrary` in the global namespace. You can use this library in typescript code as below,

```javascript
declare var customLibrary;
```

In the runtime, typescript will provide the type to the `customLibrary` variable as `any` type. The another alternative without using declare keyword is below

```javascript
var customLibrary: any;
```

Q:: What are the differences between promises and observables  
A:: Some of the major difference in a tabular form

| Promises                                                           | Observables                                                                              |
| ------------------------------------------------------------------ | ---------------------------------------------------------------------------------------- |
| Emits only a single value at a time                                | Emits multiple values over a period of time(stream of values ranging from 0 to multiple) |
| Eager in nature; they are going to be called immediately           | Lazy in nature; they require subscription to be invoked                                  |
| Promise is always asynchronous even though it resolved immediately | Observable can be either synchronous or asynchronous                                     |
| Doesn't provide any operators                                      | Provides operators such as map, forEach, filter, reduce, retry, and retryWhen etc        |
| Cannot be canceled                                                 | Canceled by using unsubscribe() method                                                   |

Q:: What is heap  
A:: Heap(Or memory heap) is the memory location where objects are stored when we define variables. i.e, This is the place where all the memory allocations and de-allocation take place. Both heap and call-stack are two containers of JS runtime.  
Whenever runtime comes across variables and function declarations in the code it stores them in the Heap.  
![heap](../images/heap.png)

Q:: What is an event table  
A:: Event Table is a data structure that stores and keeps track of all the events which will be executed asynchronously like after some time interval or after the resolution of some API requests. i.e Whenever you call a setTimeout function or invoke async operation, it is added to the Event Table.  
It doesn't not execute functions on it’s own. The main purpose of the event table is to keep track of events and send them to the Event Queue as shown in the below diagram.  
![event-table](../images/event-table.png)

Q:: What is a microTask queue  
A:: Microtask Queue is the new queue where all the tasks initiated by promise objects get processed before the callback queue.  
The microtasks queue are processed before the next rendering and painting jobs. But if these microtasks are running for a long time then it leads to visual degradation.

Q:: What is the difference between shim and polyfill  
A:: A shim is a library that brings a new API to an older environment, using only the means of that environment. It isn't necessarily restricted to a web application. For example, es5-shim.js is used to emulate ES5 features on older browsers (mainly pre IE9).  
Whereas polyfill is a piece of code (or plugin) that provides the technology that you, the developer, expect the browser to provide natively.  
In a simple sentence, A polyfill is a shim for a browser API.

Q:: How do you detect primitive or non primitive value type  
A:: In JavaScript, primitive types include boolean, string, number, BigInt, null, Symbol and undefined. Whereas non-primitive types include the Objects. But you can easily identify them with the below function,

```javascript
var myPrimitive = 30;
var myNonPrimitive = {};
function isPrimitive(val) {
  return Object(val) !== val;
}
isPrimitive(myPrimitive);
isPrimitive(myNonPrimitive);
```

If the value is a primitive data type, the Object constructor creates a new wrapper object for the value. But If the value is a non-primitive data type (an object), the Object constructor will give the same object.

Q:: What is babel  
A:: Babel is a JavaScript transpiler to convert ECMAScript 2015+ code into a backwards compatible version of JavaScript in current and older browsers or environments. Some of the main features are listed below,

1. Transform syntax
2. Polyfill features that are missing in your target environment (using @babel/polyfill)
3. Source code transformations (or codemods)

Q:: Is Node.js completely single threaded  
A:: Node is a single thread, but some of the functions included in the Node.js standard library(e.g, fs module functions) are not single threaded. i.e, Their logic runs outside of the Node.js single thread to improve the speed and performance of a program.

Q:: What are the common use cases of observables  
A:: Some of the most common use cases of observables are web sockets with push notifications, user input changes, repeating intervals, etc

Q:: What is RxJS  
A:: RxJS (Reactive Extensions for JavaScript) is a library for implementing reactive programming using observables that makes it easier to compose asynchronous or callback-based code. It also provides utility functions for creating and working with observables.

Q:: What is the difference between Function constructor and function declaration  
A:: The functions which are created with `Function constructor` do not create closures to their creation contexts but they are always created in the global scope. i.e, the function can access its own local variables and global scope variables only. Whereas function declarations can access outer function variables(closures) too.  
Let's see this difference with an example,  
**Function Constructor:**

```javascript
var a = 100;
function createFunction() {
  var a = 200;
  return new Function("return a;");
}
console.log(createFunction()()); // 100
```

**Function declaration:**

```javascript
var a = 100;
function createFunction() {
  var a = 200;
  return function func() {
    return a;
  };
}
console.log(createFunction()()); // 200
```

Q:: What is a Short circuit condition  
A:: Short circuit conditions are meant for condensed way of writing simple if statements. Let's demonstrate the scenario using an example. If you would like to login to a portal with an authentication condition, the expression would be as below,

```javascript
if (authenticate) {
  loginToPorta();
}
```

Since the javascript logical operators evaluated from left to right, the above expression can be simplified using && logical operator

```javascript
authenticate && loginToPorta();
```

Q:: What is the easiest way to resize an array  
A:: The length property of an array is useful to resize or empty an array quickly. Let's apply length property on number array to resize the number of elements from 5 to 2,

```javascript
var array = [1, 2, 3, 4, 5];
console.log(array.length); // 5
array.length = 2;
console.log(array.length); // 2
console.log(array); // [1,2]
```

and the array can be emptied too

```javascript
var array = [1, 2, 3, 4, 5];
array.length = 0;
console.log(array.length); // 0
console.log(array); // []
```

Q:: What is an observable  
A:: An Observable is basically a function that can return a stream of values either synchronously or asynchronously to an observer over time. The consumer can get the value by calling `subscribe()` method.  
Let's look at a simple example of an Observable

```javascript
import { Observable } from "rxjs";
const observable = new Observable((observer) => {
  setTimeout(() => {
    observer.next("Message from a Observable!");
  }, 3000);
});
observable.subscribe((value) => console.log(value));
```

![observables](../images/observables.png)
**Note:** Observables are not part of the JavaScript language yet but they are being proposed to be added to the language

Q:: What is the difference between function and class declarations  
A:: The main difference between function declarations and class declarations is `hoisting`. The function declarations are hoisted but not class declarations.  
**Classes:**

```javascript
const user = new User(); // ReferenceError
class User {}
```

**Constructor Function:**

```javascript
const user = new User(); // No error
function User() {}
```

Q:: What is an async function  
A:: An async function is a function declared with the `async` keyword which enables asynchronous, promise-based behavior to be written in a cleaner style by avoiding promise chains. These functions can contain zero or more `await` expressions.  
Let's take a below async function example,

```javascript
async function logger() {
  let data = await fetch("http://someapi.com/users"); // pause until fetch returns
  console.log(data);
}
logger();
```

It is basically syntax sugar over ES2015 promises and generators.

Q:: How do you prevent promises swallowing errors  
A:: While using asynchronous code, JavaScript’s ES6 promises can make your life a lot easier without having callback pyramids and error handling on every second line. But Promises have some pitfalls and the biggest one is swallowing errors by default.  
Let's say you expect to print an error to the console for all the below cases,

```javascript
Promise.resolve("promised value").then(function () {
  throw new Error("error");
});
Promise.reject("error value").catch(function () {
  throw new Error("error");
});
new Promise(function (resolve, reject) {
  throw new Error("error");
});
```

But there are many modern JavaScript environments that won't print any errors. You can fix this problem in different ways,

1. **Add catch block at the end of each chain:** You can add catch block to the end of each of your promise chains

```javascript
Promise.resolve("promised value")
  .then(function () {
    throw new Error("error");
  })
  .catch(function (error) {
    console.error(error.stack);
  });
```

But it is quite difficult to type for each promise chain and verbose too. 2. **Add done method:** You can replace first solution's then and catch blocks with done method

```javascript
Promise.resolve("promised value").done(function () {
  throw new Error("error");
});
```

Let's say you want to fetch data using HTTP and later perform processing on the resulting data asynchronously. You can write `done` block as below,

```javascript
getDataFromHttp()
  .then(function (result) {
    return processDataAsync(result);
  })
  .done(function (processed) {
    displayData(processed);
  });
```

In future, if the processing library API changed to synchronous then you can remove `done` block as below,

```javascript
getDataFromHttp().then(function (result) {
  return displayData(processDataAsync(result));
});
```

and then you forgot to add `done` block to `then` block leads to silent errors. 3. **Extend ES6 Promises by Bluebird:**
Bluebird extends the ES6 Promises API to avoid the issue in the second solution. This library has a “default” onRejection handler which will print all errors from rejected Promises to stderr. After installation, you can process unhandled rejections

```javascript
Promise.onPossiblyUnhandledRejection(function (error) {
  throw error;
});
```

and discard a rejection, just handle it with an empty catch

```javascript
Promise.reject("error value").catch(function () {});
```

Q:: What is deno  
A:: Deno is a simple, modern and secure runtime for JavaScript and TypeScript that uses V8 JavaScript engine and the Rust programming language.

Q:: How do you make an object iterable in javascript  
A:: By default, plain objects are not iterable. But you can make the object iterable by defining a `Symbol.iterator` property on it.  
Let's demonstrate this with an example,

```javascript
const collection = {
  one: 1,
  two: 2,
  three: 3,
  [Symbol.iterator]() {
    const values = Object.keys(this);
    let i = 0;
    return {
      next: () => {
        return {
          value: this[values[i++]],
          done: i > values.length,
        };
      },
    };
  },
};
const iterator = collection[Symbol.iterator]();
console.log(iterator.next()); // → {value: 1, done: false}
console.log(iterator.next()); // → {value: 2, done: false}
console.log(iterator.next()); // → {value: 3, done: false}
console.log(iterator.next()); // → {value: undefined, done: true}
```

The above process can be simplified using a generator function,

```javascript
const collection = {
  one: 1,
  two: 2,
  three: 3,
  [Symbol.iterator]: function* () {
    for (let key in this) {
      yield this[key];
    }
  },
};
const iterator = collection[Symbol.iterator]();
console.log(iterator.next()); // {value: 1, done: false}
console.log(iterator.next()); // {value: 2, done: false}
console.log(iterator.next()); // {value: 3, done: false}
console.log(iterator.next()); // {value: undefined, done: true}
```

Q:: What is a Proper Tail Call  
A:: First, we should know about tail call before talking about "Proper Tail Call". A tail call is a subroutine or function call performed as the final action of a calling function. Whereas **Proper tail call(PTC)** is a technique where the program or code will not create additional stack frames for a recursion when the function call is a tail call.  
For example, the below classic or head recursion of factorial function relies on stack for each step. Each step need to be processed upto `n * factorial(n - 1)`

```javascript
function factorial(n) {
  if (n === 0) {
    return 1;
  }
  return n * factorial(n - 1);
}
console.log(factorial(5)); //120
```

But if you use Tail recursion functions, they keep passing all the necessary data it needs down the recursion without relying on the stack.

```javascript
function factorial(n, acc = 1) {
  if (n === 0) {
    return acc;
  }
  return factorial(n - 1, n * acc);
}
console.log(factorial(5)); //120
```

The above pattern returns the same output as the first one. But the accumulator keeps track of total as an argument without using stack memory on recursive calls.

Q:: How do you check an object is a promise or not  
A:: If you don't know if a value is a promise or not, wrapping the value as `Promise.resolve(value)` which returns a promise

```javascript
function isPromise(object) {
  if (Promise && Promise.resolve) {
    return Promise.resolve(object) == object;
  } else {
    throw "Promise not supported in your environment";
  }
}
var i = 1;
var promise = new Promise(function (resolve, reject) {
  resolve();
});
console.log(isPromise(i)); // false
console.log(isPromise(promise)); // true
```

Another way is to check for `.then()` handler type

```javascript
function isPromise(value) {
  return Boolean(value && typeof value.then === "function");
}
var i = 1;
var promise = new Promise(function (resolve, reject) {
  resolve();
});
console.log(isPromise(i)); // false
console.log(isPromise(promise)); // true
```

Q:: How to detect if a function is called as constructor  
A:: You can use `new.target` pseudo-property to detect whether a function was called as a constructor(using the new operator) or as a regular function call.

1. If a constructor or function invoked using the new operator, new.target returns a reference to the constructor or function.
2. For function calls, new.target is undefined.

```javascript
function Myfunc() {
  if (new.target) {
    console.log("called with new");
  } else {
    console.log("not called with new");
  }
}
new Myfunc(); // called with new
Myfunc(); // not called with new
Myfunc.call({}); // not called with new
```

Q:: What are the differences between arguments object and rest parameter  
A:: There are three main differences between arguments object and rest parameters

1. The arguments object is an array-like but not an array. Whereas the rest parameters are array instances.
2. The arguments object does not support methods such as sort, map, forEach, or pop. Whereas these methods can be used in rest parameters.
3. The rest parameters are only the ones that haven’t been given a separate name, while the arguments object contains all arguments passed to the function

Q:: What are the differences between spread operator and rest parameter  
A:: Rest parameter collects all remaining elements into an array. Whereas Spread operator allows iterables( arrays / objects / strings ) to be expanded into single arguments/elements. i.e, Rest parameter is opposite to the spread operator.

Q:: What are the different kinds of generators  
A:: There are five kinds of generators,

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

Q:: What are the built-in iterables  
A:: Below are the list of built-in iterables in javascript,

1. Arrays and TypedArrays
2. Strings: Iterate over each character or Unicode code-points
3. Maps: iterate over its key-value pairs
4. Sets: iterates over their elements
5. arguments: An array-like special variable in functions
6. DOM collection such as NodeList

Q:: What are the differences between for...of and for...in statements  
A:: Both for...in and for...of statements iterate over js data structures. The only difference is over what they iterate:

1. for..in iterates over all enumerable property keys of an object
2. for..of iterates over the values of an iterable object.
   Let's explain this difference with an example,

```javascript
let arr = ["a", "b", "c"];
arr.newProp = "newVlue";
// key are the property keys
for (let key in arr) {
  console.log(key); // 0, 1, 2 & newValue
}
// value are the property values
for (let value of arr) {
  console.log(value); // a, b, c
}
```

Since for..in loop iterates over the keys of the object, the first loop logs 0, 1, 2 and newProp while iterating over the array object. The for..of loop iterates over the values of a arr data structure and logs a, b, c in the console.

Q:: How do you define instance and non-instance properties  
A:: The Instance properties must be defined inside of class methods. For example, name and age properties defined inside constructor as below,

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}
```

But Static(class) and prototype data properties must be defined outside of the ClassBody declaration. Let's assign the age value for Person class as below,

```javascript
Person.staticAge = 30;
Person.prototype.prototypeAge = 40;
```

Q:: What is the difference between isNaN and Number.isNaN?  
A:: 1. **isNaN**: The global function `isNaN` converts the argument to a Number and returns true if the resulting value is NaN. 2. **Number.isNaN**: This method does not convert the argument. But it returns true when the type is a Number and value is NaN.  
Let's see the difference with an example,

```javascript
isNaN(‘hello’);   // true
Number.isNaN('hello'); // false
```

Q:: How to invoke an IIFE without any extra brackets?  
A:: Immediately Invoked Function Expressions(IIFE) requires a pair of parenthesis to wrap the function which contains set of statements.

```js
(function (dt) {
  console.log(dt.toLocaleTimeString());
})(new Date());
```

Since both IIFE and void operator discard the result of an expression, you can avoid the extra brackets using `void operator` for IIFE as below,

```js
void (function (dt) {
  console.log(dt.toLocaleTimeString());
})(new Date());
```

Q:: Is that possible to use expressions in switch cases?  
A:: You might have seen expressions used in switch condition but it is also possible to use for switch cases by assigning true value for the switch condition. Let's see the weather condition based on temparature as an example,

```js
const weather = (function getWeather(temp) {
  switch (true) {
    case temp < 0:
      return "freezing";
    case temp < 10:
      return "cold";
    case temp < 24:
      return "cool";
    default:
      return "unknown";
  }
})(10);
```

Q:: What is the easiest way to ignore promise errors?  
A:: The easiest and safest way to ignore promise errors is void that error. This approach is ESLint friendly too.

```js
await promise.catch((e) => void e);
```

Q:: How do style the console output using CSS?  
A:: You can add CSS styling to the console output using the CSS format content specifier %c. The console string message can be appended after the specifier and CSS style in another argument. Let's print the red the color text using console.log and CSS specifier as below,

```js
console.log("%cThis is a red text", "color:red");
```

It is also possible to add more styles for the content. For example, the font-size can be modified for the above text

```js
console.log(
  "%cThis is a red text with bigger font",
  "color:red; font-size:20px",
);
```

Q:: What is nullish coalescing operator (??)?  
A:: It is a logical operator that returns its right-hand side operand when its left-hand side operand is null or undefined, and otherwise returns its left-hand side operand. This can be contrasted with the logical OR (||) operator, which returns the right-hand side operand if the left operand is any falsy value, not only null or undefined.

```js
console.log(null ?? true); // true
console.log(false ?? true); // false
console.log(undefined ?? true); // true
```

Q:: How do you group and nest console output?  
A:: The `console.group()` can be used to group related log messages to be able to easily read the logs and use console.groupEnd()to close the group. Along with this, you can also nest groups which allows to output message in hierarchical manner.  
For example, if you’re logging a user’s details:

```js
console.group("User Details");
console.log("name: Sudheer Jonna");
console.log("job: Software Developer");
// Nested Group
console.group("Address");
console.log("Street: Commonwealth");
console.log("City: Los Angeles");
console.log("State: California");
// Close nested group
console.groupEnd();
// Close outer group
console.groupEnd();
```

You can also use `console.groupCollapsed()` instead of `console.group()` if you want the groups to be collapsed by default.

Q:: What is the difference between dense and sparse arrays?  
A:: An array contains items at each index starting from first(0) to last(array.length - 1) is called as Dense array. Whereas if at least one item is missing at any index, the array is called as sparse.  
Let's see the below two kind of arrays,

```js
const avengers = ["Ironman", "Hulk", "CaptainAmerica"];
console.log(avengers[0]); // 'Ironman'
console.log(avengers[1]); // 'Hulk'
console.log(avengers[2]); // 'CaptainAmerica'
console.log(avengers.length); // 3
const justiceLeague = ["Superman", "Aquaman", , "Batman"];
console.log(justiceLeague[0]); // 'Superman'
console.log(justiceLeague[1]); // 'Aquaman'
console.log(justiceLeague[2]); // undefined
console.log(justiceLeague[3]); // 'Batman'
console.log(justiceLeague.length); // 4
```

Q:: What are the different ways to create sparse arrays?  
A:: There are 4 different ways to create sparse arrays in JavaScript

1. **Array literal:** Omit a value when using the array literal

```js
const justiceLeague = ["Superman", "Aquaman", , "Batman"];
console.log(justiceLeague); // ['Superman', 'Aquaman', empty ,'Batman']
```

2. **Array() constructor:** Invoking Array(length) or new Array(length)

```js
const array = Array(3);
console.log(array); // [empty, empty ,empty]
```

3. **Delete operator:** Using delete array[index] operator on the array

```js
const justiceLeague = ["Superman", "Aquaman", "Batman"];
delete justiceLeague[1];
console.log(justiceLeague); // ['Superman', empty, ,'Batman']
```

4. **Increase length property:** Increasing length property of an array

```js
const justiceLeague = ["Superman", "Aquaman", "Batman"];
justiceLeague.length = 5;
console.log(justiceLeague); // ['Superman', 'Aquaman', 'Batman', empty, empty]
```

Q:: What is the difference between setTimeout, setImmediate and process.nextTick?  
A:: 1. **Set Timeout:** setTimeout() is to schedule execution of a one-time callback after delay milliseconds. 2. **Set Immediate:** The setImmediate function is used to execute a function right after the current event loop finishes. 3. **Process NextTick:** If process.nextTick() is called in a given phase, all the callbacks passed to process.nextTick() will be resolved before the event loop continues. This will block the event loop and create I/O Starvation if process.nextTick() is called recursively.

Q:: How do you reverse an array without modifying original array?  
A:: The `reverse()` method reverses the order of the elements in an array but it mutates the original array. Let's take a simple example to demonistrate this case,

```javascript
const originalArray = [1, 2, 3, 4, 5];
const newArray = originalArray.reverse();
console.log(newArray); // [ 5, 4, 3, 2, 1]
console.log(originalArray); // [ 5, 4, 3, 2, 1]
```

There are few solutions that won't mutate the original array. Let's take a look.

1. **Using slice and reverse methods:**
   In this case, just invoke the `slice()` method on the array to create a shallow copy followed by `reverse()` method call on the copy.

```javascript
const originalArray = [1, 2, 3, 4, 5];
const newArray = originalArray.slice().reverse(); //Slice an array gives a new copy
console.log(originalArray); // [1, 2, 3, 4, 5]
console.log(newArray); // [ 5, 4, 3, 2, 1]
```

2. **Using spread and reverse methods:**
   In this case, let's use the spread syntax (...) to create a copy of the array followed by `reverse()` method call on the copy.

```javascript
const originalArray = [1, 2, 3, 4, 5];
const newArray = [...originalArray].reverse();
console.log(originalArray); // [1, 2, 3, 4, 5]
console.log(newArray); // [ 5, 4, 3, 2, 1]
```

3. **Using reduce and spread methods:**
   Here execute a reducer function on an array elements and append the accumulated array on right side using spread syntax

```javascript
const originalArray = [1, 2, 3, 4, 5];
const newArray = originalArray.reduce((accumulator, value) => {
  return [value, ...accumulator];
}, []);
console.log(originalArray); // [1, 2, 3, 4, 5]
console.log(newArray); // [ 5, 4, 3, 2, 1]
```

4. **Using reduceRight and spread methods:**
   Here execute a right reducer function(i.e. opposite direction of reduce method) on an array elements and append the accumulated array on left side using spread syntax

```javascript
const originalArray = [1, 2, 3, 4, 5];
const newArray = originalArray.reduceRight((accumulator, value) => {
  return [...accumulator, value];
}, []);
console.log(originalArray); // [1, 2, 3, 4, 5]
console.log(newArray); // [ 5, 4, 3, 2, 1]
```

5. **Using reduceRight and push methods:**
   Here execute a right reducer function(i.e. opposite direction of reduce method) on an array elements and push the iterated value to the accumulator

```javascript
const originalArray = [1, 2, 3, 4, 5];
const newArray = originalArray.reduceRight((accumulator, value) => {
  accumulator.push(value);
  return accumulator;
}, []);
console.log(originalArray); // [1, 2, 3, 4, 5]
console.log(newArray); // [ 5, 4, 3, 2, 1]
```

Q:: How do you create custom HTML element?  
A:: The creation of custom HTML elements involves two main steps,

1. **Define your custom HTML element:** First you need to define some custom class by extending HTMLElement class.
   After that define your component properties (styles,text etc) using `connectedCallback` method.
   **Note:** The browser exposes a function called `customElements.define` inorder to reuse the element.

```javascript
class CustomElement extends HTMLElement {
  connectedCallback() {
    this.innerHTML = "This is a custom element";
  }
}
customElements.define("custom-element", CustomElement);
```

2. **Use custome element just like other HTML element:** Declare your custom element as a HTML tag.

```javascript
<body>
<custom-element>
</body>
```

Q:: What is global execution context?  
A:: The global execution context is the default or first execution context that is created by the JavaScript engine before any code is executed(i.e, when the file first loads in the browser). All the global code that is not inside a function or object will be executed inside this global execution context. Since JS engine is single threaded there will be only one global environment and there will be only one global execution context.  
For example, the below code other than code inside any function or object is executed inside the global execution context.

```javascript
var x = 10;
function A() {
  console.log("Start function A");
  function B() {
    console.log("In function B");
  }
  B();
}
A();
console.log("GlobalContext");
```

Q:: What is function execution context?  
A:: Whenever a function is invoked, the JavaScript engine creates a different type of Execution Context known as a Function Execution Context (FEC) within the Global Execution Context (GEC) to evaluate and execute the code within that function.

Q:: What is debouncing?  
A:: Debouncing is a programming pattern that allows delaying execution of some piece of code until a specified time to avoid unnecessary _CPU cycles, API calls and improve performance_. The debounce function make sure that your code is only triggered once per user input. The common usecases are Search box suggestions, text-field auto-saves, and eliminating double-button clicks.  
Let's say you want to show suggestions for a search query, but only after a visitor has finished typing it. So here you write a debounce function where the user keeps writing the characters with in 500ms then previous timer cleared out using `clearTimeout` and reschedule API call/DB query for a new time—300 ms in the future.

```js
function debounce(func, timeout = 500) {
  let timer;
  return (...args) => {
    clearTimeout(timer);
    timer = setTimeout(() => {
      func.apply(this, args);
    }, timeout);
  };
}
function fetchResults() {
  console.log("Fetching input suggestions");
}
const processChange = debounce(() => fetchResults());
```

The _debounce()_ function can be used on input, button and window events
**Input:**

```html
<input type="text" onkeyup="processChange()" />
```

**Button:**

```html
<button onclick="processChange()">Click me</button>
```

**Windows event:**

```html
window.addEventListener("scroll", processChange);
```

Q:: What is throttling?  
A:: Throttling is a technique used to limit the execution of an event handler function, even when this event triggers continuously due to user actions. The common use cases are browser resizing, window scrolling etc.  
The below example creates a throttle function to reduce the number of events for each pixel change and trigger scroll event for each 100ms except for the first event.

```js
const throttle = (func, limit) => {
  let inThrottle;
  return (...args) => {
    if (!inThrottle) {
      func.apply(this, args);
      inThrottle = true;
      setTimeout(() => (inThrottle = false), limit);
    }
  };
};
window.addEventListener("scroll", () => {
  throttle(handleScrollAnimation, 100);
});
```

Q:: What is optional chaining?  
A:: According to MDN official docs, the optional chaining operator (?.) permits reading the value of a property located deep within a chain of connected objects without having to expressly validate that each reference in the chain is valid.  
The ?. operator is like the . chaining operator, except that instead of causing an error if a reference is nullish (null or undefined), the expression short-circuits with a return value of undefined. When used with function calls, it returns undefined if the given function does not exist.

```js
const adventurer = {
  name: "Alice",
  cat: {
    name: "Dinah",
  },
};
const dogName = adventurer.dog?.name;
console.log(dogName);
// expected output: undefined
console.log(adventurer.someNonExistentMethod?.());
// expected output: undefined
```

Q:: What is an environment record?  
A:: According to ECMAScript specification 262 (9.1):

> [Environment Record](https://262.ecma-international.org/12.0/#sec-environment-records) is a specification type used to define the association of Identifiers to specific variables and functions, based upon the lexical nesting structure of ECMAScript code.
> Usually an Environment Record is associated with some specific syntactic structure of ECMAScript code such as a FunctionDeclaration, a BlockStatement, or a Catch clause of a TryStatement.
> Each time such code is evaluated, a new Environment Record is created to record the identifier bindings that are created by that code.

Q:: How to verify if a variable is an array?  
A:: It is possible to check if a variable is an array instance using 3 different ways,

1. Array.isArray() method:
   The `Array.isArray(value)` utility function is used to determine whether value is an array or not. This function returns a true boolean value if the variable is an array and a false value if it is not.

```javascript
const numbers = [1, 2, 3];
const user = { name: "John" };
Array.isArray(numbers); // true
Array.isArray(user); //false
```

2. instanceof operator:
   The instanceof operator is used to check the type of an array at run time. It returns true if the type of a variable is an Array other false for other type.

```javascript
const numbers = [1, 2, 3];
const user = { name: "John" };
console.log(numbers instanceof Array); // true
console.log(user instanceof Array); // false
```

3. Checking constructor type:
   The constructor property of the variable is used to determine whether the variable Array type or not.

```javascript
const numbers = [1, 2, 3];
const user = { name: "John" };
console.log(numbers.constructor === Array); // true
console.log(user.constructor === Array); // false
```

Q:: What is pass by value and pass by reference?  
A:: Pass-by-value creates a new space in memory and makes a copy of a value. Primitives such as string, number, boolean etc will actually create a new copy. Hence, updating one value doesn't impact the other value. i.e, The values are independent of each other.

```javascript
let a = 5;
let b = a;
b++;
console.log(a, b); //5, 6
```

In the above code snippet, the value of `a` is assigned to `b` and the variable `b` has been incremented. Since there is a new space created for variable `b`, any update on this variable doesn't impact the variable `a`.
Pass by reference doesn't create a new space in memory but the new variable adopts a memory address of an initial variable. Non-primitives such as objects, arrays and functions gets the reference of the initiable variable. i.e, updating one value will impact the other variable.

```javascript
let user1 = {
  name: "John",
  age: 27,
};
let user2 = user1;
user2.age = 30;
console.log(user1.age, user2.age); // 30, 30
```

In the above code snippet, updating the `age` property of one object will impact the other property due to the same reference.

Q:: What are the differences between primitives and non-primitives?  
A:: JavaScript language has both primitives and non-primitives but there are few differences between them as below,

| Primitives                 | Non-primitives       |
| -------------------------- | -------------------- |
| These types are predefined | Created by developer |
| These are immutable        | Mutable              |
| Compare by value           | Compare by reference |
| Stored in Stack            | Stored in heap       |
| Contain certain value      | Can contain NULL too |

Q:: How do you create your own bind method using either call or apply method?  
A:: The custom bind function needs to be created on Function prototype inorder to use it as other builtin functions. This custom function should return a function similar to original bind method and the implementation of inner function needs to use apply method call.  
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

Q:: What are the differences between pure and impure functions?  
A:: Some of the major differences between pure and impure function are as below,

| Pure function                       | Impure function                                                       |
| ----------------------------------- | --------------------------------------------------------------------- |
| It has no side effects              | It causes side effects                                                |
| It is always return the same result | It returns different result on each call                              |
| Easy to read and debug              | Difficult to read and debug because they are affected by extenal code |

Q:: What is referential transparency?  
A:: An expression in javascript that can be replaced by its value without affecting the behaviour of the program is called referential transparency. Pure functions are referentially transparent.

```javascript
const add = (x, y) => x + y;
const multiplyBy2 = (x) => x * 2;
//Now add (2, 3) can be replaced by 5.
multiplyBy2(add(2, 3));
```

Q:: What are the possible side-effects in javascript?  
A:: A side effect is the modification of state through the invocation of a function or expression. These side effects makes our function impure by default. Below are some side effects which makes function impure,

1. Making an HTTP request. Asynchronous functions such as fetch and promise are impure.
2. DOM manipulations
3. Mutating the input data
4. Printing to a screen or console: For example, console.log() and alert()
5. Fetching the current time
6. Math.random() calls: Modifies the internal state of Math object

Q:: What are compose and pipe functions?  
A:: The "compose" and "pipe" are two techniques commonly used in functional programming to simplify complex operations and make code more readable. They are not native to JavaScript and higher-order functions. the `compose()` applies right to left any number of functions to the output of the previous function.

Q:: What is module pattern?  
A:: Module pattern is a designed pattern used to wrap a set of variables and functions together in a single scope returned as an object. JavaScript doesn't have access specifiers similar to other languages(Java, Python, etc) to provide private scope. It uses IIFE (Immediately invoked function expression) to allow for private scopes. i.e., a closure that protect variables and methods.  
The module pattern looks like below,

```javascript
(function () {
  // Private variables or functions goes here.
  return {
    // Return public variables or functions here.
  };
})();
```

Let's see an example of a module pattern for an employee with private and public access,

```javascript
const createEmployee = (function () {
  // Private
  const name = "John";
  const department = "Sales";
  const getEmployeeName = () => name;
  const getDepartmentName = () => department;
  // Public
  return {
    name,
    department,
    getName: () => getEmployeeName(),
    getDepartment: () => getDepartmentName(),
  };
})();
console.log(createEmployee.name);
console.log(createEmployee.department);
console.log(createEmployee.getName());
console.log(createEmployee.getDepartment());
```

**Note:** It mimic the concepts of classes with private variables and methods.

Q:: What is Function Composition?  
A:: It is an approach where the result of one function is passed on to the next function, which is passed to another until the final function is executed for the final result.

```javascript
//example
const double = (x) => x * 2;
const square = (x) => x * x;
var output1 = double(2);
var output2 = square(output1);
console.log(output2);
var output_final = square(double(2));
console.log(output_final);
```

Q:: How to use await outside of async function prior to ES2022?  
A:: Prior to ES2022, if you attempted to use an await outside of an async function resulted in a SyntaxError.

```javascript
await Promise.resolve(console.log("Hello await")); // SyntaxError: await is only valid in async function
```

But you can fix this issue with an alternative IIFE (Immediately Invoked Function Expression) to get access to the feature.

```javascript
(async function () {
  await Promise.resolve(console.log("Hello await")); // Hello await
})();
```

In ES2022, you can write top-level await without writing any hacks.

```javascript
await Promise.resolve(console.log("Hello await")); //Hello await
```

#### Chapter 2 - Coding Exercises

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna

FILE TAGS: Javascript Interview

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```