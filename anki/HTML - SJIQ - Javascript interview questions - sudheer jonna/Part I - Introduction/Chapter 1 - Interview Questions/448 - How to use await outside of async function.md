==================== Question ====================  

### How to use await outside of async function prior to ES2022?  

==================== Answer ====================  

Prior to ES2022, if you attempted to use an await outside of an async function resulted in a SyntaxError.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">await</span> <span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">resolve</span>(<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Hello await'</span>)); <span class="hljs-comment">// SyntaxError: await is only valid in async function</span>
</code></pre>
<!-- codeblock-end -->

But you can fix this issue with an alternative IIFE (Immediately Invoked Function Expression) to get access to the feature.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">(<span class="hljs-keyword">async</span> <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-keyword">await</span> <span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">resolve</span>(<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Hello await'</span>)); <span class="hljs-comment">// Hello await</span>
})();
</code></pre>
<!-- codeblock-end -->

In ES2022, you can write top-level await without writing any hacks.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">await</span> <span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">resolve</span>(<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Hello await'</span>)); <span class="hljs-comment">//Hello await</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
448

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#448-How-to-use-await-outside-of-async-function

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
