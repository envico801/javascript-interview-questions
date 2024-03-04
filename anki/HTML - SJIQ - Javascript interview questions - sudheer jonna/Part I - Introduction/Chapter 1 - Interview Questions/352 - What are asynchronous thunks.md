==================== Question ====================  

### What are asynchronous thunks  

==================== Answer ====================  

The asynchronous thunks are useful to make network requests. Let's see an example of network requests,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">fetchData</span>(<span class="hljs-params">fn</span>) {
  <span class="hljs-title function_">fetch</span>(<span class="hljs-string">'https://jsonplaceholder.typicode.com/todos/1'</span>)
     .<span class="hljs-title function_">then</span>(<span class="hljs-function">(<span class="hljs-params">response</span>) =></span> response.<span class="hljs-title function_">json</span>())
     .<span class="hljs-title function_">then</span>(<span class="hljs-function">(<span class="hljs-params">json</span>) =></span> <span class="hljs-title function_">fn</span>(json));
}
<span class="hljs-keyword">const</span> asyncThunk = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-title function_">fetchData</span>(<span class="hljs-keyword">function</span> <span class="hljs-title function_">getData</span>(<span class="hljs-params">data</span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(data);
  });
};
<span class="hljs-title function_">asyncThunk</span>();
</code></pre>
<!-- codeblock-end -->

The `getData` function won't be called immediately but it will be invoked only when the data is available from API endpoint. The setTimeout function is also used to make our code asynchronous. The best real time example is redux state management library which uses the asynchronous thunks to delay the actions to dispatch.

==================== Id ====================  
352

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
