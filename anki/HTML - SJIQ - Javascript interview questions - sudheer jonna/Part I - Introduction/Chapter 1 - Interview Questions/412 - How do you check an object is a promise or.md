==================== Question ====================  

### How do you check an object is a promise or not  

==================== Answer ====================  

If you don't know if a value is a promise or not, wrapping the value as `Promise.resolve(value)` which returns a promise

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">isPromise</span>(<span class="hljs-params">object</span>) {
  <span class="hljs-keyword">if</span> (<span class="hljs-title class_">Promise</span> &#x26;&#x26; <span class="hljs-title class_">Promise</span>.<span class="hljs-property">resolve</span>) {
     <span class="hljs-keyword">return</span> <span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">resolve</span>(object) == object;
  } <span class="hljs-keyword">else</span> {
     <span class="hljs-keyword">throw</span> <span class="hljs-string">'Promise not supported in your environment'</span>;
  }
}
<span class="hljs-keyword">var</span> i = <span class="hljs-number">1</span>;
<span class="hljs-keyword">var</span> promise = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Promise</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">resolve, reject</span>) {
  <span class="hljs-title function_">resolve</span>();
});
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">isPromise</span>(i)); <span class="hljs-comment">// false</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">isPromise</span>(promise)); <span class="hljs-comment">// true</span>
</code></pre>
<!-- codeblock-end -->

Another way is to check for `.then()` handler type

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">isPromise</span>(<span class="hljs-params">value</span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-title class_">Boolean</span>(value &#x26;&#x26; <span class="hljs-keyword">typeof</span> value.<span class="hljs-property">then</span> === <span class="hljs-string">'function'</span>);
}
<span class="hljs-keyword">var</span> i = <span class="hljs-number">1</span>;
<span class="hljs-keyword">var</span> promise = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Promise</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">resolve, reject</span>) {
  <span class="hljs-title function_">resolve</span>();
});
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">isPromise</span>(i)); <span class="hljs-comment">// false</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">isPromise</span>(promise)); <span class="hljs-comment">// true</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
412

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#412-How-do-you-check-an-object-is-a-promise-or

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
