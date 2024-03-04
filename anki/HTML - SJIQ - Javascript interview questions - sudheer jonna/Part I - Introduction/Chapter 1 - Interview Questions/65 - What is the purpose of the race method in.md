==================== Question ====================  

### What is the purpose of the race method in promise  

==================== Answer ====================  

Promise.race() method will return the promise instance which is firstly resolved or rejected. Let's take an example of race() method where promise2 is resolved first

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> promise1 = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Promise</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">resolve, reject</span>) {
  <span class="hljs-built_in">setTimeout</span>(resolve, <span class="hljs-number">500</span>, <span class="hljs-string">'one'</span>);
});
<span class="hljs-keyword">var</span> promise2 = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Promise</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">resolve, reject</span>) {
  <span class="hljs-built_in">setTimeout</span>(resolve, <span class="hljs-number">100</span>, <span class="hljs-string">'two'</span>);
});
<span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">race</span>([promise1, promise2]).<span class="hljs-title function_">then</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">value</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(value); <span class="hljs-comment">// "two" // Both promises will resolve, but promise2 is faster</span>
});
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
65

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#65-What-is-the-purpose-of-the-race-method-in

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
