==================== Question ====================  

### What is callback in callback  

==================== Answer ====================  

You can nest one callback inside in another callback to execute the actions sequentially one by one. This is known as callbacks in callbacks.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title function_">loadScript</span>(<span class="hljs-string">'/script1.js'</span>, <span class="hljs-keyword">function</span> (<span class="hljs-params">script</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'first script is loaded'</span>);
  <span class="hljs-title function_">loadScript</span>(<span class="hljs-string">'/script2.js'</span>, <span class="hljs-keyword">function</span> (<span class="hljs-params">script</span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'second script is loaded'</span>);
     <span class="hljs-title function_">loadScript</span>(<span class="hljs-string">'/script3.js'</span>, <span class="hljs-keyword">function</span> (<span class="hljs-params">script</span>) {
       <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'third script is loaded'</span>);
       <span class="hljs-comment">// after all scripts are loaded</span>
     });
  });
});
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
62

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#62-What-is-callback-in-callback

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
