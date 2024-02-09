==================== Question ====================  

### How do you make asynchronous HTTP request  

==================== Answer ====================  

Browsers provide an XMLHttpRequest object which can be used to make asynchronous
HTTP requests from JavaScript by passing the 3rd parameter as true.

```javascript
function httpGetAsync(theUrl, callback) {
  var xmlHttpReq = new XMLHttpRequest();
  xmlHttpReq.onreadystatechange = function () {
    if (xmlHttpReq.readyState == 4 && xmlHttpReq.status == 200)
      callback(xmlHttpReq.responseText);
  };
  xmlHttp.open('GET', theUrl, true); // true for asynchronous
  xmlHttp.send(null);
}
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#170-How-do-you-make-asynchronous-http-request

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
