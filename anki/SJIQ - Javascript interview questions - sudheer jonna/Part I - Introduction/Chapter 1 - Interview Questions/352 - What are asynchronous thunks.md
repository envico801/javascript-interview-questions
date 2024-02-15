==================== Question ====================  

### What are asynchronous thunks  

==================== Answer ====================  

The asynchronous thunks are useful to make network requests. Let's see an
example of network requests,

```javascript
function fetchData(fn) {
  fetch('https://jsonplaceholder.typicode.com/todos/1')
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

The `getData` function won't be called immediately but it will be invoked only
when the data is available from API endpoint. The setTimeout function is also
used to make our code asynchronous. The best real time example is redux state
management library which uses the asynchronous thunks to delay the actions to
dispatch.

==================== Id ====================  
352
<!--ID: 1707879823381-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#352-What-are-asynchronous-thunks

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
