==================== Question ====================  

### What is the purpose of EvalError object  

==================== Answer ====================  

The EvalError object indicates an error regarding the global `eval()` function. Even though this exception is not thrown by JavaScript anymore, the EvalError object remains for compatibility. The syntax of this expression would be as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">new</span> <span class="hljs-title class_">EvalError</span>([message[, fileName[, lineNumber]]])
</code></pre>
<!-- codeblock-end -->

You can throw EvalError with in try...catch block as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">try</span> {
  <span class="hljs-keyword">throw</span> <span class="hljs-keyword">new</span> <span class="hljs-title class_">EvalError</span>(<span class="hljs-string">'Eval function error'</span>, <span class="hljs-string">'someFile.js'</span>, <span class="hljs-number">100</span>);
} <span class="hljs-keyword">catch</span> (e) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(e.<span class="hljs-property">message</span>, e.<span class="hljs-property">name</span>, e.<span class="hljs-property">fileName</span>);              <span class="hljs-comment">// "Eval function error", "EvalError", "someFile.js"</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
339

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#339-What-is-the-purpose-of-evalerror-object

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
