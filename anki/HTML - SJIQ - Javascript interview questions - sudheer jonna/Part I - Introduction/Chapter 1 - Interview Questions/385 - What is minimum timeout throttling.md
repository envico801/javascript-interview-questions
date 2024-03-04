==================== Question ====================  

### What is minimum timeout throttling  

==================== Answer ====================  

Both browser and NodeJS javascript environments throttles with a minimum delay that is greater than 0ms. That means even though setting a delay of 0ms will not happen instantaneously.

**Browsers:** They have a minimum delay of 4ms. This throttle occurs when successive calls are triggered due to callback nesting(certain depth) or after a certain number of successive intervals.

Note: The older browsers have a minimum delay of 10ms.

**Nodejs:** They have a minimum delay of 1ms. This throttle happens when the delay is larger than 2147483647 or less than 1.

The best example to explain this timeout throttling behavior is the order of below code snippet.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">runMeFirst</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'My script is initialized'</span>);
}
<span class="hljs-built_in">setTimeout</span>(runMeFirst, <span class="hljs-number">0</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Script loaded'</span>);
</code></pre>
<!-- codeblock-end -->

and the output would be in

<!-- codeblock-start -->
<pre><code class="hljs language-cmd">Script loaded
My script is initialized
</code></pre>
<!-- codeblock-end -->

If you don't use `setTimeout`, the order of logs will be sequential.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">runMeFirst</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'My script is initialized'</span>);
}
<span class="hljs-title function_">runMeFirst</span>();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Script loaded'</span>);
</code></pre>
<!-- codeblock-end -->

and the output is,

<!-- codeblock-start -->
<pre><code class="hljs language-cmd">My script is initialized
Script loaded
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
385

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#385-What-is-minimum-timeout-throttling

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
