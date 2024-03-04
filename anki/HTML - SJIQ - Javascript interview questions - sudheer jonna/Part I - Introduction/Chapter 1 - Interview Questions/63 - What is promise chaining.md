==================== Question ====================  

### What is promise chaining  

==================== Answer ====================  

The process of executing a sequence of asynchronous tasks one after another using promises is known as Promise chaining. Let's take an example of promise chaining for calculating the final result,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">new</span> <span class="hljs-title class_">Promise</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">resolve, reject</span>) {
  <span class="hljs-built_in">setTimeout</span>(<span class="hljs-function">() =></span> <span class="hljs-title function_">resolve</span>(<span class="hljs-number">1</span>), <span class="hljs-number">1000</span>);
})
  .<span class="hljs-title function_">then</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">result</span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(result); <span class="hljs-comment">// 1</span>
     <span class="hljs-keyword">return</span> result * <span class="hljs-number">2</span>;
  })
  .<span class="hljs-title function_">then</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">result</span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(result); <span class="hljs-comment">// 2</span>
     <span class="hljs-keyword">return</span> result * <span class="hljs-number">3</span>;
  })
  .<span class="hljs-title function_">then</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">result</span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(result); <span class="hljs-comment">// 6</span>
     <span class="hljs-keyword">return</span> result * <span class="hljs-number">4</span>;
  });
</code></pre>
<!-- codeblock-end -->

In the above handlers, the result is passed to the chain of .then() handlers with the below work flow,

1. The initial promise resolves in 1 second,

2. After that `.then` handler is called by logging the result(1) and then return a promise with the value of result \* 2.

3. After that the value passed to the next `.then` handler by logging the result(2) and return a promise with result \* 3.

4. Finally the value passed to the last `.then` handler by logging the result(6) and return a promise with result \* 4.

==================== Id ====================  
63

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#63-What-is-promise-chaining

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
