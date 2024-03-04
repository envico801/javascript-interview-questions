==================== Question ====================  

### How to invoke an IIFE without any extra brackets?  

==================== Answer ====================  

Immediately Invoked Function Expressions(IIFE) requires a pair of parenthesis to wrap the function which contains set of statements.

<!-- codeblock-start -->
<pre><code class="hljs language-js">(<span class="hljs-keyword">function</span> (<span class="hljs-params">dt</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(dt.<span class="hljs-title function_">toLocaleTimeString</span>());
})(<span class="hljs-keyword">new</span> <span class="hljs-title class_">Date</span>());
</code></pre>
<!-- codeblock-end -->

Since both IIFE and void operator discard the result of an expression, you can avoid the extra brackets using `void operator` for IIFE as below,

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">void</span> (<span class="hljs-keyword">function</span> (<span class="hljs-params">dt</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(dt.<span class="hljs-title function_">toLocaleTimeString</span>());
})(<span class="hljs-keyword">new</span> <span class="hljs-title class_">Date</span>());
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
421

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#421-How-to-invoke-an-iife-without-any-extra-br

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
