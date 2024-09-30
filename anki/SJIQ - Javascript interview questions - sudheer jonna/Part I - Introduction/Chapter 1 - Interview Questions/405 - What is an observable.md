========== Question ==========  

### What is an observable  

========== Answer ==========  

An Observable is basically a function that can return a stream of values either synchronously or asynchronously to an observer over time. The consumer can get the value by calling `subscribe()` method.

Let's look at a simple example of an Observable

```javascript
import { Observable } from 'rxjs';
const observable = new Observable((observer) => {
    setTimeout(() => {
        observer.next('Message from a Observable!');
    }, 3000);
});
observable.subscribe((value) => console.log(value));
```

![observables](../../../../images/observables.png)

**Note:** Observables are not part of the JavaScript language yet but they are being proposed to be added to the language

========== Id ==========  
405

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#405-What-is-an-observable

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
