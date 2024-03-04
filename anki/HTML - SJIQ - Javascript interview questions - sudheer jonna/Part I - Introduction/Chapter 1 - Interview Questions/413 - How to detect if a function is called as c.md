==================== Question ====================  

### How to detect if a function is called as constructor  

==================== Answer ====================  

You can use `new.target` pseudo-property to detect whether a function was called as a constructor(using the new operator) or as a regular function call.

1. If a constructor or function invoked using the new operator, new.target returns a reference to the constructor or function.

2. For function calls, new.target is undefined.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">Myfunc</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">if</span> (<span class="hljs-keyword">new</span>.<span class="hljs-property">target</span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'called with new'</span>);
  } <span class="hljs-keyword">else</span> {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'not called with new'</span>);
  }
}
<span class="hljs-keyword">new</span> <span class="hljs-title class_">Myfunc</span>(); <span class="hljs-comment">// called with new</span>
<span class="hljs-title class_">Myfunc</span>(); <span class="hljs-comment">// not called with new</span>
<span class="hljs-title class_">Myfunc</span>.<span class="hljs-title function_">call</span>({}); <span class="hljs-comment">// not called with new</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
413

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#413-How-to-detect-if-a-function-is-called-as-c

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
