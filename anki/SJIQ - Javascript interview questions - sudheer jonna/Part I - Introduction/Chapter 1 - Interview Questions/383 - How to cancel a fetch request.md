Q: How to cancel a fetch request  
A: Until a few days back, One shortcoming of native promises is no direct way to cancel a fetch request. But the new `AbortController` from js specification allows you to use a signal to abort one or multiple fetch calls.  
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
<!--ID: 1693596687420-->

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