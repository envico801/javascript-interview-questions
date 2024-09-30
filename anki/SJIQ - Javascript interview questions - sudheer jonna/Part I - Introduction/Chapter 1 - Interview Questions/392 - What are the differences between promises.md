========== Question ==========  

### What are the differences between promises and observables  

========== Answer ==========  

Some of the major difference in a tabular form

| Promises | Observables |
| --- | --- |
| Emits only a single value at a time | Emits multiple values over a period of time(stream of values ranging from 0 to multiple) |
| Eager in nature; they are going to be called immediately | Lazy in nature; they require subscription to be invoked |
| Promise is always asynchronous even though it resolved immediately | Observable can be either synchronous or asynchronous |
| Doesn't provide any operators | Provides operators such as map, forEach, filter, reduce, retry, and retryWhen etc |
| Cannot be canceled | Canceled by using unsubscribe() method |

========== Id ==========  
392

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#392-What-are-the-differences-between-promises

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
