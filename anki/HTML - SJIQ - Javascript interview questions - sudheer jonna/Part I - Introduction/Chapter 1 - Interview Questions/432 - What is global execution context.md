==================== Question ====================  

### What is global execution context?  

==================== Answer ====================  

The global execution context is the default or first execution context that is created by the JavaScript engine before any code is executed(i.e, when the file first loads in the browser). All the global code that is not inside a function or object will be executed inside this global execution context. Since JS engine is single threaded there will be only one global environment and there will be only one global execution context.

For example, the below code other than code inside any function or object is executed inside the global execution context.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> x = <span class="hljs-number">10</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">A</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Start function A'</span>);
  <span class="hljs-keyword">function</span> <span class="hljs-title function_">B</span>(<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'In function B'</span>);
  }
  <span class="hljs-title function_">B</span>();
}
<span class="hljs-title function_">A</span>();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'GlobalContext'</span>);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
432

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#432-What-is-global-execution-context

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
