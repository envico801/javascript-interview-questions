==================== Question ====================  

### Why do we need callbacks  

==================== Answer ====================  

The callbacks are needed because javascript is an event driven language. That means instead of waiting for a response javascript will keep executing while listening for other events.

Let's take an example with the first function invoking an API call(simulated by setTimeout) and the next function which logs the message.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">firstFunction</span>(<span class="hljs-params"></span>) {
  <span class="hljs-comment">// Simulate a code delay</span>
  <span class="hljs-built_in">setTimeout</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'First function called'</span>);
  }, <span class="hljs-number">1000</span>);
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">secondFunction</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Second function called'</span>);
}
<span class="hljs-title function_">firstFunction</span>();
<span class="hljs-title function_">secondFunction</span>();
<span class="hljs-title class_">Output</span>;
<span class="hljs-comment">// Second function called</span>
<span class="hljs-comment">// First function called</span>
</code></pre>
<!-- codeblock-end -->

As observed from the output, javascript didn't wait for the response of the first function and the remaining code block got executed. So callbacks are used in a way to make sure that certain code doesn’t execute until the other code finishes execution.

==================== Id ====================  
55

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#55-Why-do-we-need-callbacks

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
