==================== Question ====================  

### How do you prevent promises swallowing errors  

==================== Answer ====================  

While using asynchronous code, JavaScript’s ES6 promises can make your life a lot easier without having callback pyramids and error handling on every second line. But Promises have some pitfalls and the biggest one is swallowing errors by default.

Let's say you expect to print an error to the console for all the below cases,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">resolve</span>(<span class="hljs-string">'promised value'</span>).<span class="hljs-title function_">then</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-keyword">throw</span> <span class="hljs-keyword">new</span> <span class="hljs-title class_">Error</span>(<span class="hljs-string">'error'</span>);
});
<span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">reject</span>(<span class="hljs-string">'error value'</span>).<span class="hljs-title function_">catch</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-keyword">throw</span> <span class="hljs-keyword">new</span> <span class="hljs-title class_">Error</span>(<span class="hljs-string">'error'</span>);
});
<span class="hljs-keyword">new</span> <span class="hljs-title class_">Promise</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">resolve, reject</span>) {
  <span class="hljs-keyword">throw</span> <span class="hljs-keyword">new</span> <span class="hljs-title class_">Error</span>(<span class="hljs-string">'error'</span>);
});
</code></pre>
<!-- codeblock-end -->

But there are many modern JavaScript environments that won't print any errors. You can fix this problem in different ways,

1. **Add catch block at the end of each chain:** You can add catch block to the end of each of your promise chains

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">resolve</span>(<span class="hljs-string">'promised value'</span>)
      .<span class="hljs-title function_">then</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
        <span class="hljs-keyword">throw</span> <span class="hljs-keyword">new</span> <span class="hljs-title class_">Error</span>(<span class="hljs-string">'error'</span>);
      })
      .<span class="hljs-title function_">catch</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">error</span>) {
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">error</span>(error.<span class="hljs-property">stack</span>);
      });
    </code></pre>
    <!-- codeblock-end -->

    But it is quite difficult to type for each promise chain and verbose too.

2. **Add done method:** You can replace first solution's then and catch blocks with done method

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">resolve</span>(<span class="hljs-string">'promised value'</span>).<span class="hljs-title function_">done</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
      <span class="hljs-keyword">throw</span> <span class="hljs-keyword">new</span> <span class="hljs-title class_">Error</span>(<span class="hljs-string">'error'</span>);
    });
    </code></pre>
    <!-- codeblock-end -->

    Let's say you want to fetch data using HTTP and later perform processing on the resulting data asynchronously. You can write `done` block as below,

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-title function_">getDataFromHttp</span>()
      .<span class="hljs-title function_">then</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">result</span>) {
        <span class="hljs-keyword">return</span> <span class="hljs-title function_">processDataAsync</span>(result);
      })
      .<span class="hljs-title function_">done</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">processed</span>) {
        <span class="hljs-title function_">displayData</span>(processed);
      });
    </code></pre>
    <!-- codeblock-end -->

    In future, if the processing library API changed to synchronous then you can remove `done` block as below,

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-title function_">getDataFromHttp</span>().<span class="hljs-title function_">then</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">result</span>) {
      <span class="hljs-keyword">return</span> <span class="hljs-title function_">displayData</span>(<span class="hljs-title function_">processDataAsync</span>(result));
    });
    </code></pre>
    <!-- codeblock-end -->

    and then you forgot to add `done` block to `then` block leads to silent errors.

3. **Extend ES6 Promises by Bluebird:**

    Bluebird extends the ES6 Promises API to avoid the issue in the second solution. This library has a “default” onRejection handler which will print all errors from rejected Promises to stderr. After installation, you can process unhandled rejections

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">onPossiblyUnhandledRejection</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">error</span>) {
      <span class="hljs-keyword">throw</span> error;
    });
    </code></pre>
    <!-- codeblock-end -->

    and discard a rejection, just handle it with an empty catch

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">reject</span>(<span class="hljs-string">'error value'</span>).<span class="hljs-title function_">catch</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {});
    </code></pre>
    <!-- codeblock-end -->

==================== Id ====================  
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
