==================== Question ====================  

### How do you receive server-sent event notifications  

==================== Answer ====================  

The EventSource object is used to receive server-sent event notifications. For
example, you can receive messages from server as below,

```javascript
if (typeof EventSource !== 'undefined') {
  var source = new EventSource('sse_generator.js');
  source.onmessage = function (event) {
    document.getElementById('output').innerHTML += event.data + '<br>';
  };
}
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#58-How-do-you-receive-server-sent-event-notif

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
