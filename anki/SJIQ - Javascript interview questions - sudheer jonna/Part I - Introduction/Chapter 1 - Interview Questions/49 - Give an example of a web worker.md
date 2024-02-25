==================== Question ====================  

### Give an example of a web worker  

==================== Answer ====================  

You need to follow below steps to start using web workers for counting example

1. Create a Web Worker File: You need to write a script to increment the count
   value. Let's name it as counter.js

```javascript
let i = 0;
function timedCount() {
  i = i + 1;
  postMessage(i);
  setTimeout('timedCount()', 500);
}
timedCount();
```

Here postMessage() method is used to post a message back to the HTML page

1. Create a Web Worker Object: You can create a web worker object by checking
   for browser support. Let's name this file as web_worker_example.js

```javascript
if (typeof w == 'undefined') {
  w = new Worker('counter.js');
}
```

and we can receive messages from web worker

```javascript
w.onmessage = function (event) {
  document.getElementById('message').innerHTML = event.data;
};
```

1. Terminate a Web Worker:  
   Web workers will continue to listen for messages (even after the external
   script is finished) until it is terminated. You can use the terminate()
   method to terminate listening to the messages.

```javascript
w.terminate();
```

1. Reuse the Web Worker: If you set the worker variable to undefined you can
   reuse the code

```javascript
w = undefined;
```

==================== Id ====================  
49

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#49-Give-an-example-of-a-web-worker

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
