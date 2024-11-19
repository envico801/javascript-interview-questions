========== Question ==========  

### How do you prevent promises swallowing errors  

========== Answer ==========  

While using asynchronous code, JavaScript’s ES6 promises can make your life a lot easier without having callback pyramids and error handling on every second line. But Promises have some pitfalls and the biggest one is swallowing errors by default.

Let's say you expect to print an error to the console for all the below cases,

```javascript
Promise.resolve('promised value').then(function () {
    throw new Error('error');
});

Promise.reject('error value').catch(function () {
    throw new Error('error');
});

new Promise(function (resolve, reject) {
    throw new Error('error');
});
```

But there are many modern JavaScript environments that won't print any errors. You can fix this problem in different ways,

1. **Add catch block at the end of each chain:** You can add catch block to the end of each of your promise chains

    ```javascript
    Promise.resolve('promised value')
        .then(function () {
            throw new Error('error');
        })
        .catch(function (error) {
            console.error(error.stack);
        });
    ```

    But it is quite difficult to type for each promise chain and verbose too.

2. **Add done method:** You can replace first solution's then and catch blocks with done method

    ```javascript
    Promise.resolve('promised value').done(function () {
        throw new Error('error');
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

    and then you forgot to add `done` block to `then` block leads to silent errors.

3. **Extend ES6 Promises by Bluebird:**

    Bluebird extends the ES6 Promises API to avoid the issue in the second solution. This library has a “default” onRejection handler which will print all errors from rejected Promises to stderr. After installation, you can process unhandled rejections

    ```javascript
    Promise.onPossiblyUnhandledRejection(function (error) {
        throw error;
    });
    ```

    and discard a rejection, just handle it with an empty catch

    ```javascript
    Promise.reject('error value').catch(function () {});
    ```

========== Id ==========  
408

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#408-How-do-you-prevent-promises-swallowing-err

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
